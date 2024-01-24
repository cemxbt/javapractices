# javapractices
10 Java questions &amp; solutions with screen recording
youtube link:
https://youtu.be/S7ljYzOm-6k

Java sorularını internette çeşitli kaynaklardan buldum ve IDE üzerinde çözmeye çalıştım. Bazılarında zorlandım ve bazı yerlerde hata aldım ancak hepsinin sonunda bir çözüme ulaştım. Aşağıya soruları ve çözümlerini bırakıyorum.

//Soru 1
//String tipinde sabit bir şifre değişkeni oluşturun.
//Girilen şifre ile değişkende tutulan değeri (12345) kıyaslasın.
//Değerler eşleşirse "Giriş Başarılı", eşleşmezse "Giriş Başarısız" yazsın.

//Soru 2
//Kullanıcının konsol ekranından 4 temel matematiksel işlemi yapabildiği bir program yazın.
//Kullanıcıya 4 işlemden birini seçeceği menüyü konsola yazdırın.
//Kullanıcıdan 2 adet tamsayı tipinde sayı girmesini isteyin, bunları değişkenlerde saklayın.
//Seçilen işleme göre işlemi yapın ve konsola yazdırın.

//Soru 3 
//Rastgele sayılardan oluşmuş 100 elemanlık tamsayı dizisindeki tüm elemanların ortalamasını alacak program yazın.
//Rastgele oluşan 100 elemanlık sayı kümesi program her restart olduğunda değişsin. Sabit elemanlı dizi olmasın.
//Ortalama almayı sağlayacak kodu bir fonksiyon halinde tasarlayın. Diziyi input olarak içine alsın.
//Ortalama alan fonksiyon ortalamayı ondalıklı sayı olarak return etsin.

//Soru 4 
//Aşağıdaki görüntüyü konsol ekranına yazdıran algoritmayı tasarlayın.
// *
// **
// ***
// ****
// *****
// ******
// *******
// ********
// *********
// **********

//Soru 5 
//Fahrenheit cinsinden verilen sıcaklığı Kelvin'e çeviren programı yazınız.
//Aşağıdaki dönüşüm formülünü kullanabilirsiniz.
//Kelvin = (Fahrenheit - 32) / 1.8 + 273.15 

//Soru 6
//4K+1 şeklinde yazılabilen sayılara Hilbert sayısı denir.
//Örneğin birkaç Hilbert sayısı şunlardır: 5, 9, 13, 17...
//Bir sayının Hilbertt sayısı olup olmadığını belirleyen program yazınız.

//Soru 7 
//Bir füzenin km cinsinden menzili ve kg cinsinden ağırlığı mevcuttur.
//Bir füze ya kara ya da hava hedefleri için tasarlanır.
//Füzelerin bu özellikleri sonradan değiştirilemez.
//Füze sınıfının (Missile) kodunu yazınız.

//Soru 8
//Bir sayının iki tamsayının kareleri toplamı şeklinde yazılıp yazılamayacağını gösteren program yazınız.
//Örneğin kullanıcı 100 girerse output şöyle olmalıdır:
//100 sayısının kare toplamı açılımları:
//0*0 + 10*10
//6*6 + 8*8
//8*8 + 6*6
//10*10 + 6*6

//Soru 9
//Kullanıcının girdiği sayının tam bölenlerini listeleyen bir program yazınız.
//Örneğin kullanıcı 36 girerse output şöyle olmalıdır: 1 2 3 4 6 9 12 18

//Soru 10
//Girilen n adet sayının harmonik ortalamasını bulan program yazınız.
//Aşağıdaki dönüşüm formülünü kullanın.
//Harmonik = n / (sayı1 + sayı2 + ... + sayın)

//Cevap 1

import java.util.Scanner;

public class odev {
    
    public static void main(String[] args) {
    
    String pass = "12345";
    System.out.print("Bir sifre giriniz:");
    Scanner scanf = new Scanner(System.in);
    String userpass = scanf.nextLine();
    
    if(userpass.equals(pass)) {
        System.out.println("Giriş Başarılı!");
    }
    else {
        System.out.println("Giriş Başarısız!");
    }
}

    }
    
//Cevap 2

import java.util.Scanner;
public class odev {
    
