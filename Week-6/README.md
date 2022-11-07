# **Writing and Presentation Week 6**

## **BACKEND STAGE**

### **MySQL Basic**

**1. Memahami Database**

<div style="  text-align: justify; text-justify: inter-word;">Database atau basis data adalah kumpulan informadi yang disimpan di dalam komputer secara sistematik sehingga dapat diperiksa menggunakan suatu program komputer untuk memperoleh informasi dari basis data tersebut. Kegunaan utama sistem basis data adalah agar pemakai mampu menyusun suatu pandangan (view) abstraksi data.</div><br />

<div style="  text-align: justify; text-justify: inter-word;">Untuk membuat Database diperlukan sebuah software yang dinamakan dengan DBMS (Database Management System). DBMS adalah sistem software yang digunakan untuk menyimpan, mengatur, dan memastikan data-data tersebut tersimpan dengan aman. Dengan DBMS, user bisa membuat, membaca, memperbarui, dan menghapus data yang ada di database.</div><br />

**2. Memahami Relasi Database**

<div style="  text-align: justify; text-justify: inter-word;">Relasi database adalah suatu hubungan antara satu tabel dengan tabel lainnya. Relasi antar tabel dihubungkan oleh Primary key dan foreign key. Beberapa Relasi Diantaranya:<ul><li>One To One</li><li>One To Many</li><li>Many To Many</li></div><br />

**3. Memahami Tipe Data pada MySQL**

-   **`A. Tipe Data String`**

    ```
    CHAR(size)
    VARCHAR(size)
    TINYTEXT
    TEXT(size)
    ENUM(val1, val2, val3, ...)
    ```

-   **`B. Tipe Data Number`**

    ```
    CHAR(size)
    VARCHAR(size)
    TINYTEXT
    TEXT(size)
    ENUM(val1, val2, val3, ...)
    ```

-   **`C. Tipe Data Waktu`**

    ```
    DATE
    DATETIME(fsp)
    TIMESTAMP(fsp)
    TIME(fsp)
    YEAR
    ```

**3. Memahami dan Melakukan Manipulasi Query Sederhana**

Contoh Sederhana CRUD MySQL

-   **`Create`**

    ```sql
    INSERT INTO tabel (entitas1, entitas2) VALUES(value_1, value_2);
    ```

-   **`Read`**

    ```sql
    SELECT * FROM tabel;
    ```

-   **`Update`**

    ```sql
    UPDATE tabel SET entitas1=value_1, entitas2=value2 WHERE id=2;
    ```

-   **`Delete`**

    ```sql
    DELETE FROM tabel WHERE id=2;
    ```

### **MySQL Lanjutan**

**1. Memahami dan Melakukan Manipulasi Query Tingkat Lanjut yang Sering Digunakan**

-   **`INNER JOIN`**

    ```sql
    SELECT column_name(s)
    FROM table1
    INNER JOIN table2
    ON table1.column_name = table2.column_name;
    ```

-   **`LEFT JOIN`**

    ```sql
    SELECT column_name(s)
    FROM table1
    LEFT JOIN table2
    ON table1.column_name = table2.column_name;
    ```

-   **`RIGHT JOIN`**

    ```sql
    SELECT column_name(s)
    FROM table1
    LEFT JOIN table2
    ON table1.column_name = table2.column_name;
    ```

-   **`MAX`**

    ```sql
    SELECT MAX(column_name)
    FROM table_name
    WHERE condition;
    ```

-   **`MIN`**

    ```sql
    SELECT MIN(column_name)
    FROM table_name
    WHERE condition;
    ```

-   **`SUM`**

    ```sql
    SELECT SUM(column_name)
    FROM table_name
    WHERE condition;
    ```

-   **`COUNT`**

    ```sql
    SELECT COUNT(column_name)
    FROM table_name
    WHERE condition;
    ```

-   **`AVG`**

    ```sql
    SELECT AVG(column_name)
    FROM table_name
    WHERE condition;
    ```

-   **`UNION`**

    ```sql
    SELECT column_name(s) FROM table1
    UNION
    SELECT column_name(s) FROM table2;
    ```

-   **`GROUP BY`**

    ```sql
    SELECT column_name(s)
    FROM table_name
    WHERE condition
    GROUP BY column_name(s);
    ```

