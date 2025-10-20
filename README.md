# Lab5-Web
# Nama : Vivit Nurul Hidayah
# NIM : 312410110
# Kelas : TI.24.A1

# Laporan Praktikum
1. Buatlah repository baru dengan nama Lab5Web.
2. Kerjakan semua latihan yang diberikan sesuai urutannya.
3. Screenshot setiap perubahannya.
4. Buatlah file README.md dan tuliskan penjelasan dari setiap langkah praktikum beserta
screenshotnya.
5. Commit hasilnya pada repository masing-masing.
6. Kirim URL repository pada e-learning ecampus

# Tugas
1. Buat script untuk melakukan validasi pada isian form.

# Input Program (Validasi form) 
```<!DOCTYPE html>
<html lang="en">
<head>
    <title>Validasi Form</title>
    <script>
        function validateForm() {
            var nama = document.forms["myForm"]["nama"].value;
            var email = document.forms["myForm"]["email"].value;
            var password = document.forms["myForm"]["password"].value;

            // Validasi Nama
            if (nama == "") {
                alert("Nama tidak boleh kosong!");
                return false;
            }

            // Validasi Email
            if (email == "") {
                alert("Email tidak boleh kosong!");
                return false;
            }
            var formatEmail = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;
            if (!email.match(formatEmail)) {
                alert("Format email tidak valid!");
                return false;
            }

            // Validasi Password
            if (password == "") {
                alert("Password tidak boleh kosong!");
                return false;
            }
            if (password.length < 6) {
                alert("Password minimal 6 karakter!");
                return false;
            }

            alert("Form berhasil dikirim!");
            return true;
        }
    </script>
</head>
<body>
    <h2>Form Validasi</h2>
    <form name="myForm" onsubmit="return validateForm()">
        Nama: <input type="text" name="nama"><br><br>
        Email: <input type="text" name="email"><br><br>
        Password: <input type="password" name="password"><br><br>
        <input type="submit" value="Kirim">
    </form>
</body>
</html>
```

# Output Program 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/cbf8e6b3-bea0-4ef5-82ed-a3f6492b52ca" />

# Penjelasan Program 
Program ini digunakan untuk mengecek apakah input pada form sudah diisi dengan benar sebelum dikirim. Validasi dilakukan menggunakan JavaScript melalui fungsi validateForm().
Ada tiga data yang dicek:
- Nama – Tidak boleh kosong
- Email – Tidak boleh kosong dan harus sesuai format (contoh: nama@gmail.com)
- Password – Tidak boleh kosong dan minimal 6 karakter
Jika ada input yang tidak sesuai, program akan menampilkan pesan peringatan menggunakan alert() dan menghentikan pengiriman form (return false).
Jika semua data valid, muncul pesan “Form berhasil dikirim!” dan form boleh diproses (return true).
Dengan adanya validasi ini, data yang dikirim menjadi lebih aman, lengkap, dan tidak kosong


# Input Program (lab5_javascript)
``` <!DOCTYPE html>
<html lang="en">
<head>
    <title>Mengenal JavaScript</title>
</head>
<body>
    <h1>Pengenalan JavaScript</h1>
    <h3>Contoh document.write dan console.log</h3>
    <script>
        document.write("Hello World");
        console.log("Hello World");
    </script>
</body>
</html>
```
# Output Program 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/539720a8-2128-4ef8-8389-f280286280b9" />

# Input Program (Alert)
``` <!DOCTYPE html>
<html lang="en"> 
<head>
    <title>alert box</title>
</head>
<body>
    <script language = "JavaScript">
        window.alert("ini merupakan pesan untuk anda")
    </script>
</body>
</html>
```
# Output Program 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/59f9a9b8-0a70-40a0-b269-6be1b60cf7c0" />

