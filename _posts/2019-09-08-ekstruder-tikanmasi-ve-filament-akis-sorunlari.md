---
layout: post
title: Ekstruder Tıkanması ve Filament Akış Sorunları
date: 2019-09-08 23:20:20 +0300
description: Nozülün Tıkanması, Filamentin Kendi Yolunu Kapatarak Tıkanması, Yay Gerginlik Ayarı, Hot End Vida Bağlantılarından Filament Sızması
img: extruder_hot_cold_end_parcalari.webp # Add image post (optional)
fig-caption: # Add figcaption (optional)
tags: [Extruder, 3D, 3D Yazıcı Sorunları]
---

 Sorunun nerede olabileceğine bakmadan önce bir ekstrüzyon sisteminin nasıl çalıştığına bakarsak sorunu daha kolay çözebiliriz.

* Tipik Bir Ekstrüzyon Sistemi
	1. Motor ve İtiş
	2. Dişli Sistemi
	3. Yay(lar)
	4. Cold End (Soğuk kısım)
	5. Hot End (Sıcak kısım)
* Sorunlar
	1. Gevşek Setskur Vida
	2. Filament Makarası Sorunları
	3. Nozülün Tıkanması
	4. Filamentin Kendi Yolunu Kapatarak Tıkanması
		1. Ekstruder Radyatörünün Soğutulması
		2. PTFE Boru ile Filament Yolu
	5. Yay Gerginlik Ayarı
	6. Hot End Vida Bağlantılarından Filament Sızması

## Tipik Bir Ekstrüzyon Sistemi

### 1. Motor ve İtiş
 Genelde, motorun miline takılan *hobbed gear* denilen bir dişli ve bu dişlinin karşına gelen bir rulman bulunur. Filament bu dişli ve rulman arasına sıkıştırılır. Motor miline bağlı dişlinin dönmesiyle de filament hareket etmiş olur.

![Extruder Hobbed Bolt]({{site.baseurl}}/assets/img/hobbed_bolt_filament.webp)

 Bazı ekstruderlerde hareketi kolaylaştırmak ve hassaslaştırmak için dişli sistemleri ile tork kazancı sağlanır. Bu tür sistemlerde motor miline küçük bir dişli, küçük dişlinin döndürdüğü büyük bir dişli ve büyük dişliye bağlı dişli vida (hobbed bolt) bulunur.

![Dişliler İle Tork Kazancı]({{site.baseurl}}/assets/img/disliler_ile_tork_kazanci.webp)

### 2. Yay(lar)
 Hobbed bolt ve rulman arasına sıkıştırılan filament her zaman aynı genişlikte değildir. Mesela aldığınız filamentin kutusunda 1.75mm yazıyor olabilir ama aynı filamentin bazı yerleri 1.70mm, bazı yerleri 1.80mm olabilir. Hobbed bolt ve rulman arasındaki mesafenin de buna göre değişebilmesi gerekir. Filament inceldiğinde daralmalı, kalınlaştığında genişlemelidir. Yoksa extrüzyon durur. Bu yüzden rulman direk vida ile değil, araya yay eklenerek tutturulur. Bazı ekstruderlerde 1, bazılarında 2 yay kullanılır.

![Ekstruder Yayları]({{site.baseurl}}/assets/img/ekstruder_yaylari.webp)

 Yaylar, filament inceldiğinde rulmanı tutan parçayı iterek rulmanı hobbed bolta yaklaştırır ve boşluk oluşmamasını sağlar.
 Tam tersi durumda, yani filament kalınlaştığında da rulmanın geri gelerek filamentin geçebilmesini sağlar.
 Eğer uygun bir yay bulamadıysanız tükenmez kalem yayı kullanabilirsiniz. Bazı tükenmez kalemlerin yayları kullanılabilir.


### 3. Cold End (Soğuk Kısım)
 Filament itildikten sonra eritilmek için sıcak uca ulaşmadan önce genelde alüminyum olan soğuk bir radyatörden geçip çelik bir barele ulaşır. Buraya kadar filament hâlâ katıdır.

![Ekstruder Parçaları]({{site.baseurl}}/assets/img/ekstruder_parcalari.webp)

### 4. Hot End (Sıcak Kısım)
 Ardından çelik barelin ucundaki ısıtılmış alüminyum bloğa bağlı nozül'e (nozzle) ulaşır ve burada erir. 

## Sorunlar

### 1. Gevşek Setskur Vida
 Ekstruder motorunun miline takılan dişlinin setskur vidası gevşemişse motor mili dönecek ama ona bağlı dişli dönmeyecektir. Eğer dişli, plastikse çok fazla sıkarsanız kırılabilir.

![Extruder Dişlisinin Setskur Vidası]({{site.baseurl}}/assets/img/extruder_setskur.webp)

### 2. Filament Makarası Sorunları
 Extruder motoru kolay dönebilen bir makaradan filamenti çekebilir ama filament makarası kolay dönmüyorsa motor filamenti çekemeyecektir.

 Makaranın yeterince kolay dönüp dönmediğini kontrol etmek için filamenti elinizle çekmeyi deneyebilirsiniz. Eğer elinizle zorlamadan çekemiyorsanız motor da çekemeyecektir.

### 3. Nozülün Tıkanması
 Nozülün tıkanması filamentle birlikte içeri giren tozdan kaynaklanıyor olabilir. Filamentin temiz ve kuru olduğundan emin olun. Genelde yazdırma sıcaklığının 20°C üzerinde filamenti elinizle itmeniz nozülü açacaktır ama söküp temizlemeniz gerekirse:

