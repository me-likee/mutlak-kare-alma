# mutlak-kare-alma
// Ekrandan girilen n tane sayının 67'den küçük yada büyük olduğuna bakan. Küçük olanların farklarının toplamını, büyük ise de farkların mutlak karelerini alarak toplayıp ekrana yazdıran console uygulamasını yazınız.

// Örnek: Input: 56 45 68 77

// Output: 33 101

string sayi=Console.ReadLine();
string[] number = sayi.Split(" ");
int fark=0;
int farktoplam=0;
double toplam=0;
for (int i = 0; i < number.Length; i++)
{
    if(int.Parse(number[i])<67)
    {
      fark=67-int.Parse(number[i]);  
      farktoplam+=fark;
    }
    else
    {
        fark=67-int.Parse(number[i]);
        toplam+=Math.Pow(Math.Abs(fark),2); 
    }
}


    Console.Write(" "+farktoplam);
    Console.Write(" "+toplam);
