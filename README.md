# c-skil1

skil.h:
#pragma once
#include <sstream>
#include <string>

class Nemandi{
    public:
        Nemandi();
        Nemandi(Nemandi_id, nafn, einkunn);
    
    private:
    int nemandi_id;
    string nafn;
    int einkunn;
};

class skraAfanga {
    public:
        skraAfanga();
        skraAfanga(int id, string nafnAfanga, int einkunn);
        bool eydaafanga(int id);
        bool uppfaeraeinkunn(int einkunn,new int einkunn);
        void printStatus();
        int getId();

    private:
        int id;
        string nafnAfanga;
        int einkunn;
};

skilmain:
#include "skil.h"
#include <iostream>
#include <sstream>

using namespace std;

skraAfanga::skraAfanga(){
    this-> id=0;
    this-> nafnAfanga = "";
    this-> einkunn = 0;
}

skraAfanga::skraAfanga(int id, string nafnAfanga, int einkunn){
    this-> id=id;
    this-> nafnAfanga = nafnAfanga;
    this-> einkunn = einkunn;
}

void skraAfanga::printStatus() {
  cout << "Afangi :" << this->id << ": " << "nafn :" << this->nafnAfanga << "einkunn :" << this->einkunn << endl;
}


int main ( ) {
// nemandi_id , nafn
Nemandi geir = Nemandi (11, "Geir") ;
// afangi_id , nafn , einkunn
geir.skraAfanga (33, "GAGN", 2.43) ;
geir.skraAfanga (34, "FORR", 3.59) ;
geir.skraAfanga (35, "ROBO", 10) ;
geir.skraAfanga (36, "KEST", 6.249) ;
// afangi_id , einkunn
geir.uppfaeraEinkunn (34, 4.49) ;
// afa n gi_id
geir.eydaAfanga(33) ;
geir.prenta() ;
return 0 ;
}
