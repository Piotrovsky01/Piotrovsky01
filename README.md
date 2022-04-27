#include <iostream>

using namespace std;

int PIN;
string daneLogowania[3];

void WczytajDane();
void WyswietlDane();


int main(){

    WczytajDane();

    WyswietlDane();

    return 0;
}

void WczytajDane(){
    cout << "Utworz login:";
    cin >> daneLogowania[0];
    system("cls");

    cout << "Utworz haslo:";
    cin >> daneLogowania[1];
    system("cls");

    cout << "Utworz PIN:";
    powtorzPIN:
    cin >> PIN;
    system("cls");

    if(PIN < 111111 || PIN > 999999){
        cout << "Wpisz 6-cyfrowy poprawny PIN:";
        goto powtorzPIN;
        system("cls");
    }
}

void WyswietlDane(){
    cout << "DANE KONTA: " << endl;
    cout << "Login: " << daneLogowania[0] << endl;
    cout << "Haslo: " << daneLogowania[1] << endl;
    cout << "Pin: " << daneLogowania[2] << endl;
}


