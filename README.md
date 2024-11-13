// 1- ATAMA OPERATÖRLERİ



/*ÖRNEKLER :    x += 2  x = x + 2 
                x -= 2  x = x - 2
                diyer örneklerde bunlar gibi */

#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    // int myNumber;
    //     myNumber = 7;
    //     myNumber += 12;
    //     printf("myNumber is : %d\n", myNumber);

    // return 0 ;

    // NOTLAR: 
    /* & opertaörü şöyle çalışır : 
        - 12 sayisini bilgisayar diliyle yazalım
        - 12 = 0 0 0 0 1 1 0 0   2nin kuvvetleri şeklinde yazılıp toplamı 12 etmesi lazım
        -  7 = 0 0 0 0 0 1 1 1  7 nin yazımıda bu 
        -  & de 1 ile 1 1 eder ona göre sonucu çıktı olarak karşımıza çıkar
        - xor = ^ da ise biri başarılı diyeri başarısız olduğu zaman sadece 1 değeri döner
        - << bunlar ise sola kaydırmak demektir yani (devamı alt satırda)
        - 7 = 0 0 0 0 0 1 1 1  7 <<= 2 demek bitleri 2 birim sola kaydır demek
        - sonuç : 7 = 0 0 0 1 1 1 0 0 bitler 2 birim kayar ve görüntü bu olur 
        - pekiştirme yap !!!*/

    /*SORU : KULLANICIDAN 4 BASAMAKLI BİR SAYI ALIP BU SAYININ RAKAMLARI 
    TOPLAMINI BULAN ALGORİTMA ?*/

    int myNumber , sum  , bolum , kalan;
        sum  = 0;
        printf("Enter a myNumber: ");
        scanf("%d", &myNumber);

    // 4. basamağı bul
    bolum  =myNumber / 1000;
    sum += bolum;
    kalan  = myNumber % 1000; 

    // 3. basamağı bul
    bolum  =kalan / 100;
    sum += bolum;
    kalan  = kalan % 100;

    // 2. basamağı bul
    bolum  =kalan / 10;
    sum += bolum;
    kalan  = kalan % 10; 

    // 1. basamağı bul
    bolum  =kalan / 1;
    sum += bolum;
    kalan  = kalan % 1000; 
    
    printf("girilen sayinin rakamlari toplami : %d\n", sum);

    return 0 ;




}

// 2- CHAR KULLANIMI


#include <stdio.h>
#include <stdlib.h>

int main()
{
    // char my_city[10] ='Van';
    // printf("My city is = %s\n", my_city);    //   %s ile olunca bütün karakterleri okuyor 
    // printf("My city is = %c\n", my_city);    //   %c ile olunca sadece baştaki karakterleri okuyor

    // return 0 ;

    char Mycity[16];
    printf("Enter a city: ");
    scanf("%s", &Mycity);            // boşluktan sonrakini okumaz
    printf("your city is : %s\n", Mycity);

    printf("\n...");

    return 0 ;
}

// 3- ÇOK BOYUTLU DİZİLER

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

// int main(void)
// {
//     int matrix[2][3] = {    // ilk [2] satırları ifade eder sonraki ise sütunları ifade eder
//                             {2,7,19},  
//                             {3,5,12}
//                        };
//     // printf("%d\n", matrix[0][0]);
//     // printf("%d\n", matrix[0][1]);
//     // printf("%d\n", matrix[0][2]);

//     // printf("%d\n", matrix[1][0]);
//     // printf("%d\n", matrix[1][1]);
//     // printf("%d\n", matrix[1][2]);

//     int i , j;

//     for(i=0;i<2;i++)        // dış for satırları ifade eder
//     {
//         for(j=0;j<3;j++)    // iç for sütunları ifade eder
//             printf("%d\n", matrix[i][j]);
//     }

//     return 0 ;
// }

// int main(void)
// {
//     int matrix[3][4];
//     int i , j;

//     for(i=0;i<3;i++)
//     {
//         for(j=0;j<4;j++)
//         matrix[i][j] = i+ j;
//     }
    
//         for(i=0;i<3;i++)
//     {
//         for(j=0;j<4;j++){
//         printf("%d\t", matrix[i][j]);
//         }
//         printf("\n\n");
//     }
//     return 0 ;
// }

// int main(void)
// {
//     int Row, Column,i,j;

//     printf("Enter number of rows: ");
//     scanf("%d", &Row);

//     printf("Enter number of column: ");
//     scanf("%d", &Column);

//     int matrix[Row][Column];

//     for(i=0;i<Row;i++)
//     {
//         for(j=0;j<Column;j++)
//         {
//             printf("\nmatrix[%d][%d]",i,j);
//             scanf("%d", &matrix[i][j]);
//         }
//     }
//     printf("Your array\n");

//     for(i=0;i<Row;i++)
//     {
//         for(j=0;j<Column;j++)
//         {
//             printf("%4d", matrix[i][j]);
//         }
//         printf("\n\n");
//     }

//     return 0 ;
// }

// x e x lik bir tablo yapmak ve major ve minör 1 yazmak

// int main(void)
// {
//     int i , j, size;

//     printf("Enter of the size of the square matrix(x<10)");
//     scanf("%d", &size);

//     int matrix[size][size];

//     for(i=0;i<size;i++)
//     {
//         for(j=0;j<size;j++){
//             matrix[i][j] = 0;
//         }
//     }
//     for(i=0;i<size;i++)
//     {
//         matrix[i][i] = 1 ;      // şuan majorleri yaptık
//         matrix[i][size-i-1] = 1 ; // burdada minörleri doldurduk
//     }
//     for(i=0;i<size;i++)
//     {
//         for(j=0;j<size;j++)
//         {
//             printf("%4d", matrix[i][j]);
//         }
//         printf("\n\n");
//     }
//     return 0 ;
// }


// int main(void)
// {   
//     int matrix[4][2][5] ={              // []ilk kısım ise boyutu ifade eder []2. kısım satırları ifade eder []3. kısım ise sütunları ifade eder
//                             {{9,2},{7,5,6}},
//                             {{7,8,10},{10,12,15,11,14}},
//                             {{15,16,17,18,9},{20,25,7}},
//                             {{1,8,9},{21,13,17,33,54}},
//                          };
//     int i,j,k;
//     for(i=0;i<4;i++)
//     {
//         for(j=0;j<2;j++)
//         {
//             for(k=0;k<5;k++)
//             {
//                 printf("%4d", matrix[i][j][k]);
//             }
//             printf("\n");
//         }
//         printf("\n\n");
//     }
// }


/*0123
  1234
  2345  */

// int main(void)
// {
//     int matrix[3][4];
//     int i, j;

//     for(i=0;i<3;i++){
//         for(j=0;j<4;j++){
//             matrix[i][j] = i+j;
//         }//iç for
//     }//dış for

//         for(i=0;i<3;i++){
//             for(j=0;j<4;j++){
//                 printf("%d\t",matrix[i][j]);
//                 }//iç for
//             printf("\n\n");
//             }//dış for
//     return 0 ;
// }

/*dışardan bir girdi alıp diziyi kendin oluşturma*/

// int main(void)
// {
//     int Row , Column,  i,j;

//     printf("Enter the rows:");
//     scanf("%d", &Row);
//     printf("Enter the column: ");
//     scanf("%d", &Column);

//     int matrix[Row][Column];

//     for(i=0;i<Row;i++)
//     {
//         for(j=0;j<Column;j++)
//         {
//             printf("\nmatrix[%d][%d]",i,j);
//             scanf("%d",&matrix[i][j]);
//         }
//     }
//     printf("Your array");

//     return 0 ;
// }

/*MAJÖR Vİ MİNOR BİR ALGORİTMA OLUŞTURMA*/

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i,j,size;

//     printf("Enter the size of the square matrix(x<10)");
//     scanf("%d",&size);

//     int matrix[size][size]; //kare bir matrix oluşturcaz
//     for(i=0;i<size;i++){
//         for(j=0;j<size;j++){
//             matrix[i][j]=0;
//         }//iç for
//     }//dış for

//     for(i=0;i<size;i++){
//         matrix[i][i]=1;//major
//         matrix[i][size-i-1]=1;//minor
//     }

//     for(i=0;i<size;i++){
//         for(j=0;j<size;j++){
//             printf("%4d",matrix[i][j]);
//         }
//         printf("\n\n");
//     }
//     return 0 ;
// }


/*SATIŞ TEMSİLCİSİ ÖRNEĞİ*/

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// void readSales();
// void writeSales();
// int sales[3][2][2];
// int i,j,k;

// int main(void)
// {
//     readSales();
//     writeSales();
//     return 0 ;
// }

// void readSales()
// {
//     for(i=0;i<3;i++){
//         printf("%d. satis temsilcisi:\n",i+1);
//         for(j=0;j<2;j++){
//             if(j==0) printf("\t matematik kitabi\n");
//             else printf("\t yazilim kitabi");
//                 for(k=0;k<2;k++){
//                     if(k==0) printf("\t Okula");
//                     else printf("\t\t Kirtasiyeye");
//                     printf(" kac adet satti: ");
//                     scanf("%d",&sales[i][j][k]);
//                 }
//         }
//         printf("\n");
//     }
// }

// void writeSales()
// {
//     i=0 , j=0, k=0;
//     int toplamOkul=0 , toplamKirtasiye = 0 , toplamMatematik= 0 , toplamYazilim = 0;

//     for(i=0;i<3;i++){
//         for(j=0;j<2;j++){
//             toplamOkul+=sales[i][j][0];//sonu 0 yapmaktaki amaç 3. indeksin 0 ında okul olduğu için
//             toplamKirtasiye+=sales[i][j][1];// sonu 1 yapmaktaki amaç 1 de kirtasiye oldğuu için
//         }
//         for(k=0;k<2;k++){
//             toplamMatematik+=sales[i][0][k]; // 2. indeksin 0 olma sebebi orda matematik oldğuu için
//             toplamYazilim+=sales[i][1][k];
//         }
//     }
//     printf("\n Okula toplam %d kitap satildi\n",toplamOkul);
//     printf("Kirtasiyeye toplam %d kitap satildi\n", toplamKirtasiye);
//     printf("toplam %d mateamtik kitabi satildi\n",toplamMatematik);
//     printf("toplam %d yazilim kitabi satildi\n",toplamYazilim);

// }

/*BİR DİZİNİN SATIR VE SÜTUNLARIN TOPLAMINI VEREN KOD?*/
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

int main(void)
{
    int i,j,sum=0;
    int matrix[5][5]={  
                        {8,6,5,4,1},
                        {7,2,4,5,6},
                        {7,8,9,8,4},
                        {8,9,4,2,1},
                        {1,2,3,4,5}
                     };
    for(i=0;i<5;i++){//satır
        for(j=0;j<5;j++){//sütun 
            printf("%4d",matrix[i][j]);//satır ve sütunları yazdırma
        }
        printf("\n\n");
    }
    
    for(i=0;i<5;i++){ //satirlarin toplami
            printf("%d. satirinin toplami",i+1);
        for(j=0;j<5;j++){
            sum+= matrix[i][j];
        }
        printf("%d\n", sum);
        sum = 0;
    }

    for(i=0;i<5;i++){   // sütunların toplamı
        printf("%d. sutunun toplami",i+1);
        for(j=0;j<5;j++){
            sum+=matrix[j][i];
        }
        printf("%d\n",sum);
        sum=0;
    }

    return 0 ;
}

4- DİZİLER 

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

// int main(void)
// {
//     int notes[3];
//     notes[0] = 7;
//     notes[1] = 19;  // dizileri bu şekildede tanımlayabiliriz...
//     notes[2] = 24;

//     int i, sum;     
//     sum = notes[0] + notes[2];  //dizilerde toplama yapabiliriz...
//     printf("%d\n",sum);

//     return 0 ;
// }

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     // double avarage=0, numbers[3];

//     // printf("Enter three numbers: ");
//     // scanf("%lf %lf %lf", &numbers[0], &numbers[1], &numbers[2]);

//     // avarage = (numbers[0] +numbers[1] +numbers[2]) /3 ;
//     // printf("avarage: %.3f\n", avarage);

//     // return 0 ;

//     int i , Square[5];      // girilen sayıya kadar olan tüm sayıların karelerini alan bi c programı

//     for(i=0;i<5;i++)
//     {
//         Square[i] = i*i;
//         printf("Square[%d]:%d\n",i,Square);
//     }
//     return 0;
// }


// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     double Degerim , Dizim[10];
//     int Secim,index;
//     do
//     {
//         printf("Make a choice (-1 to Exit )\n");
//         printf("\t1. Write to array\n");
//         printf("\t2. Read from array\n");
//         scanf("%d", &Secim);
//         if(Secim ==-1) break;
//         if(Secim != 1 && Secim !=2)
//         {
//             printf("Benimle dalga mi geciyon aq ?");
//             continue;
//         }
//         printf("Dizinin kac elemanli olacagini giriniz: ");
//         scanf("%d", &index);
//         if(index<0 || index >9)
//         {
//             printf("Söylenen deger araliginda bir index degeri giriniz");
//             continue;
//         }
//         switch(Secim)
//         {
//             case1: printf("\n Enter the Degerim: ");
//                    scanf("%lf", &Degerim);
//                    Dizim[index] = Degerim;
//                    printf("Yazdirma isleminiz basarili\n\n:)");
//                    break;
//             case2: printf("Dizim[%d]: %.2f\n\n", index, Dizim[index]);
//                    break;
//         }
        
//     }while(Secim !=-1);      // döngünün devam etme koşulunu buraya yazıyosun  
//     return 0 ;
// }

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     char name[20];
//     printf("Enter your name: ");
//     gets(name);     /*gets scanf görevinde kullanılır fakat scanf boşluktan sonrasını 
//                       okumadığı için gets kullanılır bu sayede istedğimiz kadar karakter yazabiliriz  */

//     printf("\n Your name is %s\n", name);

//     return 0 ;
// }


// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     int i,dice,howMany[7];
//     srand(time(NULL));  // rastgele sayılarda bunları anlattı zar çekildiği zaman rastgele sayı gelmesini sağlıyor

//     for(i=1; i<=100; i++)
//     {
//         dice = rand()%6+1; // 1 ile 6 arasında rastgele sayıları getirir
//     }
// }


// int main(void)
// {
//     int numbers[7],i;

//     printf("Enter array numbers: ");
//     for(i=0;i<7;i++)
//     {
//         scanf("%d", &numbers[i]);
//     }
//     printf("\n Original order: ");
//     for(i=0;i<7;i++)
//     {
//         printf("%d ", numbers[i]);
//     }
//     printf("Reverese order: ");
//     for(i=6;i<=0;i--)
//     {
//         printf("%d ", numbers[i])
//     }
//     return 0 ;

