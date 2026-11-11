# VIP Facial Recognition — Gimik Pelancaran Majlis

Halaman gimik "imbasan wajah VIP" untuk Majlis Anugerah Cemerlang SK Agama (MIS) Miri.
Aliran: imbasan wajah → **FACIAL PASS GRANTED** → kiraan 3-2-1 → video pelancaran / bunga api.

> Imbasan ini berskrip (sentiasa lulus dan papar nama yang ditetapkan) supaya selamat di atas pentas.

## Mod

| Peranti | URL |
|---|---|
| Satu peranti sahaja | `index.html` |
| Tablet (kamera, VIP pegang) | `index.html?mode=tablet&bilik=anugerah2026` |
| PC / laptop ke skrin dewan | `index.html?mode=skrin&bilik=anugerah2026` |

Tablet dan PC disegerakkan melalui **Supabase Realtime**. Kamera tablet disiarkan live ke PC melalui **WebRTC**.
Isi `supabaseUrl` dan `supabaseKey` (anon/publishable) dalam `CFG` di `index.html`. Tiada jadual diperlukan.

## Tetapan melalui URL

`nama`, `jawatan`, `mesej`, `majlis`, `tajuk`, `subtajuk`, `video`, `saatImbas`, `mode`, `bilik`

Contoh:
```
index.html?mode=skrin&bilik=anugerah2026&nama=YB%20Dato'%20Ali&jawatan=Ahli%20Parlimen&video=launch.mp4
```

## Kawalan

- **Space / Enter / →** — langkah seterusnya (sesuai untuk presenter clicker atau butang ESP32 BLE keyboard)
- **R** — reset kedua-dua peranti
- PC: klik sekali pada mula untuk aktifkan audio + skrin penuh

## Hari majlis

- Mesti dibuka melalui **https** (GitHub Pages) supaya kamera berfungsi.
- Jika Wi-Fi sekolah menyekat sambungan antara peranti, sambungkan tablet & PC ke **hotspot telefon yang sama**.
- Buat latihan penuh di dewan sebelum majlis.

## Pasang sebagai app (PWA)

Buka `https://skagamamiri.github.io/vipscan/` di Chrome (Android/PC) → tekan **⬇ PASANG APP** pada skrin pilihan mod,
atau menu ⋮ → **Install app / Add to Home screen**. Di iPad: Safari → **Kongsi** → **Add to Home Screen**.

Bila app dibuka kali pertama, pilih mod **Tablet**, **Skrin Dewan** atau **Solo** dan kod bilik. Pilihan ini diingat.
Tukar melalui butang **⇄ Tukar mod** di bawah kiri. Tekan lama ikon app (Android) untuk pintasan terus ke mod Tablet / Skrin.
