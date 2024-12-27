
# Nginx
<div style="display: flex; justify-content: space-around;">
  <img src="https://dwglogo.com/wp-content/uploads/2017/09/3630px-Nginx_logo-1024x704.png" width="400"/>
  <img src="https://dwglogo.com/wp-content/uploads/2017/09/Nginx_logo-1024x576.png" width="400"/>
</div>

## 1. Nginx Nedir?

Nginx, açık kaynaklı ve yüksek performanslı bir web sunucusu ile ters proxy sunucusu olarak tanımlanabilir. İlk kez 2004 yılında Igor Sysoev tarafından geliştirilmiş olup, günümüzde modern web altyapılarının gereksinimlerini karşılamak için yaygın bir şekilde kullanılmaktadır. Nginx'in temel hedefi, yüksek hız, ölçeklenebilirlik ve düşük kaynak kullanımı gibi önemli özellikleri bir arada sunarak, web sunucusu ve proxy sunucusu işlevlerini etkin bir biçimde yerine getirmektir.

Nginx, özellikle yüksek trafikli web siteleri için tasarlanmış olup, asenkron ve olay tabanlı yapısı sayesinde çok sayıda eşzamanlı bağlantıyı verimli bir şekilde yönetebilir. Bu yapı, Nginx’i geleneksel web sunucularına kıyasla çok daha verimli hale getirirken, aynı zamanda daha düşük bellek ve işlemci kullanımı sağlar. Bu nedenle, Nginx yalnızca web sunucusu olarak değil, aynı zamanda yük dengeleme, içerik önbellekleme ve ters proxy gibi ek işlevler de sunmaktadır.

Nginx’in yüksek performansı ve ölçeklenebilirliği, onu özellikle büyük web uygulamaları ve mikro hizmet mimarileri için ideal bir çözüm haline getirmiştir. Nginx, statik dosyaların sunulmasında olduğu kadar, dinamik içeriklerin yönetilmesinde de etkili bir biçimde kullanılabilmektedir. Ayrıca, SSL/TLS desteği ile güvenli web trafiğini yönetme, HTTP/2 desteği ile hızlı veri iletimi sağlama ve trafik yönlendirme gibi gelişmiş özelliklere sahiptir.

Nginx’in yaygın kullanım alanları arasında yüksek trafikli web siteleri, mikro hizmet mimarileri, API yönetimi ve yük dengeleme bulunmaktadır. Web uygulamaları ve servisleri arasındaki trafiği dengeleyerek, yüksek erişilebilirlik ve hata toleransı sağlamak için sıklıkla tercih edilmektedir. Ayrıca, içerik önbellekleme özelliği sayesinde web sayfalarının daha hızlı yüklenmesi ve sunucu üzerindeki yükün azaltılması sağlanmaktadır.

Sonuç olarak, Nginx, modern web altyapılarının temel taşlarından biri haline gelmiş ve dünya çapında birçok büyük teknoloji şirketi tarafından benimsenmiştir. Sağladığı yüksek performans, güvenlik ve esneklik ile hem küçük ölçekli projeler hem de büyük ölçekli kurumsal uygulamalar için uygun bir çözüm sunmaktadır.

### 1.1 Temel Özellikler
- Ters Proxy
- Yük Dengeleme
- Sanal Ana Bilgisayar
- Statik ve indeks dosyalarının sunumu, otomatik indeksleme

### 1.2 Benchmarking (Kıyaslama)
Apache HTTP Sunucusu ve Lighttpd, şu anki Nginx alternatifleri arasında yer almaktadır. Nginx, bu alternatiflere kıyasla %400 daha fazla performans sunmakta ve çok daha az CPU kullanmaktadır.

<div style="display: flex; justify-content: space-between;">
  <img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*dFTC96_ZB-CYPFfBFUsSsw.jpeg" width="41%" />
  <img src="https://miro.medium.com/v2/resize:fit:640/format:webp/1*LzYYSJeF--EvjBAwwPgweg.jpeg" width="45%" />
</div>


### 1.1.1 Reverse Proxy (Ters Proxy)
Ters proxy, istemciden gelen istekleri alıp, hedef sunucuya ileten ve sunucudan dönen yanıtları istemciye aktaran bir vekil sunucudur. Bu yapı, sunucunun varlığını ve özelliklerini gizleyerek güvenlik sağlar, istemcileri web tabanlı saldırılardan korur ve web üzerindeki yükü azaltarak daha hızlı yanıt süreleri sunar. Ayrıca, yüksek trafikli ortamlarda yük dengeleme ve ölçeklenebilirlik sağlayarak web sunucularının performansını artırır.

