# UAS_Ratu-SukmaKomala_1214007_d4TI1A
 Source Code greenfoot 
 
public void act()
    {
        // Add your action code here.
        keycontrol();
    }
    public void keycontrol()
    {
        if(Greenfoot.isKeyDown("d"))
        {
            move(5);
        }
        
        if(Greenfoot.isKeyDown("a"))
        {
            move(-5);
        }
        
        if(Greenfoot.isKeyDown("s"))
        {
            setLocation(getX(),getY()+5);
        }
        
        if(Greenfoot.isKeyDown("w"))
        {
            setLocation(getX(),getY()-5);
        }
        
    }



Penjelasan

Source code di bawah ini merupakan sebuah class baru untuk menjalankan dari project yang dibuat.

public void act()
    {
        // Add your action code here.
        keycontrol();
    }


Source code dibawah ini merupakan kode dimana tujuannya untuk menjalankan dan mengarahkan pada object yang kita buat. Yaitu dengan cara menggunakan keyboard pada laptop. Caranya seperti dibawah ini:
Klik button (d) object akan bergerak ke arah kanan 
Klik button (a)  object akan bergerak ke arah kiri
Klik button (w) object akan bergerak ke arah atas
Klik button (s) object akan bergerak ke arah bawah

public void keycontrol()
    {
        if(Greenfoot.isKeyDown("d"))
        {
            move(5);
        }
        
        if(Greenfoot.isKeyDown("a"))
        {
            move(-5);
        }
        
        if(Greenfoot.isKeyDown("s"))
        {
            setLocation(getX(),getY()+5);
        }
        
        if(Greenfoot.isKeyDown("w"))
        {
            setLocation(getX(),getY()-5);
        }
        
    }

Setelah membuat game pada aplikasi greenfoot langkah selanjutnya yaitu membuat database pada phpmyadmin (menyalakan xampp). Database ini di beri nama greenfootuas, setelah itu kita membuat dua table bernama arah yang berisikan id dan kunci, ,serta mengisikan type untuk id itu INT sedangkan untuk kunci yaitu VARCHAR. Kunci tersbut bisa di isikan dengan huruf huruf seperti d,a,w,s,gg. Database ini bertujuan untuk menjalankan object yang telah dibuat.

Berikut source code database 


public class koneksi_Dbkoneksi{      
    private static Connection koneksi;
    public static Connection getKoneksi(){
        if(koneksi == null){
            try{
                String url="mysql://localhost:3306/greenfootuas";
                String user="root";
                String password="";
                DriverManager.registerDriver(
                new com.mysql.jdbc.Driver());
                koneksi = DriverManager.getConnection(url,user,password);
                }catch (SQLException t){
                    System.out.println("ERROR MEMBUAT KONEKSI");
            }
        }
        return koneksi;
    }