// }

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// /*Dışarıdan arraya girilecek eleman sayisi girilsin ve bu sonra array sayilarini girsin
//   Bunun sonucunda  tek sayilarla cift sayiları ayrı ayrı ekrana yazdırın.   */

// int main(void)
// { 
//     int i , unit;       //unit burda dizinin kaç elemanlı olacağını belirtiyor
//     int numbers[100];

//     printf("Enter a positive unit: ");
//     scanf("%d", &unit);

//     printf("\n Enter array numbers: ");
//     for(i=0;i<unit;i++)
//     {
//         scanf("%d", &numbers[i]);
//     }
//     printf("Odd numbers:");
//     for(i=0;i<unit;i++)
//     {
//         if(numbers[i]%2==1)
//         printf("%d ", numbers[i]);
//     }
//     printf("\nEven numbers: ");
//     for(i=0;i<unit;i++)
//     {
//         if(numbers[i]%2==0)
//         printf("%d ", numbers[i]);
//     }

//     printf("\n");
//     return 0 ;
// }


// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// /*Bir sınıf en fazla 100 öğrenciden oluşabilir sınıfta bulunan öğrenci sayisini girdi olarak alıp
//   her öğrencinin okul numarasi ile notunu iki ayrı arraya okutalım sonuc olarak en düşük ve en yüksek notu alan
//   öğrenciler ekrana yazdirilsin  */

// int main(void)
// {
//     int size , i,big=0,small=100,bigIndex,smallIndex;
//     int notes[100], studentNo[100];

//     printf("Enter class of size: ");
//     scanf("%d", &size);

//     for(i=0;i<size;i++)
//     {
//         printf("Student No and note: ");
//         scanf("%d %d", &studentNo[i],&notes[i]);    
//     }
//     for(i=0;i<size;i++)
//     {
//         if(notes[i]>big)
//         {
//             big = notes[i];
//             bigIndex = i;
//         }
//         if(notes[i]<small)
//         {
//             small = notes[i];
//             smallIndex = i;
//         }
//     }
//     printf("%d numarali ogrenci en yüksek notu %d almistir\n", studentNo[bigIndex],big);
//     printf("%d numarali ogrenci en düsük notu %d almistir", studentNo[smallIndex], small);

//     return 0 ;
// }

/*Dizimizin kaç elemanlı olduğunu bulmak için kurduğumuz program*/

#include <stdio.h>
#include <stdlib.h>
#include <math.h>

// int main(void)
// {
//     int i,dizi[5] = {10,20,30,40,50};
//     for(i=0;i<5;i++){
//         dizi[i] = 3*dizi[i];
//         printf("dizinin carpilmis hali: %d\n",dizi[i]);
//     }

//     return 0 ;
// }

// int main(void)
// {
//     int dizi[10];
//     int i,j;

//     for(i=0; i<10; i++){
//         printf("%d. sayiyi giriniz:",i+1);
//         scanf("%d",&dizi[i]);
//         if(dizi[i] == 0 )
//             break;
//         j = i;
//     }

//     for(i=0 ;i<=j;i++){
//         printf("%d \n",dizi[i]);
//     }

//     return 0 ;
// }


// int main(void)
// {
//     int i,j,N,temp;
//     printf("N degerini giriniz: ");//dizinin kaç terimli olacağını gösterir
//     scanf("%d",&N);
//     printf("\n");

//     int dizi[N];//dizi  = 10
//     for(i=0;i<N;i++){//dizinin elemanlarını burda sıralıyosunuz
//         printf("%d. sayiyi giriniz:",i+1);
//         scanf("%d",&dizi[i]);
//     }

//     for(i=0;i<N-1;i++){
//         for(j=0;j<N-i-1;j++){
//             if(dizi[j]>dizi[j+1]){
//                 temp =dizi[j];
//                 dizi[j] = dizi[j+1];
//                 dizi[j+1] = temp;
//             }
//         }
//     }
//     printf("\n");
//     for(i=0;i<N;i++){
//         printf("%d\t",dizi[i]);
//     }
//     printf("\n");
//     return 0 ;
// }

// int main(void)
// {
//     int i,N;
//     printf("Bir n degeri giriniz:");
//     scanf("%d",&N);
//     printf("\n");

//     int dizi[N];

//     for(i=0;i<N;i++){
//         dizi[0] = 0;
//     }
//     for(i=0;i<N;i++){
//         printf("%d",i,dizi[i]);
//     }
//     printf("\n");
//     return 0 ;
// }


/*Kullanıcı tarafıdan girilen 10 farklı sayının en büyük olanını bulmak için oluşturulan fonkisyon*/

// int main(void)
// {
//     int i,dizi[10],EnBuyuk;
    
//     for(i=0;i<10;i++){
//         printf("%2d. sayiyi giriniz: ",i+1);
//         scanf("%d",&dizi[i]);
//     }

//     EnBuyuk = dizi[0];
//     for(i=1;i<10;i++){
//         if(dizi[i]>EnBuyuk)
//             EnBuyuk = dizi[i];
//     }
//     printf("Dizinn en buyuk elemani : %d",EnBuyuk);
//     return 0 ;
// }


// int main(void)
// {
//     int i ,N;
//     printf("Lütfen bir N tam sayisi giriniz:");
//     scanf("%d",&N);
    
//     int dizi[N];
//     for(i=0;i<N;i++){
//         dizi[i] = i;
//     }
//     for(i=0;i<N;i++){
//         printf("%d. sayisinin karesi = %d\t",i,dizi[i]*dizi[i]);
//     }
//     printf("\n");
//     return 0 ;
// }

int main(void)
{
    const BOYUT=10;
    int grafik[10]  = {19,3,15,7,11,9,13,5,17,1};
    int i,j;

    for(i=0;i<=BOYUT-1;i++){
        printf("%4d. elemanin degeri -->",i,grafik[i]);
    for(j=1;j<=grafik[i];j++){
        printf("*");
    }
    printf("\n");
    }
    return 0 ;
}

/*Kelimelerin baş harfini alma*/

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// void ozet(char* message);

// int main(void)
// {
//     char message[100];
//     puts("Enter a sentence: ");
//     gets(message);
//     ozet(message);
//     return 0 ;
// }

// void ozet(char* message)
// {
//     int i = 0;
//     while(*(message+i) != '\0')
//     {
//         if(i==0) putchar(*message);//getchar sadece tek bir karatker almak için kullanılır
//         if(*(message+i) == ' ')
//             putchar(*(message+i+1));
//             i++;
//     }
// }


/*KELİMELERİ TERSTEN YAZDIRMA*/

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// void printReverse(char*);

// int main(void)
// {
//     char message[100];

//     puts("Enter a sentence: ");
//     gets(message);

//     printReverse(message);
//     return 0 ;
// }

// void printReverse(char* message)
// {
//     int i = 0 ,lenght = 0;
//     lenght = strlen(message);
//     for(i=(lenght-1);i>=0;i--)
//     {
//         putchar(*(message+i));
//     }
// } 

/*Girilen cümlede harflerin kaçar kez kullanıldığını bulma*/
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

// void calculate(char*);

// int main(void)
// {
//     char message[100];
//     puts("Enter a sentence: ");//kullanıcıdan girdi aldın
//     gets(message);
//     calculate(message);//fonksiyonun içine gönderdin
//     return 0 ;
// }

// void calculate(char* ptr)
// {
//     int letters[26], i=0, lenght;
//     char activeLitter;
//     lenght=strlen(ptr);//cümlenin uzunluğunu bulmak için kullandık


// }

// int main(void)
// {
//     char dizi[50];
//     int i;
//     printf("Lütfen metni giriniz:");
//     gets(dizi);

//     printf("\n Karakterleri tek tek yazdir\n");
//     for(i=0;i<=dizi[i];i++){
//         printf("%c\n",dizi[i]);
//     }
//     printf("\n Tüm karakterleri yazdir \n");
//     printf(dizi);
//     printf("\n");
//     return 0 ;
// }

// int main(void)
// {
//     int dizi[2][3] = { 5,3,1,
//                        2,4,6};
//     int satir,sutun,enk,i,m,enk_satir,enk_sutun;
//     enk_sutun = 0;
//     enk_satir = 0;
//     enk=dizi[0][0];
//     for(i=0;i<2;i++){
//         for(m=0;m<3;m++){
//             if(enk>dizi[i][m]){
//                 enk = dizi[i][m];
//                 enk_satir = i;
//                 enk_sutun = m;
//             }
//         }
//     }
//     printf("En kucuk elemanin indisi[%d,%d]\n",enk_satir,enk_sutun);
//     return 0 ;
// }

// /*iki matrisin çarpımı*/
// int main()
// {
//     int a[3][3] = { 5,7,9, 
//                     0,3,0, 
//                     7,5,1};
//     int b[3][3] = { 3,3,1, 
//                     2,1,3, 
//                     1,0,0};
//     int c[3][3];
//     int i,j,k,toplam;

//     printf("C matrisi: ");
//     for(i=0;i<3;i++){
//         for(j=0;j<3;j++){
//             toplam = 0;
//             for(k=0;k<3;k++){
//                 toplam += a[i][k]*b[k][j];
//             }
//             c[i][j] = toplam;
//             printf("%4d",c[i][j]);
//         }
//         printf("\n");
//     }
//     return 0;
// }

// 5- DÖNGÜLER

// WHILE DÖNGÜSÜ

#include <stdio.h>
#include <stdlib.h>

// int main(void)
// {
//     int i = 1;

//     while(i <= 5)           /* bunun içine giren sayı döngüye giriyor
//                                yani i 5 den küçük veya eşit olana kadar 
//                                while döngüsünün içinde dönmeye devam ediyor
//                                5 ten büyük olduğu zaman ise döngüden çıkıyor */
//     {
//         printf("%d\n", i);
//         i++;
//     }
//     return 0 ;
// }


// int main(void)
// {
//     int i = 1;

//     while(i<=7)         /*bunun mantığıda i sayısı 7 den küçük veya eşit olana kadar 
//                           printf ile yazılan şeyi yazdır demek istiyo*/
//     {
//         printf("C is fantastic leangueage\n");
//         i++;
//     }
//}

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i;
//     i = 2;         

    // yazımı şu şekildedir               // do while ın özelliği normalde bu koşul döngüye girmez 
                                          // ama do whlie ile ilk başta doğruluğuna bakmaksızın döngüye alır
//     do                                    // sonra doğruluğuna bakar aradaki ince fark bu                       // ilk başta döngüye girmez ama do komutuyla doğruu veya yanlış olmasına bakmaz                             // direk içine alır
//     {
//         printf("%d\n", i);
//         i++ ;
//     }
//     while(i<=7);

//     return 0 ;                             

// }


// FOR DÖNGÜSÜ

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i ;

//     for(i = 0; i < 7 ; i++) /* for içinde 3 tane değere ayrılır:
//                                 ilk değer benim ifadem hani değerle başlıyor anlamına gelir
//                                 2. değerde koşulu belirtir
//                                 3. değerde sayacı belirtir*/
//     {
//         printf("%d\n",i);
//     }

//     return 0 ;
// }

// #include <stdio.h>
// #include <stdlib.h>

//  int main(void)
//  {
//      int i ;
//      for(i=0; i<=10 ; i++)
//      {
//          if(i==7)
//          {
//              continue;  /*continue ifadesinden sonraki ifadeleri görmez ve bi kereliğine onu atlar amacı budur*/
//          }
//      printf("%d\n", i);
//      }
//  }
//     return 0 ;
// }

// int main(void)
// {
//     int i ;
//     i = 0;

//     while(i<=10)
//     {
//         if(i == 5)
//         {
//             break;
//         }
//     printf("%d\n", i);
//     i++;
//     }
// }


/* GİRİLEN SAYININ ASAL OLUP OLMADIĞIN BULAN PROGRAM*/

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int number , i ;
//     number = 0;
//     i = 2;

//     printf("Enter a number: ");
//     scanf("%d\n", &number);

//     if( number < 0 )
//     {
//         printf("please enter a positive number");
//         return 0 ;
//     }

//     while(i < number / 2)
//     {
//         if(number%i == 0)
//         {
//             printf("%d divided by %d so it can't  be a prime", number, i);
//             return 0 ;
//         }
//         i++;
//     }
//     printf("%d is a prime number",number);
//     return 0 ;
// }


/* GİRİLEN SAYININ ASAL OLUP OLMADIĞIN BULAN PROGRAM*/

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i , j , number , control;
//     printf("Enter a number: ");
//     scanf("%d\n", &number);

//     for(i=2 ; i<=number; i++)
//     {
//         control = 1;
//         for(j=2 ; j<=i/2 ; j++)
//         {
//             if(i%j==0)
//             {
//                 control = 0;
//                 break;
//             }
//         }
//     if(control != 0 )
//     {
//         printf("%d\n", i);
//         break;
//     }
//     }
//     return 0 ;
// }

// GİRİLEN NOTLARIN ORTALASMINI BULAN PROGRAM

// #include <stdio.h>
// #include <stdlib.h>

// int main(void){
//     int i ;
//     float  examGrade , sumGrade, avarage;

//     i = 1;
//     examGrade = 0.0;
//     sumGrade = 0.0;
//     avarage = 0.0;

//     do{
//         printf("%d the exam grade: ",i);
//         scanf("%f\n", &examGrade);
//         if(examGrade == 0){
//             break;
//         }
//         if(examGrade < 0 ){
//             printf("please enter a positive number...\n");
//             continue;
//         }
//         else{
//             sumGrade += examGrade;
//         }
//         i++;
        
//     }while(examGrade != 0); // girilen sayi 0 a eşit olana kadar çalıtır demektir bunun anlamı
//     avarage = sumGrade / (i-1);
//     printf("\n you entered %d exam grades\n", (i-1));
//     printf("avarege %f\n",avarage);


//     return 0 ;
// }

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i ;
//     double wheat = 1;
//     double sumWheat = 0;

//     for(i = 1 ; i <= 64; i++)
//     {
//         printf("%d kare icin bilgine verilecek bugday sayisi : %20.f\n", i , wheat);
//         sumWheat += wheat;
//         wheat *= 2;
//     }
//     printf("\n bilgine verliecek toplam bugday sayisi : %20.f\n", sumWheat);

//     return 0 ;
// }


// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i , factoriel , number;
//     factoriel = 1;

//     printf("Enter a number: ");
//     scanf("%d\n", &number);

