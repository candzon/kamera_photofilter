
## Penjelasan Konsep pada tugas Praktikum

### 1. **Maksud `void async`**
`void async` adalah kombinasi dari dua konsep dalam Dart:
- **`void`**: Menunjukkan bahwa fungsi tersebut tidak mengembalikan nilai apa pun.
- **`async`**: Menandakan bahwa fungsi tersebut bersifat asinkron (asynchronous), artinya fungsi tersebut dapat menjalankan operasi yang membutuhkan waktu tanpa memblokir eksekusi kode lainnya.

#### Contoh:
```dart
void fetchData() async {
  print('Fetching data...');
  await Future.delayed(Duration(seconds: 2)); // Simulasi operasi async
  print('Data fetched!');
}
```

#### Penjelasan:
- Fungsi `fetchData` tidak mengembalikan nilai (`void`).
- Fungsi ini bersifat asinkron (`async`), sehingga dapat menggunakan `await` untuk menunggu operasi yang memakan waktu (seperti `Future.delayed`).
- `await` akan menunda eksekusi kode berikutnya sampai operasi selesai.

#### Kegunaan:
- Digunakan untuk menangani operasi yang membutuhkan waktu, seperti:
  - Mengambil data dari API.
  - Membaca/menulis file.
  - Menjalankan animasi atau timer.

---

### 2. **Fungsi Anotasi `@immutable`**
Anotasi `@immutable` digunakan untuk menandai sebuah kelas sebagai **immutable**, artinya objek dari kelas tersebut tidak dapat diubah setelah dibuat (bersifat _read-only_).

#### Contoh:
```dart
@immutable
class User {
  final String name;
  final int age;

  User(this.name, this.age);
}
```

#### Penjelasan:
- `@immutable` memastikan bahwa semua properti di dalam kelas harus bersifat `final` (tidak dapat diubah setelah diinisialisasi).
- Jika Anda mencoba mengubah properti setelah objek dibuat, compiler akan memberikan error.

#### Kegunaan:
- Meningkatkan keamanan dan kejelasan kode dengan memastikan objek tidak berubah setelah dibuat.
- Berguna untuk objek yang sering dibagikan atau digunakan di banyak tempat, seperti state management di Flutter.

---

### 3. **Fungsi Anotasi `@override`**
Anotasi `@override` digunakan untuk menandai bahwa sebuah metode di kelas anak (subclass) **menggantikan** (override) metode yang sudah ada di kelas induk (superclass).

#### Contoh:
```dart
class Animal {
  void makeSound() {
    print('Some generic sound');
  }
}

class Dog extends Animal {
  @override
  void makeSound() {
    print('Woof!');
  }
}
```

#### Penjelasan:
- `@override` menunjukkan bahwa metode `makeSound` di kelas `Dog` menggantikan metode `makeSound` di kelas `Animal`.
- Jika Anda salah mengeja nama metode atau metode tersebut tidak ada di superclass, compiler akan memberikan peringatan.

#### Kegunaan:
- Memastikan bahwa metode yang di-override benar-benar ada di superclass.
- Meningkatkan kejelasan kode dengan menunjukkan bahwa metode tersebut adalah implementasi ulang dari metode superclass.

---

## Ringkasan
- **`void async`**: Digunakan untuk fungsi asinkron yang tidak mengembalikan nilai.
- **`@immutable`**: Menandai kelas sebagai immutable (tidak dapat diubah setelah dibuat).
- **`@override`**: Menandai metode yang menggantikan metode dari superclass.


## Screenshots

- **`Tugas 1 Kamera`**
<img alt="Kamera" src="https://github.com/candzon/kamera_photofilter/blob/main/kamera.png?raw=true" width="70%">

- **`Tugas 2 Photo Filter`**
<img alt="Photo Filter" src="https://github.com/candzon/kamera_photofilter/blob/main/photofilter.png?raw=true" width="70%">

- **`Tugas 3 Kamera Photo Filter`**
<img alt="Kamera Photo Filter" src="https://github.com/candzon/kamera_photofilter/blob/main/kamera_photofilter.png?raw=true" width="70%">


---
