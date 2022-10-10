## writing-week3

# JS Intermediate-Array & JS Intermediate-Multidimensional Array

## JS Intermediate-Array 
Array adalah tipe data list order yang dapat menyimpan tipe data apapun di dalamnya. Array dapat menyimpan tipe data String, Number, Boolean, dan lainnya. Array didefinisikan menggunakan square brackets [] Array pada javascript dihitung dari index data ke-0 data pertama adalah index ke-0.

        let rain = ['hujan', 'angin', 'petir'];
        console.log(rain);

- Update Array
Seperti tipe data dan variabel pada umumnya, kita dapat mengupdate data pada Array. Jika menggunakan let, kita dapat mengubah array dengan array baru dan konten nilai yang ada di dalam array dengan nilai lain namun jika menggunakan Const tidak bisa melakukan update data. Namun pada Array kita dapat melakukan update konten nilai di dalam array (mutable) yang tidak bisa adalah mengubah array dengan array yang baru jika menggunakan const.

        let rain = ['hujan', 'angin', 'petir'];
        rain[1] = 'cerah'
        console.log(rain);
        
        const rain = ['hujan', 'angin', 'petir'];
        rain = ['cerah'];
        console.log(rain);  //Output Error
        
 Array memiliki 5 properti yang sering digunakan yaitu constructor, length, index, input, dan prototype.
 - Array Method
Array memiliki method atau biasa disebut built-in methods Artinya Javascript sudah memudahkan kita dengan menyediakan function/method umum yang bisa kita gunakan. Contoh Array Built-in Methods
      - .push() adalah method untuk menambahkan item  array pada urutan yang paling akhir.
      
               const buah = ["Jeruk", "Apel", "Mangga"];
               buah.push("Kiwi"); //Jeruk, Apel, Mangga, Kiwi
          
     - .pop() adalah method yang menghapus item array index terakhir.
     
              const buah = ["Jeruk", "Apel", "Mangga"];
              buah.pop(); //Jeruk, Apel
              
     - .shift() adalah method untuk menghapus item Array pada index pertama
      
              const buah = ["Jeruk", "Apel", "Mangga"];
              buah.shift(); //Apel, Mangga
              
     - .unshift() adalah method untuk menambahkan item Array pada index pertama
       
              const buah = ["Jeruk", "Apel", "Mangga"];
              buah.unshift("Lemon"); //Lemon, Jeruk, Apel, Mangga

     - .sort() adalah method untuk mengurutkan secara Ascending atau Descending Alphanumeric
     
               const buah = ["Jeruk", "Apel", "Mangga"];
               buah.sort(); //Apel, Jeruk, Mangga

### Looping pada Array

Array memiliki built in methods untuk melakukan looping yaitu .map() dan .forEach() kita harus tahu kapan menggunakan .map() dan juga .forEach()
- .forEach() adalah method untuk melakukan looping pada setiap elemen array.

              const fruits = ["apple", "orange", "cherry"];
              fruits.forEach(myFunction); 
              //0: apple 1: orange 2: cherry

- .map() melakukan perulangan/looping dengan membuat array baru.

             const numbers = [65, 44, 12, 4];
             const newArr = numbers.map(myFunction)

            function myFunction(num) {
            return num * 10;
            }
            
map() dan forEach() sama-sama melakukan looping dan mengembalikan nilai baru dari operasi yang dilakukan perbedaannya adalah .forEach tidak dapat membuat Array baru dari hasil operasi yang ada dalam looping gunakan .forEach() jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.Gunakan .map() jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

## JS Intermediate-Multidimensional Array

Multidimensional Array bisa dianalogikan dengan array of array terdapat array didalam array. 
            let rain = [
            ['hujan', 5],
            ['petir', 2],
            ];
            console.log(rain);

mengakses index multidimensional array

            let rain = [
            ['hujan', 5],
            ['petir', 2],
            ];
            console.log(rain [1]);
            
 Sama seperti array satu dimensi, multidimensional array juga dapat menggunakan Property dan Method built-in Array.

            let rain = [
            ['hujan', 5],
            ['petir', 2],
            ];
            rain.push(['matahari', 4]);
            console.log(rain);
 
### LOOPING FOR MULTIDIMENSIONAL ARRAY

            let studentsData = [['rain', 20], ['fitria', 19],];

            // looping outer array elements
            for(let i = 0; i < studentsData.length; i++){

            // get the length of the inner array elements
            let innerArrayLength = studentsData[i].length;
    
            // looping inner array elements
            for(let j = 0; j < innerArrayLength; j++) {
            console.log(studentsData[i][j]);
            }
            }
           
           
# JS Intermediate-Object