//     for(i=1; i<= number ; i++)
//     {
//         factoriel *= i ;
//     }
//     printf("%d = %d\n", number , factoriel);
//     return 0 ;
// }

        // pascal üçgeni yapımı

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int space , i , rows,j,number;
//     printf("Enter the number of rows: ");
//     scanf("%d",&rows);

//     for(i=0; i<rows; i++)   // bu for döngüsünün amacı satır sayısını belirlemek
//     {
//         for(space=1; space<=rows-i;space++){
//             printf("  ");
//         }
//         for(j=0;j<=i; j++){
//         if(j==0 || i ==0)
//         number = 1;
//         else
//         number = number*(i-j+1)/j;
        
//         printf("%4d",number);
// //         }
// //     printf("\n");
// //     }
// //     return 0 ;
// // }

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i, j, row, a=0;     // a değişkeni burda boşlukları tutsun
//     char myLitter;

//     printf("Enter a myLitter: ");   // Hangi harfi gireceğimizi seçiyoruz
//     scanf("%c" ,&myLitter);
//     printf("Please enter the number of row (odd number): ");    // kaç satır olacağını seçiyorz
//     scanf("%d", &row);
//     for(i=0;i<row;i++)
//     {
//         if(i<=row/2)    /*bu if else sayesinde boşlukları belirtmiş olduk*/
//             a++;        
//         else
//             a--;
//         for(j=1; j<a; j++)
//             printf("  ");

//         printf("%c\n", myLitter);

//     }

//     return 0 ;
// }

// 6- DOSYA OLUŞTURMA

#include <stdio.h>
#include <stdlib.h>

// int main(void)
// {
//         FILE *fp;

//         if((fp = fopen("text.doc","w")) == NULL)
//         {
//             printf("text.doc dosyasi acilamadi ...\n");
//             printf("program kapatiliyor...\n");
//             exit(0);
//         }
//         else
//         {
//             printf("text.doc dosyasi acildi...\n");
//             printf("fp nin degeri : 0x%p\n",fp);

//             printf("dosya kapatiliyor...\n");
//             fclose(fp);
//         }
// }


//  void main()
//  {
//      FILE *dd;
//      int i, no;
//      dd = fopen("d:\\rakam.txt","r");
//      /*dosya yazma modunda açılıyor*/
//      if(dd == NULL)
//      {
//          printf("sunucu bulunamadi\n");
//      }
//      else
//      {
//          for(i=1; i<=5;i++)
//          {
//              printf("%d. sayiyi giriniz: ",i);
//              scanf("%d",&no);
//              fprintf(dd,"%d\n",no);
//              fclose(dd);
//          }
//      }
//  }


// void main()
// {
//     FILE *dd;
//     int no;/*dosya okuma modunda açılıyor*/
//     if((dd = fopen("d:\\rakam.txt","r") == NULL))
//     printf("surucu veya dosya bulunamadi");
//     else
//     {
//         while(fscanf(dd,"%d",&no)!= EOF)
//             printf("%d\n",no);
//             fclose(dd);
//     }
// }

// int main(void)
// {
//     FILE *fp;

//     fp = fopen("hangiyildayiz.txt","w+");
//     if(fp == NULL)
//     {
//         printf("hangi yildayiz.txt dosyasi acimadi. \n");
//         exit(1);
//     }
//     fprintf(fp,"%s %d %s","Bu sene ",2022,"yilindayiz");
//     fclose(fp);
    
//     return 0 ;
// }

// int main(void)
// {
//     FILE *fp;
//     fp = fopen("hangiyildayiz.txt","r");

//     if ( fp==NULL)
//     {
//         printf("Dosya okunmadi\n");
//         exit(1);
//     }
//     int yil;
//     char s1[10];
//     char s2[10];
//     fscanf(fp,"%s%d%s",s1,&yil,s2);
//     printf("Yil: %d,yil");
//     return 0;
// }

// int main(void)
// {
//     FILE *fp;
//     fp = fopen("r2.txt","r");
//     if (fp == NULL)
//     {
//         printf("Dosya acarken hata olustu...\n");
//         exit(1);
//     }
//     int crs, sayac = 0;
//     int sayi, enBuyuk, enKucuk;
//     while(crs!=EOF)
//     {
//         crs = fscanf(fp,"%d",&sayi);
//         if(crs != EOF)
//         {
//             if(sayac == 0)
//             {
//                 enBuyuk = sayi;
//                 enKucuk = sayi;
//             }
//             else
//             {
//                 if(sayi>enBuyuk)
//                     enBuyuk = sayi;
//                 if(sayi<enKucuk)
//                     enKucuk = sayi;
//             }
//             sayac++;
//         }
//     }
//     printf("En buyuk sayi: %d\n",enBuyuk);
//     printf("En kucuk sayi: %d\n",enKucuk);
//     fclose(fp);
//     return 0 ;
// }

/*
    r = dosyayı verş okumak için aç 
    w = dosyayı verş yazmak için aç.Eskisini siler üstüne tekrar oluşturur
    a = dosyayı verş eklemek için aç.Sadece veri eklemek
    */

#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// int main(void)
// {
//     FILE *fptr;
//     fptr  = fopen("C:\\Users\\faika\\Desktop\\data\\data.txt.txt","w");
//     fclose(fptr);
//     return 0 ;
// }


/*DOSYA YAZMA İŞLEMİ*/
// int main(void)
// {
//     FILE *fptr;
//     fptr = fopen("C:\\Users\\faika\\Desktop\\data\\data.txt.txt","w");
//     char name = 'F', name2 = 'A';
//     if(fptr == NULL)
//         printf("file open unsuccesful!\n");
//     else
//     {   
//         for(name = 'A';name<='Z';name++)
//         {
//             putc(name,fptr);
//             putc('\n',fptr);
//         }
//         printf("Data is written to file \n");
//     }
//     fclose(fptr);
//     return 0 ;
// }


/*DOSYA YAZDIRMA*/
// int main(void)
// {
//     FILE* fptr;
//     char data[60];
//     fptr = fopen("C:\\Users\\faika\\Desktop\\data\\data.txt.txt","w");
//     if(fptr == NULL)
//         printf("File open uncuccsessul");
//     else
//     {
//         printf("Enter a sentence: ");
//         gets(data);

//         fprintf(fptr,"cumleniz: %s",data);
//         printf("data was written to file succsessfuly");
//     }
//     fclose(fptr);
//     return 0 ;
// }


/*fwrite'ın kullanımı*/
// int main(void)
// {
//     FILE* fptr;
//     int numbers[7],i;
//     fptr = fopen("C:\\Users\\faika\\Desktop\\data\\data.txt.txt","r");
//     if(fptr == NULL)
//         printf("File open unsuccsesfuly");
//     else
//     {
//         printf("Enter a 7 numbers: ");
//         //fwrite ile yazdığımız dosayı burdan okuyabilirz
//         fread(numbers,sizeof(int),7,fptr);
//         for(i=0;i<7;i++)    
//             printf("%d\n",numbers[i]);

//         //fwrite(numbers,sizeof(int),7,fptr);/*ilk sayi sonra boyutu sonra miktarı sonra hangi dosya olduğu*/

//         printf("Data was written to file successfuly\n");
//     }
//     fclose(fptr);
//     return 0 ;
// }


/*DOSYA OKUMA*/
#include <stdio.h>
#include <stdlib.h>
#include <string.h>

// int main(void)
// {
//     FILE* fptr;
//     char data[100];
//     //char myLetter;
//     fptr = fopen("C:\\Users\\faika\\Desktop\\data\\data.txt.txt","r");
//     if(fptr == NULL)
//         printf("File open unsuccessful");
//     else
//     {
//         fgets(data,10,fptr);//2.şey kaç harf okumasını söyler.Veri okumanı sağlar
//         printf("%s\n\n",data);//fputs veri yazmanı sağlar


//         // do
//         // {
//         //     myLetter=getc(fptr);// tek harf alarak ilerler
//         //     printf("Text read from file: %c\n",myLetter);//bütün tek harfleri yazdırır
//         // } while (myLetter !=EOF);
//         // printf("\nReading is over\n");
//     }
//     fclose(fptr);
//     return 0;
// }


/*KONUM GÖSTERGECİ AYARLARI*/
// int main(void)
// {
//     FILE* fptr;
//     char data[100];
//     fptr = fopen("data.txt","r");
//     if(fptr == NULL)
//         printf("File open unsuccessful");
//     else
//     {
//         printf("Konum gostergeci yeri: %d\n,",ftell(fptr));//konumun yerini bize söyler
//         fseek(fptr,50,SEEK_SET);//50 satır ileri git demek
//         printf("Konum gostergeci yeri: %d\n",fteel(fptr));
//         fgets(data,100,fptr);//100
//         printf("%s\n",data);
//         printf("Konum gostergeci yeri: %d\n",fteel(fptr));
//         rewind(fptr);//konumu en başa almak
//     }
//     fclose(fptr);
//     return 0 ;
// }

/*DOSYA KLONLAMA*/
// int main(void)
// {
//     FILE *fptr, *fptrcopy;
//     fptr = fopen("data.txt","r");
//     fptrcopy = fopen("datacopy.txt","w");
//     if(fptr == NULL)
//         printf("data.txt open unsuccsesfull");
//     else
//         if(fptrcopy == NULL)
//             printf("datacopy.txt open  unsuccsessful\n");//dosya kopyalama işi
//         else
//         {
//             while(!feof(fptr))//dosyanın sonuna kadar oku demek
//                 putc(getc(fptr),fptrcopy);
//         }
//         printf("The file has been copied\n");
//     fclose(fptr);
//     fclose(fptrcopy);
//     return 0;
// }

// FPUTS FGETC KULLANIM

// int main(void)
// {
//     FILE *fp;
//     fp = fopen("dosya.txt","w");

//     if(fp == NULL)
//     {
//         printf("Dosya olusturulurken bie hata olustu");
//         exit(1);
//     }
//     fputc('a',fp);
//     fclose(fp);

//     fp = fopen("dosya.txt","r");
//     if(fp == NULL)
//     {
//         printf("dosya olusturulurken bir hata olustu");
//         exit(1);
//     }

//     char okunan;
//     okunan = fgetc(fp);
//     if(okunan == EOF)
//     {
//         printf("karakter okunmadi");
//     }
//     else
//     {
//         printf("okunan karakter : %d\n",okunan);
//     }

//     return 0;
// }


int main(void)
{
    double x[6] = {1.1,3.3,7.1,5.4};
    double *p;
    int k ;
    for(k = 1; k< 6;k++)
    {
        printf("")
    }

}

// 7- ENUM KULLANIMI

/*Sabitlerin olduğu bir arraydir enum . Diğer adı sabitler grubudur*/

/*TANIMLAR*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// enum month{
//     JANUARY,
//     FEBRUARY,
//     MARCH,
//     APRIL,
//     MAY,
//     JUNE,
//     JULY,
//     AUGUST,
//     SEPTEMBER,
//     OCTOBER,
//     NOVEMBER,
//     DECEMBER
// };

// int main(void)
// {
//     enum month myConst;
//     myConst = JUNE;

//     if(myConst == 6 || myConst==7 || myConst == 8)
//         printf("Welcome to summer vacation\n");
//     else
//         printf("It's scholl time again\n");

//     return 0 ;
// }

/*typedef = bir variableye takma isim takmak demektir*/

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// typedef struct{
//     char* name;
//     int age;
//     float weight;
// }Student;//kısaltılmasını burda kendine göre ayarlayabilirsin

// int main(void)
// {
//     Student s1 = {"Nazli",28,62.3};
//     Student s2 = {"Ceren",25,61.7};

//     printf("Your name: %s\n", s1.name);
//     printf("Your age: %d\n",s1.age);
//     printf("your weight: %f\n",s1.weight);

//     return 0 ;
// }


/*UNİON İLE STRUCT ARASINDAKİ FARK*/
//NOT: struct lar yer ayırırken bütün karakterlere ayırılar
//Not: unionlar ise sadece büyük olanlara göre yer ayırırlar
//NOT: unionlar da sadece bir elemana ulaşabilirsiniz scanf ile
//NOT: sadece yüksek olan byte ttaki değeri tutar

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// union unionS{
//     char myLetter;
//     int x;
// }uStudent;

// int main(void)
// {
//     uStudent.x = 98;
//     printf("%d\n",uStudent.x);//98 yazdırdı 
//     printf("%c\n",uStudent.myLetter);//ama bunu yazdırmadı
// }


// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>

// int main(void)
// {
//     enum mainColors{
//         Red,
//         Blue,
//         Yellow
//     };

//     //Define variable
//     enum mainColors pixel;

//     // Set value of pixel to blue
//     //You can  set yellow or red also
//     pixel = Blue;

//     if(pixel == Red)        
//         printf("Red pixel \n");
//     else if(pixel == Blue)
//         printf("Blue pixel \n");
//     else
//         printf("Yellow pixel\n");

//     return 0 ;
// }

#include <stdio.h>
#include <stdlib.h>
#include <math.h>
#include <string.h>

// int main(void)
// {
//     //Define new data type
//     //Also define a new variable with the new data type

//     enum boolean{
//         false = 0,
//         True
//     };

//     typedef enum boolean bool; // takma isim taktım
//     bool isTrue;
//     isTrue = True;
//     if(isTrue == True)
//         printf("True \n");
//         return 0 ;
// }


#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>

// int main(void)
// {
//     enum mainColors{
//         Red,
//         Blue,
//         Yellow
//     };

//     enum mainColors pixel;
//     pixel = Blue;
//     if(pixel == Red)
//         printf("pixel == red");
//     if(pixel == Blue)
//         printf("pixel == blue");
//     else
//         printf("Yellow pixel\n");

//     return 0 ;
// }

/*typdef kullanımı*/
// int main(void)
// {
//     enum boolean{
//         false,
//         True
//     };
//     typedef enum boolean bool; // boolean ismini bool olarak tanımladım

//     bool isTrue;
//     isTrue = True;
//     if(isTrue == True)
//         printf("True\n");
//     return 0 ;

// }

// int asalSayi(int,int);
// int main(void)
// {
//     int sayi = 29;
//     int sonuc=asalSayi(sayi,sayi/2);
//     if(sonuc == 0)
//         printf("%d asal sayi degildir\n",sayi);
//     else
//         printf("%d asal sayidir\n",sayi);
//     return 0;
// }

// int asalSayi(int x,int i)
// {
//     if(x<2)
//         return 0;
//     else if(i == 1)
//         return 1;
//     else if(x%i==0)
//         return 0;
//     return asalSayi(x,i-1);
// }

enum BOOLEAN{FALSE, TRUE};
int tek(int n)
{
    return (n%2);
}