( **Nozül sıcakken kesinlikle elinizle dokunmayın!** )
1. Nozülü 240°C'a ısıtıp yaylı vidaları söküp filamenti çıkarın.
2. Nozülü sıcakken neredeyse çıkacak kadar gevşetin. Soğuduğunda sökülmeyebilir.( **Sakın elinizle dokunmayın!** )
3. Isıtmayı kapatmadan rezistansı veya termistörü çıkartmayın. Soğumasını bekleyin.
4. Nozülü söküp çıkardıktan sonra temizleyebilirsiniz. Soğuyan plastik çıkmıyorsa nozülü penseyle tutup çakmakla ısıtarak metal bir şeyle temizleyebilirsiniz.

### 4. Filamentin Kendi Yolunu Kapatarak Tıkanması
 3D yazıcılarda ekstruderin tıkanmasına sebep olan sorunlardan en sık görülenidir. Sıcak alüminyum bloktaki ısı önce çelik barele, ordan da alüminyum radyatöre geçecektir. Bu da alüminyum radyatörün ısınması anlamına gelir. Alüminyum radyatör ısınırsa filament erimesi gereken yerden çok daha geride yumuşayıp şekil değiştirecek ve şekil değiştirdikten sonra katılaşarak yolunu tıkayacaktır. Alüminyum radyatörün soğutulması ve PTFE (Teflon) boru kullanılarak filamentin yumuşadığında şekil değiştirmesinin önlenmesi gerekir.

#### a. Ekstruder Radyatörünün Soğutulması
 30x30mm bir fan alüminyum bloğu soğutmak için yeterli olacaktır. 3D yazıcılarda kullanılan fanların çalışma gerilimi genelde 12 Volt olur.

![Ekstruder Alümiyum Bloğun Fan ile Soğutlması]({{site.baseurl}}/assets/img/aluminyum_blok_sogutma_fan.webp)

 Asıl önemli nokta bu fan sadece yazdırma sırasında değil, yazıcı açık olduğu sürece **her zaman** çalışmalıdır. RAMPS üzerinde fanın bağlanması gereken yer:

![RAMPS v1.4 Üzerinde Extruder Fanı Bağlantısı]({{site.baseurl}}/assets/img/RAMPS_extruder_fan_pin.webp)
 RAMPS dışında bir kart kullanıyorsanız doğrudan 12V güç kaynağına veya kontrol kartınızın 12 Volt güç girişine bağlayabilirsiniz. Bu bağlantıyı yaptıktan sonra yazıcı açıksa yazdırma yapmıyorken bile fan çalışacaktır. Çalışmıyorsa fanı ve bağlantıları kontrol edin.
 Bu konuda dikkat etmeniz gereken bir diğer nokta yazdırma tamamlandıktan hemen sonra hot end soğumadan yazıcıyı kapatırsanız fan duracak ve ısı cold ende geçip filamenti burada eritebilir. Bu yüzden sıcaklık 40°C'a düşene kadar yazıcıyı kapatmamalısınız.

#### b. PTFE Boru ile Filament Yolu
 Alüminyum radyatörün başlangıcından başlayıp nozülün başlangıcına kadar devam eden bir PTFE boru, filamentin yumuşadığında kendini tıkamasını engelleyecektir. Bazı ekstruderlerin yanında gelen, çelik barelden nozüle kadar olan PTFE boru yetersiz kalabiliyor. Eğer böyle bir extrudere sahipseniz radyatörün başlangıcından çelik barele kadar bir PTFE boru daha eklemeniz gerekir.
 
> **PTFE boruların maksimum çalışma sıcaklığı 260°C ile sınırlıdır.**

![Çelik Barel PTFE Ekleme]({{site.baseurl}}/assets/img/barel_PTFE_ekleme.webp)

![Çelik Barel Teflon Ekleme]({{site.baseurl}}/assets/img/barel_teflon_ekleme.webp)

![Alüminyum Radyatör için Teflon PTFE Boru]({{site.baseurl}}/assets/img/extruder_ptfe_ekleme.webp)

### 5. Yay Gerginlik Ayarı
 Yaylar çok gevşekse ekstruder filamenti kavrayamayacak ve itemeyecektir. Eğer çok fazla sıkarsanız da motor hobbed boltu çeviremeyecektir.

Yayların gerginliğini kontrol etmek için:
1. Filamenti çıkartın.
2. Alüminyum radyatörden itibaren filamentin geçeceği bütün parçaları söküp ayırın.
3. Gücü kesin.
4. Extruder motorunun kablosunu çıkartın.
5. Ekstruderi elinizle hızlıca çevirerek filamentin yeterince hareket edip etmediğine bakın.

Çok kolay bir işlem değil ama yay gerginliği ile alakalı bir sorununuz varsa anlamınızı sağlayacaktır.

### 6. Hot End Vida Bağlantılarından Filament Sızması
 Isıtılan alüminyum bloğa bağlı nozül ve çelik barelin vida dişlerinin arasından erimiş plastik sızabilir. Nozül ve çelik bareli söküp vida dişlerine tesisatçıların kullandığı PTFE (Teflon) bant sarmak gerekir.
1. Vida dişlerini kir, plastik vb. her şeyden tamamen temizleyin.
2. Teflon bandı biraz gererek **saat yönünde** bir kaç tur sarın. Tersi yönde sararsanız vidayı takarken bant sökülecektir.

![Filament Sızması Sorunu Çözümü]({{site.baseurl}}/assets/img/filament_sizdirma.webp)

Çelik bareli alüminyum radyatöre bağlayan dişlere de (Fotoğrafta teflon bant sarılmamış olan dişlere) taşmayacak kadar termal macun sürmeniz filamentin yanlış yerde erimemesi için barelin daha etkili soğutulmasını sağlayacaktır.


Önerilerinizi ve hatalarımı yorumlarda belirtirseniz yazıyı ona göre güncelleyebilirim. Sorunsuz yazdırmalar...