# Input Program (Aritmatika.html)
```<!DOCTYPE html>
<html lang="en">
<head>
    <title>Contoh Program JavaScript</title>
    <script language = "JavaScript">
    function test (val1,val2)
    {
        document.write("<br>"+"Perkalian: val1*val2"+"<br>")
        document.write(val1*val2)
        document.write("<br>"+"pembagian: val1/val2"+"<br>")
        document.write(val1/val2)
        document.write("<br>"+"Penjumlahan: val1+val2"+"<br>")
        document.write(val1+val2)
        document.write("<br>"+"Pengurangan: val1-val2"+"<br>")
        document.write(val1-val2)
        document.write("<br>"+"Modulus: val1%val2"+"<br>")
        document.write(val1%val2)

    }
    </script>
</head>
<body>
    <input type ="button" name = "button1" value ="arithmetic" onclick=test(9,8)>
</html>
```
# Output Program
<img width="1365" height="223" alt="image" src="https://github.com/user-attachments/assets/01e47b7e-356b-4681-bfdb-87c0cf524f57" />
<img width="1365" height="321" alt="image" src="https://github.com/user-attachments/assets/0d307938-1673-41d3-a218-e0705e14763f" />

# Input Program (Form_INput.html)
```<!DOCTYPE html>
<html lang="en">
<head>
    <script language = "JavaScript">
    function test() {
        var val1 =document.kirim.T1.value
        if (val1%2==0)
            document.kirim.T2.value ="bilangan genap"
        else
            document.kirim.T2.value ="bilangan ganjil"
    }
    </script>
</head>
<body>
    <form method="POST" name="kirim">
        <p>BIL <input type ="text" name ="T1" size ="20">
        MERUPAKAN BIL <input type= "text" name= "T2" size= "20"></p>
        <p><input type ="button" value="TEBAK" name="B1" onclick="test()"></p>
    </form>
</body>
</html>
```
# Output Program 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/83bf2c43-7f98-4de5-94b5-11fc1e17a7d0" />

# Input Program (Form buttom)
```<!DOCTYPE html>
<html lang="en">
<head>
    <title>Objek Document</title>
</head>
<body>
    <script language="JavaScript">
    function ubahWarnaLB(warna){
        document.bgColor = warna;
    }
    function ubahWarnaLD(warna){
        document.fgColor = warna;
    }
    </script>

    <h1>Test Web</h1>
    <form>
        <input type ="button" value ="Latar Belakang Hijau" onclick="ubahWarnaLB('GREEN')">
        <input type ="button" value ="Latar Belakang Putih" onclick="ubahWarnaLB('WHITE')">
        <input type ="button" value ="Teks Kuning" onclick="ubahWarnaLD('YELLOW')">
        <input type ="button" value ="Teks Biru" onclick="ubahWarnaLD('BLUE')">   
    </form>
    <script language ="JavaScript">
        document.write("Dimodifikasi terakhir pada" +
        document.lastModified);
    </script>
</body>
</html>
```

# output Program 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/aa6ba667-a0ba-488a-a752-d18d58bd6d67" />
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/2cfcc797-900e-42c4-8907-c1409118f1b4" />

# Input Program (Fungsi)
```<!DOCTYPE html>
<html lang="en">
<head>
     <title>Contoh Program JavaScript</title>
    <script language = "JavaScript">
    function pesan(){
        alert ("Memanggil JavaScript lewat body onload")
    }
    </script>
</head>
<body onload= pesan()>
</html>
```
# Output Program 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/81b6606a-b74f-49f9-beed-640e6616bd7f" />

# Input Program ( if-else)
``` <!DOCTYPE html>
<html lang="en">
<head>
    <script language ="JavaScript">
        var nilai = prompt("nilai (0-100):", 0);
        var hasil ="";
        if (nilai >=60)
        hasil = "lulus";
        else 
        hasil ="tidak lulus";
    document.write("hasil:" +hasil);
    </script>
</head>
</html>
```
# Output Program 
<img width="1365" height="419" alt="image" src="https://github.com/user-attachments/assets/8ac7ddcc-78ae-4842-9232-e9817df0f4d7" />
<img width="304" height="184" alt="image" src="https://github.com/user-attachments/assets/dcda1161-0e57-45ea-84d5-c23eeee97aa8" />