int main(void)
{
    enum BOOLEAN sonuc;
    int x;
    printf("Bir sayi giriniz: ");
    scanf("%d",&x);
    sonuc = tek(x);
    if(sonuc==TRUE)
        puts("Girilen sayi tek");
    else
        puts("Girilen sayi cift");
    return 0;
}

// 8- FONKSİYONLAR 

// #include <stdio.h>
// #include <stdlib.h>

// void myMassage()        // return ile 0 a dönmek istemiyorsak void fonksiyonunu kullanırız                        // bir fonkisyon sadece çağırıldığında çalı                        // fonksiyonları istediğimizca kullanabilirz
// {
//     printf("Now I can  write  a function");
// }
// void nameList(char name[], int age) //ilk başta burda tanımlıyosun allta okutuyosun 
// {
//     printf("%s. you are %d year old\n",name,age);
// }


// int main()
// {

//     nameList("fehmi",32);
//     nameList("Emre",12);
//     nameList("Faik",14);
//     myMassage();
//     return 0 ;
// // }

// #include <stdio.h>
// #include <stdlib.h>
// void theMassage();
// int sumNumber(int,int);

// int main()
// {
//     int result = sumNumber(5,15);
//     printf("result is %d \n",result);
//     theMassage();
//     return 0 ;
// }

// void theMassage()       // void olduğu için yukarıda tanımlamak lazım okutmak için
// {
//     printf("I love C language");
// }

// int sumNumber(int x,int y)
// {
//     return x+y;
// }



// int sumNumber(int i);

// int main()
// {
//     int result= sumNumber(10);

//     printf("%d\n", result);

//     return 0 ;
// }

// int sumNumber(int i)
// {
//     if(i>0)
//         return i+sumNumber(i-1);
//     else
//     {
//         return 0 ;
//     }
// }

// #include <stdio.h>
// #include <stdlib.h>

// float ust_alma(float x, float y);

// int main()
// {
//     float taban = 0 ,result = 0;
//     int üst = 0;
//     printf("Enter a üst and taban: ");
//     scanf("%f%d", &taban , &üst);
//     result = üst_alma(taban, üst);
//     printf("Result: %f\n", result);
//     printf("Result: %f\n", üst_alma(2,7));
//     return 0 ;
// }

// float ust_alma(float x, int y)
// {
//     float  result = 1;
//     int i ;
//     if(y<0)
//     {
//         for(i=0;i<-y;i++){
//             result*=1/x;
//         }
//         else{    
//             for()
//         }
//     }
    
//     }
// }

// #include <stdio.h>
// #include <stdlib.h>

// void myMassage()
// {
//     printf("Now I can write a funtion");
// }
// void nameList(char name[]){ // burda istediğin kadar parametre alabilirsin  
//     printf("Hello %s\n", name);
// }
// int main()
// {
//     nameList("Faik");   // bunun içine yazdığın şey aslında 
//                         // char name[] olan kısma yazılmış oluyo ordanda pritnf ile yazdırıyosun
//     nameList("Beyza");
//     nameList("Emir taha");
//     myMassage();
//     return 0 ;
// } 


// #include <stdio.h>
// #include <stdlib.h>

// void allNumbers(int myNumbers[6])    // void kullanımında return ile geriye değer döndüremezsin
// {
//     for(int i=0;i<6;i++)
//     {
//         printf("%d\n", myNumbers[i]);
//     }
// }

// int showMe(int x)   /*burda aşağıda x in içine 2 değerini atar sonra return değeriyle fonkisyonu döndürür*/
// {
//     return 5+x;
// }

// int main()
// {
//     // int myNumbers[6] = {10,20,30,40,50,60};
//     // allNumbers(myNumbers);
//     printf("Result is %d\n", showMe(2));
//     return 0 ;
// }

/* VOİD İLE İNT FONSKİYONUN FARKI*/

// #include <stdio.h>
// #include <stdlib.h>

// int showMe(int x)
// {
//     return x+5;
// }

// int sumNumbers(int x, int y)
// {
//     return x+y;
// }

// int main()
// {
//     int myNumber = sumNumbers(1,6)*5;

//     printf("Result is %d\n", myNumber);

//     return 0 ;
// }


// USTA YAZILIMCILARIN YAPTIĞI FONKSİYONLAR

// #include <stdio.h>
// #include <stdlib.h>

// int sumNumber(int,int); // fonskiyonu burda tanımladık

// int main()
// {
//     int result = sumNumber(5,11);
//     printf("result id %d\n", result);
//     return 0 ;
// }
// int sumNumber(int x, int y)
// {
//     return x + y;
// }

//GERİ ÇAĞIRICI FONKSİYONLAR

// #include <stdio.h>
// #include <stdlib.h>

// int sumNumber(int i) ; // burda noktalı virgül kullanmak zorundayız çünkü tanım yapıyorz

// int main()
// {
//     int result = sumNumber(5);
//     printf("Result is %d\n", result);

//     return 0 ;
// }

// int sumNumber(int i)
// {
//     if(i>0)
//         return i+sumNumber(i-1);
//     else
//         return 0;
// }


// ÜS ALMA
// #include <stdio.h>
// #include <stdlib.h>

// int exponentiation(float x , int y);

// int main()
// {
//     float base=0 , result=0; //taban
//     int exponent =0; //üs
//     printf("enter a base and exponent value: ");
//     scanf("%f%d",&base ,&exponent);
//     result = exponentiation(base ,exponent);
//     printf("Result : %f\n", result);
    
//     return 0 ;
// }

// float exponentiation(float x , int y)
// {
//     float result = 1;
//     int i ;
//     if(y<0)
//     {
//         for(i=0;i<-y;i++)
//             result *=1/x;
//     }
//     else{
//     for(i=0;i<y;i++)
//         result*=x;
//     }
//     return result;
// }


// MATEMATİKSEL İŞLEMLER
// #include <stdio.h>
// #include <stdlib.h>

// void menu();    // geriye return dönmeyeceği için void yaptık
// int min(int,int);
// int max(int,int);
// int square(int);
// int cube(int);
// int absolute(int);

// int main()
// {
//     int choose=0,x,y;
//     menu();
//     printf("\nChoose a number(1-5)");
//     scanf("%d",&choose);
//     printf("\n");
//     switch(choose)
//     {
//         case 1 : printf("Enter two numbers: ");
//                  scanf("%d%d", &x,&y);
//                  printf("Min: %d\n",min(x,y));
//         break;
//         case 2 : printf("Enter two numbers: ");
//                  scanf("%d%d", &x,&y);
//                  printf("Max: %d\n", max(x,y));
//         break;
//         case 3: printf("Enter a number: ");
//                 scanf("%d", &x);
//                 printf("Square: %d\n", square(x));
//         break;
//         case 4: printf("Enter a number: ");
//                 scanf("%d", &x);
//                 printf("cube: %d\n", cube(x));
//         break;
//         case 5: printf("Enter a number: ");
//                 scanf("%d",&x);
//                 printf("absolute: %d\n", absolute(x));
//         break;
//     default: printf("Yanlis bir sayi degeri girdiniz!!!");
//     }

//     return 0 ;
// }

// void menu()
// {
//     printf("\n");
//     printf("*********\n");
//     printf("*    MENU    *\n");
//     printf("*********\n\n");
//     printf("1- Minimum\n");
//     printf("2-Maksimum\n");
//     printf("3-Kare al\n");
//     printf("4- Küp al\n");
//     printf("5- Mutlak değer al\n");
// }

// int min(int x , int y)
// {
//     if(x<y)
//         return x;
//     else    
//         return y;
// }

// int max(int x , int y)
// {
//     if(x>y)
//         return x;
//     else
//         return y;
// }
// int square(int x)
// {
//     return x*x;
// }
// int cube(int x)
// {
//     return x*x*x;
// }
// int absolute(int x)
// {
//     if(x<0)
//         return x*(-1);
//     else
//         return x;
// }


// YEREL VE GLOBAL DEĞİŞKENLER
// #include <stdio.h>
// #include <stdlib.h>

// void Increase();
// void Decrease();
// int x = 7;

// int main()
// {
//     printf("x: %d\n",x);
//     Increase();
//     printf("x:%d\n",x);
//     Decrease();
//     Decrease();
//     Decrease();
//     printf("x:%d\n",x);
// }

// void Increase()
// {
//     x++;
// }
// void Decrease()
// {
//     x--;
// }

// DÖRT BASAMAKLI SAYIYI YAZIYA ÇEVİRME

// #include <stdio.h>
// #include <stdlib.h>

// void BirlikCevir();
// void OnlukCevir();

// int main()
// {
//     int number = 0 ,d1,d2,d3,d4;
//     while(number!=-1)
//     {
//         printf("Enter a four digit number: ");
//         scanf("%d",&number);
 //        if(number==-1) break;
//         d1=number%10; // birler
//         d2=(number%100)/10; //onlar
//         d3=(number%1000)/100; //yüzler
//         d4=number/1000; //binler
//         if(d4!=1) BirlikCevir(d4);
//         printf(" Bin ");
//         if(d3!=1) BirlikCevir(d3);
//         if(d3!=0) printf(" Yuz ");
//         OnlukCevir(d2);
//         printf(" ");
//         BirlikCevir(d1);
//         printf("\n\n");
//     }

//     return 0 ;
// }

// void BirlikCevir(int number)
// {
//     switch(number)
//     {
//         case 1:printf("Bir"); break;
//         case 2:printf("İki"); break;
//         case 3:printf("Uc"); break;
//         case 4:printf("Dort"); break;
//         case 5:printf("Bes"); break;
//         case 6:printf("Alti");break;
//         case 7:printf("Yedi");break;
//         case 8:printf("Sekiz");break;
//         case 9:printf("Dokuz");break;
//     }
// }

// void OnlukCevir(int number)
// {
//     switch(number)
//     {
//         case 1:printf("on"); break;
//         case 2:printf("Yirmi"); break;
//         case 3:printf("Otuz"); break;
//         case 4:printf("Kirk"); break;
//         case 5:printf("Elli"); break;
//         case 6:printf("Altmis");break;
//         case 7:printf("Yetmis");break;
//         case 8:printf("Seksek");break;
//         case 9:printf("Doksan");break;
//     }
// }
// #include <stdio.h>
// #include <stdlib.h>

// void BirlikCevir();
// void OnlukCevir();

// int main(void)
// {
//     int number , d1,d2,d3,d4,d5;
//     while(number!=-1){
//     printf("Bes basamakli bir sayi giriniz: ");
//     scanf("%d",&number);
//     if(number==-1) break;
//     d1= number%10; //birler
//     d2= (number%100)/10; //onlar
//     d3= (number%1000)/100; //yüzler
//     d4= (number%10000)/1000; // binler
//     d4= number /10000;
//     if(d5!=1) OnlukCevir(d5);
//     if(d4!=0) BirlikCevir(d4);
//     printf(" Bin ");
//     if(d3!=1) BirlikCevir(d3);
//     if(d3!=0) printf(" Yuz ");
//     OnlukCevir(d2);
//     printf("\n");
//     BirlikCevir(d1);
//     printf("\n\n");
//     }
//     return 0 ;
// }

// void BirlikCevir(int number)
// {
//     switch(number)
//     {
//         case 1:printf("Bir");break;
//         case 2:printf("İki");break;
//         case 3:printf("Uc");break;
//         case 4:printf("Dort");break;
//         case 5:printf("Bes");break;
//         case 6:printf("Alti");break;
//         case 7:printf("Yedi");break;
//         case 8:printf("Sekiz");break;
//         case 9:printf("Dokuz");break;
//     }
// }

// void OnlukCevir(int number)
// {
//     switch(number)
//     {
//         case 1:printf("On");break;
//         case 2:printf("Yirmi");break;
//         case 3:printf("Otuz");break;
//         case 4:printf("Kirk");break;
//         case 5:printf("Elli");break;
//         case 6:printf("Altmis");break;
//         case 7:printf("Yetmis");break;
//         case 8:printf("Seksen");break;
//         case 9:printf("Doksan");break;
//     }
// }

// FAKTÖRİYEL HESAPLAMA

// #include <stdio.h>
// #include <stdlib.h>

// int factorial();

// int main(void)
// {
//     int number;

//     printf("Enter a number: ");
//     scanf("%d",&number);

//     printf("%d = %d\n", number , factorial(number));
//     return 0 ;
// }

// int factorial(int number)
// {
//     if(number == 0)
//         return 1;
//     else
//         return number*factorial(number-1);
// }

// SICAKLIK BİRİMİ DÖNÜŞTÜRME

// #include <stdio.h>
// #include <stdlib.h>

// int CelToFah(int);
// int FahToCel(int);

// int main(void)
// {
//     char choose;
//     int number;
//     printf("Fahrenheit -> Celcius icin c\n");
//     printf("Celcius --> Fahrenheit icin f\n");
//     printf("Seciminizi yapiniz: ");
//     scanf("%c", &choose);
//     switch(choose)
//     {
//         case 'c': printf("Fahrenheit degerini giriniz: ");
//                   scanf("%d",&number);
//                   printf("Celceius degeri : %d\n", FahToCel(number));
//                   break;
//         case 'f': printf("Celcius degerini girinz:");
//                   scanf("%d", &number);
//                   printf("Fahrenheit degeri : %d\n",CelToFah(number));
//                   break;
//         default:printf("Yanlis bir deger girdiniz !!!");  
//     }
// }

// int CelToFah(int c)
// {
//     return (c*9/5+32);
// }
// int FahToCel(int f)
// {
//     return ((f-32)*5/9);
// }


// BAZI MATEMATİKSEL FONKSİYONLAR



// int main(void)
// {
//     int i ;
//     for(i=0;i<5;i++)
//     {
//         printf("e uzeri %d:%.2f\n",i,exp2(i)); // exp(i)= e nin i. kuvveti ,exp2(i) = 2nin i. kuvveti
//     }
//     return 0 ;
    
// }
// int main(void)
// {
//     int i ;
//     for(i=0;i<20;i++)
//     {
//         printf("karekok %d:%f\n",i,sqrt(i)); // karekök fonksiyonuda sqrt fonskiyonu ile çalışır
//     }
//     return 0 ;
// }
#include <stdio.h>
#include <stdlib.h>
#include <math.h>

// int main(void)
// {
//     int number1 , number2;
//     printf("Enter two number : ");
//     scanf("%d %d", &number1, &number2);
//     printf("%d uzeri %d: %.2f\n", number1, number2,pow(number1 ,number2)); // üs alma fonksiyonları

//     return 0 ;
// }
 
