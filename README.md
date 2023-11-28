# State Yönetimi
State: Uygulamdaki bileşenlerimizin sahip olduğu bilgi ve özelliklerdir.

# Prop Drilling: 
Bileşenlerin yukarıdan aşağıya veri taşıması.

# Context API: 
Uygulamadaki state'i oluştuduğumuz birden fazla merkezden yönettiğimiz state yönetim aracı.

# Redux: 
Bileşenlerin sahip olduğu ve merkezi olarak tutulması gereken state'leri yöneten "merkezi state yönetim aracı"

# Neden Redux ?
Kod tekrarını önler
Performansı arttırır
Bileşen içerisindeki karmaşıklığı azaltır
Hata ayıklama daha kolaydır.
Orta ve büyük ölçekli uygulamalarda state yönetimini kolaylaştırır
# Eksi Yanı
Küçük ölçekli uygulamalarda state yönetimini için biraz aşırı bir çözüm olur muadillerine göre daha fazla kod kalabalığına neden olur.
# Redux ile ilgili bilinmesi gerekenler
- - Store: Uygulamanın bütün bileşenleri tarafından erişilebilen ve yönetilebilen state deposu.

- - Reducer: Aksiyondan aldığı talimata göre store da tuttuğumuz state'in nasıl değişeceğine karar veren yapı.

- - Action: Store'u güncellemek için reducer'a gönderdiğimiz emir/haber

* * Action iki değere sahip bir objedir.
+ type (zorunlu): Action ın görevini tanımlayan string: ("TODO_EKLE")
+ payload (duruma göre): Gönderilen eylemin verisi: {id:1,title:"merhaba"}

- - Dispatch: Action'un gerçekleştiğini reducer'a haber veren method

- - Subscribe: Bileşenlerin store'da tutulan verilere erişimini sağlama (useContext | useSelector)

- - Provider: Store'da tutulan verileri uygulamaya sağlar.

# Redux Kullanmak İçin Aşamalar:
redux, react-redux paketlerini indir √ (npm redux react-redux)
reducer / reducer'ların kurulumunu yap √ 
store'un kurulumunu yap √
store'u projeye tanıt √
# Altın Kural
Verilerin api'dan geldiği ve state'yönetimi redux'In kullanıldığı projelerde
store'u güncelleme işlemini api isteğine bağıımlı hale getirmeliyiz
ancak istek başarılı olursa değişim gerçekleşmeli
Olası Hatalar
"Değişiklik yapıyorum ama sayfayı yenilemeden gelmiyor???"

API'da > sıkıntı yok
Store'da > hata var
"Değişiklik yapıyorum sayfayı yeneleyince gidiyor!"
API'da > hata var
Store'da > sıkıntı yok

# cruidredux
