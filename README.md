# Soal 1

Sebuah perusahaan e-commerce ingin membuat sistem database untuk menyimpan data pelanggan dan pesanan.
Buatlah tabel customers dan orders dengan constraint berikut:

Tabel customers memiliki kolom:
- customer_id (integer, primary key, auto increment)
- name (varchar, tidak boleh NULL)
- email (varchar, unik, tidak boleh NULL)
- phone (varchar, tidak boleh NULL)

Tabel orders memiliki kolom:
- order_id (integer, primary key, auto increment)
- customer_id (integer, foreign key yang merujuk ke customer_id di tabel customers)
- order_date (datetime, default sekarang)
- total_amount (decimal, tidak boleh NULL, harus lebih dari 0)

Tuliskan query pembuatan dua tabel di atas dengan hubungan key nya.

# Soal 2

Deskripsi:
Diketahui database e-commerce memiliki tabel berikut:

### Tabel: customers
| customer_id | name           | email               |
|------------|---------------|----------------------|
| 1          | Alice Johnson  | alice@example.com   |
| 2          | Bob Smith      | bob@example.com     |
| 3          | Charlie Brown  | charlie@example.com |


### Tabel: orders
| order_id | customer_id | order_date          | total_amount |
|----------|------------|---------------------|--------------|
| 1        | 1          | 2024-02-01 10:00:00 | 150.00       |
| 2        | 2          | 2024-02-02 12:30:00 | 300.00       |
| 3        | 1          | 2024-02-03 15:45:00 | 250.00       |


### Tabel: order_items
| order_item_id | order_id | product_id | quantity | price  |
|--------------|----------|------------|----------|--------|
| 1            | 1        | 1          | 1        | 150.00 |
| 2            | 2        | 2          | 1        | 300.00 |
| 3            | 3        | 3          | 2        | 125.00 |
| 4            | 2        | 4          | 1        | 50.00  |


### Tabel: products
| product_id | product_name | category     |
|------------|-------------|-------------|
| 1          | Laptop      | Electronics |
| 2          | Smartphone  | Electronics |
| 3          | Headphones  | Electronics |
| 4          | Shoes       | Fashion     |
| 5          | Watch       | Accessories |



Buat query SQL untuk menampilkan daftar pelanggan yang telah membeli produk dari kategori 'Electronics', beserta total jumlah yang telah mereka belanjakan dalam kategori tersebut. Urutkan hasil dari yang paling besar total belanjaannya.