# Input Program (Method)
``` <!DOCTYPE html>
<html lang="en">
<head>
    <title>skrip JavaScript</title>
</head>
<body>
    percobaan memakai JavaScript:<br>
    <script language = "JavaScript">
        document.write("selamat mencoba JavaScript<br>")
        document.write("semoga sukses");
    </script>
</body>
</html>
```
# Output Program
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/4f780fd5-05eb-4a87-a635-212c03ba9e6e" />

# Input Program (Switch)
``` <!DOCTYPE html>
<html lang="en">
<head>
    <title>Contoh Program JavaScript</title>

    <script language ="JavaScript">
    function test ()
    {
        val1 =window.prompt("input nilai (1-5):")
        switch (val1)
        {
            case "1":
                document.write("bilangan satu")
                break;
            case "2":
                document.write("bilangan dua")
                break;
            case "3":
                document.write("bilangan tiga")
                break;
            case "4":
                document.write("bilangan empat")
                break;
            case "5":
                document.write("bilangan lima")
                break;
            default : 
                document.write("bilangan lainnya")

        }
    }
    </script>
</head>
<body>
    <input type ="button" name="button1" value ="switch" onclick=test()>
</body>
</html>
```
# Output Program 
<img width="486" height="179" alt="image" src="https://github.com/user-attachments/assets/b57eaad2-8658-471b-8f1f-5bc67a38b81c" />
<img width="1365" height="327" alt="image" src="https://github.com/user-attachments/assets/a0be8395-9dfd-4a37-a84c-2037f44ad03f" />
<img width="256" height="168" alt="image" src="https://github.com/user-attachments/assets/a7f16775-3f8a-4a55-b4a7-94a1b0aaa4b6" />

# Input Program (Prompt)
``` <!DOCTYPE html>
<html lang="en">
<head>
    <title>Pemasukan Data</title>
</head>
<body>
    <script language = "JavaScript">
    var nama = prompt("Siapa nama anda?","Masukkan nama anda");
    document.write("Hai"+ nama);
    </script>
</html>
```
# Output Program 
<img width="1365" height="343" alt="image" src="https://github.com/user-attachments/assets/fd98db21-eca7-4452-8a3d-c0274294cbc7" />

# Input Program (CheckBox)
``` <!DOCTYPE html>
<html>
<head>
    <title>Daftar Menu</title>
    <script>
        function hitung() {
            var total = document.getElementById('total').value;
            total = (total == "") ? 0 : parseInt(total);
            var harga = 0;

            if (this.checked) {
                harga = parseInt(this.value);
                total = total + harga;
            } else {
                harga = parseInt(this.value);
                total = total - harga;
            }

            document.getElementById('total').value = total;
        }
    </script>
</head>
<body>
    <h3>Daftar Menu Makanan</h3>
    <input type="checkbox" value="5000" id="m1" onclick="hitung.call(this)"> Ayam Goreng Rp. 5.000<br>
    <input type="checkbox" value="3500" id="m2" onclick="hitung.call(this)"> Tempe Goreng Rp. 3.500<br>
    <input type="checkbox" value="2000" id="m3" onclick="hitung.call(this)"> Tahu Goreng Rp. 2.000<br>
    <input type="checkbox" value="1000" id="m4" onclick="hitung.call(this)"> Sambal Rp. 1.000<br>
    <input type="checkbox" value="3000" id="m5" onclick="hitung.call(this)"> Telur Dadar Rp. 3.000<br><br>

    <strong>Total Bayar: Rp. 
        <input type="text" id="total" readonly>
    </strong>
</body>
</html>
```

# Output Program 
<img width="1366" height="768" alt="image" src="https://github.com/user-attachments/assets/3f81f7a9-7cf8-4f39-a89d-36a417efd4f4" />