Dalam dunia programming bject adalah sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method), properti adalah data lengkap dari sebuah object, method adalah action dari sebuah object. Apa saja yang dapat dilakukan dari suatu object. Object dapat diassign kedalam sebuah variabel.

            let sun = {
            nama: 'matahari',
            umur: 19,
            isVerified: true,
            }
            
 - Mengakses Object dan Property Object.

            let sun = {
            nama: 'matahari',
            umur: 19,
            isVerified: true,
            }
            console.log(sun);
        
- untuk mengakses properti juga bisa menggunakan bracket notation saat memanggil properti dari sebuah object.
        
            let sun = {
            nama: 'matahari',
            umur: 19,
            isVerified: true,
            }
            console.log(sun ['nama']);
            
Kita dapat melakukan update pada variabel dengan tipe data Object namun jika menggunakan constant pada variable object. Kita tidak bisa mengganti seluruh data object dengan object yang baru. Jadi jika membutuhkan untuk update seluruh data object gunakan ‘let’ pada saat deklarasi variabel. Sedangkan untuk mendelete object property menggunakan **delete** operator.

Jika value yang kita masukkan pada property berupa function maka itu disebut method. Biasanya kita sering menggunakan console.log() console adalah global javascript object.log() adalah property yang berupa function dari object console sehingga kita memanggila dengan cara console.log().

- Nested Object Kita bisa mengubah data yang ada pada object melalui sebuah function dan memasukkan object sebagai parameter function ini biasa disebut passed by reference.
- Looping Object Jika kita ingin menampilkan seluruh object properti. Kita bisa menggunakan looping jadi tidak perlu mengakses secara manual memanggil setiap propertinya.
          
          const object = { a: 1, b: 2, c: 3 };

          for (const property in object) {
          console.log(`${property}: ${object[property]}`);
          }
          
- Array of Object Object sama seperti Array yang bisa menyimpan banyak data kita dapat menggunakan array of object untuk data yang lebih dari satu.
          
          
# Js Intermediate-Recursive

Recursive adalah function yang memanggil dirinya sendiri sampai kondisi tertentu yang kebanyakan digunakan untuk case matematika, fisika, kimia, dan yang berhubungan dengan calculation (Recursive akan berhenti memanggil dirinya sendiri jika kondisi terpenuhi). fungsi rekursif mengeksekusi beberapa kode kemudian menjalankan fungsi lagi kecuali kondisi keluar terpenuhi (yang menghentikan rangkaian pemanggilan itu sendiri) Ciri dari rekursif:
- Fungsi rekursif selalu memiliki kondisi yang menyatakan kapan fungsi tersebut berhenti. Kondisi ini harus dapat dibuktikan akan tercapai, karena jika tidak tercapai   maka kita tidak dapat membuktikan bahwa fungsi akan berhenti, yang berarti algoritma kita tidak benar.
- Fungsi rekursif selalu memanggil dirinya sendiri sambil mengurangi atau memecahkan data masukan setiap panggilannya. Hal ini penting diingat, karena tujuan utama       dari rekursif ialah memecahkan masalah dengan mengurangi masalah tersebut menjadi masalah-masalah kecil.
Contoh Rekursive 

          const recursiveRangeSum = (num, total = 0) => {
          if (num <= 0) {
          return total;
          }
          return recursiveRangeSum(num - 1, total + num);
          };

recursiveRangeSum(3) juga akan mengembalikan 6 alih-alih hanya mendefinisikan num sebagai argumen, juga mendefinisikan total sebagai argumen kedua. Ini karena setiap variabel yang diatur di dalam fungsi rekursif hanya tersedia untuk versi tunggal fungsi tersebut (tidak semuanya), jadi kita perlu meneruskan total ke setiap rekursi fungsi.


# JavaScript Intermediate - Asynchronous - Introduction & JavaScript Intermediate - Asynchronous - Promise

## JavaScript Intermediate - Asynchronous - Introduction 

Pemrograman asinkron adalah teknik yang memungkinkan program untuk memulai tugas yang berpotensi berjalan lama dan masih dapat responsif terhadap peristiwa lain saat tugas itu berjalan, dari pada harus menunggu sampai tugas itu selesai. Setelah tugas itu selesai, program disajikan dengan hasilnya. Pada Javascript, Asynchronous JavaScript and XMLHTTP atau biasa disebut AJAX merupakan salah satu konsep yang menerapkan metode asynchronous dalam menjalankan pekerjaannya. Biasa nya AJAX digunakan untuk melakukan permintaan data (request) dan menangani sebuah tanggapan (handling response), baik response dalam bentuk XML, Javascript ataupun JSON dari sebuah Rest API.

          function makeGreeting(name) {
          return `Hello, my name is ${name}!`;
          }

          const name = 'rain';
          const greeting = makeGreeting(name);
          console.log(greeting);
          // "Hello, my name is rain!"

