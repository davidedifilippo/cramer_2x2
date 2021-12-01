# Cramer_2x2

Scaricare il file o copiare il codice in un file di nome 

        cramer_lib.h 
        
Includere cramer_lib.h nel programma principale che possiamo chimare Cramer.cpp:

    #include <iostream>
    #include "cramer_lib.h"
    using namespace std;
    
    int main(void){
    
    
    return 0;
    }

DA questo momento possiamo calcolare la soluzione di sistemi del tipo:

     ax + by = c
     dx + ey = f

Ad esempio:

     x + y = 1
    -x + y = 1
  
## Calcolo del determinante al denominatore

    
Usiamo la libreria per calcolare D:

    int determinante = D(a,d,b,e); 
    
ossia nel nostro esempio:

    int determinante = D(1,-1, 1 , 1);
    
Facciamo una prova:

    #include <iostream>
    #include "cramer_lib.h"
    using namespace std;
    
    int main(void){
    
    int determinante = D(1,-1, 1 , 1);
    cout << determinante;
    return 0;
    }
    
Che dovrebbe stampare 2


## Calcolo della x soluzione 

Se determinante != 0 posso calcolare l'ascissa della soluzione:

    int   Dx = D(c,f,b,e);
    float x = Dx/determinante;



## Calcolo della y soluzione 

Se determinante != 0 posso calcolare l'ordinata della soluzione:

     int   Dy = D(a,d,c,f);
     float y = Dx/determinante;
     
A questo punto basta stampare. La soluzione dovrebbe essere x = 0, y= 1
     












    

 





