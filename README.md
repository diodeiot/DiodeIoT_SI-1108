# SI-1108 - ESP32 8 Kanal Röle Geliştirme Modülü

![Build Status](https://github.com/diodeiot/DiodeIoT_SI-1108/workflows/Arduino%20Library%20CI/badge.svg)

![top](https://user-images.githubusercontent.com/100811304/159196422-057ac591-7716-4422-81b0-32702b35ada2.png)

## SI-1108 Nedir?
SI-1108, üzerinde ESP32 mikrodenetleyicisi bulunan 8 kanal röle geliştirme modülüdür. \
Geliştiriciler, zengin örnek kodlara sahip bu kütüphaneyi kullanarak kendi uygulamalarını kolayca geliştirebilirler.

Bu geliştirme modülü:

* Akıllı Evler
* Ev Otomasyonu
* Endüstriyel Otomasyon
* Araç İçi Otomasyon
* Güç Anahtarlama

başta olmak üzere amatör ve profesyonel herhangi bir amaç için kullanılabilir.

## Dökümantasyon
[<img alt="github-pages" width="150px" src="https://user-images.githubusercontent.com/100811304/184258420-58ed4a45-29ce-4329-9260-c54ae8973690.png" />](https://diodeiot.github.io/DiodeIoT_SI-1108)

Kaynak kodların dökümantasyonuna [buradan](https://diodeiot.github.io/DiodeIoT_SI-1108) ulaşabilirsiniz.

## Teknik Özellikler

### Pin Bağlantıları

Eleman | Pin Numarası | Lojik Seviye
-- | :--: | --
BOOT Butonu | 0 | Active Low
LED | 2 | Active Low
Röle 1 | 5 | Active High
Röle 2 | 17 | Active High
Röle 3 | 16 | Active High
Röle 4 | 4 | Active High
Röle 5 | 25 | Active High
Röle 6 | 26 | Active High
Röle 7 | 27 | Active High
Röle 8 | 14 | Active High

### Elektriksel Karakteristikler

Parametre | Minimum | Nomimal | Maximum | Birim
-- | :--: | :--: | :--: | --
Giriş Gerilimi | 4.75 | 5 | 5.5 | V
Giriş Akımı | | 0.56 | | A
Röle Anahtarlama Akımı | | | 10 | A
Röle Anahtarlama Gerilimi | | | 250 | VAC

> :warning: **Uyarı**\
> Sadece 5V güç kaynağı ile kullanın.

> :warning: **Uyarı**\
> Güç kaynağını doğru polaritede bağlayın.

### Termal Bilgiler

Parametre | Minimum | Nomimal | Maximum | Birim
-- | :--: | :--: | :--: | --
Çalışma Sıcaklığı | -40 | | 85 | °C

### Mekanik Bilgiler

Parametre | Minimum | Nomimal | Maximum | Birim
-- | :--: | :--: | :--: | --
Genişlik | | 80 | | mm
Uzunluk | | 96 | | mm
Yükseklik | | 19.1 | | mm

## Gerekenler

## 1. SI-1108 Geliştirme Modülü
SI-1108 geliştirme modülünü aşağıdaki online marketlerden edinebilirsiniz:

[<img alt="özdisan" width="150px" src="https://user-images.githubusercontent.com/111313342/185208516-03412fa5-7c2a-4f45-a1b3-a4b5fa2b1e6d.png" />](https://ozdisan.com/)

[<img alt="direnc net" width="150px" src="https://user-images.githubusercontent.com/111313342/185208523-e1d5a133-d13e-490f-8011-0b83b9cfd852.png" />](https://www.direnc.net/)

[<img alt="robotistan" width="150px" src="https://user-images.githubusercontent.com/111313342/185208535-c1e5e80d-dee9-4cf9-b6ce-97cbf80e2975.png" />](https://www.robotistan.com/)

## 2. USB-UART Dönüştürücü
SI-1108 geliştirme modülünü bilgisayara bağlamak için 3.3V usb-uart dönüştürcü kullanmanız gerekmektedir. 
Dönüştürücünün `RX` `TX` `GND` pinlerini modülün `TX` `RX` `GND` pinlerine bağlayın.

> :warning: **Uyarı**\
> Modülü bilgisayarınıza bağlamak için modüle harici güç kaynağı bağlamanız gerekmektedir.

## 3. 5V Güç kaynağı
SI-1108 geliştirme modülüne 5V minimun 1A güç kaynağı bağlamalısınız.

> :warning: **Uyarı**\
> Güç kaynağını doğru polaritede bağlayın.

## 4. SI-1108 Kütüphanesi
Bu kütüphane SI-1108 geliştirme modülü için yazılmış arduino ESP32 kütüphanesidir. Geliştiriciler, zengin örnek kodlara sahip bu kütüphaneyi kullanarak kendi uygulamalarını kolayca geliştirebilirler.

> :warning: **Uyarı**\
> Bu kütüphane sadece Arduino IDE 1.5.x ve üzeri versiyonları ile uyumludur.

### Arduino IDE Kurulumu
Bu kütüphaneyi kullanmak için ilk olarak Arduino IDE gereklidir. Eğer sisteminizde Arduino IDE yüklü değil ise [burada](https://www.arduino.cc/en/software) anlatıldığı şekilde programın son sürümünü yükleyebilirsiniz.

### ESP32 Arduino Çekirdeğini Yükleme
Arduino IDE'nizi kurduktan sonra ESP32 mcu'nuzda kod geliştirmek için kullanacağınız ESP32 arduino çekirdeğini yüklemelisiniz. Bu yüklemeyi [burada](https://docs.espressif.com/projects/arduino-esp32/en/latest/installing.html) anlatıldığı şekilde arduino ide'nizdeki kütüphane yöneticisi ile kolayca yapabilirsiniz.

### SI-1108 Kütüphanesi Kurulumu

![image](https://user-images.githubusercontent.com/111313342/184759106-1a6046e1-6c6a-4bdc-900e-66309659d711.png)

SI-1108 kütüphanesini kurmak için yukarıda görüldüğü gibi kütüphaneyi zip halinde bilgisayarınıza indirin.

![image](https://user-images.githubusercontent.com/100811304/159194858-39a47764-ab8b-4f42-8298-798982687959.png)

Daha sonra arduino idenizi açıp yukarıda görülen seçeneğe tıklayıp indirdiğiniz SI-1108 kütüphanesini bilgisayarınıza kurun.

Bu adımları tamamladıktan sonra arduino idenizden dilediğiniz SI-1108 kütüphane örneklerini inceleyebilirsiniz.

## Örnek Kodlar
Örnek kodlara [buradan](./examples) erişebilirsiniz.

* [Buton ile Röle Kontrolü](./examples/button_relay_control/button_relay_control.ino) \
Bu örnekte kartın üzerindeki BOOT butonuna her bastığınızda sırası ile röleler açılmaktadır.

* [MQTT Protokolü ile Röle Kontrolü](./examples/mqtt_relay_control/mqtt_relay_control.ino) \
Bu örnekte mqtt ile kartın üzerindeki röleleri uzaktan kontrol ediyoruz.

* [Seri Konsol ile Röle Kontrolü](./examples/serial_terminal_relay_control/serial_terminal_relay_control.ino) \
Bu örnekte seri konsol ile kartın üzerindeki röleleri kontrol ediyoruz.

## Kütüphaneye Katkıda Bulunma
SI-1108 kütüphanesine katkılarınızı memnuniyetle karşılarız.
Kütüphaneye dilediğiniz katkıyı `Pull Request` ile yapabilirsiniz.

## Lisans
LGPL (GNU Kısıtlı Genel Kamu Lisansı)

![license](https://upload.wikimedia.org/wikipedia/commons/thumb/3/3b/LGPLv3_Logo.svg/200px-LGPLv3_Logo.svg.png)
