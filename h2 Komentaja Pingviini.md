# Komentaja Pingviini

### Lue ja tiivistä 
- Linuxin komentorivi vaikuttaa tehokkaalta työkalulta, kun komennot tulevat ulkomuistista ja niiden toiminnan ymmärtää syvällisesti.
- Artikkeli on hyvä yleisen tason perehdytys Linuxin komentorivin perusteista. Tästä on näppärä käydä lunttaamassa kun tutustuu ja hrajoittelee käyttöjärjestelmän kanssa ensimmäistä kertaa.
- Pidän siitä, miten komentojen yhdistelemisestä ja putkittamisesta annetaan konkreettisia esimerkkejä.

### Ympäristö
Tein harjoituksen 28.8.2025 kotitoimistossani. Koneena oli Lenovo V14 G4 AMN.

### Asenna micro-editori
17:40   
Aloitin päivittämällä pakettilistan komennolla __sudo apt-get update__. Seuraavaksi hain micro-editoria __apt-cache search micro__-komennolla, mutta lista oli niin jäätävän pitkä että päätin putkittaa edellisen komennon __grep ^micro__-komennolla. Tämä rajasi tuloksia riittävästi, kuten alla olevasta kuvasta näkyy. Komennolla __apt-cache show micro | less__ tutustuin editorin dokumentaatioon. Dokumentaatiosta näki paljon kiinnostavaa tietoa, kuten esim. ohjelman version, ohjelman koon, lyhyen kuvauksen sekä paljon muuta. Dokumentaatiossa suositeltiin myös lataamaan xclip-nimisen ohjelman, joka parantaa micron toiminnallisuutta mahdollistamalla tekstin kopioimisen ja liittämisen terminaalissa (opensourse.com).  

17:52   
Lopuksi asensin sekä micron __sudo apt-get -y install micro__-komennolla. Xclip oli jo valmiiksi asennettuna.
![](images/h2/micro-asennus.png)



### Lähteet
opensource.com. Copy and paste at the Linux command line with xclip.
Luettavissa: https://opensource.com/article/19/7/xclip. Luettu: 28.8.2025.