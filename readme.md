<h1>Perubahan apa saja yang dilakukan dari MVC ke clean architecture? </h1>

# Pembuatan Domain
Pada design pattern MVC, tidak ada domain. Pada clean architecture, terdapat domain sebagai layer terluar yang tidak bergantung pada framework. Domain berguna untuk merangkai sebuah model/tabel yang nantinya akan di implementasikan oleh model sehingga dapat terkoneksi ke database

# Pembuatan Abstract method Repository 
Pada design pattern MVC, tiap repository langsung di implementasikan menggunakan tekonologi database tertentu. Namun , di clean architecture terdapat pembuatan abstract method, yaitu method-method yang merupakan rancangan (blueprint) sebuah fungsi. Setelah itu, barulah method-method dari sebuah repository di implementasikan dengan menggunakan teknologi database tertentu. Hal ini berguna untuk menjaga konsistensi data, mempermudah pengujian, dan bila ingin merubah teknologi implementasi, hanya merubah di file-file implementasi nya tanpa harus memikiri perubahan pada bisnis logic(use case)/controllers

# Logika bisnis terpisah
Dalam MVC, logika bisnis sering kali langsung diimplementasikan di Controller, yang membuatnya sulit untuk diuji dan dipelihara. Namun, dalam Clean Architecture, logika bisnis dipisahkan ke dalam Use Case (Interactor), sehingga arsitektur menjadi lebih modular, fleksibel, dan mudah diuji.