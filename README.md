# Genetik Algoritma ile Nakliye Rotasında Yakıt ve Zaman Optimizasyonu
Senaryo 3

Bu projede, bir lojistik firmasının nakliye sürecinde yakıt tüketimi ve zaman maliyeti dengesini sağlamak amacıyla genetik algoritma kullanılmıştır. Problem, sürekli değerli ve kısıtlı bir optimizasyon problemi olarak ele alınmıştır.

---

## Problem Tanımı

Karar değişkenleri:
- Ortalama hız (km/h)
- Araç yük kapasitesi (ton)

Amaç, verilen amaç fonksiyonunu maksimize ederek en uygun hız ve yük kombinasyonunu bulmaktır.

---

## Amaç Fonksiyonu

y = -2*v - 3*p + 0.1*v*p

---

## Değişkenler ve Kısıtlar

- Ortalama hız: 40 <= v <= 100 ve v >= 60
- Yük kapasitesi: 2 <= p <= 10
- Motor gücü kısıtı: v * p <= 700

Kısıtlar algoritma içerisinde düzeltme (repair) yöntemi ile uygulanmıştır.

---

## Genetik Algoritma Yapısı

- Gerçek değerli kromozom yapısı (avg speed, payload)
- Seçim yöntemi: Turnuva seçimi
- Çaprazlama: Arithmetic (blend) crossover
- Mutasyon: Gaussian mutasyon
- Elitizm: En iyi 2 birey korunmuştur

---

## Sonuçlar

Algoritma sonucunda elde edilen en iyi çözüm:

- Ortalama hız: 60 km/h
- Yük kapasitesi: 10 ton
- Motor gücü: 600 (700 sınırının altında)
- Amaç fonksiyonu değeri: -90

Minimum hız ve maksimum yük kısıtları bağlayıcıdır. Motor gücü kısıtı bağlayıcı değildir.

---

## Çalıştırma

Python 3 gereklidir.

Gerekli kütüphane:
pip install matplotlib

Notebook dosyasını açarak tüm hücreleri çalıştırmanız yeterlidir.

---

