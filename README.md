# Praktikum4

![Screenshot 2024-10-30 080850](https://github.com/user-attachments/assets/307b18df-0738-4d52-a427-30453c3db94f)

## class BangunDatar

```

package bangundatar;

abstract class BangunDatar {
    abstract float luas();
    abstract float keliling();
       
    }

```
<p>* Pada abstrak class bangun datar memiliki dua metode abstrak, yaitu luas dan keliling. konsep abstrak digunakan pada class bangun datar 
karena merupakan sebuah konsep abstrak dalam geometri yang mewakili bentuk-bentuk dua dimensi yang memiliki luas seperti lingkaran, segitiga, dan persegi.</p>

## class Lingkaran

```

package bangundatar;


public class Lingkaran extends BangunDatar {
   private int r;
    
   public  Lingkaran(int r){
        this.r = r;
    }

    @Override
    float luas() {
       return (float) (Math.PI *r*r);
    }

    @Override
    float keliling() {
        return (float) (2*Math.PI*r);
    }
    
}
```
## class segitiga

```

package bangundatar;

public class Segitiga extends BangunDatar{
    private int alas, tinggi;
    
    public Segitiga(int alas, int tinggi){
        this.alas = alas;
        this.tinggi = tinggi;
        
    }

    @Override
    public float luas() {
       return (float) (0.5*alas*tinggi);
    }

    @Override
    public float keliling() {
        //keliling segitiga membutuhkan panjang sisi-sisinya
        // asumsikan ini adalah segitiga siku-siku
        float sisiMiring = (float) Math.sqrt(alas*alas*tinggi*tinggi);
        return (float)(alas+tinggi+sisiMiring);
        
    }
    
    
}
```
## class persegi

```

package bangundatar;

public class Persegi extends BangunDatar {
    private int sisi;
    
    public Persegi(int sisi){
        this.sisi = sisi;
    }

    @Override
   public float luas() {
       return(float)(sisi*sisi);
        
    }

    @Override
    public float keliling() {
        return(float)(4*sisi);
    }
    
}
```
<p>* class lingkaran, segitiga, dan persegi merupakan class turunan dari bangun datar yang mengimplementasikan metode luas dan keliling sesuai rumusnya masing-masing</p>
<p>* Lingkaran yang memiliki atribut jari-jari, segitiga memiliki atribut alas dan tinggi, dan persegi memiliki atribut sisi. </p>

## class main

```

package bangundatar;

public class Utama {
    public static void main(String[] args){
        // membuat object
        Lingkaran lingkaran = new Lingkaran(7);
        Segitiga segitiga = new Segitiga(5,3);
        Persegi persegi = new Persegi(8);
        
        // memanggil method
        System.out.println ("Lingkaran:");
        System.out.println("Luas lingkaran: " + lingkaran.luas());
        System.out.println("Keliling lingkaran: " + lingkaran.keliling());
        
        System.out.println("Segitiga:");
        System.out.println("Luas segitiga: " + segitiga.luas());
        System.out.println("Keliling segitiga: " + segitiga.keliling());
 // Perlu diubah jika diketahui sisi lainnya
 
        System.out.println("Persegi:");
        System.out.println("Luas persegi: " + persegi.luas());
        System.out.println("Keliling persegi: " + persegi.keliling());
 
 
    }
    
}
```
<p>* class main untuk membuat objek dari masing-masing class lalu memanggil metode luas dan keliling untuk menghitung dan menampilkan hasilnya.</p>

## Output


![output](https://github.com/user-attachments/assets/0c7b2370-4894-425d-9e1d-47d4957d9169)



