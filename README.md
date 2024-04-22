# Daka-Heldian_2113025020_UTS-Augmented-Reality
Nama : Daka Heldian
NPM  : 2113025020
Mata Kuliah Augmented Reality-Semester 6-PTI

Deskripsi tugas:
buatlah halaman web yang dapat menampilkan AR berupa::
rumah yang dihasilkan dari penggabungan minimal 5 objek 3D :: 30 poin
terdapat teks AR yang merupakan nama dan NPM kalian :: 20 poin
sertakan teks AR yang menjadi penjelasan pada setiap objek (mengenai bagian apa dalam rumah yang dibentuk) :: 10 poin
kirimkan link Github menuju file halaman website tersebut (.html) :: 10 poin
pastikan objek tersebut (rumah) dapat tampil dalam tampilan AR :: 30 poin
deadline:: Minggu, 21 April 2024; 23:59 WIB
pastikan hasil yang kalian kumpulkan berbeda dengan rekan kalian, jika ada yang sama, maka akan disamakan juga nilainya (0)

Source Code:
<!DOCTYPE html>
<html>
<head>
    <title>Rumah 3D - Daka Heldian</title>
    <script src="https://aframe.io/releases/1.2.0/aframe.min.js"></script>
</head>
<body>
    <a-scene>
        <!-- Nama dan NPM (a-text) -->
        <a-text value="DAKA HELDIAN (2113025020)" position="0 7 -1" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="12"></a-text>

        <!-- Atap Rumah (a-cone) -->
        <a-cone position="5.5 4 -5" height="3" radius-bottom="6" color="brown"></a-cone>
        <a-cone position="0 4 -5" height="3" radius-bottom="5" color="brown">
            <a-text value="Atap Rumah" position="0 2 0" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="8"></a-text>
        </a-cone>

        <!-- Badan Rumah (a-box) -->
        <a-box position="0 1 -5" width="6" height="4" depth="4" color="red"></a-box>
        <a-box position="6 1 -5" width="8" height="4" depth="4" color="yellow">
            <a-text value="Badan Rumah (tembok)" position="-2 -1.3 2.2" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="8"></a-text>
        </a-box>

        <!-- Pintu (a-box) -->
        <a-box position="-1.5 0 -4" width="1.5" height="3" depth="2" color="brown">
            <a-text value="Pintu" position="-0.1 0.5 1" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="8"></a-text>
        </a-box>

        <!-- Jendela (a-box) -->
        <a-box position="0.6 0.7 -4" width="1.5" height="1.5" depth="2" color="blue">
            <a-text value="Jendela" position="0 0.5 1" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="8"></a-text>
        </a-box>
        <a-box position="4.5 0.7 -4" width="1.5" height="1.5" depth="2" color="blue">
            <a-text value="Jendela" position="3 0.5 1" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="8"></a-text>
        </a-box>
        <a-box position="7.6 0.7 -4" width="1.5" height="1.5" depth="2" color="blue">
            <a-text value="Jendela" position="-3.2 0.5 1" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="8"></a-text>
        </a-box>

        <!-- Latar (a-plane) -->
        <a-plane position="0 -1 -5" rotation="-90 0 0" width="30" height="20" color="green"></a-plane>
        <a-text value="Latar Rumput" position="-2 -0.5 2.2" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="5"></a-text>


        <!-- Cerobong Asap (a-cylinder) -->
        <a-cylinder position="8.5 4 -5" rotation="0 45 0" radius="0.2" height="2" color="#445451"></a-cylinder>
        <a-text value="Cerobong Asap" position="7.5 5.5 -5" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="8"></a-text>

        <!-- Pohon (mix) -->
        <a-sphere position="-8 4 -4" radius="1.8" color="green"></a-sphere>
        <a-cylinder position="-8 1 -4" rotation="0 45 0" radius="0.2" height="5" color="#592101">
            <a-text value="Pohon" position="-1.5 1 1" color="#000000" align="center" width="8" font="https://cdn.aframe.io/fonts/mozillavr.fnt" font-size="8"></a-text>
        </a-cylinder>
        
        <!-- Dalam atap dan Kamera -->
        <a-light type="ambient" color="#445451"></a-light>
        <a-light type="point" intensity="2" position="2 4 4"></a-light>
        
        <!-- Kamera Augmented Reality (AR) dengan kursor dan kontrol keyboard -->
        <a-entity camera look-controls wasd-controls position="0 1.6 0" cursor="rayOrigin: mouse;"></a-entity>

        <!-- Latar Belakang (a-sky) -->
        <a-sky color="#87CEEB"></a-sky>
    </a-scene>
</body>
</html>


