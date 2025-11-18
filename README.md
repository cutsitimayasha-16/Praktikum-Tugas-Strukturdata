
# **Implementasi Stack dan Queue di Python**

Dokumentasi ini menjelaskan implementasi dasar struktur data **Stack** dan **Queue** menggunakan bahasa Python.
Keduanya menggunakan tipe data **list**, karena Python menyediakan operasi yang efisien seperti `append()`, `pop()`, dan indexing.
Implementasi struktur data Stack dan Queue menggunakan tipe data list Python sangat membantu dalam memahami prinsip dasarnya: LIFO (Last-In, First-Out) untuk Stack dan FIFO (First-In, First-Out) untuk Queue.

# STACK
Stack adalah struktur data linier yang menerapkan prinsip LIFO (Last-In, First-Out). 
Artinya elemen yang terakhir dimasukkan ke dalam tumpukan adalah elemen pertama yang akan dikeluarkan.
# Kode Program Stack

```python
# Membuat stack kosong
stack = []

# Menambahkan elemen ke stack (push)
stack.append('X')
stack.append('Y')
stack.append('Z')
print("Stack:", stack)

# Menghapus elemen paling atas (pop)
topElement = stack.pop()
print("Pop:", topElement)

# Melihat elemen paling atas tanpa menghapus (peek)
peekElement = stack[-1]
print("Peek:", peekElement)

# Mengecek apakah stack kosong
isEmpty = not bool(stack)
print("isEmpty:", isEmpty)

# Menghitung jumlah elemen dalam stack
print("Size:", len(stack))
```

---

# Penjelasan Stack

### 1. Inisialisasi Stack

Pertama saya membuat sebuah list kosong sebagai tempat tumpukan data:

```python
stack = []
```

### 2. Push (Menambahkan Elemen ke Atas Stack)

Data baru dimasukkan ke **bagian paling atas** stack menggunakan `append()`:

```python
stack.append('X')
stack.append('Y')
stack.append('Z')
```

Setelah proses ini, isi stack:
**['X', 'Y', 'Z']**

### 3. Pop (Mengambil Elemen Paling Atas)

Untuk mengambil elemen paling atas, saya memakai `pop()` tanpa indeks:

```python
topElement = stack.pop()
```

Yang keluar adalah `'Z'` karena dia dimasukkan terakhir.

### 4. Peek (Melihat Elemen Paling Atas)

Untuk mengecek data di bagian atas stack tanpa mengeluarkannya:

```python
peekElement = stack[-1]
```

### 5. isEmpty (Cek Stack Kosong atau Tidak)

Untuk memeriksa apakah stack sedang tidak berisi elemen apa pun:

```python
isEmpty = not bool(stack)
```

### 6. Size (Menghitung Jumlah Elemen)

Untuk mengetahui sisa elemen dalam stack:

```python
len(stack)
```


# Hasil Eksekusi
Stack: ['X', 'Y', 'Z']
Pop: Z
Peek: Y
isEmpty: False
Size: 2


# Kesimpulan

* **Stack** di Python dapat dibuat menggunakan tipe data **list**.
* Stack berjalan menggunakan prinsip **LIFO (Last In, First Out)**.
* Operasi utama pada stack meliputi:

  * `append()` → menambah elemen ke atas (push)
  * `pop()` → menghapus elemen paling atas (pop)
  * `stack[-1]` → melihat elemen paling atas (peek)
* Struktur stack sering dipakai di proses seperti **riwayat halaman browser, undo/redo, kompilasi program, dan pengecekan kurung pada string**.



# QUEUE
Antrian adalah struktur data linier yang menerapkan prinsip FIFO (First-In, First-Out).
Artinya elemen yang pertama dimasukkan ke dalam antrian adalah elemen pertama yang akan dikeluarkan.

# Kode Program Queue

```python
# Membuat antrian kosong
queue = []

# Menambahkan elemen ke antrian (enqueue)
queue.append('A')
queue.append('B')
queue.append('C')
print("Queue:", queue)

# Mengambil elemen paling depan (dequeue)
element = queue.pop(0)
print("Dequeue:", element)

# Melihat elemen terdepan tanpa menghapus (peek)
frontElement = queue[0]
print("Peek:", frontElement)

# Mengecek apakah queue kosong
isEmpty = not bool(queue)
print("isEmpty:", isEmpty)

# Menghitung jumlah elemen di dalam queue
print("Size:", len(queue))
```

---

# Penjelasan Queue

### 1. Inisialisasi Queue

Pertama, aku membuat sebuah list kosong sebagai tempat data antrian:

```python
queue = []
```

### 2. Enqueue (Menambah Data ke Antrian)

Elemen baru dimasukkan ke bagian **belakang** antrian menggunakan `append()`:

```python
queue.append('A')
queue.append('B')
queue.append('C')
```

Setelah langkah ini, isi antriannya adalah:
**['A', 'B', 'C']**

### 3. Dequeue (Menghapus Data Paling Depan)

Untuk mengambil elemen terdepan, digunakan `pop(0)`:

```python
element = queue.pop(0)
```

Elemen `'A'` keluar terlebih dahulu karena dialah yang masuk paling awal.

### 4. Peek (Melihat Data Terdepan Tanpa Mengambil)

Untuk sekadar melihat elemen yang berada di depan antrian:

```python
frontElement = queue[0]
```

### 5. isEmpty (Pengecekan Apakah Queue Kosong)

Digunakan untuk mengetahui apakah antrian berisi elemen atau tidak:

```python
isEmpty = not bool(queue)
```

### 6. Size (Menghitung Jumlah Elemen)

Untuk mengetahui sisa elemen yang ada:

```python
len(queue)
```

---

# Hasil Eksekusi

```
Queue: ['A', 'B', 'C']
Dequeue: A
Peek: B
isEmpty: False
Size: 2
```

---

# Kesimpulan

* Struktur **Queue** di Python bisa dibuat dengan bantuan tipe data **list**.
* Cara kerja queue mengikuti aturan **FIFO (First In, First Out)**.
* Operasi dasar pada queue meliputi:

  * `append()` → menambah data ke belakang (enqueue)
  * `pop(0)` → mengambil data dari depan (dequeue)
  * `queue[0]` → melihat elemen terdepan (peek)
* Struktur queue sering digunakan dalam simulasi **antrian pelanggan, sistem printer, schedulers**, dan proses yang membutuhkan urutan.









