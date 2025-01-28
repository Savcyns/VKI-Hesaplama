import tkinter

# Pencere
window = tkinter.Tk()
window.title("VKİ Hesaplayıcısı")
window.minsize(300, 300)

# Kilo Girişi İçin Label(Yazı)
label_1 = tkinter.Label(text="Kilonuzu Giriniz (kg):")
label_1.pack()

# Kilo Girişi İçin Entry(Girdi)
entry_1 = tkinter.Entry()
entry_1.pack()

# Boy Girişi İçin Label (Yazı)
label_2 = tkinter.Label(text="Boyunuzu Giriniz (m):")
label_2.pack()

# Boy Girişi İçin Entry (Girdi)
entry_2 = tkinter.Entry()
entry_2.pack()

# Sonuç Gösterimi İçin Label  (Yazı)
result_label = tkinter.Label(text="")
result_label.pack()

# VKİ Hesaplama Fonksiyonu (try:ilk denenecek olmazsa except:ilkin alternatifi çalıştırılır)
def vki_hes():
    try:
        # Kullanıcı girişlerini al
        kilo = float(entry_1.get())
        boy = float(entry_2.get())
        
        # VKİ hesapla
        vki = kilo / boy**2
        
        # VKİ'ye göre kategori belirle
        if vki < 18.5:
            kategori = "Zayıf"
        elif 18.5 <= vki < 25:
            kategori = "Normal"
        elif 25 <= vki < 30:
            kategori = "Fazla Kilolu"
        elif 30 <= vki < 35:
            kategori = "1. Derece Obezite"
        elif 35 <= vki < 40:
            kategori = "2. Derece Obezite"
        else:
            kategori = "3. Derece Obezite"
        
        # Sonucu göster
        result_label.config(text=f"VKİ'niz: {vki:.2f} ({kategori})")
    except ValueError:
        # Hatalı girişler için uyarı göster
        result_label.config(text="Lütfen geçerli sayılar girin.")

# Button (Hesaplama Butonu)
button = tkinter.Button(text="Hesapla", command=vki_hes)
button.pack()

# Pencereyi Çalıştır
window.mainloop()
