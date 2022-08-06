# Some-Information-About-Java-
java keys

JDK Nedir?
JDK, Java uygulamaları geliştirmek için gerekli tüm araçları bize sağlar. İçerisinde JVM, JRE, Java kütüphaneleri, Java Compiler ve Interpreter içerir. Bir java uygulaması geliştirmek için JDK yüklememiz yeterlidir çünkü diğer araçları JDK içerisinde barındırır.

JVM Nedir?
Yani JVM sistemin üzerinde çalışarak Java kodlarının her sistemde çalışabilmesini sağlar. Bunu yapabilmesi için her sisteme özel bir JVM olması gerekir. Sistemin Java kodu ile uygun bir şekilde çalışabilmesi için gerekli düzenlemeleri JVM yapar. Bizim yapmamız gereken tek şey Java kodunun çalışacağı makineye uygun JVM'yi yüklemek ve kodumuzu derlemektir.

![image](https://user-images.githubusercontent.com/93288833/183244262-522057fe-dbba-4460-a3f3-ca3df30d7ace.png)

Garbage Collection Nedir?
Başlangıçta varsayılan olarak var olan erişilebilir değerler bulunmaktadır bunlar hiçbir zaman silinemez.

Örneğin:

O anda içinde bulunulan fonksiyonların yerel değişkenleri.
Birbirini çağıran fonksiyonların arasında gönderdikleri parametreler, değişkenler.
Global değişkenler.
(dahili değişkenler.)
Bu değerlere kökler veya roots denir.

Eğer kökten herhangi bir değişkene erişilebiliyorsa, bu zincirleme referanslarla veya referanslarla olabilir, bu durumda o değişken erişilebilirdir.

Örneğin, yerel bir obje özellikleri içinde başka bir obje kullanırsa, o kullandığı obje de erişilibilir olmaktadır. Eğer referans verilen obje de başka bir objeye referans verirse o da erişilebilir olur. Detaylı bir örneği aşağıdaki gibidir.

JavaScript arka planda Çöp Toplama işlemini çalıştırır. Bu tüm erişelemeyen objeleri silme işini yapar.

.jar nedir?
JAR, Java arşivi anlamına gelir. Adından da anlaşılacağı gibi, bir arşiv dosyası - bu, taşınabilirlik ve depolama alanını azaltmak gibi nedenlerle bir arada paketlenmiş, diğer dosyaları içeren tek bir dosya olduğu anlamına gelir.

Abstract Class

Abstract Class, yani soyut sınıflardır. Soyut Sınıfların ortak özelliklerini kullanabilmekteyiz. Soyut Sınıflar kendisinden türeyen sınıflardır.  Soyut sınıflardan nesne oluşturulamaz. Bunun yerine extends edilerek yeni sınıflara o özelliği kullanılarak soyut metodlar üretilir.

Soyut metotlar alt sınıflar için extends edildiği sınfın özelliklerini kullanarak farklı sonuçlar üretir.Her  alt sınıfa da  override edilmek zorundadır. Başka nesnelerden bağımsız ve habersiz bir şekilde çalışır. Yazılımlarımızda bir işin belirli özelliklerini tekrar tekrar kullanma durumunda kaldığımız zamanlarda aynı işin farklı metodlarını çağırarak işlem yapmamıza olanak sağlamaktadır.

Abstract Class Kullanım Şekli

public abstract class SINIF_ADI //sınıf tanımlaması
{
         public abstract METOD(); //soyut method tanımlaması
         
}
 public class SINIF_ADI extends TURETILEN_SINIF //alt sınıf tanımlaması
{
   
}

Örnek;

public abstract class Ogrenci_Sinifi {

    private String ad;
    private String soyad;
    private int numara;

    public abstract String getAd();

    public abstract String getSoyad();

    public int getNumara() {
        return this.numara;
    }

    public class Ogrenci extends Ogrenci_Sinifi {

        public String getAd() {
            return "Burak";
        }

        public String getSoyad() {
            return "Kutbay";
        }

        public int getNumara() {
            System.out.println(super.getNumara());
            return super.getNumara();
        }
    }
}

