# muslimadailyrepo

Berkas data publik untuk aplikasi **MuslimaDaily**, disajikan lewat GitHub Pages.

## `official_dates.json`

Tanggal resmi awal bulan hijriah per negara, hasil penetapan pemerintah setempat (sidang isbat dan sejenisnya). Aplikasi mengunduh berkas ini paling sering sekali per 24 jam. Penyesuaian ±1 yang dibuat pengguna selalu lebih diutamakan.

URL: `https://esarijal.github.io/muslimadailyrepo/official_dates.json`

Format:

```json
{
  "version": 2,
  "updated": "2027-02-07",
  "countries": {
    "ID": { "1448-09": "2027-02-08" }
  }
}
```

- Kunci bulan: `yyyy-MM` (tahun hijriah, bulan 1–12). Yang dipakai aplikasi: 09 Ramadan, 10 Syawal, 12 Dzulhijjah.
- Nilai: tanggal masehi hari pertama bulan itu, `yyyy-MM-dd`.
- Kunci negara: kode ISO 3166-1 alpha-2 (`ID`, `MY`, ...).

## Cara memperbarui

1. Tambahkan atau ubah tanggal **hanya dari penetapan resmi**. Jangan mengarang atau memperkirakan tanggal. Kalau belum ada penetapan, biarkan kosong; aplikasi akan memakai hitungan di perangkat.
2. Naikkan `version` (bilangan bulat). Aplikasi menolak berkas dengan versi lebih rendah dari salinan yang sudah dimilikinya.
3. Perbarui `updated` dengan tanggal hari ini.
4. Pastikan JSON valid, lalu commit ke `main`. GitHub Pages memperbarui berkas dalam beberapa menit.

Berkas ini tidak boleh memuat data pengguna apa pun.
