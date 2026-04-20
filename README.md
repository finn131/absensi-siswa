# Absensi Siswa RFID (Versi Pengumpulan)

Paket ini berisi **source code web + database** untuk dijalankan langsung di komputer lokal.

## Isi Paket
- `backend/` -> source code API Flask
- `frontend/` -> source code React (Vite)
- `backend/database.db` -> database SQLite

## Requirement
- Python 3.10+
- Node.js 18+ dan npm

## Cara Menjalankan

### 1) Jalankan Backend
```bash
cd backend
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
python app.py
```

Backend berjalan di:
- `http://localhost:5000`

### 2) Jalankan Frontend
Buka terminal baru:
```bash
cd frontend
cp .env.example .env
npm install
npm run dev
```

Frontend berjalan di:
- `http://localhost:5173`

## Akun Login Default
- Admin: `admin` / `admin`
- Petugas: `petugas` / `petugas`

## Data Sample
- Database SQLite sudah disertakan di `backend/database.db`
- Data sample siswa: 32 siswa
- UID sample awal:
  - `A1B2C3D4`
  - `E5F6G7H8`
  - `I9J0K1L2`
  - `M3N4O5P6`
  - `Q7R8S9T0`
- UID siswa 6-32 mengikuti pola `RFID0006` sampai `RFID0032`

## Reset Ulang Database (Opsional)
Jika ingin reset database ke data sample awal:
```bash
cd backend
python init_db.py
```