Di sini, makeGreeting() adalah fungsi sinkron karena pemanggil harus menunggu fungsi tersebut menyelesaikan pekerjaannya dan mengembalikan nilai sebelum pemanggil dapat melanjutkan. Itulah tepatnya yang dapat dilakukan oleh fungsi asinkron. Kode Asynchronous dapat dibuat menggunakan Promise dan Async/Await.

### Penerapan Didalam Javascript

- Event handlers
Event handlers benar-benar merupakan bentuk pemrograman asinkron Beberapa API asinkron awal menggunakan Event handlers dengan cara XMLHttpRequest, yang memungkinkan kita  membuat permintaan HTTP ke server remote  menggunakan JavaScript. Beberapa contoh event yang ada di browser :
    -onchange terjadi saat elemen HTML mengalami perubahan
    -onclick terjadi saat elemen HTML diklik
    -onmouseover terjadi saat elemen HTML mengalami hover
    -onmouseout terjadi saat kursor keluar dari elemen HTML
    -onkeydown terjadi saat user menekan tombol di keyboard
    -onload terjadi saat browser selesai memuat semua elemen HTML

- Callbacks
Callbacks hanyalah fungsi yang diteruskan ke fungsi lain, Callbacks akan dipanggil pada waktu yang tepat. callback merupakan event utama penerapan fungsi asinkron dalam JavaScript namun sebagian besar API asinkron modern tidak menggunakan callback. 

## JavaScript Intermediate - Asynchronous - Promise

A Promise in short:

“Imagine you are a kid. Your mom promises you that she’ll get you a new phone next week.”

You don’t know if you will get that phone until next week. Your mom can really buy you a brand new phone, or she doesn’t.

That is a promise. A promise has three states. They are:

Pending: You don’t know if you will get that phone
Fulfilled: Mom is happy, she buys you a brand new phone
Rejected: Mom is unhappy, she doesn’t buy you a phone

Promise pada javascript didibaratkan seperti **perjanjian** yang dimana sebuah perjanjain awal dibuat memiliki status menunggu sampai terjadi kejadian (event) yang membuatnya terselesaikan (resolved) atau tidak terpenuhi (rejected). Sebuah Promise memiliki 3 status berikut ini

-Tertunda (pending): keadaan awal, kode di dalam Promise akan terus dijalankan hingga callback resolve atau reject terpanggil
-Terpenuhi (resolved): janji berhasil diselesaikan, ditandai dengan terpanggilnya callback function resolve
-Tertolak (rejected): janji tidak bisa terpenuhi, ditandai dengan terpanggilnya callback function reject

          const ifResolved = (pesan) => {
          console.log(`Terpenuhi karena ${pesan}`)
          }
          const ifRejected = (err) => {
          console.log(`Tidak terpenuhi karena ${err}`)
          }

          const myPromise = new Promise((resolve, reject) => {
          let x = 10
          if (x <= 10) {
          resolve("Nilai kurang dari atau sama dengan 10")
          }
          reject("Nilai lebih dari 10")
          }).then(ifResolved, ifRejected)
         // callback function ifResolved akan terpanggil jika status promise resolved
         // callback function ifRejected akan terpanggil jika status promise rejected 


# Js Intermediate-Web Storage

Web storage adalah salah satu Web API yang dapat menyimpan data secara lokal pada sisi client. Berbeda dengan objek atau array, data yang disimpan pada objek atau array JavaScript bersifat sementara, dan akan hilang jika terjadi reload atau pergantian URL pada browser. Sedangkan data yang disimpan pada Web Storage akan bertahan lebih lama karena data akan disimpan pada storage browser. Sebelum HTML5, kita melakukan hal ini dengan menggunakan cookies, namun penyimpanan cookies terbatas. Dengan hadirnya Web Storage kita dapat menampung data lebih besar dan tentunya lebih aman. Web API menyediakan dua tipe Web Storage untuk kita gunakan, yakni sessionStorage dan localStorage.

Pada sessionStorage atau localStorage data yang disimpan adalah nilai primitif seperti number, boolean, atau string. Namun kita juga dapat menyimpan data berbentuk objek dengan mengubahnya dalam bentuk string, begitu pula sebaliknya ketika kita ingin menggunakan datanya kembali.Untuk menyimpan dan mengakses data pada storage, metode yang digunakan adalah key-value. Di sini key menjadi sebuah kunci untuk mengakses data pada storage.

