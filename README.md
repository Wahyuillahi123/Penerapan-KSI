# Penerapan-KSI-Menggunakan-Kriptografi
Implementasi Keamanan Sistem Informasi Dengan Kriptografi Caesar Cipher Pada Fitur Login Di Aplikasi Sekolah Kita Berbasis Website.

# Install NPM
``` html
$ npm install cryptr
```

# Algoritma Sederhana
Javascript
``` html
  <script>

    setInterval(function(){

      var urutanabjad = 'ABCDEFGHIJKLMNOPQRSTUVWXYZ';
      var balikanjad =  'ZYXWVUTSRQPONMLKJIHGFEDCBAZYXWVUTSRQPONMLKJIHGFEDCBA';
      var output='';

      const plaintext = document.querySelector('#plaintext').value;
      console.log(plaintext);
      const arah = document.querySelector('#arah').value;
      console.log(arah);
      var pergeseran = document.querySelector('#pergeseran').value;
      pergeseran=pergeseran/1;
      console.log(pergeseran);

      //ULANGI SESUAI BANYAK NILAI YG MASUK;
      for(var i=0;i<plaintext.length;i++){
        //mengetahui huruf apa di index tertentu;
        //misal dalam variabel plaintext di index ke(i) adalah huruf 'w';
        var huruf=plaintext.charAt(i);//w
        //setelah mengetahui suatu huruf di index tertentu,
        //cari dalam variabel urutanabjad urutan berapa huruf itu misal 'w';
        var urutanabjadd=urutanabjad.indexOf(huruf);//23
          //================================================
            //logika;
            if(arah=='kanan'){
              
              urutanabjadd=urutanabjadd+pergeseran;
              console.log(urutanabjadd);
            }
            if(arah=='kiri'){
              
              urutanabjadd=26+(urutanabjadd-pergeseran);
              console.log(urutanabjadd);
            }
          //================================================
        //setelah mengetahui nomer urut suatu huruf dalam variabel urutanabjad;
        //lalu cari urutan yg didapat akan diubah ke huruf apa? balikanjad;
        //contoh huruf "w" menjadi "d", dengan mencari sesuai index urutanabjad yg didapat;
        var balikanjadd=balikanjad.charAt(urutanabjadd);//d

        //setelah selesai push ke variabel output;
        output=output+balikanjadd;
        console.log(output);
      }

      var hasil = document.querySelector('.hasil').innerHTML='Hasil : '+output; 

    },100);
    
  </script>
    
```

Html
``` html
    <div class="container">
      <div class="row">
        <div class="col-lg-3"></div>
        <div class="col-lg-6">
          <div class="card">
            <div class="card-header hasil">Hasil :</div>
            <div class="card-body">
              <form id="cek" name="cek" class="cek">
                <div class="form-group">
                  <label for="exampleInputEmail1">Masukan Plaintext</label>
                  <input type="text" class="form-control" id="plaintext" name="plaintext" placeholder="JASAKUMEDIA" />
                  <small id="emailHelp" class="form-text text-muted">Kalimat yang akan di enkripsi, gunakan huruf besar</small>
                </div>
                <select class="form-control form-control-sm" id="arah" name="arah">
                  <option value="kanan">Geser Kanan</option>
                  <option value="kiri">Geser Kiri</option>
                </select>
                <div class="form-group">
                  <label for="exampleInputPassword1">Jumlah Pergeseran</label>
                  <input type="text" class="form-control" id="pergeseran" name="pergeseran" placeholder="misal geser 3" />
                </div>
                <button type="submit" class="btn btn-primary col-lg-12">Reset Ulang</button>
              </form>
            </div>
          </div>
        </div>
        <div class="col-lg-3"></div>
      </div>
    </div>
```

# Support
Follow my instagram : https://www.instagram.com/wahyu_illahi07/ 
Youtube Channel : https://www.youtube.com/playlist?list=PL2DC6n3PrEKVXN9nvzONe9idXa9BgCusj