// int main(void)
// {
//     double x = 6.20, result;
//     result = cbrt(x);   // küp kök alma fonksiyonu
//     result = ceil(x);   // ondalıklı sayıyı yukarı yuvarlamak için kullanılır
//     result = floor(x);  // ondalıkıl olan sayiyi bir alt sayıya yuvarlar
//     result = fabs(x);   // girilen sayiyinin mutlak değerini verir bize
//     printf("Result:%.2f\n", result);

//     return 0 ;   
// }

// FDİM KODU NASIL ÇALIŞIR

// int main(void)
// {
//     double x=7 , y=19 , z = 3 ,result;
//     result = fabs(x);
//     printf("%.2f ve %.2f sayilarinin farki: %.2f\n",x,y,fdim(x,y));
//     printf("%.2f ve %.2f sayilarinin farki: %.2f\n",x,z,fdim(x,z));
//     /*fdim kodu iki float değeri çıkartır pozitif se aynen söyler negatifse 0 değerine eşitler*/
//     // hypot fonksiyonuda girdiğin sayıların hipotenüslerini alır
//     return 0 ;
// }

// isfinite fonksiyonu

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>
// /*FOnksiyonun amacı sonsuz bir sayı olup olmadığını kontrol etmek 
//   Eğer sonsuz bir sayı değilse 1 sonsuz bir sayıysa 0 değerini döndürür*/

// // isgreater fonksiyonu iki şeyi karşılaştırmak için kullanılır
// int main(void)
// {
//     double x=19,y=0.12,z=7.14/0.00;

//     printf("%.2f degeri sonsuz  bir deger %s\n",x,isfinite(x)? "degildir":"dir");
//     printf("%.2f degeri sonsuz  bir deger %s\n",y,isfinite(y)? "degildir":"dir");
//     printf("%.2f degeri sonsuz  bir deger %s\n",z,isfinite(z)? "degildir":"dir");

//     return 0 ;
// }


// RASTGELE SAYI ÜRETME FONKSİYONU

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     int i , number;
//     srand(time(NULL));  // bu ise her sayiların farklı okunması için yazılan koddur
//     for(i=0;i<10;i++)
//     {
//         number = rand()%10; //%10 un anlamı 0 ile 9 arasında rastgele sayı üretmek anlamına gelir
//         //number = rand();
//         number = rand()%6+1; //buda 1 ile 6 arasında bir sayi verir 
//         printf("%d. rasgele sayi : %d\n", i, number);
//     }
//     return 0 ;
// }

/* Sayı tahmin oyunu*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     int randomNumber, guessNumber,guessCount,score=100;
//     srand(time(NULL));
//     randomNumber = (rand()%100) +1;
//     printf("1 ile 100 arasinda bir sayi tuttum\n");
//     printf("Tahmin et :)\n");

//     while(guessNumber!=1)
//     {
//         printf("Tahmin sayisini giriniz: ");
//         scanf("%d", &guessNumber);
//         if(guessNumber==-1) break;
//         if(guessNumber<1 || guessNumber >100)
//         {
//             printf("i ile 100 arasinda bir sayi gir dedim pezevenk\n");
//             continue;
//         }// if end
//         guessCount++;
//         if(guessNumber==randomNumber){
//             printf("Afferin amk %d. defada sonunda bildin", guessCount);
//             break;}
//         else{
//             if(guessNumber>randomNumber)
//                 printf("Daha kücük bir sayi girmelisin!!!\n");
//             else
//                 printf("Daha büyük bir sayi girmelisin!!!\n");
//             score-=10;
//         }

//     }// while end
//     printf("\n Puanin 100 üzerinden %d\n", score<0 ? 0: score);
//     return 0 ;
// }

/*getchar ve putchar fonksiyonunun kullanımı*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     char myKey;
//     printf("Bir tusa basiniz:");
//     myKey = getchar();  // ekrana bir harf yazdırmak için bu fonksiyonu kullanırız
//     myKey = putchar(54);  // buda o sayinin ascıı kodunu söyler 
//     printf("%c tusuna bastiniz\n", myKey);
//     printf("tusun ASCII kodu : %d\n", myKey);
//     printf("%c tusuna bastiniz\n",&putchar);
//     printf("tusun ASCII kodu : %d\n", myKey);
//     putchar(65);
//     return 0 ;
// }

/*TİP SORGULAMA FONSKİYONLARI*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>
// #include <ctype.h>

// int main(void)
// {
//     int number;
//     printf("Enter a number (0-255): ");
//     scanf("%d",&number);
//     printf("\n the character you entered:%c\n", number);
//     if(isalnum(number)) // A-Z , a-z, 0-9
//                         // isalpha da ise sadece büyük ve küçük harfler vardır
//                         // isdigit ise sadece rakamları ister
//                         // islower sadece küçük harf olup olmadığını kontrol eder
//                         // toupper küçük harfi büyük harfe çevirir
//                         // tolower büyük harfi küçük harfe çevirmektir
//         printf("correct\n");
//     else
//         printf("wrong\n");

//     return 0 ;
    
// }

// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>

// int maximum(int,int,int);
// int main(void)
// {
//     int a,b,c;
//     printf("3 tam sayi giriniz: ");
//     scanf("%d%d%d",&a,&b,&c);
//     printf("Maximum:%d\n",maximum(a,b,c));
//     return 0 ;
// }

// int maximum(int x,int y,int z)
// {
//     int max = x;
//     if(y>max)
//         max =y;
//     if(z>max)
//         max = z;
//     return max;
// }

// #include <stdio.h>
// void bNotu(int vize, int final)
// int main(void)
// {
//     int vize, final;
//     printf("Yil sonu notu hesaplanacak ogrencinin\n");
//     printf("vize ve final notunu giriniz");
//     scanf("%d%d",vize,final);
//     bNotu(vize,final);
//     return 0 ;
// }
// void bNotu(int vize, int final)
// {
//     float ort;
//     ort = vize*0.4 + final*0.6;
//     printf("Basari notu = %2.f\n",ort);
// }


#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>

// void kelimeBirlestir(char c1[], char c2[]);
// int main(void)
// {
//     char kelime1[50],kelime2[50];
//     printf("Lütfen 1. kelimeyi giriniz: ");
//     gets(kelime1);
//     printf("Lütfen 2. kelimeyi giriniz: ");
//     gets(kelime2);
//     kelimeBirlestir(kelime1,kelime2);
//     return 0 ;
// }

// void kelimeBirlestir(char c1[], char c2[])
// {
//     int i,j=0;
//     for(i=strlen(c1);i<strlen(c1) + strlen(c2);i++)//i=4 4<9
//     {
//         c1[i] = c2[j];
//         j++;
//     }
//     printf("\nEkran ciktisi: %s\n",c1);
// }

// int func(int num)
// {
//     int res = 0;
//     if(num<0){
//         printf("\nhata!\n");
//     } 
//     else if(num == 1)
//     return num;
//     else{
//         res = num * func(num-1);
//         return res;
//     }
// }

// int main(void)
// {
//     int num = 5;
//     int fact = func(num);
//     if(fact > 0)
//     printf("\n[%d] in faktöriyeli : [%d]\n",num,fact);
//     return 0 ;
// }

// int Fibonacci(int);

// int main(void)
// {
//     int n,i=0,c;
//     scanf("%d",&n);
//     printf("Fibonacci Sayilari: \n");
//     for(c=1;c<=n;c++){
//         printf("%d\n",Fibonacci(i));
//         i++;
//     }
//     return 0 ;
// }

// int Fibonacci(int n)
// {
//     if(n==0)
//         return 0 ;
//     else if(n == 1)
//         return 1;
//     else
//         return(Fibonacci(n-1)+Fibonacci(n-2));
// }
// int usAlma(int ,int);
// int main(void)
// {
//     int taban = 4;
//     int us = 3;
//     int sonuc;
//     sonuc = usAlma(taban,us);
//     printf("(%d)^%d = %d\n",taban,us,sonuc);
//     return 0 ;
// }

// int usAlma(int taban, int us)
// {
//     if(us==0)
//         return 1;
//     return taban* usAlma(taban,(us-1));
// }

// int carpmaIslemi(int x, int y);
// int main(void)
// {
//     int sayi1 = 15;
//     int sayi2 = 6;
//     int sonuc = carpmaIslemi(sayi1,sayi2);
//     printf("%d * %d = %d\n",sayi1,sayi2,sonuc);
//     return 0 ;
// }

// int carpmaIslemi(int x ,int y)
// {
//     if(y==0)
//         return 0 ;
//     return x + carpmaIslemi(x,(y-1));
// }


// int asalSayi(int,int);
// int main(void)
// {
//     int sayi=29;
//     int sonuc = asalSayi(sayi,sayi/2);
//     if(sonuc == 0)
//         printf("%d asal sayi degildir",sayi);
//     else
//         printf("%d asal sayidir",sayi);
//     return 0 ;
// }

// int asalSayi(int x, int i)//x=29 , i = 29/2
// {
//     if(x<2)
//         return 0;
//     if(i == 1)
//         return 1;
//     if(x%i ==0) 
//         return 0;
//     return asalSayi(x,i-1);
// }
#include <stdio.h>
#include <stdlib.h>
/*toupper = küçük harfleri büyük harfşere döndürme*/
// int main(void)
// {
//     char cumle[100];
//     int i;

//     printf("Lutfen cumleyi giriniz: ");
//     gets(cumle);

//     cumle[0] = toupper(cumle[0]);
//     for(i=0;i<strlen(cumle);i++){
//         if(cumle[i] == ' ')
//             cumle[i+1] = toupper(cumle[i+1]);
//     }
//     printf("\n Duzenlenen Cumle: %s\n",cumle);
//     return 0 ;
// }

/*tersten yazdırma*/
// int main(void)
// {
//     char cumle[100];
//     int i;

//     printf("Lutfen bir cumle giriniz: ");
//     gets(cumle);//10 karakterli bir cümle girdiğimizi varsayalım

//     for(i=strlen(cumle);i>=0;i--){
//         printf("%c",cumle[i]);
//     }
//     return 0 ;
// }


/*Girilen cümlede istediğin harfi bulmak*/
// int main(void)
// {
//     char cumle[100], harf;
//     int i,harf_sayisi = 0,harf_Pozisyon[50];
//     printf("Lutfen cumleyi giriniz: ");
//     gets(cumle);
//     printf("\n");
//     printf("Lutfen aranacak harfi giriniz: ");
//     scanf("%c",&harf);
//     for(i=0;i<=strlen(cumle);i++){
//         if(cumle[i] == harf){
//             harf_Pozisyon[harf_sayisi] = i;
//             harf_sayisi++;
//         }
//     }
//     if(harf_sayisi == 0){
//         printf("aradiginiz harf bunulanamadi...");
//     }
//     else{
//         printf("Toplam bulunan harf sayisi: %d\n",harf_sayisi);
//         for(i=0;i<harf_sayisi;i++){
//             printf("Cumledeki pozisyon: %d\n",harf_Pozisyon[i]);
//         }
//     }
//     return 0 ;
// }


/*srand fonksiyonu*/

// int main(void)
// {
//     int x,i;
//     srand(500);
//     for(i=1;i<=5;i++){
//         x = 1 + rand()%6;
//         printf("%d. sayi =%d\n",i,x);
//     }
//     return 0 ;
// }
#include <stdio.h>
#include <stdlib.h>
#include <string.h>
/*dışarıdan girilen 3 değerin hangisi daha büyüktür*/
// int maximum(int, int ,int);
// int main(void)
// {
//     int a,b,c;
//     printf("3 tam sayi giriniz: ");
//     scanf("%d%d%d",&a,&b,&c);
//     printf("Maximum: %d\n",maximum(a,b,c));
//     return 0 ;
// }

// int maximum(int x, int y, int z)
// {
//     int max = x;
//     if(y>max)
//         max = y;
//     if(z>max)
//         max = z;
//     return max;
// }

/*void değer döndğrmeyen fonksiyonlar*/
// void kare();
// int main()
// {
//     kare();
// return 0 ;
// }
// void kare()
// {
//     int x,karesi;

//     printf("Karesi hesaplanacak sayiyi giriniz: ");
//     scanf("%d",&x);
//     karesi = x*x;
//     printf("%d nin karesi %d\n",x,karesi);
// }

/*iki kelime birleştirme*/

// void Kelime_Birlestir(char c1[], char c2[]);
// int main(void)
// {
//     char kelime1[50], kelime2[50];
//     printf("Lütfen 1. kelimeyi giriniz: ");//4 kelime girdik farzet
//     gets(kelime1);
//     printf("Lütfen 2. kelimeyi giriniz: ");//5 kelime girdik farzet
//     gets(kelime2);

//     Kelime_Birlestir(kelime1,kelime2);
//     return 0 ;
// }

// void Kelime_Birlestir(char c1[], char c2[])
// {
//     int i, j= 0;
//     for(i=strlen(c1); i<strlen(c1) + strlen(c2);i++){
//         c1[i] = c2[j];
//         j++;
//     }
//     printf("\nEkran Ciktisi: %s\n",c1);
// }

/*kutu çizmek*/
// void kutu_ciz(int satir, int sutun);
// int main(void)
// {
//     kutu_ciz(10,30);
//     return 0;
// }

// void kutu_ciz(int satir, int sutun)
// {
//     int j;
//     for(; satir>0; satir--){
//         for(j=sutun;j>0;j--){
//             printf("*");
//             printf("\n");
//         }
//     }
// }


// int Fibonacci(int);
// int main(void)
// {
//     int n, i = 0,c;
//     scanf("%d",&n);
//     printf("\nFibonacci sayilari\n");
//     for(c=1;c<=n;c++){
//         printf("%d\n",Fibonacci(i));
//     i++;
//     }
//     return 0;
// }

// int Fibonacci(int n)
// {
//     if(n==0)
//         return 0 ;
//     else if(n==1)    
//         return 1;
//     else 
//         return (Fibonacci(n-1)+Fibonacci(n-2));
// }

// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>
// #include <math.h>

// int ekok(int a, int b);

// int main(void)
// {
//     int a,b,s;
//     printf("Iki tam sayi giriniz: ");
//     scanf("%d%d",&a,&b);
//     if(a>b)
//     s=ekok(a,b);
//     else
//     s=ekok(b,a);
//     printf("Girilen sayilar icin ekok:%d\n",s);
//     return 0 ;
// }

// int ekok(int a, int b)
// {
//     static int temp= 0;
//     if(temp%b==0 && temp%a==0)
//     return temp;
//     temp++;
//     ekok(a,b);
//     return temp;
// }

// 9- İÇ İÇE FOR

// İÇ İÇE FOR DÖNGÜSÜ

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i , j;

//     for(i=1 ; i<= 4; i++)
//     {

//         for(j=1 ; j<=3 ; j++)
//         {
//             printf("Hello C \n");
//         }
//             printf(".......\n");
//     }
//     return 0 ;

