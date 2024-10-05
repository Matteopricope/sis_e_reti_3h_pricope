/******************************************************************************

Implementare, in un linguaggio di programmazione a scelta, un programma che controlli la parità.

Inserire nel programma almeno 3 casi di test.

Oltre al codice si consegna la documentazione, secondo il formato descritto nel file
@pricope cristian matteo 4H
*******************************************************************************/
#include <iostream>
using namespace std;

bool controllaParita(int n);
int main()
{
    int numero;
    
    cout<<"inserisci un numero intero -> ";
    cin>>numero;
    cout<<endl;
    
    if(controllaParita(numero)){
        cout<< "il numero che hai inserito ha parita di bit pari"<<endl;
    }else{
        cout<<"il numero che hai inserito ha parita di bit dispari"<<endl;
    }
    
    
    return 0;
}
bool controllaParita(int n){
    int conta=0;
    
    while(n!=0){
        conta+=(n&1);
        n=n/2;
    }
    return (conta%2==0);
}
