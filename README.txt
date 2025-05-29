# my-pintos-tests

**Pintos**, C diliyle yazılmış, 32-bit x86 mimarisi üzerinde çalışan basit bir öğretici işletim sistemidir. Bu depo, orijinal Pintos projesinde tanımlı olan **tüm testleri başarıyla geçen** eksiksiz bir uygulamayı içermektedir.

📚 Pintos hakkında daha fazla bilgi için orijinal proje sayfasına bakabilirsiniz:
[http://web.stanford.edu/class/cs140/projects/pintos/pintos.html](http://web.stanford.edu/class/cs140/projects/pintos/pintos.html)

---

## 🚀 Gerçekleştirilen Özellikler

Bu uygulama, modern bir işletim sistemi çekirdeğinde beklenen tüm ana bileşenleri ve geliştirmeleri içermektedir:

* ✅ **Adil Zamanlayıcı (Scheduler)**

  * Giriş/Çıkış ağırlıklı ve CPU ağırlıklı yükleri etkili biçimde işler.
* ✅ **Öncelikli Zamanlama (Priority Scheduling)**

  * Öncelik bağışı (priority donation) desteğiyle öncelik tersine dönmesini engeller.
* ✅ **Sanal Bellek Sistemi (Virtual Memory)**

  * Disk takası (swap)
  * Dosya eşleme (memory-mapped files / mmap)
  * Paylaşımlı salt-okunur sayfalar
* ✅ **Çoklu İş Parçacıklı Dosya Sistemi**

  * Geri yazma tampon belleği (write-back buffer cache)
  * Önden okuma (read-ahead)
  * Seyrek dosya desteği (sparse files)

---

## 📦 Teslim Bilgisi

### GRUP

```
2023280154  Melih Takyacı     melih.takyaci@ogr.deu.edu.tr
2023280140  Emre Özdemir      emre.ozdemir23@ogr.deu.edu.tr
2022280128  Eren Önder        eren.onder@ogr.deu.edu.tr
2022280050  Emir Mutlu        emir.mutlu@ogr.deu.edu.tr

```

### ÖN HAZIRLIKLAR

* 1. ödevde yaşanan aksaklık nedeniyle bu ödevle birlikte teslim edilmiştir. Aşağıda hem Ödev 1 hem de Ödev 3’e ait kodlar ve içerikler yer almaktadır.
* Ek kaynak olarak sadece Pintos belgeleri, Stanford ders materyalleri ve [Surya’nın rehberi](https://tssurya.wordpress.com/2014/08/16/installing-pintos-on-your-machine/) kullanılmıştır.

---

## 🔧 Kurulum ve Derleme

### Gereksinimler

* `-m32` desteği olan GCC (32-bit toolchain)
* QEMU
* Python 2 veya uyumlu `perl` scriptleri
* `make`, `gdb` ve standart Unix araçları

### Hızlı Başlangıç

```bash
cd src/threads
make check   # Thread testlerini çalıştırır

cd ../userprog
make check   # Kullanıcı programı testlerini çalıştırır

cd ../vm
make check   # Sanal bellek testlerini çalıştırır

cd ../filesys
make check   # Dosya sistemi testlerini çalıştırır
```

---

## 📚 Proje Katkı Bilgileri

### src

* Pintos çekirdeği ilk olarak Ben Pfaff [blp@cs.stanford.edu](mailto:blp@cs.stanford.edu) tarafından yazılmıştır.
* Ek özellikler Anthony Romano [chz@vt.edu](mailto:chz@vt.edu) tarafından katkıda bulunulmuştur.
* İşletim sistemi yapısı, UC Berkeley'den Nachos sisteminden esinlenmiştir. Bazı kaynak dosyalar Nachos C++ kodunun C diline doğrudan çevrilmiş halleridir ve UCB lisansını taşır.

### projects

* Projeler öncelikle Ben Pfaff [blp@cs.stanford.edu](mailto:blp@cs.stanford.edu) tarafından tasarlanmıştır.

* Godmar Back [godmar@gmail.com](mailto:godmar@gmail.com) proje tasarımına önemli katkılarda bulunmuştur.

* Projeler, Stanford Üniversitesi CS140 dersindeki TA’lar tarafından tasarlanmış önceki Nachos projelerinden türetilmiştir. Katkıda bulunan bazı isimler:

  * Yu Ping [yph@cs.stanford.edu](mailto:yph@cs.stanford.edu)
  * Greg Hutchins
  * Kelly Shaw [kashaw@cs.stanford.edu](mailto:kashaw@cs.stanford.edu)
  * Paul Twohey [twohey@cs.stanford.edu](mailto:twohey@cs.stanford.edu)
  * Sameer Qureshi [squreshi@cs.stanford.edu](mailto:squreshi@cs.stanford.edu)
  * John Rector

* Koşul değişkeni (condition variable) örnek kodu, Dawson Engler ve Mendel Roseblum’un ders slaytlarından alınmıştır.