// }


// SORU ÇÖZÜMÜ

//  #include <stdio.h>
//  #include <stdlib.h>

//  int main(void)
//  {
//     int i,j,sharp=0;

//     printf("Enter the number of sharp: ");
//     scanf("%d\n", &sharp);

//      for(i=1; i<=sharp ; i++)
//      {
//         for(j=1; j<=i; j++)
//         {
//             printf("#");
//         }
//             printf("\n");
//      }

//         for(i=1; i<=sharp ; i++)
//      {
//         for(j=sharp; j>=i; j--)
//         {
//             printf("#");
//         }
//             printf("\n");
//      }

//     return 0 ;
//  }

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int number, i=1 ,smallestNumber= 0 , largestNumber = 0;

//     do
//     {
//         printf("Enter the number: ");
//         scanf("%d\n", &number);

//         if(number == 0) break;
//         if(number<smallestNumber) smallestNumber
//     }
// }

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int first ,second, third , i ,number;
//     first = 1;
//     second = 1;
//     third = 1;

//     printf("Enter a number: ");
//     scanf("%d\n", &number);
//     printf("1 1");
//     for(i=1; i<=number ; i++)
//     {
//          first = second;
//          second = third;
//          third = first + second;
//             if(i<=number-2)
//                 printf("%d ", third);
//     }

//     printf("\n\n %d. eleman: %d\n", i-1, first);
//     return 0 ;
// }


    /* 1
       22
       333
       4444 bunun yap */


// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i ,j , number;

//     printf("Enter a number valoue: ");
//     scanf("%d" ,&number);

//     for(i=1; i<=5 ; i++)
//     {
//         for(j=1 ; j<= i ; j++)
//         {
//             printf("%d", i);
//         }
//         printf("\n");
//     }
//     return 0 ;
// }


/*1
  22
  333
  4444
  55555  */

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i , j , number;

//     printf("Enter a number value: ");
//     scanf("%d\n", &number);

//     for(i=1 ; i<=number ; i++)
//     {
//         for(j=1 ; j<= ; j++)
//         {
//             printf("%d", i);
//         }
//     printf("\n");
//     }

//     return 0 ;
// }


// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i , j , number;

//     printf("Enter anumber value: ");
//     scanf("%d", &number);

//     for(i=0; i<3 ; i++)
//     {
//         for(j=1 ; j<=number-i; j++ )
//         {
//             printf("%d", i+1);
//         }
//         printf("\n");
//     }
//     return 0 ;
// }


// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i ,j ,number;

//     printf("Enter a number value: ");
//     scanf("%d\n", &number);

//     for(i=1 ; i<=number ; i++)
//     {
//         for(j=1 ; j<=number; j++)
//         {
//             if(i==1 || i== number || j==1 || j==number)
//             {
//                 printf("* ");
//             }
//             else
//             {
//                 printf("  ");
//             }
//         }
//         printf("\n");
//     }
//     return 0 ;
// }

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int i,j,number;

//     printf("Enter a number value: ");
//     scanf("%d", &number);

//     for(i=1; i<=number; i++)  // satır sayısını belli eder
//     {
//         for(j=1;j<=number-i;j++)
//         {
//             printf("  ");
//         }
//         for(j=1;j<=i*2-1;j++)
//         {
//             printf("* ");
//         }
//         printf("\n");
//     }
//     return 0;
// }


// int main(void)
// {
//     int space , i ,rows;

//     printf("Enter a number of rows: ");
//     scanf("%d", &rows);

//     for(i=0; i<rows ;i++)
//     {
//         for(space=1 ; space<=rows-i; space++)
//         {
//             printf("  ");
//         }
//     printf("7\n");
//     }
//     return 0 ;
// }

#include <stdio.h>
#include <stdlib.h>
#define ORAN 1.609344

// int main()
// {
//     char secim;
//     float mesafe, sonuc;

//     printf("Hangisi? (Mil:M/m veya Kilometre: K/k): ");
//     gets(secim);
//     printf("\n");

//     if((secim=='M')||(secim=='m')){
//         printf("Kac mil yol aldiniz: ");
//         scanf("%f",&mesafe);
//         sonuc =mesafe*ORAN;
//         printf("\n%6.2f Mil = %6.2f Kilometre\n",mesafe,sonuc);
//     }
//     else if{
//         printf("Kac kilometre yol aldiniz: ");
//         scanf("%f",&mesafe);
//         sonuc = mesafe/oran;
//         printf("\n%6.2f Kilometre = %6.2f Mil\n",mesafe,sonuc);
//     }
//     else{
//         printf("Yanlis harf girildi...\n");
//     }
//     return 0 ;
// }



// int main(void)
// {
//     int i=0,j;
//     while(i<5){
//         j = 0;
//         while(j<i+1){
//             printf(" * ");
//             j++;
//         }
//         printf("\n");
//         i++;
//     }
// }

int main(void)
{
    int sayi = 0;
    int n = 0;

    printf("Bir sayi giriniz: ");
    scanf("%d",&sayi);
    printf("\n");
    do{
        n++;
        printf("%d",n);
    }while(n<sayi);
    printf("\n");
    return 0 ;
}

// 10- KOŞULLU İFADELER

// DERS 14...

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int score;
//     printf("Enter a score: ");
//     scanf("%d", &score);

//     if(score > 60)
//     {
//         printf("congratulations you passed the exam\n");
//         printf("your score : %d \n\n", score);
//     }
//     else
//     {
//         printf("unfortunately you did not pass the exam \n\n");
//     }

//     return 0 ;
// }

// KISA YOL LA İF BLOĞU OLUŞTURMAK

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int score;
//     printf("Enter a score");
//     scanf("%d", &score);

//     (score >= 60) ? printf("you passed to exam \n\n") : printf("you failed the exam"); //   koşul doğru ise : dan önceki printf yazdırılır yanlış ise : dan sonraki printf yazdırılır.

//     return 0 ;

// }

/* ÖRNEKLER:
    1 - SORU : kullanıcıdan alınan sayıları karşılaştır
    2 - SORU : Basit bir kitap sipariş ve indirim programı yapalım*/

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     float sayi_1 , sayi_2;
//     printf("Enter a sayi1 , sayi2 : ");
//     scanf("%f %f", &sayi_1 , &sayi_2);

//     if(sayi_1 >sayi_2)
//     {
//         printf("1. sayi 2. sayidan buyuktur ");
//     }
//     else 
//     {
//         printf("2. sayi 1. sayidan buyuktur");
//     }

//     return 0 ;
// }

        // ÖRNEKLER ...

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int bookPrice , orderQuantity; // kitabın fiyatı ve sipariş miktarı    
//     // indirim oranı , indirimsiz fiyat , kitabın indirimli fiyatı, toplam
//     float discountRate , noDiscountPrice , discountPrice , sum;
//     bookPrice = 20;     // kitabın fiyatı
//     orderQuantity = 0;  // sipariş miktarı

//     printf("kac adet siparis etmek istersiniz: ");
//     scanf("%d", &orderQuantity);

//     if(orderQuantity >= 60)
//     {
//         discountPrice = 0.30;
//     }
//     else
//     {
//         if(orderQuantity>= 30 && orderQuantity <60)
//         {
//             discountPrice = 0.20;
//         }
//         else if(orderQuantity >= 10 && orderQuantity < 30)
//         {
//             discountPrice = 0.12;
//         }
//         else 
//         {
//             discountPrice = 0.01;
//         }
//     }
//     noDiscountPrice = orderQuantity * bookPrice;
//     printf("Kitabin indirimsiz fiyati : %f TL", noDiscountPrice);

//     return 0 ;
// }

/* 1- TBMM ' inde  toplantı yeter sayısını sağlanıpsağlanmadığını 
      kontrol eden program
   2- Girilen sayinin tek mi çiftmi olduğunu bulan program */

// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int partyA , partyB , partyC , currentCouncilor;
//     const int sumCouncilor = 600;   // sabiti olduğu yerde atama yapman lazim

//     printf("meslekteki partilerin milletvekili sayilarini giriniz: ");
//     scanf("%d %d %d", &partyA , &partyB , &partyC);

//     currentCouncilor = partyA + partyB + partyC;
    
//     if(currentCouncilor<200)
//     {
//         printf("gerekli toplanti sayisina  ulasilmadi ");
//         printf("toplanti yeter sayisi 200 dur\n");
//     }
//     else 
//     {
//         printf("Meclis toplantiya hazirdir");
//     }

//     return 0 ;
// }

// #include <stdio.h>
// #include <stdlib.h>

            // GİRİLEN SAYİ TEKMİ ÇİFTMİ OLDUĞUNA BAKALIM

// int main(void)
// {   
//     int h;
//     printf("Enter a h: ");
//     scanf("%d", &h);

//     if(h%2 == 0 )
//     {
//         printf("Girdigin sayi cift sayidir");
//     }
//     else 
//     {
//         printf("Girdigin sayi tek sayidir");
//     }

//     return 0 ;
// }


// #include <stdio.h>
// #include <stdlib.h>

// //  Kullanıcıdan alınan  üç sayının en büyüğünü ve en küçüğünü koşullu 
// //  Koşullu ifadelerle tespit eden program

// int main(void)
// {
//     int number1 , number2 , number3 , max , min;
//     printf("Enter a numbers: ");
//     scanf("%d %d %d", &number1 , &number2 , &number3);

//     if(number1 >number2 && number1 >number3)
//     {
//         max = number1;
//     }
//     else if(number2 > number1 && number2 > number3)
//     {
//         max = number2;
//     }
//     else
//     {
//         max = number3;
//     }

//         if(number1 < number2 && number1 < number3)
//     {
//         min = number1;
//     }
//     else if(number2 < number1 && number2 < number3)
//     {
//         min = number2;
//     }
//     else
//     {
//         min = number3;
//     }

//     printf("girdigin max deger : %d\n", max);
//     printf("girdigin min deger : %d\n", min);

//     return 0 ;
// }

// #include <stdio.h>
// #include <stdlib.h>

//     // Kenar uzunluklari girilen üçgenin hangi tür üçgen olduğunu bul?

// int main(void)
// {
//     int a , b , c;
//     char en_uzun_kenar;

//     printf("Ucgenin kenar uzunluklarini giriniz: ");
//     scanf("%d %d %d", &a , &b ,&c);

//     if(a > b && a >c)
//     {
//         en_uzun_kenar = 'a';
//     }
//     else if(b>a && b>c)
//     {
//         en_uzun_kenar = 'b';
//     }
//     else
//     {
//         en_uzun_kenar = 'c';
//     }
     
//     // ---------------------------

//     if(en_uzun_kenar == 'a')
//     {
//         if(a*a == b*b + c*c)
//         {
//             printf("Dik acili ücgen");
//         }
//         else if(a*a > b*b + c*c)
//         {
//             printf("Genis acili ücgen");
//         }
//         else if(a*a < b*b + c*c)
//         {
//             printf("Dar acili ücgen");
//         }
//         else
//         {
//             printf("Girdigin degerde ücgen tanimli degil");
//         }
//     }
//     // -------------------------
//     else if(en_uzun_kenar == 'b')
//     {
//                 if(b*b == a*a + c*c)
//         {
//             printf("Dik acili ücgen");
//         }
//         else if(b*b > a*a + c*c)
//         {
//             printf("Genis acili ücgen");
//         }
//         else if(b*b < a*a + c*c)
//         {
//             printf("Dar acili ücgen");
//         }
//         else
//         {
//             printf("Girdigin degerde ücgen tanimli degil");
//         }
//     }
//     // -------------------

//     else if(en_uzun_kenar == 'c')
//     {
//         if(c*c > a*a + b*b)
//         {
//             printf("Girdigin ücgen genis acili ücgendir");
//         }
//         else if(c*c == a*a + b*b)
//         {
//             printf("Dik acili bir ücgendir");
//         }
//         else if(c*c < a*a + b*b)
//         {
//             printf("Girdigin ücgen dar acili ücgendir");
//         }
//         else
//         {
//             printf("Girdigin degerlerle ücgen olusturulmaz");
//         }
//     }   

//     return 0 ;
// }


// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int number , newnumber , part1 , part2 ;
//     printf("Enter a number: ");
//     scanf("%d", &number);

//     //abcd
//     part1 = number / 100;
//     part2 = number % 100;
//     newnumber = (part1 + part2) * (part1 + part2);

//     if(newnumber == number)
//     {
//         printf("%d aradigimiz sayi ozel sayidir", newnumber);
//     }
//     else
//     {
//         printf("%d aradigimiz sayi ozel sayi değildir hatta hiç bisey degildir",newnumber);
//     }

//     return 0;
// }

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     int number , squarteRoot ; 

//     printf("Enter a number: ");
//     scanf("%ld",&number );

//     if(number < 0 )
//     {
//         printf("plase do not do this...");
//     }
//     else 
//     {
//         squarteRoot = sqrt(number);
//         if(squarteRoot * squarteRoot == number)
//         {
//             printf("square root of %d is an integer\n", squarteRoot);
//         }
//         else
//         {
//             printf("No it is not \n");
//         }
//     }
    

//     return 0 ;

// }


/*SORU : Bir gsm operatörü  4 dk kadar konuşma ücretini 0.30 tl olarak belirlemiştir
     ancak konuşma süresi  4 dakikayı aşarsa bundan sonraki her dakika için  ek olarak  0.07 tl  almaktadır
     telefon görüşmesinin süresini dakika cinsinden girdi olarak alan ve konuşmasını ücretini hesaplayanC programını oluşturlaım*/ 


// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     float talkTime , fee;

//     printf("Enter a talkTime : ");
//     scanf("%f", & talkTime);

//     if(talkTime <= 4)
//     {
//         fee = 0.30;
//     }
//     else 
//     {
//         fee = 0.30 + (talkTime - 4)*0.07;
//     }

//     printf("odedigin ucret : %f", fee);

//     return 0 ;
// }

/* bir üçgenin açılarını girdi olarak alan ve bu üçgenin  eş kenar ikiz kenar  veya çeşit kenar ğçgen olup
    olmadığında bak*/

#include <stdio.h>
#include <stdlib.h>

int main(void)
{
    int aci_1 , aci_2 , aci_3;

    printf("Lutfen aci degerlerini giriniz : ");
    scanf("%d %d %d", &aci_1 , & aci_2 , &aci_3);

    if(aci_1 + aci_2 + aci_3 != 180)
    {
        printf("Bu degerlerle ucgen olusturulmaz...");
    }

    else if(aci_1 == aci_2 == aci_3)
    {
        printf("Bu ucgen es kenar ucgendir...");
    }
    else if(aci_1 == aci_2 || aci_2 == aci_3)
    {
        printf("Bu ucgen ikiz kenar ucgendir");
    }
    else
    {
        printf("Bu ucgen cesit kenar ucgendir...");
    }

    return 0 ;
}