-   **`HAVING`**

    ```sql
    SELECT column_name(s)
    FROM table_name
    WHERE condition
    GROUP BY column_name(s)
    HAVING condition
    ORDER BY column_name(s);
    ```

**2. Memahami Relational Antar Table**

<div style="  text-align: justify; text-justify: inter-word;">Beberapa Macam Relasi Pada Database: </div><ul><li>One To One<p>Relasi One to One adalah relasi yang mana setiap satu baris data pada tabel pertama hanya berhubungan dengan satu baris pada tabel kedua.</p></li><li>One To Many<p>Relasi One to Many adalah relasi yang mana setiap satu baris data pada tabel pertama berhubungan dengan lebih dari satu baris pada tabel kedua.</p></li><li>Many To Many<p>Relasi Many to Many adalah relasi yang mana setiap lebih dari satu baris data dari tabel pertama berhubungan dengan lebih dari satu baris data pada tabel kedua. Artinya, kedua tabel masing-masing dapat mengakses banyak data dari tabel yang direlasikan.</p></li></ul><br />

### **Authentication & Authorization**

**1. Memahami Beberapa Variasi Authentication dan Authorization**

<div style="  text-align: justify; text-justify: inter-word;">Ada Beberapa Variasi Mengenai Authentication dan Authorization: </div>
<ul><li>Single Factor Authentication<p>SFA (single factor authentication) adalah jenis autentikasi yang meminta pengguna untuk memasukkan ID pengguna. Kemudian proses autentikasi pun akan berjalan dengan meminta pengguna untuk memasukkan password yang tepat dan sesuai dengan ID pengguna</p></li><li>Multi Factor Authentication<p>Multi-factor Authentication (MFA) merupakan metode otentikasi yang mengharuskan pengguna untuk menyediakan dua atau lebih faktor verifikasi seperti password, otp dan pertanyaan lain</p></ul>

**2. Memahami Perbedaan Authentication, Authorization, dan Encryption**

-   **Authentication**
    <div style="  text-align: justify; text-justify: inter-word;">Authentication adalah proses dimana seorang user (melalui berbagai macam akses fisik berupa komputer dll) mendapatkan hak akses kepada suatu entity.</div>

-   **Authorization**
    <div style="  text-align: justify; text-justify: inter-word;">Authorization adalah proses penentuan apakah user tersebut diizinkan / ditolak untuk melakukan satu atau beberapa action akses terhadap resources tertentu dalam sistem.</div>

-   **Encryption**
    <div style="  text-align: justify; text-justify: inter-word;">Encryption adalah metode pengamanan yang mengubah informasi biasa menjadi kode yang menyembunyikan arti sebenarnya. Ilmu di balik encryption atau enkripsi serta dekripsi informasi dikenal sebagai kriptografi.</div>

**3. Membuat Authentication dan Authorization**

Membuat Authentication dan Authorization Sederhana Menggunakan Express JS dan JWT

```js
const express = require("express");
const jwt = require("jsonwebtoken");
const app = express();
const port = 3000;

app.use(express.json());

const users = [{ _id: 1, email: "a@gmail.com", pasword: "a123" }];
const KEY_JWT = "INIKEYJWT";

const middleware = (req, res, next) => {
	try {
		const auth = req.headers.authorization;
		const token = auth.split(" ")[1];
		jwt.verify(token, KEY_JWT);
		next();
	} catch (error) {
		return res.status(401).send({
			status: res.statusCode,
			message: "Oops Silahkan Login!",
		});
	}
};

app.get("/login", (req, res) => {
	let { email, password } = req.body;
	let data = users.find((x) => x.email == email && x.pasword == password);
	if (data) {
		let token = jwt.sign(data._id, KEY_JWT);
		return res.status(200).send({
			status: res.statusCode,
			message: "Login Berhasil",
			token,
		});
	} else {
		return res.status(404).send({
			status: res.statusCode,
			message: "Data User Not Found",
		});
	}
});

app.get("/data", middleware, (req, res) => {
	return res.status(200).send({
		status: res.statusCode,
		message: "GET Data User",
		users,
	});
});

app.listen(port, () => {
	console.log(`App listening on port ${port}`);
});
```
