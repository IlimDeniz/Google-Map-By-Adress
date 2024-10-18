Google Maps Adres Tabanlı Entegrasyon

Daha önce projelerimde, Google Maps üzerinde bulunan "Yerleştir" butonu ile iframe kodlarını alarak web sitelerime entegre ediyordum. Ancak son projelerimde, adres girildiğinde Google Maps'in iframe kodunu otomatik olarak alabilmek için bir API entegrasyonuna ihtiyaç duydum. Bunun için Google Cloud Platform üzerinden bir hesap oluşturmak gereklidir. Aşağıda adım adım bu süreci açıklıyorum.
1. Google Cloud Platform Hesabı Oluşturma

İlk olarak, Google Cloud Platform üzerinden bir hesap oluşturmanız gerekmektedir. Bunun için:

    Google Cloud Console adresine gidin ve hesap oluşturma işlemini tamamlayın.

2. Proje Oluşturma

Hesabınızı oluşturduktan sonra, Google Cloud Console üzerinden bir proje oluşturmalısınız. Bunun için:

    Sağ üst köşede yer alan proje seçme menüsünden New Project seçeneğine tıklayın.
    Proje adını belirleyin ve projenizi oluşturun.

3. Maps JavaScript API'sini Etkinleştirme

Projeyi oluşturduktan sonra, Google Maps API entegrasyonu için gerekli olan Maps JavaScript API'yi etkinleştirmeniz gerekiyor. Adımlar şu şekilde:

    Sol taraftaki menüden APIs & Services bölümüne gidin.
    API Library sekmesine geçin.
    "Maps JavaScript API" araması yapın ve ilgili API'ye tıklayın.
    Açılan sayfada Enable butonuna basarak API'yi etkinleştirin.

4. API Anahtarını Alma

API'yi etkinleştirdikten sonra, proje içerisinde kullanacağımız API anahtarını oluşturmanız gerekmektedir. Bunun için:

    APIs & Services bölümünden Credentials sekmesine tıklayın.
    Create Credentials butonuna tıklayın ve API Key seçeneğini seçin.
    Oluşturulan API anahtarını kaydedin, bu anahtarı projemizde kullanacağız.

5. API Anahtarını Kullanma

Google Maps API anahtarını aldıktan sonra, web sitenize ekleyeceğiniz iframe koduna bu anahtarı ekleyebilirsiniz. Adresi dinamik olarak göstermek için kullanmanız gereken kod şu şekildedir:

<iframe 
    src="https://www.google.com/maps/embed/v1/place?key=[API_KEY]&q=[ADRES]" 
    width="100%" 
    height="450" 
    style="border:0;" 
    allowfullscreen="" 
    loading="lazy">
</iframe>

    [API_KEY] kısmına aldığınız API anahtarını,
    [ADRES] kısmına ise göstermek istediğiniz adresi yazmanız yeterlidir.

Başarıyla tamamlanan bu adımlar sonucunda, Google Maps iframe’i sitenizde dinamik olarak kullanılabilir hale gelecektir. İyi çalışmalar
