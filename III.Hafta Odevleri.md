# .NET

.NET, .NET Framework, 2000 yılında Microsoft tarafından geliştirilmeye başlanmış olup ileriki yıllarda .NET Foundation topluluğuna devredilmiş yazılım geliştirme platformudur. İçerisinde bulundurduğu kütüphane ve templateler sayesinde günümüzde en güncel sürümü olan .NET 5 ile birlikte bilgisayar, web, cep telefonu, oyun ve yapay zeka gibi çeşitli alanlarda kullanılabilen bir paltforma dönüşmüştür. .Net platformu programlama dillerinden bağımsız olarak çalışır ve farklı programlama dilleri kullanılarak yazılım geliştirilmesine imkan verir. 

# .NET Derleme Süreci

Örneğin C# ile yazdığınız bir kod derleyici ile ortak dil altyapısına (Common Language Infrastructure-CLI) uyarlanır. Buradan sonra ortak ara dil derleyicisi (Common Intermediate Language-CIL) kodu platforma uygun dile dönüştürmek üzere ortak dil çalışma zamanı derleyicisine (Common Language Runtime-CLR) gönderir. CLR’ in işlevi CIL tarafından gönderilen kodu makine diline dönüştürmektir. Böylece C# (yada diğer platform dilleri ile) yazılan kod derlenmiş ve çalıştırılabilir hale getirilmiş olur.

[Kaynak I](https://dotnet.microsoft.com/)

[Kaynak II](https://www.teknologweb.com/microsoft-net-nedir)

[Kaynak III](https://www.youtube.com/watch?v=MNywsguVPsc&ab_channel=SinanHoca)

--------------------------------------------------------------------------------------

# Roslyn Compiler

Roslyn, .NET Derleyici platformu olup C# ve Visual Basic, .NET dilleri gibi bir çok dil için açık kaynaklı derleyici ve kod analizi API'sidir. Proje özellikle C # ve [VB.NET](http://vb.net/) derleyicilerinin kendi kendini barındıran sürümlerini içerir.

[Kaynak](https://github.com/dotnet/roslyn)

----------------------------------------------------------------------------------------

# Restful servisler nasıl çalışır? Alternatifleri nelerdir ve nasıl çalışırlar?

REST, HTTP protokolü kullanan client ile server arasındaki iletişimi sağlayan mimari sistemdir. Servislerle iletişim halinde kalacak servis yönelimli sistemler için kullanılan transfer yöntemidir. XML ve JSON verilerini taşıyarak uygulamanın iletişimini sağlamaktadır. REST mimarisi kullanılan servislere de Restful servisler denir. Esnek bir yapıdadır.

Restful ervisleirn günümüzde farklı alternatifleride mevcuttur. 

## OData

Gönderilen sorgu istekleri sunucu tarafından işlenerek sonuçlar üretilmekte ve cliente gönderilmektedir. Ayrıca talep edilen metada verileri ile OData'nın kullandığı veriler istemciye gönderilmektedir.

## SOAP

Veri formatı olarak XML kullanıldığı için veri boyutu oldukça yüksektir. Belirli kurallara göre yazılma zorunda olup XML Root elemanı bulundurulur. Bu dosya içerisinde Hader, Body, Fault  alanları mevcuttur.

## GraphQL

Graph database ile ilgisi olmayıp *Facebook* tarafından geliştirilmektedir. GraphQL, İstemci tarafından istenile verilerin belirtilmesini sağladığı gibi ilgili verinin birden fazla kaynağa ulaşmasını kolaylaştırır.

-------------------------------------------------------------------------------------

# Extension Method

C# 3.0 ile birlikte sunulan *Extension Method,* struct veya class yapılarının modify edilmeden bu struct veya class yapılarına extension metodlar eklenmesini sağlamaktadır. Genişletilebilir metod olarak tanımlanan bu metod sayesinde günümüzde birçok yapılan işin kolaylaştığı söylenebilir.

## Yazım Kuralları

Static bir class içerisinde static olarak tanımlanmalıdır. Metod içerisinde tanımlı parametrelerden 1 tanesi *this keyword*'ün tanımlı olması gereklidir. Extenden uygulanacak class'ın ilk parametri önüne *this keyword*'ü tanımlanmalıdır.

------------------------------------------------------------------------------------

# MVC Alternatifleri

- HMVC (Hierarchical Model-View-Controller)
- MVVM (Model-View-ViewModel)
- MVA (Model View Adapter)
- RMR (Resource-Method-Representation)
- ADR (Action-Domain-Responder)
- MVP (Model View Presenter)
- PAC (Presentation Abstraction Control)

------------------------------------------------------------------------------------

# Architectural Pattern

Yazılım alanında mimari alanlarda sorunlara çözümler öneren yazılım desenlerine mimari desenler denir. Mimari desenler, yazılım sistemlerinde alt bölümlerde ilişkiler ve sorumluluklarda temel ve yapısal organizasyon şemalarını ortaya koymaktadır.

------------------------------------------------------------------------------------

# ViewData, ViewBag ve TempData Farkları Nelerdir ?

ViewData ile ViewBag aynı çalışma mantığına sahip olduğu gibi ViewData dictionary of objectdir. Bu nedenle elemanlara *key* ile ulaşılabilir. Ancak ViewBag dinamik bir yapıya sahiptir.

TempData ise veriyi geçici olarak tutar ve TempData bize controller ile actioanlar arasıda köprü görevi görür. Ancak bu köprü görevini HTTP istek süres kadar tutar. Yapılan bu isteğe **TempData.Keep()** methodu kullanılarak geri çağrılabilir.
