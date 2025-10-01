# C-programming-language-Lesson-1
# C Programlama Başlangıç Rehberi

Hoş geldiniz! Bu repo, C programlama diline yeni başlayanlar için hazırlanmış kapsamlı bir rehberdir.

## 📚 İçindekiler

- [C Nedir?](#c-nedir)
- [Gerekli Araçlar](#gerekli-araçlar)
- [İlk Programınız](#ilk-programınız)

## 🎯 C Nedir?

C, 1972 yılında Dennis Ritchie tarafından Bell Laboratuvarlarında geliştirilen, güçlü ve esnek bir programlama dilidir. Düşük seviyeli bellek erişimi ile yüksek seviyeli programlama özelliklerini bir araya getiren C, bugün hala en popüler dillerden biridir.

### Neden C Öğrenmeliyim?

- **Temel Dil:** C++, Java, C# gibi birçok modern dilin temelini oluşturur
- **Performans:** Donanıma yakın çalıştığı için son derece hızlıdır
- **Bellek Kontrolü:** Bellek yönetimini tam anlamanızı sağlar
- **Yaygın Kullanım:** İşletim sistemleri (Linux, Windows), gömülü sistemler, oyun motorları
- **İş Fırsatları:** Embedded, IoT, sistem programlama alanlarında yüksek talep

### C Nerelerde Kullanılır?

**İşletim Sistemleri:**
- Linux çekirdeği tamamen C ile yazılmıştır
- Windows'un büyük bir kısmı C ile geliştirilmiştir
- macOS'un temelindeki Unix sistemi C ile yazılmıştır

**Gömülü Sistemler:**
- Arduino programlama
- Mikrodenetleyiciler
- IoT cihazları
- Otomotiv sistemleri

**Oyun ve Grafik:**
- Oyun motorlarının temel katmanları
- OpenGL ve DirectX gibi grafik kütüphaneleri
- Yüksek performans gerektiren uygulamalar

**Veritabanları:**
- MySQL
- PostgreSQL
- Redis

### C'nin Avantajları ve Dezavantajları

**Avantajlar:**
- Çok hızlı çalışır
- Küçük boyutlu programlar üretir
- Donanım kontrolü sağlar
- Taşınabilir (portable) kod yazabilirsiniz
- Zengin kütüphane desteği

**Dezavantajlar:**
- Bellek yönetimi manuel yapılır (malloc/free)
- Hata ayıklama zor olabilir
- Güvenlik açıklarına (buffer overflow) dikkat etmek gerekir
- Nesne yönelimli programlama özelliği yoktur

## 🛠️ Gerekli Araçlar

### Windows İçin Kurulum

#### 1. MinGW (Minimalist GNU for Windows)

MinGW, Windows'ta GCC derleyicisini kullanmanızı sağlar.

**Kurulum Adımları:**

1. [MinGW-w64](https://sourceforge.net/projects/mingw-w64/) adresinden indirin
2. Kurulum sırasında Architecture: x86_64 seçin
3. Kurulum tamamlandıktan sonra PATH'e ekleyin:
   - Windows Ayarları → Sistem → Gelişmiş sistem ayarları
   - Ortam Değişkenleri → Path → Yeni
   - `C:\mingw-w64\mingw64\bin` ekleyin

**Test:**
```bash
gcc --version
```

#### 2. Code::Blocks IDE

Başlangıç için ideal bir IDE'dir, içinde derleyici bulunur.

1. [Code::Blocks](http://www.codeblocks.org/) adresinden "mingw" içeren versiyonu indirin
2. Kurulumu tamamlayın
3. Yeni proje: File → New → Project → Console Application

#### 3. Visual Studio Code

Daha profesyonel bir editör için VS Code kullanabilirsiniz.

**Gerekli Eklentiler:**
- C/C++ (Microsoft)
- Code Runner
- C/C++ Compile Run

**Ayarlar:**
1. VS Code'u açın
2. Extensions → "C/C++" ara ve yükle
3. MinGW'yi PATH'e eklediğinizden emin olun

### Linux İçin Kurulum

#### Ubuntu/Debian Tabanlı Sistemler

```bash
# GCC ve gerekli araçları yükle
sudo apt update
sudo apt install build-essential

# GDB debugger
sudo apt install gdb

# Kurulumu kontrol et
gcc --version
make --version
gdb --version
```

#### Fedora/RedHat Tabanlı Sistemler

```bash
# Geliştirme araçlarını yükle
sudo dnf groupinstall "Development Tools"
sudo dnf install gcc gdb make

# Kurulumu kontrol et
gcc --version
```

#### Arch Linux

```bash
# Base-devel paketi
sudo pacman -S base-devel

# Kurulumu kontrol et
gcc --version
```

### macOS İçin Kurulum

#### Xcode Command Line Tools

```bash
# Komut satırı araçlarını yükle
xcode-select --install

# Kurulumu kontrol et
gcc --version
clang --version
```

#### Homebrew ile GCC

```bash
# Homebrew yoksa önce yükleyin
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# GCC yükle
brew install gcc

# Kurulumu kontrol et
gcc-13 --version  # Versiyon numarası değişebilir
```

### Online Derleyiciler

İnternet üzerinden hızlıca kod test etmek için:

**1. OnlineGDB**
- URL: https://www.onlinegdb.com/
- Özellikleri: Debugger, kod paylaşımı
- Ücretsiz ve hızlı

**2. Repl.it**
- URL: https://replit.com/
- Özellikleri: Gerçek zamanlı işbirliği, proje kaydetme
- Hesap oluşturma gerekiyor

**3. Programiz**
- URL: https://www.programiz.com/c-programming/online-compiler/
- Özellikleri: Basit ve temiz arayüz
- Hızlı test için ideal

**4. Compiler Explorer**
- URL: https://godbolt.org/
- Özellikleri: Assembly kodunu gösterir
- İleri seviye öğrenme için harika

### Hangi Aracı Seçmeliyim?

**Yeni Başlıyorsanız:**
- Windows: Code::Blocks (kolay kurulum)
- Linux/Mac: Terminal + nano/vim (klasik yöntem)
- Herhangi bir platform: OnlineGDB (kurulum gerektirmez)

**Biraz Deneyim Kazandıktan Sonra:**
- Visual Studio Code (tüm platformlar için önerilen)
- Terminal + GCC (profesyonel yaklaşım)

## 🚀 İlk Programınız

## 🔹 Veri | Data
- Veri (Data): sayı, metin, görüntü gibi ham bilgilerin temsilidir.  
- İşlenmedikçe bilgiye dönüşmez.  
- Kaydedilen veya ölçülen değerlerdir.  

---

## 🔹 Değişken | Variable
- Bellekte belli bir alanı işgal eden ve isimlendirilmiş bilgi.  
- Programlarda giriş/çıkış işlemleri için kullanılır.  

**Tanımlama Örneği | Example:**

```c
int sayi;     // tamsayı | integer
float pi;     // ondalıklı sayı | float
char harf;    // tek karakter | character
```

---

## 🔹 Değişkene Değer Atama | Assigning a Value
C’de atama için `=` operatörü kullanılır. | In C, the `=` operator is used for assignment.

```c
#include <stdio.h>
int main() {
    int sayi;
    sayi = 42;
    printf("sayi değişkeninin değeri: %d\n", sayi);
    return 0;
}
```

---

## 🔹 Değişken İsimlendirme Kuralları | Variable Naming Rules
- Harf veya `_` ile başlamalıdır. | Must start with a letter or `_`.  
- Türkçe karakterler kullanılmaz. | No Turkish letters allowed.  
- Büyük/küçük harf farklıdır. | Case-sensitive.  
- Anahtar kelimeler kullanılamaz. | Keywords cannot be used.  

---

## 🔹 Kodlama Kültürü | Coding Style
- **camelCase** → `ortalamaNot` | `averageGrade`  
- **PascalCase** → `OrtalamaNot` | `AverageGrade`  
- **snake_case** → `ortalama_not` | `average_grade`  

---

## 🔹 Veri Tipleri ve Format Belirteçleri | Data Types and Format Specifiers
- **int** → tam sayı (`%d`) | integer  
- **float** → ondalıklı sayı (`%f`) | floating-point  
- **double** → daha hassas ondalıklı sayı (`%lf`) | double precision  
- **char** → tek karakter (`%c`) | single character  
- **string (char array)** → metin (`%s`) | string  
- **void** → dönüş değeri olmayan fonksiyon | no return type  

---

## 🔹 Örnek Kodlar | Example Codes

### Integer Kullanımı | Integer Example
```c
int sayi = 42;
printf("Bu bir tam sayıdır: %d\n", sayi);
```

### Float Kullanımı | Float Example
```c
float pi = 3.14159;
printf("Pi sayısı: %f\n", pi);
```

### Double Kullanımı | Double Example
```c
double ciftHassasSayi = 3.141592653589793;
printf("Çift Hassas Sayi: %.11lf\n", ciftHassasSayi);
```

### Char Kullanımı | Char Example
```c
char karakter = 'A';
printf("Karakter: %c\n", karakter);
```

---

## 🔹 sizeof() Fonksiyonu | sizeof() Function
Bellekte kaplanan alanı gösterir | Shows memory size:

```c
printf("int: %d bayt\n", sizeof(int));
printf("short: %d bayt\n", sizeof(short));
```

---

## 🔹 scanf() ile Veri Girişi | Taking Input with scanf()
```c
#include <stdio.h>
int main() {
    float sayi;
    printf("Bir sayı giriniz: ");
    scanf("%f", &sayi);
    printf("Girilen sayı: %f\n", sayi);
    return 0;
}
```

---

## 📌 Özet | Summary
- Veri → Ham bilgi | Data → Raw information  
- Değişken → Bellekte isimlendirilmiş bilgi alanı | Variable → Named memory space  
- Veri Tipleri → int, float, double, char, string | Data Types → int, float, double, char, string  
- Giriş/Çıkış İşlemleri → `printf()`, `scanf()` | I/O Operations → `printf()`, `scanf()`  
- Kodlama kültürü → camelCase, PascalCase, snake_case | Coding style → camelCase, PascalCase, snake_case  


### 1. Merhaba Dünya

En klasik başlangıç programı:

```c
#include <stdio.h>

int main() {
    printf("Merhaba Dünya!\n");
    return 0;
}
```

**Kod Açıklaması:**
- `#include <stdio.h>`: Standart girdi/çıktı kütüphanesini dahil eder
- `int main()`: Programın başlangıç noktası
- `printf()`: Ekrana yazı yazdırır
- `\n`: Yeni satır karakteri
- `return 0`: Programın başarıyla sonlandığını belirtir

### 2. Derleme ve Çalıştırma

#### Windows (MinGW)
```bash
# Derleme
gcc merhaba.c -o merhaba.exe

# Çalıştırma
merhaba.exe
```

#### Linux/Mac
```bash
# Derleme
gcc merhaba.c -o merhaba

# Çalıştırma
./merhaba
```

#### Code::Blocks
1. Build → Build (F9)
2. Build → Run (Ctrl+F10)

#### VS Code
1. Dosyayı kaydedin (Ctrl+S)
2. Terminal → New Terminal
3. Yukarıdaki komutları kullanın

### 3. Kullanıcıdan İsim Alma

```c
#include <stdio.h>

int main() {
    char isim[50];  // 50 karakterlik dizi
    
    printf("Adınızı girin: ");
    scanf("%s", isim);
    
    printf("Merhaba %s! Hoş geldin.\n", isim);
    
    return 0;
}
```

**Çıktı:**
```
Adınızı girin: Ahmet
Merhaba Ahmet! Hoş geldin.
```

### 4. Basit Matematik İşlemleri

```c
#include <stdio.h>

int main() {
    int sayi1, sayi2, toplam;
    
    printf("İki sayı girin: ");
    scanf("%d %d", &sayi1, &sayi2);
    
    toplam = sayi1 + sayi2;
    
    printf("%d + %d = %d\n", sayi1, sayi2, toplam);
    
    return 0;
}
```

**Çıktı:**
```
İki sayı girin: 5 8
5 + 8 = 13
```


### Sık Karşılaşılan Hatalar ve Çözümleri

**1. "stdio.h: No such file or directory"**
- Çözüm: GCC doğru kurulmamış, kurulumu kontrol edin

**2. "undefined reference to 'main'"**
- Çözüm: `main()` fonksiyonunu tanımlayın

**3. Türkçe karakterler görünmüyor**
```c
#include <stdio.h>
#include <locale.h>

int main() {
    setlocale(LC_ALL, "Turkish");
    printf("Türkçe karakterler: ğüşıöç\n");
    return 0;
}
```

**4. scanf sonrası program kapanıyor**
```c
getchar();  // Enter tuşunu bekler
```

### Alıştırmalar

Aşağıdaki programları kendiniz yazmayı deneyin:

1. İki sayının ortalamasını hesaplayan program
2. Kullanıcının girdiği sayının tek mi çift mi olduğunu bulan program
3. Dikdörtgenin alanını ve çevresini hesaplayan program
4. Kullanıcının girdiği üç sayıdan en büyüğünü bulan program
5. Basit bir not ortalaması hesaplayıcı

---

**Sonraki Adımlar:** Temel kavramları öğrendikten sonra değişkenler, operatörler ve kontrol yapılarına geçebilirsiniz. İyi çalışmalar! 🚀
