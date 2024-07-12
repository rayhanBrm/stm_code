# Proyek STM32CubeIDE

Repositori ini berisi kode yang dihasilkan dari STM32CubeIDE berdasarkan konfigurasi yang ditentukan. Kode yang dihasilkan dapat dikompilasi untuk menghasilkan file `.hex` dan `.bin`, yang kemudian dapat di-flash ke papan STM32 menggunakan STM32 ST-LINK Utility.

## Daftar Isi

- [Ikhtisar Proyek](#ikhtisar-proyek)
- [Struktur File](#struktur-file)
- [Memulai](#memulai)
- [Contoh Kode](#contoh-kode)

## Ikhtisar Proyek

Proyek ini menunjukkan penggunaan STM32CubeIDE untuk menghasilkan dan mengompilasi kode untuk mikrokontroler STM32. Setelah di-flash ke papan, kode akan menjalankan fungsionalitas yang diinginkan seperti yang didefinisikan dalam file `main.c`.

## Struktur File

- `Core/src/main.c`: Ini adalah file utama yang dihasilkan oleh STM32CubeIDE. Kode yang relevan terletak antara baris 90 dan 102.

## Memulai

Ikuti langkah-langkah ini untuk menyiapkan dan menjalankan proyek:

1. **Konfigurasi Awal**: Pastikan konfigurasi yang diinginkan telah ditentukan di STM32CubeIDE.
2. **Generate Kode**: STM32CubeIDE akan menghasilkan kode yang diperlukan, termasuk `main.c`.
3. **Kompilasi Proyek**: Kompilasi proyek untuk menghasilkan file `.hex` dan `.bin`.
4. **Flash ke Papan**:
   - Gunakan STM32 ST-LINK Utility untuk mengunggah file `.hex` atau `.bin` ke papan STM32.
   - Setelah proses unggah selesai, papan akan berisi dan menjalankan kode yang diinginkan.
  
## Contoh Kode

```c
  HAL_GPIO_WritePin(GPIOC, GPIO_PIN_13, GPIO_PIN_SET);

  /* USER CODE END 2 */

  /* Infinite loop */
  /* USER CODE BEGIN WHILE */
  while (1)
  {
    /* USER CODE END WHILE */
	  HAL_GPIO_WritePin(GPIOC, GPIO_PIN_13, 0);
	  HAL_Delay(5000);
	  HAL_GPIO_WritePin(GPIOC, GPIO_PIN_13, 1);
	  HAL_Delay(2000);
	  

