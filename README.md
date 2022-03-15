

import java.util.Scanner;
import java.util.LinkedList;
import java.util.Queue;
public class tugasqueue  {

    public static void main(String[] args) {

        int menu,id;
        String nama,barang;
        Scanner input=new Scanner(System.in);
        Scanner in = new Scanner(System.in);
        Scanner str = new Scanner(System.in);
        //deklarasi queue
        Queue<Integer> nomor= new LinkedList<>();
        Queue<String> name= new LinkedList<>();
        Queue<String> perlu= new LinkedList<>();

System.out.println("Selamat datang di Mini Market");
                
        do{
            System.out.println("\n\n");
            System.out.println("\t\t\t\t==============================");
            System.out.println("\t\t\t\t\t  PILIH MENU  ");
            System.out.println("\t\t\t\t==============================");
            System.out.println("\t\t\t\t1. Masuk antrian");
            System.out.println("\t\t\t\t2. Antrian Dipanggil");
            System.out.println("\t\t\t\t3. Lihat data antrian");
            System.out.println("\t\t\t\t4. Keluar");
            System.out.println("\t\t\t\t==============================");
            System.out.print("\t\t\t\t     Pilihan Anda : ");
            menu=input.nextInt();
            System.out.println("\n");
            if(menu==1){
                System.out.println("\t\t\t\t==============================");
                System.out.print("\t\t\t\tMasukan Nomor        : ");
                id = in.nextInt();
                nomor.add(id);
                System.out.print("\t\t\t\tMasukan nama      : ");
                nama = str.nextLine();
                name.add(nama);
                System.out.print("\t\t\t\tMasukan barang : ");
                barang = str.nextLine();
                perlu.add(barang);

            }else if(menu==2){
                if(nomor.isEmpty()){
                    System.out.println("\t\t\t\tCEK KEMBALI PELANGGAN ANDA!!");
                }else{
                System.out.println("\t\t\t\tNOTICE!!");
                System.out.println("\t\t\t\tPemanggilan atas nama : "+name.poll());
                nomor.remove();
                perlu.remove();
                }
            }else if(menu==3){
                if(nomor.isEmpty()){
                    System.out.println("\t\t\t\tTIDAK ADA PELANGGAN!!");
                }else{
                    
                    System.out.println("\t\t\t\t==============================");
                    System.out.println("\t\t\t\t         DATA PELANGGAN");
                    System.out.println("\t\t\t\t==============================");
                    System.out.println("\t\t\t\t|| NOMOR         : "+nomor);
                    System.out.println("\t\t\t\t|| NAMA       : "+name);
                    System.out.println("\t\t\t\t|| Barang  : "+perlu);
                    System.out.println("\t\t\t\t==============================");
                    System.out.println("\t\t\t\t|| PELANGGAN PERTAMA  : "+name.peek());
                    System.out.println("\t\t\t\t|| TOTAL PELANGGAN    : "+name.size());
                }
            }else if(menu==4){
                System.out.println("\n\t\t\t\t**** Terima Kasih ****");
            }else{
                System.out.println("\n\t\t\t\tTidak tersedia!!");
            }
        }while(menu!=4);
    }
}