Sağladığı Avantajlar:
- Reverse proxy'ler, sunucuların varlığını ve özelliklerini gizleyebilir,
- İstemcileri web tabanlı saldırılara karşı koruyabilir,
- Reverse proxy'ler, web sunucuları üzerinden yükü azaltarak web isteklerine hızlı bir şekilde cevap verebilir.

![Ters Proxy](https://miro.medium.com/v2/resize:fit:750/format:webp/1*DJBLIoHFLDH8Aged532YfA.png)

### 1.1.2 Load Balancing (Yük Dengeleme)
Yük dengeleme, gelen isteklerin birden fazla sunucuya eşit bir şekilde dağıtılması işlemidir. Bu yöntem, sistemin performansını ve verimliliğini artırarak, aynı zamanda yüksek erişilebilirlik ve hata toleransı sağlar. Yük dengeleme, işlemlerin paralel olarak gerçekleştirilmesini mümkün kılarak, işlem sürelerini kısaltır ve kullanıcı deneyimini iyileştirir.

<img src="https://miro.medium.com/v2/resize:fit:1400/format:webp/1*fruOlA7WzZmkrkiCmBf_5Q.png" width="65%" />

## 2. Neden Nginx Kullanılmalı?

### 2.1 Tek Giriş Noktası
NGINX, uygulamaların veya mikro hizmetlerin yönetimini tek bir giriş noktasından sağlar. Kullanıcılar, sabit bir genel IP adresi aracılığıyla trafiğe erişebilirken, NGINX dinamik olarak konteynerleri dağıtabilir veya kaldırabilir. Yük dengeleme özelliği sayesinde, gelen trafiği uygun mikro hizmetlere yönlendirerek sistemin performansını ve ölçeklenebilirliğini artırır. Bu özellik, NGINX'i özellikle mikro hizmet mimarileri ve yüksek trafikli uygulamalar için ideal bir çözüm haline getirir.

### 2.2 Önbellekleme
NGINX, statik ve dinamik içerikler için etkili bir önbellekleme mekanizması sunar. Bu mekanizma, her isteğin mikro hizmetlere yönlendirilmesini gereksiz kılarak, sık kullanılan verilerin önbellekte saklanmasını sağlar. Bu sayede, arka uç sistem üzerindeki yük azalır ve uygulamanın performansı ile yanıt süresi önemli ölçüde iyileşir. Yüksek trafikli uygulamalarda, bu yaklaşım kullanıcı deneyimini iyileştirmek ve sistem kaynaklarını verimli kullanmak için kritik bir öneme sahiptir.

### 2.3 Çoklu Uygulama Yönetimi
NGINX, birden fazla arka uç uygulamasıyla çalışırken trafiği verimli bir şekilde yönetir. Gelen trafiği proxy olarak yönlendirir ve her isteği uygun mikro hizmet veya konteynere aktarır. Bu yapı, uygulama akışlarını optimize eder ve sistemin performansını artırırken, yapılandırma ve yönlendirme kurallarının kesinti olmaksızın güncellenmesine olanak tanır. Böylece karmaşık uygulamaların yönetimi kolaylaşır.

### 2.4 A/B Testi
NGINX, A/B testi uygulamaları için trafik yönetimi sağlar. Trafiği bölerek, belirli kullanıcı gruplarını yeni mikro hizmetlere veya uygulama sürümlerine yönlendirir. Bu yöntem, farklı sürümlerin performansını gerçek zamanlı olarak ölçmeyi ve kullanıcı analizleri yapmayı mümkün kılar. A/B testi, kullanıcı deneyimini iyileştirmek ve en verimli tasarımı belirlemek için önemli bir araçtır.

### 2.5 Konsolide Günlük Kaydı
NGINX, tüm web trafiğini tek bir günlük formatında kaydederek merkezi bir günlükleme sistemi sunar. Mikro hizmetler için ayrı günlük dosyaları tutmak yerine, tüm trafiği tek bir noktada toplar ve yönetir. Bu yaklaşım, günlük analizlerini ve sistem takibini daha verimli hale getirir.

### 2.6 Ölçeklenebilirlik ve Hata Toleransı
NGINX, yük dengeleme ve sağlık kontrolleri özellikleri ile yüksek ölçeklenebilirlik ve hata toleransı sağlar. Bu özellik, yeni mikro hizmetlerin eklenmesini veya mevcut olanların kaldırılmasını kolaylaştırır. Sağlık kontrolleri sayesinde trafik, yanıt vermeyen mikro hizmetlere yönlendirilmez, bu da sistemin kesintisiz çalışmasını sağlar.

### 2.7 Kesintisiz Hizmet ve Sıfır Kesinti Süresi
NGINX, yazılım güncellemeleri veya yükseltmeleri sırasında bağlantı kesilmeden çalışmaya devam eder. Bu özellik, web sunucusunda sıfır kesinti süresi sağlayarak kritik uygulamalarda sürekli hizmet sunumunun kesintiye uğramamasını garantiler. Böylece, sistemdeki herhangi bir değişiklik, kullanıcı deneyimini etkilemeden gerçekleştirilebilir.

### 2.8 DoS Saldırılarına Karşı Koruma
NGINX, DoS (Denial of Service) ve DDoS (Distributed Denial of Service) saldırılarına karşı etkili koruma sunar. Trafiği yönetme ve sınırlama özellikleri ile saldırılara karşı sistemin dayanıklılığını artırır. Ayrıca, aşırı yüksek trafik ile gelen istekler sınırlanarak, uygulamanın doğru bir şekilde çalışması sağlanır.

## 3. Nginx Kullanmanın Avantajları ve Özellikleri
- **Tutarlı Kod Tabanı:** NGINX, alternatif web sunucularına kıyasla daha tutarlı bir kod tabanı sunar, bu da bakım ve geliştirilebilirlik açısından büyük bir avantaj sağlar.
- **Kolay Yapılandırma ve Modern Tasarım:** NGINX, basit ve esnek bir yapılandırma sunarak, diğer web sunucularına göre daha modern ve anlaşılır bir tasarım sağlar.
- **Olay Tabanlı Yapı:** Olay tabanlı yapısı sayesinde, NGINX birden fazla bağlantıyı yönetebilir ve bağlam değiştirme nedeniyle oluşan ek yükten kaçınarak yüksek verimlilikle çalışır.
- **Düşük Bellek ve Kaynak Kullanımı:** NGINX, minimal bellek ve kaynak kullanımı ile yüksek verimlilik sağlar, bu da düşük maliyetli ve verimli bir çözüm sunar.
- **Web Performansının Artırılması:** NGINX, web sitelerinin hızını artırarak, daha iyi bir kullanıcı deneyimi sağlar ve SEO (arama motoru optimizasyonu) açısından Google sıralamasını iyileştirmeye yardımcı olur.
- **Uyumluluk:** NGINX, Ruby, Python, WordPress, Joomla gibi yaygın olarak kullanılan web uygulamaları ile tam uyumlu çalışır.
- **Dinamik İçeriği Statik İçeriğe Dönüştürme:** Dinamik içerikleri statik içeriğe dönüştürme yeteneği, web sitesi hızını artırır ve sunucu üzerindeki yükü azaltır.
- **Eşzamanlı Bağlantı Yönetimi:** NGINX, binlerce eşzamanlı bağlantıyı aynı anda işleyerek yüksek trafik ve yoğun yük altında bile yüksek performans sağlar.

## 4. Nginx Kullanmanın Dezavantajları
- **Yapılandırma Zorlukları:** NGINX, esnek ve güçlü bir yapılandırma sunmasına rağmen, başlangıç seviyesindeki kullanıcılar için yapılandırma dosyalarını anlamak ve yönetmek zor olabilir. Özellikle karmaşık proxy ayarları ve yük dengeleme yapılandırmaları, deneyimsiz kullanıcılar için zorlu olabilir.
- **Dinamik İçerik Desteği:** NGINX, statik içerik konusunda oldukça verimli olmasına rağmen, dinamik içerik sunma konusunda Apache gibi bazı rakiplerine göre daha az verimlidir. PHP veya diğer dinamik içerik sunan uygulamaların işlenmesi için harici çözümler (FastCGI gibi) gereklidir, bu da yapılandırma sürecini karmaşıklaştırabilir.
- **Modülerlik Eksikliği:** NGINX, modüler yapısı ile bazı avantajlar sunsa da, Apache gibi diğer web sunucularına kıyasla daha sınırlı bir modül ekosistemine sahiptir. Bu, kullanıcıların belirli ihtiyaçlarına göre özelleştirmelerde sınırlamalarla karşılaşmasına neden olabilir.
- **İleri Düzey Özellikler İçin Öğrenme Eğrisi:** NGINX, gelişmiş özellikler ve yapılandırmalar için daha fazla bilgi ve deneyim gerektirir. Özellikle yük dengeleme, SSL/TLS yapılandırması ve HTTP/2 gibi ileri düzey konularda uzmanlık gerektiren bir öğrenme eğrisine sahiptir.
- **Yazılım Desteği:** NGINX’in geniş bir topluluğu olsa da, ticari destek için genellikle NGINX Plus’a geçmek gereklidir. Bu durum, özellikle küçük işletmeler veya kişisel projeler için ek maliyetler yaratabilir.
- **Hata Ayıklama Zorlukları:** NGINX’in hata mesajları, özellikle karmaşık yapılandırma hatalarında, bazen kullanıcılar için yeterince açıklayıcı olmayabilir. Bu durum, sistem yöneticilerinin veya geliştiricilerinin sorunları çözmelerini zorlaştırabilir.
