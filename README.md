<h1>GOMSIS</h1>
<h1>Raspberry PI PIR Sensör ve Webcam ile EMAIL Resim Gönderme</h1>
<p>PROJENİN AMACI ARM MİMARİSİ OLAN RASPBERRY Pİ DONANIM KARTI, PIR SENSOR VE WEBCAM İLE HAREKET ALGILANMASI İLE WEBCAMDEN RESİM ÇEKİLEREK KULLANICIYA ÇEKİLEN RESMİ MAİL OLARAK PAYLAŞMAKTIR.</p>
<p>Projenin adım adım yapılış videosunu ve projenin sunum videosunu video.txt'e uzantılı text dosyasından ulaşabilirsiniz.</p>
<h1>Proje Gereksinimleri</h1>
<p>1-Raspberry Pi 3B+</p>
<p>2-PIR Sensor</p>
<p>3-Webcam</p>
<p>4-Micro SD Kart 16 GB</p>
<p>5-Adaptör 5V-3A  USB-C</p>
<p>6-Bağlantı için gerekli kablolar</p>
<h1>İşletim Sistemi</h1>
<p>Raspbian İşletim Sistemi</p>
<h1>İşletim Sisteminin Kurulumu</h1>
<p>SD Card Formatter programı ile SD Kart formatlanabilir. Daha sonra "Win32 Disk Imager" programı ile SD Kart'a önceden indirilen Rasbian işletim sistemi yüklenebilir. Ayrıca proje anlatım videosunun ilk dakikasında işletim sisteminin kurulumunu bulabilirsiniz.</p>
<p><a href="https://www.raspberrypi.org/downloads/raspberry-pi-os/" target="_blank">Rasbian işletim sistemi indirme linki</a></p>
<p><a href="https://www.sdcard.org/downloads/formatter/" target="_blank">SD Card Formatter programı indirme linki</a></p>
<p><a href="https://sourceforge.net/projects/win32diskimager/" target="_blank">Win32 Disk Imager programı indirme linki</a></p>
<h1>HC- SR501 AYARLANABILIR IR HAREKET ALGILAMA SENSÖRÜ - PIR</h1>
<p>• PIR : PASİF KIZILÖTESİ SENSOR, GÖRÜŞ ALANINA GİREN NESNELERDEN YAYILAN KIZILÖTESİ IŞIK MİKTARINI ÖLÇEN SENSÖR.</p>
<p>• PIR SENSÖRLERI, BIR ORTAMDA OLUŞAN CANLI HAREKETINI ALGILAMAK IÇIN KULLANILAN SENSÖRLERDIR.</p>
<p>• DIJITAL ÇIKIŞLI OLAN BU MODÜL ;</p>
<pre><code>• ORTAMDA HAREKET ALGILAMADIĞI ZAMAN LOJIK 0, 

• HAREKET ALGILADIĞI ZAMAN ISE LOJIK 1 ÇIKIŞI VERMEKTEDIR.
</code></pre>
<p>• SENSÖR ÜZERINDE SX VE TX OLMAK ÜZERE IKI ADET POTANSIYOMETRE BULUNMAKTADIR.</p>
<pre><code>• SX POTANSIYOMETRESI SENSÖRÜN GÖRME MESAFESINI 3 ILE 5 METRE ARASINDA DEĞIŞTIRMEKTEDIR. 

• TX POTU ISE SENSÖR GÖRDÜKTEN SONRA NE KADAR SÜRE DAHA ÇIKIŞ PININDEN LOJIK 1(3.3V) ÇIKIŞINI VERECEĞINI AYARLAMAKTADIR.
</code></pre>
<h1>Web CAM EVEREST SC-301</h1>
<p>• USB2.0 YÜKSEK HIZLI VERI ARAYÜZÜ, USB1.1 ILE UYUMLU.</p>
<p>• BIRDEN FAZLA GÜVENLIK ÖZELLIKLERI, YÜKSEK KALITEDE DAHILI MIKROFON ÖZELLIKLERI.</p>
<p>• OTOMATIK YÜZ IZLEME IÇIN YAZILIM FONKSIYON, ÇOK ETKILI FOTOĞRAF KARESI</p>
<p>• CMOS RENKLI GÖRÜNTÜ ALGILAYICI</p>
<p>• YAZLIMSAL 12 MP. DONANIMSAL 640X480 PIKSEL</p>
<p>• ÇÖZÜNÜRLÜK: 640X480 PIKSEL</p>
<p>• GÖRÜNTÜ BOYUTU: 4000X3000 PIKSELE KADAR</p>
<p>• FRAME HIZI: 30 FPS / SN</p>
<h1>Donanım Yapısı</h1>
<p>• USB WEBCAM RASPBERRY Pİ’ DAKİ USB PORTUNA BAĞLANIR. PIR SENSÖRÜNÜN GERİLİM VE TOPRAK BESLEMESİNİ RASPBERRY Pİ’ YA AİT 5 VOLT VE GROUND PİNLERİNE BAĞLANDIKTAN SONRA OUT PİNİ’DE HERHANGİ BİR GPIO PİNİNE BAĞLANABİLİR.</p>
<p>• YAPILAN PROJEDE PIR SENSÖRÜNÜN OUT PİNİ GPIO 17 PİNİNE BAĞLANMIŞTIR.</p>

<h1>Proje Adımları</h1>
<pre><code>1-) Raspbian İşletim sistemini Sd karta yükle.
2-) Güncelemeleri gerçekleştir.
3-) Donanım Bağlantılarını gerçekleştir.
4-) Raspberry Pi için Python GPIO kütüphanesini kur.
    Kurulum için :
        -wget https://pypi.python.org/packages/source/R/RPi.GPIO/RPi.GPIO-0.5.11.tar.gz
        - tar -xvf RPi.GPIO-0.5.11.tar.gz
        - cd RPi.GPIO-0.5.11
        - sudo python setup.py install
5-)Standart USB webcam kütüphanesini kur.
    Kurulum için :
        - sudo apt-get install fswebcam
6-) SSMTP kütüphanesini kur.
    Kurulum için:
        - sudo apt-get install ssmtp
        - sudo apt-get install mailutils
        - sudo nano /etc/ssmtp/ssmtp.conf
</code></pre>

