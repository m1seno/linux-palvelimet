### Ympäristö
Tein harjoituksen 20.9.2025 kotitoimistossani Kaarinassa. Koneena oli Lenovo V14 G4 AMN. Käyttöjärjestelmänä Windows 11 Pro version 23H2.

### Nimi
18:15 Aloitin vuokraamalla Namecheapiltä oman domainnimen. Päätin olla käyttämätt GitHub educationsin alennusta, koska se koski ainoastaan .me -suffixeja. Rekisteröidyin palvelussa käyttäjäksi, laitoin kaksivaiheisen tunnistautumisen päälle, ja syötin maksutiedot.

![](images/h5/domainnimi.png)

18:40 Seuraavaksi laitoin vielä domainnimeni osoittamaan virtuaalipalvelimelleni. Seuraamalla ohjeita (Lehto. 14.2.2022), menin Namecheapin sivuilla Dashboard -> vuokratun domainin kohdalta Manage -> Advanced DNS. Poistin Host Recordsista Redirect Recordin ja lisäsin kaksi A Recordia alla olevan kuvan mukaisesti:

![](images/h5/osoittaminen.png)

Tein viime viikolla ylimääräisen tehtävän, jossa virtuaalipalvelimelle lisättiin uusi name based virtual host. Nyt kun kirjoitin selaimeen miikanordblad.com, niin tämä kyseinen NBVH tuli näkyviin.

![](images/h5/testi.png)

20:00 Lopuksi kävin vielä tekemässä muutoksia viime viikon vaapaaehtoiseen tehtävään.

Muutin NBVH:n .conf -tiedoston nimen.
````
$ cd /etc/apache2/sites-available/ 
$ sudo mv miikanordblad.me.conf miikanordblad.com.conf
````
Kävin tietenkin myös vaihtamassa tiedoston sisällön:

![](images/h5/conf.png)

Sitten vaihdoin kansion nimen missä html-tiedosto on:

```
$ mv public-sites/miikanordblad.me public-sites/miikanordblad.com
```
Lopulta ajoin vielä komennot:
```
$ sudo a2ensite miikanordblad.com
$ sudo systemctl reload apache2
```
Tarkistin tietysti vielä että sivu latautuu selaimeen.

### Lähteet
Colleen Branch. 24.8.2020. What is a Subdomain? Definition & Examples. Luettavissa: https://www.namecheap.com/blog/what-is-a-subdomain-dp/. Luettu: 20.9.2025.

Susanna Lehto. 14.2.2022. Teoriasta käytäntöön pilvipalveluiden avulla (h4). Luettavissa: https://susannalehto.fi/2022/teoriasta-kaytantoon-pilvipalvelimen-avulla-h4/. Luettu: 20.9.2025.