// 11- POİNTER KULLANIMI

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// // int main(void)
// // {
// //     char name = 'F'; // 1 byte
// //     int x = 7; // 4 byte
// //     printf("%c", name);

// //     return 0 ;
// // }

// /* Bellekten adres okuma */
// int main(void)
// {
//     int x = 7;
//     float y = 3.14;
//     double z=4.23456;
//     char name='F';

//     printf("x variable:%d\n",x);
//     printf("y variable:%f\n",y);
//     printf("z variable:%f\n",z);
//     printf("name variable:%c\n\n", name);

//     printf("x variable address:%x\n",&x);/*Adres öğrenmek için printf in içine & işaretini koymamız lazım!!!*/
//     printf("y variable address:%x\n",&y);
//     printf("z variable address:%x\n",&z);
//     printf("name variable address:%x\n\n",&name);
    
//     return 0 ;
// }

/* POİNTER TANIMLAMASI*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     int x = 7;      /*pointerlerin türleri yoktur*/
//     int* ptr= &x;   /*pointerler böyle yıldız ile tanımlanır pointerler sadece bellek adresini tutarlar*/
//     printf("x:%d\n",x);
//     printf("x variable address:%x\n",&x); // x in adresini öğrenmek için & koyduk
//     printf("x variable address:%x\n", ptr);
//     printf("ptr variable address:%x\n",&ptr);//burdada ptr nin adresini bulak için & bu işareti koyduk
//     printf("x variable:%d\n",*ptr);//* ise o adresdeki değeri getirmeni sağlar                

//     return 0 ;
// }

/*POİNTERLERİN KULLANIMI*/

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     int x=7;
//     int* ptr;
//     ptr = &x;
//     printf("x variables %d\n", x);
//     *ptr=19; // x değişkenini kullanmadan x değerini değiştirdik
//     printf("x variables new value %d\n",x);
//     /*NOT: birden fazla pointer tek bir adresi aynı anda alabilir*/
//     return 0 ;
// }

/*POİNTERLERDE DEĞER ARTIRMA (UZMANLIK İŞİ)*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     char name='f';
//     double y=3.109;
//     int x = 7;

//     char* nameptr=&name;
//     double* yptr=&y;
//     int* xptr=&x;

//     printf("First adress: \n\n");

//     printf("name's firts adress:%x\t value:%c\n",nameptr,*nameptr);
//     printf("y's first adress: %x\t value: %f\n",yptr,*yptr);
//     printf("x's first adress: %x\t value: %d\n\n",xptr ,*xptr);// *xptr o bayttaki değeri sana verir

//     nameptr++;  // 1 byte
//     yptr+=4;    // 32 byte
//     xptr-=3;    // 12 byte
    
//     printf("next adress : \n\n");   // adres değiştirdik 
//     // ama bilmediğimiz bir şeyi değiştirirsek kodumuzu mahvetmil oluruz
//     printf("name 's next adress:%x\t value%c\n",nameptr,*nameptr);
//     printf("y's next adress: %x\t value%f\n", yptr,*yptr);
//     printf("x's next adress: %x\t value%d\n", xptr,*xptr);

//     return 0 ;
// }


/*POİNTERLER İLE FONKSİYOLARI KULLANMA*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// double getSquare(double *ptr);

// int main(void)
// {
//     double number, result;

//     printf("Enter a number: ");
//     scanf("%d",&number);

//     result = getSquare(&number);

//     printf("Square of number %.2f\n\n", result);

//     return 0 ;
// }

// double getSquare(double *ptr)
// {
//     return  *ptr  *  *ptr;
// }

/*BİR FONKSİYON İLE ADRES GÖNDERME*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// float* squareRoot(float* ptr); // karekök alma fonksiyonu

// int main(void)
// {
//     float number;
//     float* ptr; // number in türüne göre yazıyoruz

//     printf("Enter the number: ");
//     scanf("%d",&number);

//     ptr=squareRoot(&number);    // adres gönderiyoruz
//     printf("Square root of number: %.2f\n\n", *ptr);
//     return 0 ;
// }

// float* squareRoot(float* ptr)
// {
//     *ptr = sqrt(*ptr);
//     return ptr;
// }

/*POİNTERLER İLE ARRAYLAR*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     char myLitters[7] = {'a','b','c','d','e','f','h'};
//     // bir arrayın ismi o arrayın ilk elemanının bellek adresini tutar !!!

//     printf("Ilk elemanin adresi: %x\n",&myLitters[0]);//& bu işaret o elemanın adresini söyler
//     printf("Ilk elemanin adresi: %x\n", myLitters);
//     // dizinin adresini iki şekildede alabiliriz
//     printf("ikinci elemanin adresi: %x\n",&myLitters[1]);
//     printf("ikinci elemanin adresi: %x\n", myLitters);

//     printf("ücüncü elemanin adresi: %x\n",&myLitters[2]);
//     printf("ücüncü elemanin adresi: %x\n", myLitters);
//     // Dizinin değerini iki şekilde alabiliriz
//     printf("Ilk elemanin degeri:%c\n",myLitters[0]);//iki farklı şekildede alabiliriz
//     printf("Ilk elemanin degeri:%c\n",*myLitters);

//     printf("Ikinci elemanin degeri:%c\n", myLitters[1]);
//     printf("Ikinci elemanin degeri:%c\n",*(myLitters+1));
//     return 0 ;
// }

/*POİNTERLERİ DÖNGÜLERDE KULLANMAK*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// int main(void)
// {
//     char myLetter[5] = {'x','y','z','a','f'};
//     int myNumbers[5] = {7,1,19,23,5};
//     int i;

//     printf("MY LETTER\n");
//     printf("-----------\n");
//     for(i=0;i<5;i++)
//     {
//         printf("myLetter[%d]:%c\n",i,*(myLetter+i));//*(myLetter+i) o adresteki değeri verir
//     }

//     printf("myNumbers Array\n");
//     printf("----------------\n");
//     for(i=0;i<5;i++)
//     {
//         printf("myNumbers[%d]:%d\n",i,*(myNumbers+i));
//     }
//     // adresler arraylerde yan yana dizilir diğerleri gibi rastgele değil
//     return 0 ;
// }

/*DİZİ FONKSİYON ÖRNEKLERİ*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// void myArray(int*);// fonksiyonu burda tanımladık

// int main(void)
// {
//     int numbers[6]={15,32,6,7,14,31};
//     int i ;
//     int size,array;
//     size = sizeof(numbers)/sizeof(numbers[0]); //numberın kaç elemanlı olduğunu buluyor
//     printf("Önceki durum\n");
//     printf("---------------\n");
//     for(i=0;i<size;i++){// ilerleyen zamanda karakter sayısı değişebilceği için 6 yerine size yazmak daha iyi
//         printf("Number[%d]:%d\n",i,numbers[i]);
//     }
//     myArray(numbers);
//     printf("\nSonraki durum\n");
//     for(i=0;i<size;i++){
//         printf("Number[%d]:%d\n",i,numbers[i]);
//     }
//     array = sizeof(numbers[0]);
//     printf("sizeof: %d",array);
//     return 0 ;

// }

// void myArray(int* numbers)  // tanımlamayı unutma
// {
//     int j=0;
//     for(j=0;j<6;j++){
//         *(numbers+j)*=3;
//     }
// }

// /*örnek*/
// // #include <stdio.h>
// // #include <stdlib.h>
// // #include <math.h>

// // void characterScroll(char* , int); //burda tam tanımlamaya gerek yok
// // int main(void)
// // {
// //     char characters[] = {'H','a','s','a','n'};
// //     int size = sizeof(characters)/sizeof(characters[0]);
// //     characterScroll(characters,size);
// //     return 0 ;
// // }

// // void characterScroll(char* characters, int size)
// // {
// //     int i=0,j=0;
// //     for(i=0;i<size+1;i++){
// //         for(j=i;j<size;j++){//0123456  1234560 2345601
// //             printf("%c", *(characters +j));
// //         }
// //         for(j=0;j<i;j++){// 0 01 012 0123 01234
// //             printf("%c",*(characters + j));
// //         }
// //         printf("\n");
// //     }
// // }



// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>

// int main(void)
// {
//     int *p;
//     int **pp;
//     int val=1903;
//     //p işaretcisine val değeri atanıyor
//     p = &val;
//     // pp işaretcisine p işaretcisinin adresi atanıyor
//     pp = &p;

//     printf("Degerler:\n*************\n");
//     printf("val = %d\n",val);
//     printf("*p = %d\n",*p);
//     printf("**pp = %d\n",**pp);
//     printf("Adresler:\n************\n");
//     printf("&val = %d\n",&val);
//     printf("p = %d\n",p);
//     printf("&p = %d\n",&p);
//     printf("pp = %d\n",pp);

//     return 0 ;
// }


#include <stdio.h>
#include <stdlib.h>

//int main(void)
// {
//     char *pk,k='a';
//     int *pt,t = 22;
//     double *pg,g=5.5;
     
//     pk = &k;
//     pt = &t;
//     pg = &g;

//     printf("Onceki adresler: pk = %p pt = %p pg \n= %p",pk,pt,pg);
//     printf("Onceki degerler: *pk = %c *pt = %d pg \n= %f\n\n",*pk,*pt,*pg);

//     pk++;
//     pt--;
//     pg= pg+10;

//     printf("Sonraki adresler: pk = %p pt = %p pg \n= %p",pk,pt,pg);
//     printf("Sonraki degerler: *pk = %c *pt = %d pg \n= %f\n\n",*pk,*pt,*pg);

//     return 0 ;
// }


// int main(void)
// {
//     int i;
//     int b[] = {10,20,30,40};

//     int *pb = b;

//     printf("YONTEM 1 : DIZI INDISLERI\n");
//     for(i=0;i<=3;i++){
//         printf("b[%d]:\t%d\n",i,b[i]);
//     }

//     printf("\nYONTEM 2: ISARETCI OFFSET\n");
//     for(i=0;i<=3;i++){
//         printf("*(pb+ %d):\t%d\n",i,*pb+i);
//     }

//     printf("\nYONTEM 3: DIZI/ISARETCI OFFEST\n");
//     for(i=0;i<=3;i++){
//         printf("*(b+%d):\t%d\n",i,*(b+i));
//     }

//     return 0 ;
// }


// int main(void)
// {
//     int *ip;
//     int idizi[5] = {6,20,30,65,95};
//     printf("isaretci bellek adresi: %p\n\n",&ip);
//     ip = &idizi[4];
//     printf("isaretcinin icerdigi adres:%p\n",ip);
//     printf("isaretcinin gosterdigi degisken degeri:%d\n\n",*ip);
//     ip-=2;//ip-=(4*sizeof(int));
//     printf("isaretcinin icerdigi adres :%p\n",ip);
//     printf("isaretcinin gosterdigi degisken degeri:%d\n\",*ip);
// }

#include <string.h>
#include <ctype.h>
#include <stdlib.h>
#include <stdio.h>

// int main(void)
// {
//     int *p;
//     p = NULL;

//     printf("\n p isaretcisinin adresi = %p\n\n",p);
//     if(p){
//         printf("p isaretcisi  NULL degil\n");
//     }
//     else
//         printf("p isaretcisi NULL dur");
//     return 0 ;
// }


// int main(void)
// {
//     int *p;
//     int **pp;
//     int val = 1903;

//     //p işaretcisine val adresi atanıyor
//     p = &val;
//     //pp işaretcisine p işaretcisinin adresi atanıyor
//     pp = &p;
    
//     printf("Degerler: \n******\n");
//     printf("val = %d \n",val);
//     printf("*p = %d\n",*p);
//     printf("**pp = %d\n",**pp);
//     printf("Adresler\n**********\n");
//     printf("&val = %p\n",&val);
//     printf("p = %p\n",p);
//     printf("&p = %p\n",&p);
//     printf("pp = %p\n",pp);

//     return 0 ;
// }

/*pointerlerde arttıram işlemi değerin cinsine bağlıdır
    eğer int ise = 4 artar
    eğer char ise = 1 artar
    eğer doubel ise = 8 artar*/
// int main(void)
// {
//     int *ip;
//     int idizi[5] = {6,20,30,65,95};
//     printf("isaretci bellek adresi: %p\n\n",&ip);
//     ip = &idizi[4];
//     printf("isaretcinin icerdigi adres: %p\n\n",ip);
//     printf("isaretcinin gosterdigi degsiken degeri: %d\n\n",*ip);
//     ip-=2;//ip-=(4*sizeof(int))
//     printf("isaretcinin icerdigi adres:&p\n",ip);
//     printf("isaretcinin gosterdigi degisken degeri: %d\n\n",*ip);
//     return 0 ;
// }    

// int main(void)
// {
//     char s[80],*p;
//     p = &s[0];
//     printf("Kucuk harfleri kullanarak bir kelime giriniz: ");
//     gets(s);
//     while(*p){//*p == 0 olana kadar çalışmasını sağlar
//         printf("%c",toupper(*p++));
// //     }
// // }

// int* MinSayiBul(int a[],int boyut);

// int main(void)
// {
//     int a[5] = {4,7,-3,-5,9};
//     int *p,k;
//     //indis dizi ve adresini ekrana bas
//     for(k=0;k<5;k++){
//         printf("%d\t%d\t%p\n",k,a[k],&a[k]);
//     }
//     p = MinSayiBul(a,5);
//     printf("\n En kucuk deger: %d\n",*p);
//     printf("\nEn kucun adres: %p\n",p);
//     return 0 ;
// }

// int* MinSayiBul(int a[],int boyut)
// {
//     int i;
//     int ek, *pek;
//     ek = a[0];
//     for(i=1;i<boyut;i++){
//         if(*(a+i)<ek){
//             ek = *(a+i);
//             pek= (a+i);
//         }
//     }
//     return pek;
// }

// 12- STRUCT KULLANIMI

// // struct'larda birden fazla variable kullanabiliriz
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// struct students{// students kendi oluşturduğum bir veri yani int gibi
//     char myLetter;
//     char* name;
//     char* lastname;
//     int no;
//     float score;
//     char parentName[40];
// };

// int main(void)
// {

//     // Atamayı tek satırdada halledebiliriz
//     struct students x={'A',"Murat","Bastug",1923,95.6,"Ahmet"}; //sttudents int gibi bir veri x te variable'dir
    
