# Program Paket Sederhana

## Soal

Sebuah jasa pengiriman memiliki aturan biaya yang bergantung pada beberapa faktor. Biaya dasar pengiriman ditetapkan sebesar Rp 10.000.
Jika berat paket melebihi 5 kg, maka akan dikenakan tambahan biaya sebesar Rp 5.000. Selain itu, jika jarak pengiriman lebih dari 10 km, maka ada tambahan biaya sebesar Rp 8.000. 
Jika pelanggan memilih layanan pengiriman express, maka akan dikenakan tambahan biaya sebesar Rp 20.000. Namun, jika pelanggan merupakan member, mereka akan mendapatkan diskon 10% dari total biaya pengiriman yang dihitung sebelum diskon. 

Buatlah sebuah fungsi dalam Python yang dapat menghitung total biaya pengiriman berdasarkan aturan tersebut, dengan parameter berat paket, jarak pengiriman, jenis pengiriman (biasa atau express), serta status keanggotaan pelanggan (member atau non-member).

# Demo program

```python
def hitung_biaya_pengiriman(berat, jarak, express=False, member=False):
    # Biaya dasar
    biaya = 10000
    
    # Tambahan biaya jika berat lebih dari 5 kg
    if berat > 5:
        biaya += 5000
    
    # Tambahan biaya jika jarak lebih dari 10 km
    if jarak > 10:
        biaya += 8000
    
    # Tambahan biaya untuk layanan express
    if express:
        biaya += 20000
    
    # Diskon untuk member
    if member:
        biaya *= 0.9  # Diskon 10%
    
    return int(biaya)  # Konversi ke integer untuk hasil biaya dalam rupiah
```
