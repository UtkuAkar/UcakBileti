# UcakBileti

import java.util.Scanner;

public class UcakBileti {
    public static void main(String[] args) {

        double sonuc,sonuc1,sonuc2,sonuc3,sonuc4,sonuc5,sonuc6;
        double gd1,gd2,gd3,gdt1,gdt2,gdt3;;

        double mesafe,indirim1,indirim2,indirim3,indirim4,indirim5,indirim6;
        int yas, yolculuktipi;

        Scanner input = new Scanner(System.in);

        System.out.println("Mesafenizi Girin : ");
        mesafe = input.nextDouble();

        System.out.println("Yaşınızı Giriniz : ");
        yas = input.nextInt();

        System.out.println("Tek bilet almak için : 1'e Basınız\nGidiş-Dönüş almak için : 2'ye Basınız");
        yolculuktipi = input.nextInt();

        sonuc = mesafe * 0.10;

        if (mesafe > 0 && yas > 0) {
            if (yolculuktipi == 1 || yolculuktipi == 2) {
                switch (yolculuktipi) {
                    case 1:
                        if (yas < 12) {
                            indirim1=sonuc*0.50;
                            sonuc1=sonuc-indirim1;
                            System.out.println("Odeyeceniz Miktar  =" + sonuc1);
                        }else if (yas>=12 && yas<=24) {
                            indirim2=sonuc*0.10;
                            sonuc2=sonuc-indirim2;
                            System.out.println("Odeyeceniz Miktar =" + sonuc2);
                        }else if (yas>65) {
                            indirim3=sonuc*0.30;
                            sonuc3=sonuc-indirim3;
                            System.out.println("Odeyeceniz Miktar =" + sonuc3);
                        }else if(yas>24 && yas <65){
                            System.out.println("Odeyeceniz Miktar =" + sonuc);
                        }
                        break;

                    case 2:
                        if (yas < 12) {
                            indirim4=sonuc*0.50;
                            sonuc4=sonuc-indirim4;
                            gd1=sonuc4*0.20;
                            gdt1=(sonuc4-gd1)*2;
                            System.out.println("Odeyeceniz Miktar  =" + gdt1);
                        }else if (yas>=12 && yas<=24) {

                            indirim5=sonuc*0.10;
                            sonuc5=sonuc-indirim5;
                            gd2=sonuc5*0.20;
                            gdt2=(sonuc5-gd2)*2;

                            System.out.println("Odeyeceniz Miktar  =" + gdt2);
                        }else if (yas>65) {
                            indirim6=(sonuc*0.30);
                            sonuc6=sonuc-indirim6;
                            gd3=sonuc6*0.20;
                            gdt3=(sonuc6-gd3)*2;
                            System.out.println("Odeyeceniz Miktar =" + gdt3);
                        }
                        break;
                    default:
                        System.out.println("Hatalı İşlem");

                }


                }
            } else {
                System.out.println("Yanlış Değer Giridiniz");
            }


        }


}
