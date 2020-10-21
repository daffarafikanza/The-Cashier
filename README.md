# The-Cashier

Aplikasi sederhana ini mencakup fungsi perhitungan nilai pertukaran mata uang dari dollar ke rupiah. Jadi 1$ = Rp. 15.000

## Scope & Functionalities

- User bisa memasukkan angka yang mereka inginkan
- User dapat menyentuh tombol hitung
- User akan mendapatkan info `INVALID` jika yang dimasukkan selain angka

## How Does it Works?

Diawali dari method `MainWindow` pada class `MainWindow.xaml.cs`, kita mendeklarasikan menjadi......

```csharp
public MainWindow()
        {
            InitializeComponent();
            currency = new CurrencyController();
        }
```

logika perhitungan terdapat pada class `CurrencyController.cs` sebagai berikut cara kerjanya.......

```csharp
public string usdToIdr(string nominal)
        {
            var nominalDouble = Convert.ToDouble(nominal);
            var result = nominalDouble * 15000;
            return Convert.ToString(result);
        }
```
