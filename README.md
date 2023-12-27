# Selenium-IDE-Commands

**Selenium IDE**
Selenium, test otomasyonunu kolaylaştıran en popüler açık kaynaklı araçlardan biridir. Selenium IDE'de test komut dosyaları Java, C#, Python gibi çeşitli programlama dillerinde oluşturulabilir. Selenium yalnızca web uygulamalarının test edilmesine izin verir. Selenium bir araç paketidir ve her araç farklı test ihtiyaçlarına hizmet eder.

Selenese komutları, Selenium IDE'de test senaryoları oluşturan komutlar olarak adlandırılır. Selenese, çeşitli web işlemlerini gerçekleştirmek için Selenium IDE'de kullanılan komutların setleridir. Bu, Selenium IDE'de kodlama betikleri geliştirmek için kullanılır. Eleman konumlandırıcı, bir komutun hangi HTML öğesine işaret edeceğini Selenium'un belirlemesine yardımcı olur. Bu konumlandırıcılar, Mozilla'nın FirePath ve FireBug eklentileri kullanılarak tespit edilebilir.

Selenese kullanarak web tarayıcılarında birden fazla işlem gerçekleştirebilirsiniz:

1. Web sayfalarının değerlendirilmesi.
2. Bozuk bağlantıların kontrol edilmesi.
3. Giriş alanlarının test edilmesi.
4. Belirli içeriğin kontrol edilmesi.
5. Formların ve tablo verilerinin gönderilmesi.
6. Pencere boyutunun ve fare seçeneklerinin test edilmesi.
7. Uyarıların değerlendirilmesi.

Selenium komutları (Selenese) üç kategori altında sınıflandırılır: Eylemler, Erişimciler ve Uyarılar.

**Eylemler**, bir uygulamanın durumunu kontrol eden Selenium IDE komutlarıdır. Eylem komutları, şu gibi birden çok olayı içerir:

 - open (URL)
 - get(URL)
 - find_element(by, value)
 - click ()
 - clickAt (****locator****, coord)
 - doubleClick ()
 - focus ()
 - mouseDown()
 - refresh()
 - pause(time)
 - close()
 - echo(statement)
vb.

**Erişimciler**, uygulamanın durumunu kontrol etmek ve sonucu bir değişkende saklamak için kullanılan Selenium komutlarıdır. Erişimci komutları genellikle doğrulamaları otomatik olarak oluşturmak için kullanılır.

Bu bağlantıya tıkla. 
Seçenek belirle ve seç. 
Bu kutuya tıkla.

 - storeConfirmation (variable_Name)
 - storeTitle (variableName)
 - storeText (locator, variable_Name)
 - storeAllFields (variable_Name)
 - storeVisible (locator, variable_Name) vb.

**Doğrulamalar**, testçilerin bir uygulamanın durumunu kontrol etmelerine/doğrulamalarına olanak tanıyan Selenium komutlarıdır. Farklı türde doğrulamalar şunlardır:

 - assert: Eğer assert doğrulaması başarısız olursa, test otomatik
   olarak sonlandırılacaktır.

 - verify: Verify başarısız olduğunda yürütme durmaz, ancak bir
   başarısızlık kaydı döndürür.

 - waitfor: Koşul doğru olana kadar bekler ve durur.

Selenium IDE'de yaygın olarak kullanılan bazı komutlar:

**open**: Belirtilen bir URL'ye gider.

    open | https://www.example.com


**click**:Belirtilen bir öğeye tıklar.

    click | id=elementID
    
**type**: Belirtilen bir metin alanına metin yazar.
 
     type | id=elementID | SampleText

**sendKeys**: Klavye girişini simüle eder.

      sendKeys | id=elementID | ${KEY_ENTER}
      
**assert**:   Bir koşulun doğru olup olmadığını doğrular. Örneğin:
  
      assert | text | ExpectedText
      
**verify**: assert'e benzer, ancak doğrulama başarısız olursa yürütmeyi durdurmaz.
   
    verify | elementPresent | id=elementID
    
 **waitFor**:     Belirtilen bir koşul karşılanana kadar yürütmeyi duraklatır.
 
    waitFor | elementPresent | id=elementID
    
**store**:     Bir değeri daha sonra kullanmak üzere bir değişkende saklar.
    
    store | text | id=elementID | variableName
 
 **echo**: Log' a bir mesaj yazdırır.
  
    echo | This is a sample message
  

**executeScript** :JavaScript kodunu yürütür.

     executeScript | alert('Hello, World!'); | 



  Bu komutlar, bir web sayfasındaki öğeleri tanımlamak için konumlandırıcılarla birlikte kullanılabilir. Konum belirleyiciler, web sayfasındaki belirli öğelerle etkileşim kurmak için ID, ad, XPath, CSS seçicileri vb. gibi çeşitli özniteliklere dayalı olabilir. Komutlar ve parametreleri, belirli bir test senaryosu için gereken eylemlere ve doğrulamalara bağlı olarak değişebilir.
