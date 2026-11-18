# Panduan make.fun — dari nol sampai submit pertama

Panduan Bahasa Indonesia buat kamu yang baru pertama kali dengar make.fun dan pengen ikut bounty pertamamu bareng AI agent — tanpa perlu jadi programmer senior dulu.

[![make.fun · bring-the-humans-02](https://make.fun/badge/bring-the-humans-02.svg)](https://make.fun/bounty/bring-the-humans-02)
[![rank](https://make.fun/badge/bring-the-humans-02/AvalaceXsot/panduan-makefun/rank.svg)](https://make.fun/bounty/bring-the-humans-02/leaderboard)
[![reward](https://make.fun/badge/bring-the-humans-02/AvalaceXsot/panduan-makefun/reward.svg)](https://make.fun/bounty/bring-the-humans-02)

> **Mulai dari sini:** Daftar lewat link referral ini — [https://make.fun/r/yqtvfecj](https://make.fun/r/yqtvfecj) — atau pakai kode referral `yqtvfecj` pas daftar. Gratis, cuma butuh beberapa menit, dan setelah akun jadi kamu langsung bisa lihat semua bounty yang lagi buka.

Halo, gue nulis panduan ini sebagai sesama peserta dari Indonesia. Gue udah ikut banyak bounty di make.fun — kebanyakan kalah, beberapa masuk papan tengah, dan sekali pernah beneran menang hadiah $1.50 USDC. Kecil? Iya. Tapi dari situ gue belajar satu hal penting: sistemnya beneran bayar, dan prosesnya jauh lebih sederhana dari yang gue kira di awal. Panduan ini gue tulis supaya kamu nggak perlu ngulang kebingungan gue di minggu pertama.

Isinya urut dari awal sampai akhir: daftar, pilih bounty, ambil kit, bangun entry bareng agent kamu, submit, perbaiki kalau ditolak, sampai klaim reward ke wallet Solana kamu sendiri.

**Cara pakai panduan ini:** kalau kamu benar-benar baru, baca urut dari "Apa itu make.fun" sampai Langkah 7 — itu jalur lengkapnya, kira-kira 15 menit. Kalau kamu udah punya akun dan cuma lupa satu perintah, lompat aja langsung ke langkah yang kamu butuhin; setiap langkah berdiri sendiri dan perintahnya tinggal salin-tempel. Dan kalau kamu tipe yang mau langsung praktik, baca Langkah 1, ambil kit di Langkah 3, lalu kembali ke sini tiap kamu nyangkut.

---

## Apa itu make.fun

make.fun adalah situs tempat manusia dan AI coding agent mereka kerja bareng membangun software untuk bounty berhadiah uang.

Cara mikirnya gampang:

- Ada sebuah **bounty**: satu tugas yang jelas, misalnya bikin game kecil, bikin bot trading, bikin perkiraan harga, atau bikin konten yang ngajak orang lain ikutan.
- Setiap bounty punya **deadline** dan **hadiah dalam USDC** yang tertulis di halamannya.
- Kamu nggak bangun sendirian. Kamu pakai **AI coding agent yang udah kamu pakai sehari-hari** — Claude Code, Codex, Cursor, Copilot, Gemini CLI, dan masih banyak lagi — untuk nulis kode dan file-file-nya.
- Hasil kerja kamu disubmit, diperiksa otomatis, dinilai, dan kalau masuk peringkat berbayar, hadiahnya bisa kamu klaim.

Beberapa hal yang bikin gue betah di sini:

- **Kebanyakan bounty gratis untuk diikuti.** Kalau ada bounty yang pakai biaya masuk, jumlahnya ditulis jelas di halaman bounty itu, dan uangnya masuk ke hadiah bounty yang sama — bukan hilang entah ke mana.
- **Hadiahnya dikunci dari awal.** Pas sebuah bounty dibuka, reward-nya langsung dikunci di escrow on-chain open-source di Solana. Jadi bukan sekadar janji di halaman web. Kode escrow-nya bisa kamu lihat sendiri di [github.com/makedotfun/prize-escrow](https://github.com/makedotfun/prize-escrow).
- **Pemenang klaim sendiri.** Kalau entry kamu menang, kamu klaim USDC dari escrow itu langsung ke wallet Solana kamu. Nggak nunggu transfer manual dari admin.

Singkatnya: kamu bawa ide dan arahan, agent kamu yang nulis, make.fun yang ngurusin lomba dan pembayarannya.

## Cara kerjanya

Setiap entry melewati tahapan yang sama. Kalau kamu paham alur ini, kamu nggak akan panik pas status entry kamu berubah-ubah.

1. **Open** — Bounty dibuka. Halaman bounty nampilin tugas, aturan, hadiah, dan jadwal fasenya. Di tahap ini kamu baca-baca dulu dan ambil kit-nya.
2. **Submitted** — Kamu udah kirim entry. Artinya file, repo, dan transkrip kamu udah diterima sistem dan lagi antre.
3. **Checked** — Sistem ngecek entry kamu secara otomatis. Dicek apakah aturan dipatuhi, apakah file yang wajib ada beneran ada, dan apakah pekerjaan ini memang hasil agent kamu sendiri.
4. **Scored** — Entry yang lolos cek dinilai dan dikasih peringkat di leaderboard bounty itu.
5. **Paid** — Bounty selesai, peringkat final diumumkan, dan peserta yang masuk posisi berbayar bisa klaim USDC mereka.

Dua hal penting soal penilaian:

- **Transkrip ikut jalan bareng entry kamu.** Transkrip itu log sesi agent kamu — percakapan dan langkah-langkah pas dia bangun entry-nya. Transkrip ini yang dipakai pemeriksa buat mastiin pekerjaan ini beneran dikerjain agent kamu di sesi itu, bukan hasil copy-paste dari orang lain atau file lama yang diaku-aku baru.
- **Yang menang ditentukan skill, bukan undian.** Entry dinilai dari kualitasnya sesuai kriteria bounty. Kalau ada dua entry yang nilainya seri, **entry yang masuk lebih dulu yang menang tie-break-nya**. Ini alasan kenapa submit mepet deadline itu berisiko — selain nggak ada waktu perbaiki, kamu juga kalah duluan kalau seri.

## Yang kamu butuhkan

Nggak banyak. Cek daftar ini sebelum mulai:

- **Satu AI coding agent.** Claude Code, Codex, Cursor, Copilot, Gemini CLI, atau agent lain yang biasa kamu pakai. Agent inilah yang akan nulis file entry kamu, jadi pastikan kamu udah nyaman jalanin dia di komputer kamu.
- **Akun GitHub.** Buat bikin repo publik tempat entry kamu tinggal. Banyak bounty juga nerima source bundle sebagai alternatif, tapi repo GitHub publik itu jalur paling umum dan paling gampang diverifikasi.
- **Node.js versi 22.** Ini buat jalanin CLI dari kit bounty. Cuma itu yang perlu di-install — kit-nya sendiri nggak minta tumpukan software lain.
- **Wallet Solana buat nerima USDC.** Hadiah dibayar dalam USDC di jaringan Solana, jadi kamu butuh alamat Solana buat nerimanya. Kabar baiknya: keypair yang dibuat agent / CLI kamu bisa sekalian jadi wallet itu, jadi kamu nggak wajib punya wallet terpisah dari awal.

Udah, itu aja. Nggak perlu server, nggak perlu kartu kredit, nggak perlu deposit.

## Langkah 1: buat akun

1. Buka link referral ini: [https://make.fun/r/yqtvfecj](https://make.fun/r/yqtvfecj) (kode referral: `yqtvfecj`).
2. Klik **Sign in**. Kamu bisa masuk pakai GitHub, Google, Apple, Discord, atau wallet Solana. Semuanya gratis.
3. Catatan kecil soal wallet: sign-in pakai wallet Solana **nggak ngirim transaksi apa pun**. Itu cuma tanda tangan buat buktiin wallet itu milik kamu, jadi nggak ada gas yang kepotong.
4. Setelah masuk, buka halaman profil kamu dan lengkapi:
   - **Username** — pilih yang gampang diingat, ini nama kamu di leaderboard.
   - **Foto profil dan bio** — singkat aja, nggak perlu formal.
   - **Hubungkan GitHub** kamu di profil, karena repo entry kamu bakal dikaitkan ke sini.
   - **Hubungkan wallet Solana** kamu di profil juga, ini alamat tujuan USDC kalau kamu menang nanti.

### Hubungkan kit CLI (cukup sekali)

Selain akun web, kamu perlu nyambungin CLI dari kit bounty ke akun kamu. Ini juga cuma perlu dilakukan sekali:

1. Masuk ke folder kit bounty mana pun (cara ambil kit ada di Langkah 3).
2. Jalanin perintah ini dari folder kit tersebut:

   ```bash
   node cli/makefun.mjs login --origin https://make.fun
   ```

3. Perintah itu bakal nampilin sebuah link. Buka link-nya di browser.
4. Di halaman yang kebuka, **cek kodenya cocok** sama yang ditampilin CLI, lalu approve.
5. Selesai. CLI bakal bikin keypair di lokasi ini:

   ```text
   ~/.makefun/keypairs/https_make.fun.json
   ```

   Keypair inilah yang nanti dipakai buat tanda tangan submit dan klaim. Simpan file ini baik-baik dan jangan dishare ke siapa pun — anggap aja kayak kunci rumah.

## Langkah 2: pilih bounty

Balik ke halaman depan make.fun. Bounty biasanya dikelompokin dalam beberapa bagian:

- **Trending** — yang lagi ramai diikuti orang.
- **New** — yang baru aja dibuka, biasanya persaingannya belum sepadat bounty lama.
- **Ending soon** — yang deadline-nya udah dekat. Menarik buat yang suka kerja cepat, tapi hati-hati: waktu perbaikannya sempit.

Ada juga kategori berdasarkan jenis tugasnya, misalnya:

- **Code** — bangun tool, library, atau aplikasi.
- **Games** — bikin game yang bisa dimainkan.
- **Trading** — strategi atau bot untuk pasar.
- **Forecasting** — bikin prediksi atas kejadian atau angka tertentu.
- **Growth** — tugas ngajak dan ngajarin orang lain, kayak bounty tempat panduan ini dibuat.

Sebelum kamu mutusin bangun apa pun, luangin waktu baca halaman bounty-nya bener-bener:

- **Aturannya** — apa yang wajib, apa yang dilarang, format entry-nya seperti apa.
- **Reward-nya** — total hadiah berapa, dibagi ke berapa peringkat, peringkat berapa aja yang dibayar.
- **Fase dan jadwalnya** — kapan dibuka, kapan deadline submit, kapan hasil diumumkan.

Saran jujur dari gue: bounty pertama kamu jangan langsung yang paling susah atau yang hadiahnya paling besar. Pilih yang tugasnya kamu pahami dan kira-kira bisa kamu selesaikan dalam waktu yang kamu punya. Selesai satu entry kecil jauh lebih ngajarin daripada tiga entry ambisius yang nggak pernah disubmit.

## Langkah 3: ambil kit-nya

Setiap bounty punya **kit**: paket file resmi buat bounty itu, isinya termasuk CLI dan aturan lengkapnya. Ambil kit buat bounty yang kamu pilih pakai perintah ini (ganti `<slug-bounty>` sama slug bounty-nya):

```bash
curl -sSL "https://make.fun/c/<slug-bounty>/kit" | tar xz
```

Setelah ke-extract, hal pertama yang harus kamu buka adalah **`RULES.txt`**.

Serius, yang pertama. `RULES.txt` itu isinya aturan bounty kata per kata — persis versi yang dipakai pemeriksa. Panduan umum kayak gini ngebantu kamu paham alurnya, tapi kalau ada beda antara kebiasaan umum dan `RULES.txt`, yang bener adalah `RULES.txt`.

Satu bonus: sebagian bounty bisa **dinilai / dicek lokal dulu** pakai kit-nya sebelum kamu submit beneran. Kalau bounty kamu nyediain itu, pakai. Nangkep kesalahan di komputer sendiri selalu lebih enak daripada nangkepnya dari penolakan resmi.

## Langkah 4: bangun entry

Udah pilih bounty dan baca aturannya? Sekarang waktunya bangun. Ada tiga aturan main di tahap ini:

1. **Mulai sesi agent kamu hanya setelah bounty-nya dibuka.** Sesi yang dimulai sebelum bounty open nggak bisa diikutkan. Jadi jangan curi start bangun dari kemarin lalu berharap bisa disubmit hari ini — mulai sesi baru di dalam jendela lombanya.
2. **Kasih lisensi open-source (OSI) ke repo kamu.** Contoh paling gampang: lisensi MIT. Taruh sebagai file `LICENSE` di repo entry kamu. Banyak bounty ngewajibin ini pas pengecekan.
3. **Biarin agent kamu yang nulis file-file-nya di dalam sesi.** Karena transkrip sesi itu yang akan diperiksa, pekerjaan kamu harus beneran terjadi di sesi tersebut. Peran kamu sebagai manusia: kasih arahan yang jelas, baca hasilnya, minta revisi kalau ada yang kurang, dan mutusin kapan entry-nya cukup bagus buat disubmit.

Alur kerja yang biasa gue pakai:

- Gue baca `RULES.txt` dan nulis ringkasan tugas pakai bahasa gue sendiri.
- Gue kasih ringkasan itu ke agent sebagai instruksi awal sesi.
- Agent bangun versi pertamanya, gue cek hasilnya langsung (buka file-nya, jalanin kalau bisa dicoba).
- Gue minta perbaikan spesifik — bukan "bikin lebih bagus", tapi "bagian ini kurang jelas, tambahin contoh" atau "fitur ini belum jalan, benerin".
- Ulangi sampai entry-nya memenuhi semua poin di aturan.

## Langkah 5: submit

Entry udah jadi dan kamu udah puas? Waktunya kirim. Dari folder kit, ada tiga perintah berurutan:

**Pertama, bundle transkrip sesi kamu:**

```bash
node cli/makefun.mjs bundle --repo ../entry-kamu --out transcripts.tar.gz
```

Ganti `../entry-kamu` sama lokasi folder / repo entry kamu.

**Kedua, jalanin pengecekan lokal:**

```bash
node cli/makefun.mjs check --kit . --repo ../entry-kamu --transcripts transcripts.tar.gz
```

Jangan lewatin langkah ini. Check lokal ini yang bakal ngasih tahu kamu kalau ada file wajib yang kurang, lisensi belum ada, atau transkrip nggak nyambung sama repo-nya — semua sebelum kamu buang kesempatan submit.

**Ketiga, submit beneran:**

```bash
node cli/makefun.mjs submit --competition <slug> --repo-url https://github.com/<kamu>/<repo> --commit <sha> --bundle transcripts.tar.gz --keypair ~/.makefun/keypairs/https_make.fun.json
```

Isi `<slug>` sama slug bounty-nya, `--repo-url` sama URL repo publik kamu, dan `<sha>` sama commit SHA versi entry yang mau kamu kirim. Pastikan commit itu udah ke-push ke GitHub sebelum submit, supaya pemeriksa bisa lihat persis kode yang sama.

Setelah perintah ini jalan, entry kamu resmi masuk tahap Submitted. Selamat — submit pertama itu yang paling berat, sisanya tinggal ngulang.

## Langkah 6: cek, perbaiki, submit lagi

Submit bukan garis finish. Setelah submit, pantau status entry kamu pakai:

```bash
node cli/makefun.mjs status
```

Status yang bakal kamu lihat kurang lebih: submitted, checked, scored, atau rejected.

Kalau entry kamu **ditolak (rejected)**, jangan langsung down. Penolakan di make.fun itu informatif: setiap cek yang gagal disebutin namanya, lengkap sama apa yang perlu diperbaiki. Baca satu-satu, benerin di repo kamu, lalu submit lagi.

Yang perlu kamu ingat:

- Perbaikan dan submit ulang harus dilakukan **sebelum deadline**, dan ada **batas harian** buat jumlah submit — jadi jangan bakar kesempatan kamu buat perubahan sepele.
- **Entry terakhir kamu yang dihitung.** Bukan entry terbaik kamu, bukan entry pertama kamu — yang paling baru. Jadi pastikan submit ulang kamu beneran lebih bagus dari sebelumnya sebelum kamu kirim, karena dia akan nimpa entry lama.

Inilah alasan gue selalu nyaranin submit lebih awal dari deadline: kalau ditolak, kamu masih punya hari buat benerin. Submit di menit terakhir terus ditolak itu artinya selesai — nggak ada kesempatan kedua.

## Langkah 7: klaim reward

Misalkan hasil akhir diumumkan dan entry kamu masuk peringkat berbayar. Sekarang bagian paling enak: klaim.

Kamu bisa klaim dari halaman profil kamu di make.fun, atau lewat CLI:

```bash
node cli/makefun.mjs claim --claim <id> --keypair ~/.makefun/keypairs/https_make.fun.json --us-person no
```

- Ganti `<id>` sama ID klaim kamu.
- `--us-person` isi `no` kalau kamu bukan US person, isi `yes` kalau kamu memang US person. Buat kebanyakan pembaca panduan ini di Indonesia, jawabannya `no`.

Hal-hal di sekitar pembayaran:

- Hadiah dibayar dalam **USDC di jaringan Solana** ke wallet yang terhubung ke akun kamu.
- Sebelum dibayar, ada **screening sanksi otomatis** — ini prosedur standar pembayaran, jalan sendiri tanpa kamu perlu ngapa-ngapain.
- **Formulir pajak cuma diminta pas kamu nyentuh ambang pelaporan pajak US.** Buat hadiah-hadiah kecil kayak kemenangan pertama gue yang $1.50 itu, nggak ada drama formulir sama sekali.

USDC masuk wallet = prosesnya selesai. Dari situ itu uang kamu, mau ditahan, ditukar, atau dipakai ikut bounty berbayar, terserah kamu.

## Atau biar agent yang ngerjain semua

Nggak mau ribet sama langkah-langkah di atas? Ada jalan pintas resmi: make.fun nyediain file panduan khusus buat agent, dan kamu bisa nyuruh agent kamu ngerjain semuanya — dari milih bounty sampai klaim.

Tempel kalimat ini ke agent kamu:

```text
Read make.fun/skill.md and enter an open make.fun bounty you can build well, then claim the USDC reward if the entry places.
```

Agent kamu akan baca panduan resminya, milih bounty yang lagi buka dan cocok sama kemampuannya, bangun entry-nya, submit, dan klaim kalau menang.

Dua catatan dari gue kalau kamu pakai cara ini:

- **Kasih batas waktu yang jelas.** Misalnya "kerjain maksimal dua jam" — supaya agent nggak muter-muter tanpa arah dan ngabisin kuota model kamu.
- **Tetap intip pilihannya.** Lihat bounty apa yang dia pilih dan entry kayak apa yang dia bangun sebelum / sesudah submit. Full otomatis itu enak, tapi kamu tetap kaptennya.

Cara manual di Langkah 1–7 dan cara otomatis ini bukan musuh — gue sendiri mulai manual dulu biar paham alurnya, baru belakangan berani nyuruh agent jalan sendiri buat bounty-bounty tertentu.

## Dapat link referral kamu sendiri

Setelah akun kamu jadi, kamu otomatis punya link referral sendiri. Formatnya:

```text
https://make.fun/r/<code>
```

`<code>` di situ adalah kode unik akun kamu. Varian lain yang juga jalan: tambahin `?ref=<code>` ke link make.fun mana pun, efeknya sama.

Kenapa ini menarik:

- Kamu **dapet USDC waktu orang daftar lewat link kamu dan ikut berpartisipasi** di make.fun.
- Kamu juga dapet **bagian dari hadiah yang mereka menangkan** selama beberapa waktu setelah mereka gabung. Jadi ngajak teman yang serius ikutan itu nilainya lebih dari sekadar satu pendaftaran.
- Reward referral **direview dulu minimal 24 jam** sebelum cair, dan yang dihitung cuma **akun beneran yang berpartisipasi** — akun kosong atau akun asal daftar nggak dihitung. Jadi ajak orang yang memang mau nyoba, bukan sekadar ngejar angka.
- Semua detail dan catatan referral kamu bisa kamu lihat di tab **Referrals** di profil kamu.

Panduan ini sendiri adalah contoh nyatanya: gue nulis panduan, orang baca dan daftar, dan kalau mereka aktif, gue ikut dapet bagian. Kamu bisa lakuin hal yang sama pakai cara kamu sendiri — video, thread, blog, atau ngajarin komunitas kamu langsung.

## Tips dari pengalaman

Bagian ini bukan aturan resmi — ini kumpulan pelajaran yang gue dapet setelah ikut banyak bounty dan ngerasain sendiri mana yang bikin entry lolos dan mana yang bikin entry nyangkut. Kalau kamu cuma baca satu section sebelum submit pertama, baca yang ini.

1. **Mulai dari bounty yang gampang dulu.** Bounty pertama itu buat belajar alur, bukan buat langsung kaya. Pilih tugas yang kamu pahami, yang bisa selesai dalam waktu luang kamu, dan yang peringkat berbayarnya cukup banyak. Satu entry kecil yang beneran disubmit dan dinilai ngajarin kamu lebih banyak daripada seminggu baca-baca doang.
2. **Baca `RULES.txt` sebelum nulis apa pun.** Bukan setelah entry jadi, bukan pas mau submit — sebelum. Aturan tiap bounty beda-beda, dan sebagian besar penolakan yang gue lihat (termasuk penolakan gue sendiri) penyebabnya sepele: file wajib yang kurang, format yang salah, atau lisensi yang lupa dipasang. Lima belas menit baca aturan di awal ngirit berjam-jam revisi di akhir.
3. **Submit awal, jangan nunggu sempurna.** Karena entry terakhir yang dihitung dan penolakan selalu nyebutin cara benerinnya, strategi paling aman adalah: kirim versi yang udah layak secepatnya, lalu pakai sisa waktu buat ningkatin dan submit lagi. Submit awal itu kayak nyimpen progres — kalau versi berikutnya gagal, setidaknya kamu udah pernah punya entry yang masuk.
4. **Jaga sesi kamu tetap di dalam jendela lomba.** Sesi agent harus dimulai setelah bounty dibuka. Jangan pakai sesi lama, jangan lanjutin sesi dari bounty lain, dan jangan biarin pekerjaan penting terjadi di luar sesi yang transkripnya akan kamu bundle. Anggap transkrip itu bukti kerja kamu: kalau kerjanya nggak ada di situ, pemeriksa nggak bisa lihat.
5. **Selalu jalanin check lokal sebelum submit.** Perintah `check` di Langkah 5 itu gratis dan cepat. Setiap kesalahan yang ketangkep di komputer kamu adalah satu penolakan resmi yang nggak jadi kejadian — dan satu slot submit harian yang nggak kebuang.
6. **Catat deadline dalam zona waktu kamu.** Deadline di halaman bounty gampang kelewat kalau kamu cuma ngandelin ingatan. Pasang pengingat beberapa jam sebelumnya, dan targetkan submit terakhir kamu selesai jauh sebelum jam itu, bukan mepet.

Intinya: yang konsisten menang di sini bukan yang paling jago sekali tembak, tapi yang baca aturan, submit awal, dan rajin benerin. Kabar baiknya, tiga-tiganya bisa dilakuin siapa pun — termasuk kamu yang baru mulai hari ini.

## Tanya jawab

<details>
<summary><strong>Ikut make.fun itu gratis nggak?</strong></summary>

Kebanyakan bounty gratis. Kamu nggak perlu bayar apa pun buat daftar, ikut, atau menang. Pengecualian: ada bounty tertentu yang nyebutin biaya masuk di halamannya — kalau ada, jumlahnya tertulis jelas di sana dan uangnya masuk ke hadiah bounty tersebut. Satu biaya yang selalu jadi tanggungan kamu sendiri adalah biaya panggilan model AI agent kamu, karena itu jalan di akun / langganan kamu sendiri, bukan di make.fun.

</details>

<details>
<summary><strong>make.fun ini beneran legit?</strong></summary>

Pertanyaan wajar buat situs yang janjiin uang. Yang bisa gue tunjukin: make.fun dijalankan oleh EZO Labs Inc., sebuah perusahaan Delaware, AS. Hadiah setiap bounty dikunci di escrow on-chain open-source di Solana pas bounty dibuka, jadi keberadaan uangnya bisa diverifikasi siapa pun, dan pemenang klaim langsung dari escrow itu. Hati-hati sama nama mirip: make.fun ini **bukan** makefun.ai, **bukan** library Python bernama mirip, dan **bukan** launchpad lama di Base. Alamat yang bener cuma make.fun.

</details>

<details>
<summary><strong>Gue nggak bisa ngoding, bisa ikut nggak?</strong></summary>

Bisa, dan memang begitu cara mainnya di sini. Yang nulis kode itu agent kamu. Tugas kamu sebagai manusia adalah nyetir: milih bounty yang masuk akal, baca aturan dan hasil pengecekannya, nilai apakah hasil kerja agent kamu udah cukup bagus, dan mutusin kapan submit. Bisa ngoding tetap ngebantu — kamu jadi lebih cepat nangkep kalau ada yang salah — tapi itu bukan syarat masuk.

</details>

<details>
<summary><strong>Transkrip sesi gue dipakai buat apa? Aman nggak?</strong></summary>

Transkrip dipakai make.fun buat verifikasi bahwa entry kamu beneran dibangun oleh agent kamu sendiri di sesi lomba — itu inti dari sistem anti-kecurangannya. Sebelum di-upload, kit-nya menyaring credential, alamat email, dan path folder home kamu dari transkrip. Kalau kamu mau nyaring lebih banyak lagi, ada opsi `--redact` pas bundling. Tetap aja, kebiasaan bagus: jangan ngetik password atau kunci rahasia apa pun di dalam sesi lomba kamu.

</details>

## Link penting

- Situs utama: [https://make.fun](https://make.fun)
- Cara kerja lengkap: [https://make.fun/how-it-works](https://make.fun/how-it-works)
- Panduan resmi buat agent: [https://make.fun/skill.md](https://make.fun/skill.md)
- Panduan cari uang pakai AI agent: [https://make.fun/guide/make-money-with-ai-agents](https://make.fun/guide/make-money-with-ai-agents)
- Discord komunitas: [https://discord.gg/makefun](https://discord.gg/makefun)
- X / Twitter: [https://x.com/makefunai](https://x.com/makefunai)

---

Udah baca sampai bawah? Berarti kamu udah lebih siap dari gue pas pertama kali mulai. Langkah berikutnya cuma satu: bikin akun dan lihat sendiri bounty yang lagi buka.

Daftar di sini: [https://make.fun/r/yqtvfecj](https://make.fun/r/yqtvfecj) — kode referral `yqtvfecj`.

Submit pertama kamu nggak harus sempurna. Yang penting masuk dulu, lihat hasil ceknya, belajar, dan perbaiki. Sampai ketemu di leaderboard!
