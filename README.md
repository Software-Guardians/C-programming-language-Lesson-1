# C-programming-language-Lesson-1
🚀 C Programlama Diline Giriş
Güçlü ve hızlı programlama dünyasına hoş geldiniz!
________________________________________
🎯 C Nedir?
C programlama dili, 1970'lerde Dennis Ritchie tarafından geliştirilen, hızlı, güçlü ve taşınabilir bir programlama dilidir. İşletim sistemlerinden oyunlara, gömülü sistemlerden süper bilgisayarlara kadar her yerde kullanılır.
⭐ Neden C Öğrenmeliyim?
•	Temel güç: Diğer dillerin babası sayılır
•	Hız canavarı: Çok hızlı çalışan programlar yazabilirsin
•	Sistem programlama: Bilgisayarın derinliklerine inebilirsin
•	Geniş kullanım: Linux, Windows, Arduino... her yerde C var!
________________________________________
🛠️ İlk Adımlar
Gerekli Araçlar
•	Derleyici: GCC (Linux/Mac) veya MinGW (Windows)
•	Kod Editörü: VS Code, Code::Blocks, veya basit bir metin editörü
•	Terminal: Komut satırı bilgisi
İlk Program: Merhaba Dünya! 👋
#include <stdio.h>

int main() {
    printf("Merhaba Dünya! 🌍\n");
    return 0;
}
Bu kod nasıl çalışır?
•	#include <stdio.h> → Giriş/çıkış kütüphanesini dahil et
•	int main() → Programın başlangıç noktası
•	printf() → Ekrana yazı yazdır
•	return 0 → Program başarıyla bitti
________________________________________
📊 Veri Tipleri ve Değişkenler
Temel Veri Tipleri
Tip	Boyut	Açıklama	Örnek
int	4 byte	Tam sayılar	42, -17
float	4 byte	Ondalıklı sayılar	3.14, -2.5
double	8 byte	Daha hassas ondalık	3.14159265
char	1 byte	Karakterler	'A', 'z', '5'
Değişken Tanımlama
#include <stdio.h>

int main() {
    // Değişken tanımlamaları
    int yas = 20;
    float boy = 1.75;
    char harf = 'A';
    
    printf("Yaş: %d\n", yas);
    printf("Boy: %.2f\n", boy);
    printf("Harf: %c\n", harf);
    
    return 0;
}
________________________________________
🧮 Operatörler
Matematik Operatörleri
int a = 10, b = 3;

int toplam = a + b;     // 13
int fark = a - b;       // 7
int carpim = a * b;     // 30
int bolum = a / b;      // 3 (tam bölme)
int kalan = a % b;      // 1 (mod alma)
Karşılaştırma Operatörleri
int x = 5, y = 3;

x == y  // Eşit mi? (false)
x != y  // Eşit değil mi? (true)
x > y   // Büyük mü? (true)
x < y   // Küçük mü? (false)
x >= y  // Büyük eşit mi? (true)
x <= y  // Küçük eşit mi? (false)
________________________________________
🔀 Koşullu İfadeler (if-else)
#include <stdio.h>

int main() {
    int puan = 85;
    
    if (puan >= 90) {
        printf("Harika! A aldın! 🏆\n");
    } else if (puan >= 80) {
        printf("Güzel! B aldın! 👍\n");
    } else if (puan >= 70) {
        printf("İdare eder, C aldın 📚\n");
    } else {
        printf("Daha çok çalışmalısın 💪\n");
    }
    
    return 0;
}
________________________________________
🔄 Döngüler
For Döngüsü
// 1'den 10'a kadar sayıları yazdır
for (int i = 1; i <= 10; i++) {
    printf("%d ", i);
}
printf("\n");
While Döngüsü
int sayac = 0;
while (sayac < 5) {
    printf("Döngü: %d\n", sayac);
    sayac++;
}
Çarpım Tablosu Örneği 📋
#include <stdio.h>

int main() {
    int sayi = 7;
    
    printf("=== %d'nin çarpım tablosu ===\n", sayi);
    for (int i = 1; i <= 10; i++) {
        printf("%d x %d = %d\n", sayi, i, sayi * i);
    }
    
    return 0;
}
________________________________________
📝 Diziler (Arrays)
#include <stdio.h>

