&nbsp;Sürücü Uykululuk Tespiti (Driver Drowsiness Detection)



Bu proje, sürücülerde \*\*uyku hali ve dikkat kaybını\*\* gerçek zamanlı olarak tespit etmek amacıyla geliştirilmiştir. 

Sistem, yüz üzerindeki göz noktalarını kullanarak \*\*Göz En/Boy Oranı (Eye Aspect Ratio - EAR)\*\* hesaplar ve

bu değere göre sürücünün \*\*aktif, uykulu (drowsy) veya uyuyor (sleeping)\*\* durumunda olup olmadığını belirler.



Uyku hali tespit edildiğinde \*\*sesli alarm\*\* ile kullanıcı uyarılır.



---



\## Projenin Özellikleri



\- Gerçek zamanlı kamera görüntüsü ile çalışma

\- Göz kırpma ve göz kapama durumunun EAR metriği ile analizi

\- Kullanıcıya özel \*\*kalibrasyon\*\* (yüz ve göz yapısına uyum)

\- Düşük ışık koşullarına uyum

\- Uykululuk durumunda \*\*düzenli sesli alarm\*\*

\- Yüz ve göz noktalarının ekranda görselleştirilmesi



---



\## Kullanılan Teknolojiler ve Kütüphaneler



\- \*\*Python\*\*: Ana programlama dili

\- \*\*OpenCV (cv2)\*\*: Kamera erişimi ve görüntü işleme

\- \*\*Dlib\*\*: Yüz tespiti ve 68 noktalı yüz işaretleme modeli

\- \*\*NumPy\*\*: Matematiksel hesaplamalar

\- \*\*Pygame\*\*: Sesli alarm sistemi

\- \*\*Imutils\*\*: Yüz işaret noktalarının dönüştürülmesi



---



\## Proje Dosya Yapısı



driver-drowsiness-detection

│

├── src

│ └── drowsinessproje.ipynb # Ana proje kodu (Jupyter Notebook)

│

├── models

│ └── shape\_predictor\_68\_face\_landmarks.dat # Yüz işaretleme modeli

│

├── assets

│ └── alarm.opus # Uyku durumunda çalan alarm sesi

│

└── README.md



yaml

Kodu kopyala



---



\## Çalışma Mantığı (Özet)



1\. Kamera üzerinden yüz tespiti yapılır.

2\. Göz çevresindeki noktalar kullanılarak EAR değeri hesaplanır.

3\. Başlangıçta kısa bir \*\*kalibrasyon süreci\*\* ile referans EAR belirlenir.

4\. EAR değerine göre durum sınıflandırılır:

&nbsp;  - \*\*Active (Aktif)\*\*

&nbsp;  - \*\*Drowsy (Uykulu)\*\*

&nbsp;  - \*\*Sleeping (Uyuyor)\*\*

5\. Sleeping durumunda sesli alarm devreye girer ve durum devam ettiği sürece tekrar eder.



---



\## Notlar



\- Proje \*\*Jupyter Notebook ortamında\*\* geliştirilmiş ve test edilmiştir.

\- Model dosyası (`shape\_predictor\_68\_face\_landmarks.dat`) Dlib kütüphanesine aittir.

\- Bu proje eğitim ve akademik amaçlı geliştirilmiştir.



---



\## Geliştirme Süreci



Bu proje, farklı kalibrasyon yöntemleri ve eşik değerleri denenerek adım adım geliştirilmiştir.

Kod zaman içinde iyileştirilmiş, yanlış pozitif alarm problemleri azaltılmıştır.



---



\## Lisans



Bu proje eğitim amaçlıdır. Ticari kullanım için ek düzenlemeler gerekebilir.

