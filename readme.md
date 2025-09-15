
# Proje Özeti

İlk yardım eğitimini hem öğreten hem de ölçen, Unity ile geliştirilecek bir oyunlaştırma projesi. Oyuncu; etkileşimli mikro dersler, gerçekçi senaryolar ve zaman baskısı altındaki sınavlarla temel ilk yardım becerilerini (CPR, kanama kontrolü, hava yolu tıkanıklığı, şok, yanık, kırık/çıkık, epilepsi nöbeti, zehirlenme, AED kullanımı vb.) öğrenir ve pekiştirir.

---
![ExampleUI](https://github.com/cmlcrn17/EmergencyResponseTraining/ilkyardim.jpeg)




## 1) Hedef Kitle & Platform

* **Hedef kitle:** 16+ yaş; kurum içi eğitim, sürücü kursları, okullar, STK’lar.
* **Platformlar:** PC (Windows/Mac), mobil (iOS/Android), ileride WebGL demo.
* **Oyun süresi:** 10–15 dakikalık modüller; toplam içerik 3–5 saat.

---

## 2) Öğrenme Hedefleri (SMART)

1. Oyuncular, **CPR**’ın ABC yaklaşımını ve kompresyon ritmini 10 dakika içinde açıklayabilsin.
2. **Kanama kontrolü** için bası, elevasyon ve turnike adımlarını doğru sıralasın.
3. **Boğulma (Heimlich)** müdahalesinde yaş grubuna göre doğru tekniği seçsin.
4. **AED**’yi güvenli biçimde kurup yönlendirmeleri takip etsin.
5. **Değerlendirme modu**nda %80+ başarıya ulaşsın.

---

## 3) Oyun Modları

* **Eğitim (Learn):** Kısa etkileşimli dersler + mini uygulamalar (QTE, sürükle-bırak, doğru sırayı dizme).
* **Senaryo (Sim):** Zaman akışlı, dallanan olaylar (örn. kafe, ofis, yol kenarı). Kararlara göre hasta durumu değişir.
* **Sınav (Assess):** Rastgeleleştirilmiş vaka bankasından sorular + kısa simülasyonlar; süre sınırı.
* **Serbest Pratik (Sandbox):** Bası ritmini metronomla çalış, turnike bağlama pratikleri.
* **Kooperatif (Opsiyonel V2):** 2–4 kişilik çevrim içi vaka çözümü ve rol paylaşımı.

---

## 4) Çekirdek Oyun Döngüsü

1. **Hazırlık:** Senaryoya giriş, hedefler, ekipman listesi.
2. **Değerlendirme:** Güvenlik, bilinç kontrolü, yardım çağırma, ABC adımları.
3. **Müdahale:** Doğru eylemleri seç/uygula (envanter, pozisyonlama, kompresyon QTE).
4. **Geri Bildirim:** Anlık ipuçları (Eğitim), gecikmeli puanlama (Sınav).
5. **Pekiştirme:** Hata analizi, tekrar/iyileştirme önerisi, rozet/XP.

---

## 5) Oynanış Mekanikleri

* **Karar Ağaçları:** Dallanma ve yanıt sürelerine göre sonuçlar.
* **Vital Takibi:** Nabız, solunum, cilt rengi; yanlış adımlarda kötüleşme.
* **QTE & Ritim:** CPR için 100–120/dk metronom, isabet penceresi.
* **Envanter & Ortam Etkileşimi:** İlk yardım çantası, çevreden materyal toplama (bez, çubuk vb.).
* **İpucu Sistemi:** Eğitim modunda üç kademeli ipucu; sınavda kapalı.
* **Spaced Repetition:** Tekrar yüzeyleyen mikro sorular; zayıf alanlara adaptasyon.

---

## 6) Puanlama, Rozetler ve Geri Bildirim

* **Skor Bileşenleri:** Doğruluk (%), hız, güvenlik (hata/ihmal), kaynak kullanımı.
* **Rozet Örnekleri:** “Altın Kompresyon”, “Kanama Ustası”, “Sakin Kurtarıcı”.
* **Seviyeleme:** XP ile modül açma; sınavda seviye sınırı yok.
* **Hata Raporu:** Yanlış adım, doğru sıralama, kaçırılan kontrol noktaları; tekrar önerileri.

---

## 7) İçerik & Vaka Bankası

* **Vaka yapısı:** Ortam + hasta profili + başlangıç durumu + olay akışı + dallanan sonuçlar.
* **Parametreleme:** Zorluk (Easy/Normal/Hard), rastgele dikkat dağıtıcılar, ekipman mevcudiyeti.
* **Kapsam:** CPR/AED, kanama, boğulma, yanık, kırık-çıkık, şok, nöbet, alerjik reaksiyon, zehirlenme.

### Örnek Senaryo: “Kafede Boğulma”

* **Durum:** 45 yaş erkek öksürüyor, solunum sesli, 30 sn sonra bilinci azalıyor.
* **Hedef:** Yabancı cismi çıkarmak, gerekirse bilinç kaybında CPR.
* **Kritik kararlar:** Öksürüyebiliyorsa teşvik mi, 5 sırt vuruşu mu, 5 abdominal itiş mi, ne zaman 112?
* **Hatalar:** Aşırı güç, yanlış yaş tekniği, gecikmiş yardım çağrısı.
* **Başarı:** Saniye bazlı zaman çizelgesinde oksijen satürasyonu iyileşir, olay kapanır.

---

## 8) Teknik Mimari (Unity)

* **Motor:** Unity 2022 LTS veya 2023 LTS, **URP**.
* **Paketler:** Cinemachine, Timeline, Addressables, New Input System, TextMeshPro, Localization, Netcode for GameObjects (V2 opsiyonel), Unity Mediation (gerekirse), Recorder (QA için).
* **Sahne Mimari:** Hub (Ana Menü) → Eğitim Modülleri → Senaryo Sahneleri → Sınav.
* **Veri Odaklı Tasarım:** Senaryo, soru bankası, ipuçları **ScriptableObject** tabanlı.
* **Adreslenebilir İçerik:** DLC/ek paketlerle yeni vakalar eklenebilir.
* **Analitik:** Unity Analytics veya özel xAPI gönderimi; hata/başarı event’leri.

---

## 10) Değerlendirme Motoru & LMS Entegrasyonu

* **Soru Tipleri:** Çoktan seçmeli, sürükle-bırak sıralama, mini-sim adımı (ör. 5 sırt vuruşu akışı).
* **Adaptif Test:** Zayıf öğrenilen konuları daha sık sorma.
* **xAPI/SCORM (Opsiyonel):** Cihazdan LRS/LMS’e gönderim: `experienced`, `answered`, `passed/failed`, skor ve süre.
* **Raporlama:** Modül/konu bazında başarı, son deneme puanı, zaman çizelgesi.

---

## 11) Erişilebilirlik & Yerelleştirme

* **Arayüz:** Büyük font, yüksek kontrast, renk körlüğü paletleri.
* **Seslendirme & Altyazı:** Tüm eğitim metinleri için.
* **Basit Mod:** Daha geniş QTE penceresi, ekstra ipucu.
* **Yerelleştirme:** Localization paketiyle TR/EN çok dilli.

---

## 12) Güvenlik, Etik ve Uyarılar

* **Uyarı:** “Oyun gerçek tıbbi danışma yerine geçmez.”
* **İçerik Hassasiyeti:** Kan/yaralanma şiddeti ayarı; turnike vb. tartışmalı adımlar için kaynak notu.

---

## 13) Üretim Planı (12 Hafta Örnek)

* **Hafta 1–2:** Ön prod: GDD, teknik keşif, temel sahneler, veri modeli.
* **Hafta 3–4:** Eğitim modülleri (CPR, kanama), temel UI/UX, metronom QTE.
* **Hafta 5–6:** 3 senaryo (kafe, ofis, trafik), envanter sistemi.
* **Hafta 7–8:** Sınav modu, vaka bankası araçları, analitik event’leri.
* **Hafta 9:** Erişilebilirlik, yerelleştirme altyapısı.
* **Hafta 10:** QA, telemetry tuning, dengeleme.
* **Hafta 11:** Beta; kurum içi pilot test.
* **Hafta 12:** Yayın hazırlığı, içerik paketleme (Addressables).

**Ekip** (minimum): 1 Unity dev, 1 teknik tasarımcı, 1 içerik/SME (ilk yardım uzmanı), 1 3D/2D artist, 1 QA.

---

## 14) Test Stratejisi

* **Birim test:** Karar ağaçları ve skorlamada PlayMode/EditMode testleri.
* **Oyun içi telemetri:** Yanlış adım ısı haritaları, ortalama süreler.
* **Kullanıcı testleri:** 5–8 katılımcı ile görev tamamlama.

---

## 15) Sanat & Ses

* **Görsel Stil:** Düşük-orta poligon, temiz UI; dikkat dağıtmayan palet.
* **Ses:** Metronom, ortam sesleri, sakinleştirici rehber ses; kritik hatalarda kısa uyarı tonu.

---

## 16) Başarı Metrikleri (KPI)

* Eğitim modüllerinde **tamamlama oranı ≥ %75**
* Sınav modunda **ilk denemede başarı ≥ %60**, ikinci denemede ≥ %80
* Ortalama seans süresi **≥ 8 dk**
* Tekrar dönüş oranı (7 gün) **≥ %35**

---

## 17) Riskler & Önlemler

* **Tıbbi doğruluk:** SME ile içerik doğrulama, kaynak listesi.
* **Cihaz çeşitliliği:** URP + kalite ayar profilleri; mobilde performans bütçesi.
* **Aşırı zorluk:** Adaptif ipucu ve zorluk merdiveni.

---

## 18) Yol Haritası (V2+)

* Kooperatif vaka çözümü, lider panoları.
* Karma gerçeklik (AR) ile ilk yardım çantası etkileşimi.
* Genişletilmiş vaka paketleri (okul, fabrika, afet).
