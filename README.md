IdeaSoft Hediye Paketi Bileşeni

IdeaSoft ürün detay sayfasına ücretli hediye paketi seçenekleri ekleyen, mobil uyumlu bir tema bileşenidir.

Geliştiren: Midas Dijital E-Ticaret Danışmanlık

Özellikler

Birden fazla ücretli paket seçeneği

Seçilen paket ürününü ana üründen sonra otomatik olarak sepete ekleme

IdeaSoft'un yerleşik data-selector="add-to-cart" mekanizmasıyla çalışma

Mobil uyumlu modern görünüm

Hediye paketi ürünlerinin kendi sayfalarında bileşeni gizleme

JavaScript ile seçili seçenek vurgusu

Dosyalar

ideasoft-gift-package/
├── assets/
│   ├── gift-package.css
│   └── gift-package.js
├── gift-package.twig
├── LICENSE
└── README.md

Kurulum

gift-package.twig dosyasını IdeaSoft temanızın uygun snippet klasörüne yükleyin.

gift-package.css ve gift-package.js dosyalarını tema asset klasörüne yükleyin.

detail.twig içinde .product-cart-buttons bloğunun hemen üstüne aşağıdaki satırı ekleyin:

{% include "html/snippets/product/gift-package.twig" %}

Tema dosya yolunuz farklıysa include yolunu kendi klasör yapınıza göre değiştirin.

Dosyaları ayrı yüklemek istemiyorsanız gift-package.twig içeriğini aynı konuma doğrudan yapıştırabilir, CSS ve JavaScript'i ilgili tema dosyalarına ekleyebilirsiniz.

Ürünleri düzenleme

Hediye paketi ürünlerini önce IdeaSoft yönetim panelinde normal ürün olarak oluşturun. Sonra gift-package.twig içindeki her seçenekte şu alanları değiştirin:

<input type="radio" name="giftProducts" value="464">
<span class="md-gift-package__price">+100,00 TL</span>
<a href="/urun/hediye-paketi">Görüntüle</a>

value: IdeaSoft ürün ID'si

Fiyat metni: Müşterinin göreceği tutar

href: Paket ürününün bağlantısı

Gerçek sepet fiyatı IdeaSoft'taki ürün kartından alınır. Twig dosyasındaki fiyat yalnızca bilgilendirme metnidir.

Yeni paket ürünlerinin kendi sayfalarında bileşenin görünmemesi için üstteki hariç tutma listesini güncelleyin:

{% if product.id not in [464, 465] %}

Uyumluluk notu

Bileşen, sepete ekleme butonunda aşağıdaki IdeaSoft işaretlemesini kullanan temalar için hazırlanmıştır:

data-selector="add-to-cart"
data-context="detail"
data-product-id="..."

Özel olarak değiştirilmiş temalarda buton seçicisinin gift-package.js içinde uyarlanması gerekebilir.

Lisans

MIT Lisansı ile sunulmuştur.
