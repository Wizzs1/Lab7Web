| 🐻 | DATA MAHASISWA |
| -------- | --- |
| **Nama** | Wisnu Ikhwansyah Saputra|
| **NIM** | 312010305 |
| **Kelas** | TI.22.A3 |
| **Mata Kuliah** | Pemrograman Web |

---

## Tugas
Buatlah File PHP dengan nama FORM INPUT DATA.php

### code

    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta http-equiv="X-UA-Compatible" content="IE=edge">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Form input data</title>
    </head>
    <body>
        <h2>Data Diri</h2>
        <form method="POST">
            <fieldset>
            <legend>Form Input data</legend>
            <p>
                <label>Nama :</label>
                <input type="text" name="nama" placeholder="Masukan Nama " />
            </p>
            <p>
                <label>Tanggal Lahir :</label>
                <input type="date" name="tgl_lahir" />
            </p>
            <p>
                <label>Pekerjaan :</label>
                <select name="pekerjaan">
                    <option value="Web Developer">Web Developer</option>
                    <option value="Karyawan Swasta">Karyawan Swasta</option>
                    <option value="Guru">Guru</option>
                    <option value="Dan Lainnya">Dan Lainnya</option>
                </select>
            </p>
            <p>
                <label>Gaji :</label>
                <select name="gaji">
                    <option value="2.000.000 s/d 3.500.000">2.000.000 s/d 3.500.000</option>
                    <option value="3.500.000 s/d 7.000.000">3.500.000 s/d 7.000.000</option>
                    <option value="7.000.000 s/d 10.000.000">7.000.000 s/d 10.000.000</option>
                    <option value="Dan Lainnya">Dan Lainnya</option>
                </select>
            </p>
            <p>
                <input type="submit" name="submit" value="Kirim" />
            </p>
            </fieldset>
        </form>
    
        <fieldset>
        <legend>Hasil</legend>
        <?php
        $nama = @$_POST['nama'];
        $tgl_lahir = @$_POST['tgl_lahir'];
        $pekerjaan = @$_POST['pekerjaan'];
        $gaji = @$_POST['gaji'];
    
        $tanggal_lahir = new DateTime(@$_POST['tgl_lahir']);
        $sekarang = new DateTime("today");
        if ($tanggal_lahir > $sekarang) { 
        $umur = "0";
        }
        $umur = $sekarang->diff($tanggal_lahir)->y;
        
        echo "Nama = $nama <br>";
        echo "Umur = $umur tahun <br>";
        echo "Pekerjaan = $pekerjaan <br>";
        echo "Gaji = $gaji <br>";
        ?>
        </fieldset>
    </body>
    </html>

### Output

<img width="960" alt="Screenshot 2023-11-15 221549" src="https://github.com/Wizzs1/Lab7Web/assets/110619093/1f550117-c842-46a1-9d02-14f3aba95413">
