# Program-C_TLS21
Angelica Callysta Viera_FoxPro

<!-- Calculating Gender Based Ideal Weight Program -->

#include <iostream>
#define CENTI_TO_METER 0.01

using namespace std;

int main()
{
    int gender, beratBadan, tinggiBadan;
    float tinggiBadanM, tinggiBadanKuadrat, bodyMassIndex, perlibelTinggi, persepuluhTinggi, beratIdealCe, beratIdealCo;
    
    cout<<"Hidup sehat dengan berat badan ideal\n\n";
    cout<<"Apakah gender anda? (tulis 1 untuk perempuan dan 0 untuk laki-laki : ";
    cin >> gender;
    cout<<"Berapa berat badan anda? : ";
    cin >> beratBadan;
    cout<<"Berapa tinggi badan anda? (dalam cm) :";
    cin >> tinggiBadan;
    
    // hitung body mass index
    tinggiBadanM = tinggiBadan*CENTI_TO_METER;
    tinggiBadanKuadrat = tinggiBadanM*tinggiBadanM;
    bodyMassIndex = beratBadan/tinggiBadanKuadrat;
    
    if(bodyMassIndex<18.5){
        cout<<"\nAnda kekurangan berat badan!";
        cout<<"\nPesan : \nTambahkan porsi karbohidrat dan lemak pada menu makan anda. \nPerbanyak olahraga yang menambah masa otot seperti push up dan bersepeda.";
    }
    else if(bodyMassIndex>=18.5 && bodyMassIndex<24.9){
        cout<<"\nKeren! Anda memiliki berat badan normal!";
        cout<<"\nPesan : \nPertahankan berat badan anda dengan rajin mengkonsumsi buah, sayur, dan protein. \nLakukan olahraga rutin seperti jogging dan senam serta perbanyak air putih.";
    }
    else if(bodyMassIndex>=25 && bodyMassIndex<=29.9){
        cout<<"\nAnda mengalami kelebihan berat badan";
        cout<<"\nPesan : \nKurangi porsi karbohidrat dan lemak pada menu makan anda. \nPerbanyak olahraga yang mampu membakar lemak seperti cardio, zumba, dan lari. Perbanyak konsumsi air putih untuk mempercepat metabolisme.";
    }
    else{
        cout<<"\nAnda mengalami kegemukan (obesitas)";
        cout<<"\nPesan : \nKurangi porsi karbohidrat, gula, dan lemak pada menu makan anda. \nPerbanyak olahraga yang mampu membakar lemak seperti cardio, zumba, dan lari. Perbanyak konsumsi air putih untuk mempercepat metabolisme.";
        
    }
    
    // hitung berat ideal
    if(gender==1){
        perlibelTinggi = (tinggiBadan - 100)*0.15;
        beratIdealCe = (tinggiBadan - 100) - perlibelTinggi;
        cout<<"\nNamun, Berat ideal anda adalah "<<beratIdealCe<<" kg";
    }
    else{
        persepuluhTinggi = (tinggiBadan - 100)*0.1;
        beratIdealCo = (tinggiBadan - 100) - persepuluhTinggi;
        cout<<"\nNamun, Berat ideal anda adalah "<<beratIdealCo<<" kg";
    }
    
    
    return 0;
}