- Cache
Cache dalam web browser adalah teknologi yang diguanakan untuk menyimpan atau asset dapat berupa (data, gambar, file dan dokumen lain sebagainya) ketika website    dimuat pertama kali, sehingga ketika web tersebut di-load kembali akan mejadi lebih cepat karena tidak perlu men-download kembali file-file dari server.

- Cookie
Cookie adalah sebagin kecil dari data yang dikirim dari sebuah situs web dan disimpan dalam komputer pengguna oleh web browser ketika pengguna tersebut sedang membuka halaman dari suatu webiste tertentu. Sebenarnya ketika kita menggunakan web browser sangat sering sekali bekerja dengan cookie, misalkan :
Menyimpan Login informasi pada website yang telah di akses oleh user, menyimpan Configurasi website misal bahasa, memberikan Rekomendasiberdasarkan aktivitas dari web browser dapat berupa iklan, playlist, berita dan lain sebagainya.

- Session Storage 
Session Storage adalah penyimpanan website pada sisi klien yang digunakan untuk menyimpan data selama web-browser atau tab yang memuat halaman suatu website belum ditutup atau keluar (close). Session Storage dalam membangun sistem berbasis website biasanya digunakan untuk menyimpan user identity sebagai login status.

- Local Storage 
Local Storage adalah jenis penyimpanan web yang memungkinkan situs dan aplikasi menyimpan dan mengakses data langsung di browser tanpa tanggalmasa berlaku atau kedaluwarsa. Artinya, data yang disimpan pada web browser akan tetap ada bahkan setelah jendela web browser ditutup. Local Storage hanya dapat dihapus dengan menggunakan JavaScript Command, atau dapat juga menghapushapus data di local storage dengan cara Clear Browser Cache. 


# JavaScript Intermediate - Asynchronous - Fetch & JavaScript Intermdiate - Asynchronous - Async Await

## JavaScript Intermediate - Asynchronous - Fetch

Fetch API menyediakan antarmuka JavaScript untuk mengakses dan memanipulasi bagian protokol, seperti permintaan dan tanggapan. Ini juga menyediakan metode fetch() global yang menyediakan cara mudah dan logis untuk mengambil sumber daya secara asinkron di seluruh jaringan.Fetch merupakan cara baru dalam melakukan network request. Pada dasarnya fungsi fetch memanfaatkan sebuah Promise, sehingga untuk menggunakan nya pastikan browser sudah mendukung Untuk menggunakan fetch, cukup gunakan keyword fetch() kemudian tuliskan URL yang akan dituju di dalam tanda kurung tersebut.

        fetch('http://example.com/movies.json')
       .then((response) => response.json())
       .then((data) => console.log(data));

Karena fetch mengembalikan sebuah Promise, maka untuk response handling nya kita gunakan fungsi then (jika Promise tersebut mengembalikan resolve) dan catch (jika Promise tersebut mengembalikan reject). Jika request pada fetch berhasil dilakukan, maka blok then akan terpanggil dan mengembalikan nilai objek sesuai response yang didapat. Apabila fungsi fetch gagal dilakukan, maka blok catch akan terpanggil dan menampilkan eror pada console. Kemudian untuk mengambil nilai objek yang dikembalikan pada blok then, kita dapat memanggil kembali fungsi then setelah pemanggilan fungsi catch.


## JavaScript Intermdiate - Asynchronous - Async Await

### Async

async function adalah fitur baru dari javascript yang ditambahkan pada tahun 2017. Sebelumnya kita telah belajar menulis kode asynchronous dengan menggunakan Promise, nah Async function adalah cara mudah untuk menjadikan fungsi apapun menjadi Promise dengan hanya menambah keyword async.

        / buat sebuah async function
        const myAsync = async function () {
        let x = 10
        if (x <= 10) {
        // Tidak perlu menggunakan resolve, cukup return
       // untuk memberi tanda bahwa async function selesai
        return "Nilai kurang dari atau sama dengan 10"
        }
        throw Error("Nilai lebih dari 10")
        }

        // Karena Async function menghasilkan Promise
       // maka kita bisa gunakan method then dan catch juga
        myAsync()
        .then((pesan) => {
         console.log(pesan)
        })
        .catch((err) => {
        console.log(err)
        })

### Await

Operator await digunakan untuk menunggu Promise selesai (resolved), nilai yang didapatkan oleh await bisa berupa Promise maupun data biasa dalam bentuk resolved Promised. await hanya bisa digunakan di dalam sebuah async function.

        const getData = async () => {
        let data = await window.fetch("...")
        let obj = await data.json() // dijalankan hanya jika variabel data terisi
        console.log(obj) // dijalankan hanya jika variabel obj terisi
        }

          getData().catch((err) => {
          console.log(err)
      })
      console.log("...")
