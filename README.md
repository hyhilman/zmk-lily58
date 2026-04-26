ZMK Lily58 untuk Super Mini / Promicro Wireless NRF52840.

## Keymap (Coding-focused: vim + ghostty + macOS)

Custom 4-layer keymap with home row mods, sticky shift, caps word, and a
dedicated macOS window-management layer.

### Layer 0 — Base

```
,-----------------------------------------.                    ,-----------------------------------------.
| ESC  |  1   |  2   |  3   |  4   |  5   |                    |  6   |  7   |  8   |  9   |  0   |  `   |
|------+------+------+------+------+------|                    |------+------+------+------+------+------|
| TAB  |  Q   |  W   |  E   |  R   |  T   |                    |  Y   |  U   |  I   |  O   |  P   |  -   |
|------+------+------+------+------+------|                    |------+------+------+------+------+------|
| CTRL |A / ⌘ |S / ⌥ |D / ⌃ |  F   |  G   |                    |  H   |  J   |K / ⌃ |L / ⌥ |; / ⌘ |  '   |
|------+------+------+------+------+------+------.      .------+------+------+------+------+------+------|
| SK⇧  |Z /WIN|  X   |  C   |  V   |  B   |  [   |      |  ]   |  N   |  M   |  ,   |  .   |  /   |CAPSWD|
`-------------+------+------+------+------+------|      |------+------+------+------+------+-------------'
                     | LALT | LGUI | NAV  |ENTER |      |SPACE | SYM  | BSPC | RGUI |
                     `---------------------------'      `---------------------------'
```

- `A/⌘ S/⌥ D/⌃` and mirrored `K/⌃ L/⌥ ;/⌘` — **home row mods**: tap = letter, hold = modifier (Cmd / Option / Control).
- `Z/WIN` — tap = `z`, hold = activate Window layer (Layer 3).
- `SK⇧` — **sticky shift**: tap, next single key is shifted (no holding).
- `CAPSWD` — **caps word**: tap, next word is capitalized until space/punctuation. Perfect for `MAX_RETRIES`, `JSON_PARSE`.
- Inner thumb keys: `[` and `]` direct (vim text-objects stay one-tap).
- Shift is intentionally NOT on home row — it gets held too often. Use `SK⇧` or `CAPSWD` instead.

### Layer 1 — Lower / Nav (hold left thumb)

```
,-----------------------------------------.                    ,-----------------------------------------.
| BTCLR| BT1  | BT2  | BT3  | BT4  | BT5  |                    |      |      |      |      |      |      |
|------+------+------+------+------+------|                    |------+------+------+------+------+------|
|      |      |      |      |      |      |                    | HOME | PGDN | PGUP | END  |      |      |
|------+------+------+------+------+------|                    |------+------+------+------+------+------|
|      | UNDO | CUT  | COPY |PASTE | REDO |                    | LEFT | DOWN |  UP  |RIGHT |      |      |
|------+------+------+------+------+------+------.      .------+------+------+------+------+------+------|
|      |      |      |      |      |      |      |      |      |      |      |      | DEL  | INS  |      |
`-------------+------+------+------+------+------|      |------+------+------+------+------+-------------'
                     |      |      | ████ |      |      |      |      |      |      |
                     `---------------------------'      `---------------------------'
```

- Right hand `HJKL` → arrow keys (vim spatial — works in any app).
- Above arrows → `HOME / PGDN / PGUP / END`.
- Left hand → Mac clipboard macros (Cmd+Z / X / C / V / Shift+Z).
- Top row → Bluetooth controls.

### Layer 2 — Raise / Symbols (hold right thumb)

```
,-----------------------------------------.                    ,-----------------------------------------.
|  F1  |  F2  |  F3  |  F4  |  F5  |  F6  |                    |  F7  |  F8  |  F9  | F10  | F11  | F12  |
|------+------+------+------+------+------|                    |------+------+------+------+------+------|
|      |  !   |  @   |  #   |  $   |  %   |                    |  ^   |  &   |  *   |  (   |  )   |  ~   |
|------+------+------+------+------+------|                    |------+------+------+------+------+------|
|      |  =   |  +   |  -   |  _   |  /   |                    |  \   |  |   |  :   |  {   |  }   |  ?   |
|------+------+------+------+------+------+------.      .------+------+------+------+------+------+------|
|      |      |      |      |      |      |      |      |      |      |      |      |  <   |  >   |      |
`-------------+------+------+------+------+------|      |------+------+------+------+------+-------------'
                     |      |      |      |      |      |      | ████ |      |      |
                     `---------------------------'      `---------------------------'
```

- Bracket cluster on right cols 10–11: `()` row 2, `{}` row 3, `<>` row 4.
- Programming-heavy left side row 3: `= + - _ /`.
- F1–F12 on top row.

### Layer 3 — Window (hold Z) — macOS window/tab management

```
,-----------------------------------------.                    ,-----------------------------------------.
|      |      |      |      |      |      |                    | ⌘1   | ⌘2   | ⌘3   | ⌘4   | ⌘5   | ⌘6   |
|------+------+------+------+------+------|                    |------+------+------+------+------+------|
|      | ⌘Q   | ⌘W   | ⌘H   | ⌘N   | ⌘T   |                    |      | ⌘[   | ⌘]   |      |      |      |
|      |QUIT  |CLOSE |HIDE  |NEW   |TAB   |                    |      |SPLIT←|SPLIT→|      |      |      |
|------+------+------+------+------+------|                    |------+------+------+------+------+------|
|      | ⌃←   | ⌃→   | ⌃↑   | ⌃⌘F  |      |                    | ⌘⌥←  | ⌘⇧`  | ⌘`   | ⌘⌥→  |      |      |
|      |SPC←  |SPC→  |MISSN |FULL  |      |                    |TAB←  |WIN←  |WIN→  |TAB→  |      |      |
|------+------+------+------+------+------+------.      .------+------+------+------+------+------+------|
|      | ████ | ⌘M   | ⌘C   | ⌘V   |      |      |      |      |      |      |      |      |      |      |
|      |      |MIN   |COPY  |PASTE |      |      |      |      |      |      |      |      |      |      |
`-------------+------+------+------+------+------|      |------+------+------+------+------+-------------'
                     |      |      |      |      |      |      |      |      |      |
                     `---------------------------'      `---------------------------'