//     //NOT:  X2 = X diyerek struct ları kopyalayabilirz
//     // x.myLetter = 'A';   // atama yaparkende nokta koyarak atama yapılır
//     // x.name = "Murat";
//     // x.lastname = "Bastug";
//     // x.no = 1923;
//     // x.score = 95.6;
//     // strcpy(x.parentName,"Yarrak");

// /*Struct'ları yazdırmak */
//     printf("Letter: %c\n",x.myLetter);
//     printf("Name: %s\n",x.name);
//     printf("lastname: %s\n",x.lastname);
//     printf("no: %d\n",x.no);
//     printf("score: %.2f\n",x.score);
//     printf("parentName: %s\n", x.parentName);

//     printf("-----------------------\n");



//     return 0 ;
// }


// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// struct Car{
//     char brand[60];
//     char model[60];
//     int year;
// };

// int main(void)
// {
//     struct Car c1 = {"Opel","Corsa",1990};
//     struct Car c2 = {"Ford","Focus",1999};
//     struct Car c3 = {"BMW","X5",1998};

//     printf("%s %s %d\n",c1.brand,c1.model,c1.year);
//     printf("%s %s %d\n",c2.brand,c2.model,c2.year);
//     printf("%s %s %d\n",c3.brand,c3.model,c3.year);
// }

/*UYGULAMA*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// struct myDate{
//     int day;
//     int month;
//     int year;
// };

// int main(void)
// {
//     struct myDate x;
//     struct myDate y;

//     printf("Enter your date of birth: ");
//     scanf("%d%d%d", &x.day,&x.month,&x.year);

//     printf("Enter today's date: ");
//     scanf("%d%d%d",&y.day,&y.month,&y.year);

//     if(x.day>y.day)
//     {
//         y.day+=30;
//         y.month-=1;
//     }
//     if(x.month>y.month)
//     {
//         y.month+=12;
//         y.year-=1;
//     }

//     printf("\n You have lived\n");
//     printf("%d day , %d month, %d year\n",y.day-x.day,y.month-x.month,y.year-x.year);
//     printf("till now \n\n");

//     return 0 ;
// }

/*Struct'lerin dizilerde kullanımı*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// struct books{
//     char bookname;
//     char writer;
//     int page;
//     int year;
// };

// int main(void)
// {
//     int i; //döngüde sayaç için
//     struct books x[2];//2 tane kullanmak manasına gelir

//     //kullanımı
//     x[0].bookname="Harry Potter ve Felsefe Tasi";
//     x[0].writer = "J.K Rowling";
//     x[0].page = 238;
//     x[0].year = 1960;

//     x[1].bookname ="Bu ulke";
//     x[1].writer = "Cemil meric";
//     x[1].page = 245;
//     x[1].year = 1960;

//     for(i=0;i<2;i++)
//     {
//         printf("%d. book\n",i+1);
//         printf("Book name: %s\n", x[i].bookname);
//         printf("write :%s\n",x[i].writer);
//         printf("page: %d\n",x[i].page);
//         printf("year: %d\n", x[i].year);
//     }

//     return 0 ;
// }


/*Struct yi fonksiyonlarla nasıl kullanılır*/

// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// struct info{
//     char* name;
//     int age;
// };
// void showMe(struct info );// böyle belirtmek zorundayız
// int main(void)
// {
//     struct info x;
//     x.name="Faik";
//     x.age = 19;

//     showMe(x);

//     return 0 ;
// }
// void showMe(struct info x)
// {
//     printf("Name : %s\n", x.name);
//     printf("Age: %d\n", x.age);
// }


/*struct'lerin pointerlerle kullanımı*/
// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>

// struct books{
//     char* bookname;
//     char* writer;
//     int page;
//     int year;
// };

// int main(void)
// {
//     struct books x;
//     struct books* y;
//     y = &x;
//     (*y).bookname="Bu Ulke";
//     (*y).writer = "Cemil Meric";
//     (*y).page = 256;
//     (*y).year = 1960;

//     printf("Book name: %s\n",(*y).bookname);
// //     printf("Writer : %s\n", (*y).writer);
// //     printf("page: %d\n", (*y).page);
// //     printf("year: %d\n",(*y).year);

// //     return 0 ;
// // }


// /*iç içe struct'lar*/
// // #include <stdio.h>
// // #include <stdlib.h>
// // #include <math.h>

// // struct candidateInfo{
// //     char* name;
// //     char* lastname;
// //     int age;
// //     int note;
// //     float avarege;
// // };
// // struct interview{
// //     char* interviewer;
// //     char* interviewDate;
// //     struct candidateInfo candidate;
// //     int interviewNote;
// // };

// // int main(void)
// // {
// //     struct interview y;
// //     y.interviewer = "Muslume gun";
// //     y.interviewDate = "25.05.2009";
// //     y.interviewNote = 85  ;

// //     // iç içe struct'ları böyle alırız
// //     y.candidate.name = "yarak";
// //     y.candidate.lastname = "kafali";
// //     y.candidate.age = 18;
// //     y.candidate.note = 80;
// //     y.candidate.avarege = 2.69;

// //     return 0 ;
// // }

// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>
//  struct Ogrenci
//  {
//     int No;
//     char Ad[50];
//     char Soyad[50];
//     int Cinsiyet;
//     int FakulteBolum;
//     float GenelOrtalama;
//  };
//  int main(void)
//  {
//     struct Ogrenci ogrenci_bilgisi1,ogrenci_bilgisi2;

//     ogrenci_bilgisi1.No =1;
//     strcpy(ogrenci_bilgisi1.Ad,"Ada");
//     strcpy(ogrenci_bilgisi1.Soyad,"KILINC");
//     ogrenci_bilgisi1.FakulteBolum = 11;
//     ogrenci_bilgisi1.GenelOrtalama = 4.5;

//     ogrenci_bilgisi2 = ogrenci_bilgisi1;
//     printf("1. OgreciNo: %d\n",ogrenci_bilgisi1.No);
//     printf("2. OgrenciNo: %d\n",ogrenci_bilgisi2.No);

//     return 0 ;

//  }


// #include <stdio.h>
// #include <stdlib.h>
// #include <string.h>

// void fonk1(char cd);
// void fonk2(char cd1);
// int main(void)
// {
//     char cd1 = 87;/*'W' 01010111*/
//     char cd2;
//     printf("Karakter Degeri: %d %d",cd1,cd1);

// fonk1(cd1);
// cd2 = fonk2(cd1);

// printf("Karakter degeri: %c %d",cd2,cd2);/*'u' 01110101*/
// fonk1(cd2);
// return 0 ;

// void fonk1(char cd)
// {
//     int id;
//         for(id=128;id>0;id/=2){
//             if(cd&id) printf("1");
//         }
//         else printf("0");
//         printf("\n");
// }
// char fonk2(char cd1)
// {
//     struct yap1{
//         char cd1:4;
//         char cd2:4;
//     };
//     union bir1{
//         char cd1;
//         struct yap1 yd1;
//     }bd1;
    
//     char cd2;
//     bd1.cd1 = cd1; //1
//     cd2 = bd1.yd1.cd1; //2
//     bd1.yd1.cd1 = bd1.yd1.cd2; //3
//     bd1.yd1.cd2 = cd2; //4
//     return bd1.cd1;
// }
// }


// #include <stdio.h>
// #include <stdlib.h>

// int main(void)
// {
//     int tam = 33;
//     int *ptam;

//     ptam = &tam;

//     printf("tam icerik = \t %d \n ",tam);
//     printf("tam adres = \t %p \n", &tam);
//     printf("tam adres = \t %d \n",*ptam); //tam ın adrsini kaydeder

//     return 0 ;
// }

#include <stdio.h>
#include <stdlib.h>
// struct deneme{
//     int yas;
//     char ad;
// }mn;
// struct deneme fonk(void);
// int main(void)
// {
//     mn = fonk();
//     printf("yas: %d\n ad:%c\n",mn.yas,mn.ad);
//     return 0 ;
// }

// struct deneme fonk(void)
// {
//     struct deneme mn;
//     mn.yas = 21;
//     mn.ad = 'A';
//     return mn;
// }

// struct yap{
//     int id;
//     char cd;
// }yd;
// void fonk(struct yap yd);
// int main(void)
// {
//     struct yap yd;
//     yd.id = 21;
//     yd.cd = 'A';
//     fonk(yd);
//     printf("%d %c",yd.id,yd.cd);
//     return 0 ;
// }
// void fonk(struct yap yd)
// {
//     yd.id+=5;
//     yd.cd+=5;
//     printf("%d %c\n",yd.id,yd.cd);
// }


// #include <stdio.h>
// #include <stdlib.h>
// #include <math.h>
// #include <string.h>

// struct yap2{
//     char cdizi[30];
// };
// struct yap1{
//     char cdizi1[15];
//     char cdizi2[15];
//     int id;
//     struct yap2 yd2;
// }yd1;

// int main(void)
// {
//     strcpy(yd1.cdizi1,"Algoritma ve");
//     strcpy(yd1.cdizi2,"Programlama 2");
//     yd1.id=35;
//     strcpy(yd1.yd2.cdizi,"Manisa Celal bayar üniversitesi");
//     printf("%s%s%d\n",yd1.cdizi1,yd1.cdizi2,yd1.id);//yazdırma
// }

#include <stdio.h>
#include <stdlib.h>
#include <string.h>
#include <math.h>
// // struct deneme
// // {
// //     int yas;
// //     char ad;
// // }mn;

// // int main(void)
// // {
// //     printf("deneme yapisinin uzunlugu: %d\n",sizeof(struct deneme));
// //     printf("deneme yapisinin uzulugu:%d\n",sizeof(sizeof (mn)));
// // }



// struct Ogrenci
// {
//     int no;
//     char Ad[50];
//     char Soyad[50];
//     int Cinsiyet;
//     int FakulteBolum;
//     float genelOrtalama;
// };

// void OgrenciBilgisiYazdirma(struct Ogrenci ogr)
// {
//     printf("No:%d\n Ad:%s\n",ogr.no,ogr.Ad);
// }

// int main(void)
// {
//     struct Ogrenci ogrenci_test;
//     ogrenci_test.no = 1000;
//     strcpy(ogrenci_test.Ad,"test");
//     OgrenciBilgisiYazdirma(ogrenci_test);
//     return 0 ;
// }


// typedef struct
// {
//     char plaka[50];
//     char Model[50];
//     char Renk[50];
// }AracOzellik;
// typedef struct
// {
//     AracOzellik Ozellikler;
//     char girisSaati[12];
// }Arac;
// typedef struct
// {
//     Arac Araclar[1000];
//     int arac_sayisi;
// }Otopark;
// Otopark BaharOtopark = {0};
// int main(void)
// {
//     AracEkle();
//     AracEkle();
//     Araclari_Listele();
//     return 0 ;
// }
// void AracEkle()
// {
//     Arac arc;
//     printf("\nArac bilginizi giriniz:\n");
//     printf("Plaka:");
//     gets(arc.Ozellikler.plaka);
// }


// struct Ogrenci
// {
//     int No;
//     char Ad[50];
//     char Soyad[50];
//     int Cinsiyet;
//     int FakulteBolum;
//     float GenelOrtalama;
// };

// int main(void)
// {
//     struct Ogrenci ogrenci_bilgisi1,ogrenci_bilgisi2;

//     ogrenci_bilgisi1.No = 1;
//     strcpy(ogrenci_bilgisi1.Ad,"Ada");
//     strcpy(ogrenci_bilgisi1.Soyad,"Kilinc");
//     ogrenci_bilgisi1.FakulteBolum = 11;
//     ogrenci_bilgisi1.GenelOrtalama = 4.5;

//     ogrenci_bilgisi2 = ogrenci_bilgisi1;

//     printf("1. OgrenciNo: %d\n",ogrenci_bilgisi1.No);
//     printf("2. OgrenciN: %d\n",ogrenci_bilgisi2);
//     return 0 ;
// }


// struct yap2{
//     char cdizi[30];
// };
// struct yap1{
//     char cdizi1[15];
//     char cdizi2[15];
//     int id;
//     struct yap2 yd2;
// }yd1;
// int main(void)
// {
//     strcpy(yd1.cdizi1,"Algoritma ve");
//     strcpy(yd1.cdizi2,"Programlama");
//     yd1.id=35;
//     strcpy(yd1.yd2.cdizi,"Manisa celal bayar üniversitesi");
//     printf("%s%s%d\n",yd1.cdizi1,yd1.cdizi2,yd1.id);
//     printf("%s",yd1.yd2.cdizi);
//     return 0;
// }

// struct daire
// {   char ad[20];
//     struct birim
//     {
//         char ad[20];
//         struct personel
//         {
//             char soyad[20];
//             char ad[20];
//             int sicilNo;
//             int derece;
//         }baskan,sef,memur[10];
//     }altbirim[15];
// }m;

// int main(void)
// {
//     m.altbirim[7].sef.sicilNo = 2457;
//     printf("%d\n",m.altbirim[7].sef.sicilNo);
// }


// struct Ogrenci
// {
//     int No;
//     char Ad[50];
//     char Soyad[50];
//     int Cinsiyet;
//     int FakulteBolum;
//     float GenelOrtalama;
// };
// void OgrenciBilgisiYazdir(struct Ogrenci ogr)
// {   
//     printf8("No: %d\n Ad: %s\n",ogr.No,ogr.Ad);
// }
// int main(void)
// {
//     struct Ogrenci ogrenci_test;
//     ogrenci_test.No = 1000;
//     strcpy(ogrenci_test.Ad,"test");
//     OgrenciBilgisiYazdir(ogrenci_test);
//     return 0 ;
// }

// #include <stdio.h>
// #include <stdlib.h>
// typedef struct
// {
//     char plaka[50];
//     char model[50];
//     char renk[50];
// }AracOzellik;
// typedef struct
// {
//     AracOzellik Ozellikler;
//     char girisSaati[12];
// }Arac;
// typedef struct
// {
//     Arac Araclar[1000];
//     int aracSayisi;
// }Otopark;
// Otopark BaharOtoPark = {0};
// int main(void)
// {
//     AracEkle();
//     AracEkle();
//     AracListele();
//     return 0 ;
// }
// void AracEkle()
// {
//     Arac arc;
//     printf("\nArac bilgilerini giriniz: \n");
//     printf("\nplaka");
//     gets(arc.Ozellikler.plaka);
//     printf("\nModel: ");
//     gets(arc.Ozellikler.model);
//     printf("\nRenk");
//     gets(arc.Ozellikler.renk);
//     printf("Giris saati: ");
//     gets(arc.girisSaati);
//     BaharOtoPark.Araclar[BaharOtoPark.aracSayisi] = arc;
//     BaharOtoPark.aracSayisi++;
// }