int main() {
    // Dizi tanımlama
    int notlar[5] = {85, 92, 78, 96, 88};
    
    // Dizideki elemanları yazdır
    printf("Notlarınız:\n");
    for (int i = 0; i < 5; i++) {
        printf("Not %d: %d\n", i+1, notlar[i]);
    }
    
    // Ortalama hesaplama
    int toplam = 0;
    for (int i = 0; i < 5; i++) {
        toplam += notlar[i];
    }
    
    float ortalama = toplam / 5.0;
    printf("Ortalamanız: %.2f\n", ortalama);
    
    return 0;
}
________________________________________
🎮 Pratik Projeler
1. Sayı Tahmin Oyunu
#include <stdio.h>
#include <stdlib.h>
#include <time.h>

int main() {
    srand(time(NULL));
    int gizliSayi = rand() % 100 + 1;
    int tahmin, deneme = 0;
    
    printf("🎯 1-100 arası bir sayı tuttum!\n");
    
    do {
        printf("Tahmininiz: ");
        scanf("%d", &tahmin);
        deneme++;
        
        if (tahmin > gizliSayi) {
            printf("📉 Daha küçük bir sayı dene!\n");
        } else if (tahmin < gizliSayi) {
            printf("📈 Daha büyük bir sayı dene!\n");
        } else {
            printf("🎉 Tebrikler! %d denemede bildin!\n", deneme);
        }
    } while (tahmin != gizliSayi);
    
    return 0;
}
2. Basit Hesap Makinesi
#include <stdio.h>

int main() {
    char operator;
    double sayi1, sayi2, sonuc;
    
    printf("🧮 Basit Hesap Makinesi\n");
    printf("Bir işlem seçin (+, -, *, /): ");
    scanf("%c", &operator);
    
    printf("İki sayı girin: ");
    scanf("%lf %lf", &sayi1, &sayi2);
    
    switch(operator) {
        case '+':
            sonuc = sayi1 + sayi2;
            break;
        case '-':
            sonuc = sayi1 - sayi2;
            break;
        case '*':
            sonuc = sayi1 * sayi2;
            break;
        case '/':
            if (sayi2 != 0) {
                sonuc = sayi1 / sayi2;
            } else {
                printf("❌ Sıfıra bölme hatası!\n");
                return 1;
            }
            break;
        default:
            printf("❌ Geçersiz işlem!\n");
            return 1;
    }
    
    printf("Sonuç: %.2lf %c %.2lf = %.2lf\n", sayi1, operator, sayi2, sonuc);
    
    return 0;
}
________________________________________
🎓 İpuçları ve En İyi Uygulamalar
✅ Yapılması Gerekenler
•	Kodunu yorumla: // Bu bir yorum satırı
•	Anlamlı değişken isimleri kullan: yas > x
•	Girintileri düzenli kullan
•	Her zaman return 0; ile bitir
❌ Yapılmaması Gerekenler
•	Değişken tanımlamadan kullanma
•	Buffer overflow riskine karşı dikkatli ol
•	Bellek sızıntıları yaratma
🔧 Hata Ayıklama İpuçları
// printf ile değişken değerlerini kontrol et
printf("DEBUG: x = %d, y = %d\n", x, y);

// Koşulların doğru çalışıp çalışmadığını kontrol et
if (x > y) {
    printf("x büyük\n");
} else {
    printf("y büyük veya eşit\n");
}
________________________________________
🚀 Sıradaki Adımlar
Temel C'yi öğrendikten sonra:
1.	Fonksiyonlar - Kodunu modüler hale getir
2.	Pointerlar - C'nin süper gücü
3.	Struct'lar - Kendi veri tiplerini oluştur
4.	Dosya işlemleri - Verilerini kaydet
5.	Dinamik bellek yönetimi - malloc() ve free()
________________________________________
🌟 Son Söz
C öğrenmek bir maraton, sprint değil. Sabırlı ol, sürekli pratik yap ve kodlama keyfini çıkar! Her programcının C bilmesi, güçlü bir temel oluşturur.
Mutlu kodlamalar! 💻✨
________________________________________
Bu rehber başlangıç seviyesi için hazırlanmıştır. Sorularınız için programlama topluluklarına katılmayı unutmayın!