```

- Right hand `HJKL` → tab-prev / window-prev / window-next / tab-next (tabs horizontal, windows vertical).
- Top right → `Cmd+1` … `Cmd+6` to jump to tab N directly.
- Left hand row 2 → app actions (Quit / Close / Hide / New / NewTab).
- Left hand row 3 → Spaces (`Ctrl+←` `Ctrl+→`), Mission Control (`Ctrl+↑`), Fullscreen (`Cmd+Ctrl+F`).
- `⌘[` / `⌘]` → ghostty split nav (or browser back/forward).

### Combos (active on Base layer only)

Press two keys simultaneously (within 50ms):

| Combo | Output |
|---|---|
| `Q` + `W` | `()` cursor between |
| `E` + `R` | `{}` cursor between |
| `U` + `I` | `[]` cursor between |
| `O` + `P` | `<>` cursor between |

### Tuning

If home row mods misfire (letters fire as mods, or vice versa), adjust in `config/lily58.keymap`:

```
&mt {
    flavor = "tap-preferred";
    tapping-term-ms = <200>;   // raise = favors letters; lower = favors mods
    quick-tap-ms = <125>;
};
```

---

## Original repo notes

[ZMK STUDIO](https://zmk.studio/)
Ada update baru ZMK Studio remapping tanpa perlu di flash 

[Full Dokumentasi ZMK](https://zmk.dev/docs)


Tools :
[ZMK Keymap Editor](https://nickcoutsos.github.io/keymap-editor/)
Video fork repository :
[Tutorial Mapping ZMK](https://youtu.be/cAi5pnkz48M)

<img width="3827" height="2705" alt="Image" src="https://github.com/user-attachments/assets/fa0b5a4a-d71e-4bee-a56c-bf8bce3d2299" />



Prosedur Reset Keyboard Split
Lakukan langkah-langkah berikut untuk mereset semua bagian keyboard split Anda:
- Masukkan setiap bagian keyboard split ke mode bootloader. Dengan cara tekan 2x tombol reset saat USB terhubung akan muncul drive baru, untuk flash nya cukup drag & drop di disk bootloader
- Flash salah satu bagian keyboard dengan firmware reset pengaturan setting_reset.uf2.
- Ulangi langkah 2 pada bagian lainnya dari keyboard split.
- Flash image firmware yang sebenarnya untuk setiap bagian keyboard split (misalnya my_board_left.uf2 untuk bagian kiri, my_board_right.uf2 untuk bagian kanan).
- Jika central dan peripheral tidak saling terhubung setelah menyelesaikan langkah-langkah ini, akan membantu untuk mereset central dan peripheral pada waktu yang hampir bersamaan. Biasanya dilakukan dengan menghubungkan pin reset ke ground pada setiap mikrokontroler keyboard Anda, menekan tombol reset, atau mematikan lalu menyalakan keduanya dengan sakelar daya.
- Setelah selesai, Anda harus menghapus/lupakan keyboard dari perangkat host mana pun yang sebelumnya terpasang, lalu lakukan pairing ulang, karena informasi pairing tersebut juga telah dihapus dari keyboard.
  

🔵 Penjelasan Bluetooth ZMK (Versi Sederhana)
Keyboard ZMK menggunakan sistem Bluetooth yang aktif secara otomatis. Pada layar keyboard, Anda akan melihat angka dan simbol yang menjelaskan status koneksi.

📌 1. Angka = Slot Bluetooth
Angka yang tampil di layar menunjukkan slot penyimpanan perangkat (Bluetooth Profile). <br>
Contoh: <br>
Angka 1 di layar = menggunakan BT_SEL 0 <br>
Angka 2 di layar = menggunakan BT_SEL 1 <br>
Dan seterusnya <br>
Setiap slot dapat menyimpan satu perangkat.



📌 2. Simbol “X”
Jika muncul ikon X, artinya:
Slot tersebut pernah digunakan, tetapi
Tidak sedang terhubung ke perangkat mana pun


📌 3. Pairing Ulang
Jika ingin melakukan pairing ulang untuk slot yang sedang dipakai:
Tekan tombol BT_CLR pada keymap
Layar akan berubah menjadi ikon gerigi (slot di-reset)
Lakukan pairing dari perangkat Anda
Jika berhasil, simbol akan berubah menjadi ikon centang


📌 4. Slot Tidak Bisa Ditimpa
Slot Bluetooth tidak bisa langsung ditimpa perangkat baru.
Jika slot tersebut sudah pernah terhubung ke perangkat lain, Anda harus:
Pindah ke slot lain (BT_SEL berikutnya), atau
Hapus slot dengan tombol BT_CLR

📌 5. Contoh Penggunaan Slot <br> 
Rekomendasi pembagian slot: <br>
BT_SEL 0 → PC <br>
BT_SEL 1 → Tablet <br>
BT_SEL 2 → Mac <br>
Dengan begitu, Anda hanya perlu mengganti slot saat berpindah perangkat.
