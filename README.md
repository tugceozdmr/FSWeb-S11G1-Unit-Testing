# Birim Testleri (Unit Testing) React Modül Projesi: Stranger Things

Bu sprint'de bugün unit testingi incelediniz. Bu projede, öğrendiklerimizi pekiştireceğiz.

## Giriş

Bir yazılımcı olarak, sık sık oluşturduğunuz özellik ve hatta diğer geliştiricilerin oluşturduğu özellikler için testler yazmanız istenecektir. Bu projede, sizden başka birinin yazdığı kodu test etmenizin istendiği bir durumu ele alacağız.

Projeyi çalıştırın ve inceleyin. Kullanıcı bakış açısıyla projeyi inceleyin ve özellikleri kullanmaya çalışın. Projeyi iyice anladıktan sonra uygulamanızda neleri test edeceğiniz konusunda bir fikriniz olacaktır.

![Stranger Örnek](örnek_proje.gif)

**_Görevlerinizi tek tek tamamladığınızdan ve ilerlemeden önce her bir görevi test ettiğinizden emin olun._**


## Talimatlar

### Görev 1: Proje Kurulumu

* [ ] Forklayın.
* [ ] Klonlayın
* [ ] Ana dizine gidin
* [ ] `npm install`
* [ ] `npm start`


### Görev 2: Proje Gereksinimleri

Testleri "./src/components/tests/" klasörü içindeki dosyalara yazacaksınız. 

#### Episode Bileşeni

> _Bu bileşen, tek bir bölüm değerinde veri görüntüler. Bunu test etmek için, bileşene proplarla farklı değişkenler atamalıyız._

- [ ] Episode bileşeni renderlarını gösteren bir test yazın, test prop olarak size sağlanan episode datasını bileşene gönderin
- [ ] Spesifik bir değişken göstermek için test datasını modifiye edin. Episode bileşenine gönderdiğiniz spesifik değişkenin, bileşende beklendiği gibi görüntülendiğini test edin. **Spesifik değeri test etmek için en az 3 adet farklı tipte girdi gönderip, beklenen değeri karşılaştırın.**
- [ ] Episode bileşenine bir image url gönderilmediğinde bir default değer gösterir ('https://i.ibb.co/2FsfXqM/stranger-things.png'). image özelliği "null" olarak ayarlanmış yeni bir test verisi parçası oluşturun. Görüntülenen imagein `alt` etiketinin './stranger_things.png' olarak ayarlanıp ayarlanmadığını test edin.

### Show bileşeni

> _Bu bileşen, öne çıkan şovumuzla ilgili tüm genel bilgileri içerir. Burada bir kez daha data props ile çalışacağız, test için bir fonksiyon ile manipüle edeceğiz ve datadaki değişim için bileşenimizi yeniden render edeceğiz._

- [ ] Show verilerini doğru biçimde içeren örnek bir veri yapısı oluşturun. Her show, bir isim(name), özet(summary) ve sezonları(seasons) içeren bir dizi(array) ve herbirinin içinde bir id, isim ve (boş) bölüm listesi dizisi(array) içermelidir. Console.log kullanarak show datasının içeriğini inceleyebilirsiniz..
- [ ] Test datanızı show propuna ve selectedSeason propuna "none" gönderip Show bileşenini test edin.
- [ ] show propuna null gönderildiğinde Loading bileşeninin görüntülendiğini test edin. (Loading bileşenini test etmek için önce içeriğini inceleyin.)
- [ ] show propuna test datasını gönderdiğinizde, select optionlarında test datanızın içindeki sezonlarla aynı sezon listesinin bulunup bulunmadığını test edin.
- [ ] Bir item seçildiğinde, handleSelect fonksiyonunun çağırıldığını test edin. Select DOM elementine nasıl ulaşabileceğinize ve seçmeyi nasıl tetikleyeceğinize şu sayfadan bakabilirsiniz: [userEvent](https://testing-library.com/docs/ecosystem-user-event/).
- [ ] selectedSeason propu "none" ken episode bileşeninin render edilmediği,ve selectedSeason propunun geçerli bir sezon girildiğinde render edildiğini test edin.

### Display Bileşeni

> _Bu bileşen, uygulamanın state değerlerini tutar ve api çağrılarını işler. Bu bileşenin testlerinde, harici modülleri mocklayarak  async / wait / waitFor ile çalışıyorsunuz._

- [ ] Herhangi bir prop gönderilmeden Display bileşenini test edin.
- [ ] Önceki testlerde kullandığınız show test datasını kopyalayın ya da yeniden oluşturun.
- [ ] "Press get the show data" butonuna tıklandığında, show bileşeninin görüntülendiğini test edin. Testinizi oluştururken api çağrısını ve state değişikliğini hesaba kattığınızdan emin olun.
- [ ] "Press get the show data" butonuna tıklandığında, select optionlarda render edilen sezon sayınızın test datanızdakiyle aynı olduğunu test edin.
- [ ] Display bileşenine gönderdiğiniz opsiyonel fonksiyonel propa dikkat ediniz. Butona basıldığında bu fonksiyonun çağırıldığını test ediniz.

### Esnek görevler

- Episodes bileşeni için bir test paketi ekleyin.

- `TVMaze` APIsine göz atın. Diğer popüler showların başlıklarını içeren bir dropdown ekleyin. Kullanıcı tarafında, başka showlara tıklandığında o showun verisini gösteren özellik ekleyin.

- Episodeye tıklandığında episode sayfasına yönlendiren React Router ekleyin