    public static void main(String[] args) {
        
        int sayi1,sayi2,islemler;
        Scanner scanf = new Scanner(System.in);
        
        System.out.println("**********");
        System.out.println("1 - Toplama");
        System.out.println("2 - Cikarma");
        System.out.println("3 - Carpma");
        System.out.println("4 - Bölme");
        System.out.println("**********");
        
        System.out.print("Birinci sayiyi giriniz : ");
        sayi1 = scanf.nextInt();
        
        System.out.print("İkinci sayiyi giriniz : ");
        sayi2 = scanf.nextInt();
        
        System.out.print("Bir islem seciniz : ");
        islemler = scanf.nextInt();
        
        if(islemler == 1) {
            System.out.println("Toplama isleminin sonucu = " + (sayi1+sayi2));
        }
        else if(islemler == 2) {
            System.out.println("Cikarma isleminin sonucu = " + (sayi1-sayi2));
        }
        else if(islemler == 3) {
            System.out.println("Carpma isleminin sonucu = " + (sayi1*sayi2));
        }
        else if(islemler == 4) {
            System.out.println("Bolme isleminin sonucu = " + (sayi1/sayi2));
        }
        else {
            System.out.println("Tanimlanmamis islem");
        }
    }
}
//Cevap 3 

import java.util.Random;

public class odev {
    
    public static void main(String[] args) {
        int[] sayilar = new int[100];
        
        for(int i=0;i<100;i++) {
            Random rand = new Random();
            int sayi = rand.nextInt(1000);
            sayilar[i] = sayi;
        }
        
        double ort = ortalama(sayilar);
        System.out.println("ortalama : " + ort);
    }
    
     public static double ortalama(int[] dizi) {
         double toplam = 0;
         for(int i = 0; i<100; i++) {
             toplam+=dizi[i];
             
         }
         
         return toplam/100;
     }
    
}
//Cevap 4

public class odev {
    

public static void main(String[] args) {
    
    int uzunluk = 10;
    for(int satir = 0; satir<uzunluk; satir++) {
        System.out.print("");
        
        for(int sutun = 0; sutun<satir; sutun++) {
            System.out.print("*");
        
        }
        System.out.println("");
    }
}
}
//Cevap 5

import java.util.Scanner;

public class odev {
    
    public static void main(String[] args) {
        
        Scanner input = new Scanner(System.in);
        System.out.print("Fahrenheit cinsinden sıcaklık giriniz: ");
        double fahrenheit = input.nextDouble();
        double kelvin = (fahrenheit - 32) / 1.8 + 273.15;
        System.out.println("Sıcaklık Kelvin cinsinden: " + kelvin);
        input.close();
    }
}
//Cevap 6

import java.util.Scanner;

public class odev {
    
    public static void main(String[] args) {
        
        Scanner input = new Scanner(System.in);
        System.out.print("Bir sayi giriniz: ");
        int sayi = input.nextInt();
        if (sayi % 4 == 1) {
            System.out.println("Sayı Hilbert sayısıdır.");
        }
        else {
            System.out.println("Sayı Hilbert sayısı değildir.");
        }
        input.close();
    }
}
//Cevap 7

public class Missile {
    
    private final double range;
    private final double weight;
    private final boolean airTarget;
    
    public Missile(double range, double weight, boolean airTarget) {
        
        this.range = range;
        this.weight = weight;
        this.airTarget = airTarget;
    }
    
    public double getRange() {
        return range;
    }
    
    public double getWeight() {
        return weight;
    }
    
    public boolean isAirTarget() {
        return airTarget;
    }
    
    
}

//Cevap 8

import java.util.Scanner;

public class odev {
    
    public static void main(String[] args) {
        
        Scanner input = new Scanner(System.in);
        System.out.println("Bir sayı giriniz: ");
        int number = input.nextInt();
        System.out.println(number + " sayısının kare toplamı açılımları:");
        for (int i = 0; i <= Math.sqrt(number); i++) {
            
            int j = (int) Math.sqrt(number - i * i);
            if (i * i + j * j == number) {
                System.out.println(i + "" + i + "+" + j + "" + j);
            }
        }
        input.close();
    }
}

//Cevap 9

import java.util.Scanner;

public class odev {
    
    public static void main(String[] args) {
        
        Scanner input = new Scanner(System.in);
        System.out.println("Bir sayı giriniz:");
        int number = input.nextInt();
        System.out.println(number + " sayısının tam bölenleri:");
        for (int i = 1; i <= number / 2; i++) {
            
            if (number % i == 0) {
                
                System.out.print(i + " ");
            }
        }
        input.close();
    }
}

//Cevap 10

import java.util.Scanner;

public class odev {
    
    public static void main(String[] args) {
        
        Scanner input = new Scanner(System.in);
        System.out.println("Kaç adet sayı gireceksiniz?");
        int n = input.nextInt();
        double sum = 0;
        for (int i =1; i <= n; i++) {
            
            System.out.println(i + ". sayıyı giriniz:");
            int number = input.nextInt();
            sum += 1.0 / number;
        }
        double harmonic = n / sum;
        System.out.println("Girilen " + n + " sayının harmonik ortalaması:" + harmonic);
        input.close();
    }
}


