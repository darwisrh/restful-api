# RESTFUL API
![alt text](./images/rest-api.png "Restful API Architecture")
## Integrasi Aplikasi
Secara garis besar terdapat 4 cara untuk melakukan integrasi aplikasi, yaitu :
  ### - File sharing
      - Merupakan cara integrasi aplikasi untuk berbagi file
      - Integrasi menggunakan file sharing adlah hal yang paling mudah dilakukan
      - Biasanya aplikasi yan memiliki data akan membuat file, dan yang membutuhkan data akan membaca data tersebut dari file
      - File sharing sangat bermanfaat ketika integrasi dilakukan antara aplikasi yang tidak terhubung secara langsung
  
  ### - Database sharing
      - Merupakan integrasi antara aplikasi yang memanfaatkan database untuk berbagi data 
      - Database sangat mudah dilakukan ketika aplikasi berada ditempat yang sama dan mengakses data yang sama
      - Aplikasi hanya perlu menyimpan data ke database secara langsung
  
  ### - Remote Procedur Invocation
      - Merupakan mekanisme integrasi antara aplikasi dengan cara membuat API yang bisa digunakan oleh aplikasi lain
      - Aplikasi yang memilki data akan meembuat API, dan aplikasi yang membutuhkan data akan menggunakan API untuk mendapatkan data dari aplikasi tesebut
      - Cara ini terbilang sulit, tapi juga yang paling populer
      - Hal ini karena merupakan Remote Procedur Invocation, integrasi bisa dilakukan dengan cara real-time, dan kompleksitas internal data aplikasi tidak perlu di ekspos ke aplikasi lain

  ### - Messaging
      - Merupakan cara integrasi aplikasi yang memanfaatkan aplikasi message broker atau message bus
      - Aplikasi yang memiliki data akan mengirim data ke aplikasi message broker, dan aplikasi yang membutuhkan data akan mengambil data dari message broker
      - Messaging sekilas mirip dengan RPI, namun yang membedakan adalah, messaging tidak real-time, kadang butuh waktu sampai ke aplikasi yang menerima data, sederhananya proses di Messaging data adalah 'Asynchronous' sedangkan proses di RPI adalah 'Synchronous'.

## Pengenalan API
  - API singkatan dari Application Programming Interface
  - API adalah perantara untuk menghubungkan satu pihak dengan pihak lain agar bisa saling berkomunikasi
  API berisi kumpulan prosedur, fungsi, cara berkomunikasi atau peralatan untuk berkomunikasi
  - Pihak yang terlibat dalam API bisa dalam bentuk perangkat kunak ataupun perangkat keras
  - API sebenarnya sama dengan RPI, hanya sekarang lebih populer dengan istilah API daripada RPI
  
  ### Contoh penggunaan API 
  Saat kita menggunakan sistem operasi, sistem operasi tidak bisa langsung berkomunikasi dengan perngkat keras, sistem operasi membutuhkan API berupa driver yang perlu dipasang terlebih dahulu agar perangkat keras bisa terdeteksi oleh sistem operasi.

  ### Contoh Implementasi API
  - Driver perangkat keras, sebagai API untuk sistem operasi
  - SOAP (Simple Object Access Protocol)
  - CORBA (Common Object Request Broker Architecture)
  - RESTful API
  - Apache Thrift
  - Protocol Buffer
  - GRPC
  - Etc.

## Pengenalan RESTful API
  - REST singkatan dari REpresentational State Transfer
  - RESTful API merupakan salah satu implementasi API yang memanfaatkan HTTP sebagai protokol komunikasinya
  - Walaupun SOAP juga berjalan diatas HTTP, namun RESful API sangat sederana dibanding SOAP
  - RESTful API sangat mudah digunakan, dan bisa diadaptasi di semua bahasa pemrograman secara mudah 
  - Saat ini RESTful API sudah menjadi standar API yang banyak digunakan ketika kita membuat sistem yang butuh menyediakan API untuk pihak lain

## Kenapa RESTful API
  - Menggunakan HTTP sebagai protokol komunikasi
  - Pembuatan RESTful API sangat mudah karena seperti membuat web pada umumnya
  - Mudah digunkan oleh client baik itu aplikasi web ataupun non web seperti aplikasi desktop ataupun aplikasi mobile
  - Ringan dan mudah dimengerti oleh manusia

## A. Architectural Constraints
  REST (REpresentational State Transfer) merupakan architecture pattern yang dikenalkan olej Roy Fielding tahun 2000. REST didesain berjalan menggunakan HTTP, dan sering digunakan sebagai Web Services. Roy Fielding memperkenalkan beberapa design principal ketika kita akan membuat REST. Berikut adalah beberapa design principal agar web services sesuai dengan RESful API :
  - Client-server
  - Stateless
  - Cacheable
  - Uniform interface
  - Layered system
  - Code on demand