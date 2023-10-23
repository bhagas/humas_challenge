# Library Application with MySql


## Summary

Pada sebuah aplikasi, penggunaan *database* sebagai *persistent storage* sangatlah essentials. *database* membantu kita untuk menyimpan hal-hal yang bersifat dinamis.

## Levels

### Level 0: Store and get it now

Pada release kali ini, kita akan membuat aplikasi kita lebih dinamis dengan menyimpan data-data di dalam array `books` ke dalam sebuah table di `MySQL`. Buatlah sebuah table dengan nama `books` dan skema sebagai berikut:

| Field          | Datatype | Modifiers              |
| :------------- | :------- | :--------------------- |
| id             | SERIAL   | PRIMARY KEY            |
| author         | VARCHAR  | NOT NULL               |
| title          | VARCHAR  | NOT NULL               |
| borrowed_name  | VARCHAR  |                        |
| published_year | INT      |                        |
| is_returned    | BOOL     | NOT NULL DEFAULT FALSE |
| borrowed_date  | DATE     |                        |
| returned_date  | DATE     |                        |

Setelah berhasil, buatlah koneksi antara aplikasi yang kita buat dengan database `MySQL` tersebut.

### Level 1: Create CRUD Operations

Setelah aplikasi berhasil terkoneksi dengan `MySQL`, sekarang saatnya kita membuat CRUD operations pada aplikasi kita.

Buatlah peubahan pada kode kalian untuk dapat melakukan CRUD operations dengan detail seperti dibawah:

| Method | Route          | Keterangan                                                   |
| :----- | :------------- | :----------------------------------------------------------- |
| GET    | /books         | Menampilkan semua data buku yang tersimpan di dalam database |
| POST   | /books         | Menerima data yang dikirimkan melalui form dan melakukan *insertion* pada database |
| PUT    | /books/:id     | Melakukan *update* pada buku berdasarkan `id`yang dikirimkan |
| GET    | /books/search? | Menampilkan semua data buku berdasarkan `querystring` yang dikirimkan |
| DELETE | /books/:id     | Melakukan *delete* action terhadap data buku berdasarkan `id` yang dikirimkan |

Silahkan pastikan perubahan tersebut sesuai dengan halaman-halaman yang telah tersedia berdasarkan fungsinya masing-masing.
