# The-Cashier

Aplikasi kasir sederhana ini berfungsi untuk melakukan perhitungan transaksi barang/jasa dengan menginputkan, nama item, jumlah, dan harga.

## Scope & Functionalities

- User bisa memasukkan nama item, jumlah, dan harga
- User dapat memelih tipe barang/jasa
- User tidak bisa menginputkan selain angka di kolom jumlah dan harga

## How Does it Works?

Setelah pendeklarasian pada `Item.cs`, dilanjutkan dengan penginisialisasian seluruh bahan sebagai media yang nantinya akan menjadi perwakilan dari variable yang akan diinputkan oleh pengguna.

```csharp
public MainWindow()
        {
            InitializeComponent();
            calculator = new Calculator();
            listBox.ItemsSource = calculator.getListItem();
        }
```

Inisialisasi List dan Perhitungan Barang dan Jesa terdapat pada class `Item.cs` sebagai berikut

```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```
