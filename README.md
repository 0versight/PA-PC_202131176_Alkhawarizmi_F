# Ujian Akhir Semester melakukan Praktik Remove Background


# Dasar Teori
  ## I. Pendahuluan

A. Penghapusan latar belakang adalah teknik penting dalam pemrosesan gambar yang memisahkan subjek gambar dari latar belakangnya. 

B. Teknik ini banyak digunakan di berbagai industri, termasuk e-commerce, periklanan, forensik, dan pencitraan medis, hingga peningkatan kualitas gambar dan fokus pada elemen-elemen tertentu dalam sebuah gambar.

  ## II. Apa itu Penghilangan Latar Belakang?

A. Penghapusan latar belakang adalah proses pemisahan latar depan (subjek gambar) dari latar belakang (background).  

B. Teknik ini sangat penting dalam pemrosesan gambar, karena memungkinkan kita untuk fokus pada subjek dengan menghilangkan elemen apa pun yang mengganggu di latar belakang.

C. Namun, menghapus latar belakang secara akurat dari gambar dapat menjadi tantangan karena faktor-faktor seperti latar belakang yang kompleks, detail rumit pada subjek, dan berbagai kondisi pencahayaan.

  ## III. Teknik Penghilangan Latar Belakang
Ada beberapa teknik manual dan otomatis untuk menghapus latar belakang:

A. Teknik manual meliputi:
- Metode Jalur Kliping: Teknik Ini melibatkan pembuatan jalur di sekitar subjek dan menghapus latar belakang.
- Teknik Masking Gambar: Teknik ini digunakan ketika subjek dan latar belakang memiliki warna yang sama atau ketika subjek memiliki detail yang rumit seperti rambut atau bulu.
- Alat Penghapus Latar Belakang: Alat ini terdapat dalam perangkat lunak editor gambar yang dapat digunakan untuk menghapus latar belakang secara manual.

B. Teknik otomatis meliputi:
- Segmentasi Berbasis Warna: Teknik ini memisahkan subjek dan latar belakang berdasarkan perbedaan warnanya.
- Thresholding: Teknik Ini melibatkan pengaturan nilai ambang batas untuk memisahkan subjek dan latar belakang berdasarkan nilai pikselnya.
- Algoritma Machine Learning: Algoritma ini dapat dilatih untuk mengidentifikasi dan menghapus latar belakang dari gambar secara akurat.

## IV. Bagaimana Penghilangan Latar Belakang Bekerja?

A. Penghapusan latar belakang bekerja dengan mengidentifikasi perbedaan antara subjek dan latar belakang. Ini dapat didasarkan pada warna, nilai piksel, atau fitur pembeda lainnya. 

B. Proses ini melibatkan beberapa langkah, termasuk segmentasi gambar, ekstraksi fitur, dan pengeditan gambar.

## V. Keuntungan dan Aplikasi Penghilangan Latar Belakang

A. Penghapusan latar belakang dapat secara signifikan meningkatkan kualitas gambar dengan memfokuskan pada subjek. 

B. Aplikasi ini banyak digunakan dalam:
- Fotografi produk e-commerce: Untuk menyorot produk dengan menghapus latar belakang yang mengganggu.
- Desain grafis dan iklan: Untuk membuat visual yang menarik dengan menggabungkan gambar yang berbeda.
- Analisis forensik: Untuk fokus pada elemen tertentu dalam gambar untuk analisis yang lebih terperinci.
- Pencitraan medis: Untuk mengisolasi struktur atau wilayah tertentu untuk visualisasi dan analisis yang lebih baik.

## VI. Kesimpulan

A. Penghapusan latar belakang memainkan peran penting dalam gambar, yang secara signifikan berdampak pada berbagai industri dan aplikasi. 

B. Terlepas dari tantangannya, Teknik ini terus menjadi teknik penting dalam meningkatkan kualitas gambar dan memfokuskan pada elemen tertentu dalam gambar. Seiring kemajuan teknologi, kita dapat mengharapkan teknik penghapusan latar belakang yang lebih canggih dan akurat di masa depan.


### Baris Program
```bash
from rembg import remove
from PIL import Image
import matplotlib.pyplot as plt
```

### Gambar Asli
```bash
def remove_background(gambar_asli, gambar_hasil):
    input_image = Image.open(gambar_asli)

    plt.subplot(1, 2, 1)
    plt.imshow(input_image)
    plt.title('Gambar Asli')
```
### Menghapus latar belakang
    output_image = remove(input_image)
### Menampilkan gambar setelah latar belakang dihapus
    plt.subplot(1, 2, 2)
    plt.imshow(output_image)
    plt.title('Gambar tanpa Background')
### Menyimpan gambar yang telah dihapus latar belakang
```bash
    output_image.save(gambar_hasil)
    
    plt.tight_layout()
    plt.show()
gambar_asli = 'ALE.jpg'
gambar_hasil = 'ALE_OUTPUT.png'
remove_background(gambar_asli, gambar_hasil)
```
## Penjelasan baris program
1. from rembg import remove

2. from PIL import Image

3. import matplotlib.pyplot as plt

4. def remove_background(gambar_asli, gambar_hasil):
   
5. input_image = Image.open(gambar_asli)

6. plt.subplot(1, 2, 1)

7. plt.imshow(input_image)

8. plt.title('Gambar Asli')

9. output_image = remove(input_image)

10. plt.subplot(1, 2, 2)

11. plt.imshow(output_image)

12. plt.title('Gambar tanpa Background')

13. output_image.save(gambar_hasil)
    
14. plt.tight_layout()

15. plt.show()

16. gambar_asli = 'ALE.jpg'

17. gambar_hasil = 'ALE_OUTPUT.png'

18. remove_background(gambar_asli, gambar_hasil)
