 
# University Z.:

Kampuksen sisätilapaikannukseen perustuva sosiaalinen mobiilizombipeli. Vaatimusmäärittely. Tarkoitettu TV12S1-ryhmän ja opettajiensa silmien hiveltäväksi ja näköhermojensa hyväiltäväksi.

Tattitiimi Developers

Ryhmän jäsenet: Joonas Schwanck, Velipekka Rahkola, Janne Savela

8.12.2013

V. 0.1 BETA
 
## 1. Johdanto 
 
### Projektin yleiskuvaus, projektin tausta
Sisätilapaikannukseen perustuva sosiaalinen mobiilizombipeli. Paikannus tapahtuu Metropolian toimipisteessä rakennuksen langattoman verkon signaalien avulla. Pelissä on kahdenlaisia hahmoja: zombuja ja ihmisiä. Peli toimii samalla tavalla kuin hippa.

### Sovelluksen yleiskuvaus
Mobiilisovellus, ladattavissa kaikille alustoille.
Power-uppeja (zombina) tai aseita (ihmisenä) löytää tiloista joihin on vaikea pääsy tai joihin pääsee vain ajoittain. Esimerkiksi: opehuone, siivouskomero, studio ja muut lukitut tilat. Peliin voisi myöhemmin yhdistää muita tehtäviä. Esimerkiksi kirjastosta voisi vihjeen perusteella löytää kirjan jonka väliin on piilotettu qr-koodi. Tämän "tiedon" tai "avaimen" avulla voisi avata uusia tehtäviä. Skenaariokohtainen päämääränä voisi olla esimerkiksi ulospääsy lukitusta koulusta tai vastalääkkeen kehittäminen. 

Kun ihmispelaaja saa pureman, hän muuttuu hetken päästä zombiksi ja saa zombin suppeamman karttanäkymän eli pelaaja "tyhmenee". Zombi kuolee kahden iskun jälkeen eli kahden raajanmenetyksen jälkeen. Tämän jälkeen pelaaja voi liittyä uudestaan julkiseen peliin käydessään tietyllä alueella. Privaattipelien tai skenaarioiden säännöt ovat skenaariokohtaisia.

#### Peli sisältää kolmenlaisia pelejä: 

##### Kaikille avoimet pelit
+ avoin peruspeli
+ skenaariot eli tehtävät

##### Suljetut privapelit
+ Valvojan luomat ryhmäkohtaiset skenaariot
 
## 2. Käyttötapaukset (mitä sillä voi tehdä)
 
### Käyttäjäryhmien määrittely

+ ihminen
+ zombi
+ Valvoja
+ kehittäjä
 
### Käyttötapauskaavio(t)

#### Pelaaja 
 + Sisäänkirjautuminen/pelin avaaminen
 + olemassa olevaan peliin liittyminen
 + omien tietojen selaaminen
 + omien tietojen muuttaminen
 + kartan selaaminen
 + kartalla liikkuminen
 
##### ihminen
 + aseen poimiminen
 + aseen käyttäminen vaaratilanteessa
 + ryhmänäkymän valitseminen

##### zombi
 + pureminen
 + power-uppien poimiminen
 + power-uppien käyttäminen
 + kuolleesta zombusta ihmiseksi muuttuminen

#### Valvoja
 + kenttien luominen
 + kartan muuttaminen
 + tilojen rajojen määrittely
 + käyttäjien lisääminen
 + käyttäjien poistaminen
 + peli- ja ei pelialueden luonti
 + ryhmien luonti
 + privaatti- eli ryhmäpelin luonti
 + aseiden ja power-uppien asettaminen ja piilottaminen

#### kehittäjä
 + tyylien muuttaminen
 + grafiikan vaihtaminen
 + signaalien skannaaminen
 
![liite1](http://users.metropolia.fi/~joonassc/ohjelmistotuotanto/kkaavio.gif)

### Käyttäjäskenaariot (mallipohjaan perustuen: alkutila, normaali 
eteneminen, lopputila, mikä voi mennä vikaan...)

### Kuvaa yhden (pää)käyttötapauksen kulku vuokaaviona
Ihmispelaaja
 ![liite2](http://users.metropolia.fi/~joonassc/ohjelmistotuotanto/kskenaario1.gif)
 
## 3. Järjestelmäarkkitehtuuri
 
### Korkean abstraktiotason yleiskuvaus
![liite3](http://users.metropolia.fi/~joonassc/ohjelmistotuotanto/arkkitehtuuri.gif)

### Järjestelmän pääkomponentit ja niiden toiminnallisuuksien määrittely
 
## 4. Vaatimukset (jäljitettävässä, (mitattavassa) muodossa)
 

### toiminnalliset vaatimukset (functional requirements)
 + käyttäjän paikka tulee paikantaa viiden metrin tarkkuudella
 + zombin puremasta popup-ilmoitus, ikkunassa voi puolustatua mikäli on saanut aseen.
 + zombi voi halutessaan puraista lähellä olevaa ihmistä
 + aseita ja power-uppeja voi asettaa näkyville tai piilottaa tiloihin
 + aseita ja power-uppeja voi poimia lähietäisyydeltä
 + ihminen näkee zombit kartalla
 + zombi näkee ihmiset kartalla ollessaan lähialueella
 + zombi menettää raajoja: kaksi menetettyä raajaa niin zombi kuolee

 
#### power-upit
+ weapon malfunction/out of ammo!
+ hyper zombie: voi syödä seinän läpi
+ flambeeraus: zombi syttyy tuleen:  zombin ulottuvuus kasvaa eli puree pitemmän matkan päästä

### laadulliset vaatimukset (non-functional requirements)
+ kartan on päivityttävä reaaliaikaisesti
+ pelin tapahtumien tulee päivittyä reaaliaikaisesti
 
pohdittavaa

### kuinka taata järjestelmän helppokäyttöisyys?
+ selkeät valikot
+ käyttäjä ei voi joutua ikinä "umpikujaan" mistä ei pääse mihinkään suuntaan

### kuinka taata järjestelmän luotettavuus? Listaa mahdolliset järjestelmävirheet ja kuinka niistä toivutaan
+ paljon resursseja ja tehokas järjestelmä
+ wlan-yhteyden pätkiminen -> puhelimen päivitys

### järjestelmälläsi on paljon käyttäjiä, kuinka taata että järjestelmässä on riittävästi tehoja? Millaisia metriikkoja käyttäisit?
+ järjestelmä on tehokas ja dynaaminen
 
### Mitä muita ei-funktionaalisia vaatimuksia olisi syytä kuvata?
+ käyttöjärjestelmä ja sen versiot, alusta 

### Millaisia metriikkoja käyttäisit, jotta vaatimukset ovat riittävän yksiselitteisiä?
+ tarpeeksi yksinkertaisia, ei laajoja
 
## 5. Käyttöliittymä
 
### Millaisia näkymiä järjestelmässä on? Miten toiminnallisuuksia niissä on?

![liite4](http://users.metropolia.fi/~velipekr/Ohjelmistotuotanto/Menu-N%e4kym%e4.png)
![liite5](http://users.metropolia.fi/~velipekr/Ohjelmistotuotanto/Pelinakyma.png)

+ Aluksi näytöllä on kirjautumisikkuna jos kyseisen käyttäjän tarvitsee kirjautua erikseen. Muuten mennään suoraan pääikkunaan
+ Menunäkymä on pelin pääikkuna.
+ Kartan reunoilla on kuvitettuja nappeja joista pääsee eri valikoihin tai toimintoihin.
+ Asevalikko 
+ Kaverit/ryhmäikkuna: kavereita voi poistaa/lisätä, myös ryhmäkohtaiset privaattipelit
+ Find Game: voi valita pelattavan julkisen skenaarion

### Kuvaile jokainen näkymä ja mihin sitä käytetään 
+ Kirjautumisikkuna: ensimmäinen näkymä jossa käyttäjä kirjautuu sisään peliin
+ Pääikkuna, eli Menu-ikkuna, voi etsiä pelin, palata peliin Map-linkistä, siirtyä asetuksiin
+ Pelinäkymä: karttanäkymä jossa näkyy muut käyttäjät, kartan reunoilla on kuvitettuja nappeja joista pääsee eri valikoihin tai toimintoihin
+ Asevalikko: saat valita mitä asetta käytät ihmisenä ja mitä power upia käytät zombina
+ Kaverit/ryhmäikkuna: kavereita voi poistaa ja lisätä, myös ryhmän/luokan sisäiset privaattipelit
+ Find Game: voi valita pelattavan julkisen skenarion
+ Quit valikko: voit kirjautua ulos pelistä

### Kuvaile siirtymät käyttöliittymänäkymien välillä

+ Siirtymät tapahtuu linkkejä painamalla, joka vie seuraavaan valikkoon/näkymään.
+ ![linkki5](http://users.metropolia.fi/~velipekr/Ohjelmistotuotanto/FLOWCHART1.png)
 
## 6. Projektin hallinta, reflektio
 
### Listatkaa työhön kuluneet tunnit, so. kuinka monta tuntia dokumentin kirjoittamiseen meni aikaa per henkilö.
+ Joonas 11h
+ Velipekka 8,5h
+ Janne 3h

### Työmäärä verrattuna odotuksiin
Tehtävä: kehitä kattava mobiilisovellus ideasta käyttöliittymäluonnoksiin tunneissa. Työmääräarvio alustavanluonteiselle vaatimusmaarittelylle ilman aikaisempaa kokemusta ohjelmistotuotannosta oli noin kahdeksan tuntia per naama. Mutta kun aiheeseen pääsi käsiksi ja sovelluksen ominaisuuksia alkoi putoilla, tuntimäärä venähti. Oli hankalaa määritellä kaikki pienetkin ominaisuudet mahdollisimman yksiselitteisellä tavalla. Pään sisällä idea on yksinkertainen, mutta kun se on esiteltävä suuremmalle yleisölle kaikenkattavalla tavalla, siitä tulee vaikeaa. Ohjelmistotuotannossa on huomioitava kaikki mahdolliset risteyskohdat sekä hahmoteltava niille haaratumat ja niiden risteyskohdat ja niin edelleen.

Kiehtoviempien ja poteniaalisimpien sovellusten määrittely jää heikoksi tai niitä ei tehdä koska ne on "tapettava" määrittelemällä ne tiukasti. Toisin sanoen niiden ei anneta enää hengittää. Tässä prokkiksessa tietysti oletetaan, että sovellus on jo mietitty niin pitkälle kuin se on mahdollista kehittää. Mutta paras vaatimusmäärittelyhän muuttuu projektin edetessä.

Yksi hankala puoli määrittelyssä oli ideoiden esittely. Eli jalostamattomien toiminnallisuuksien esiintuonti. Miten ehdottaa ideaa toiminnallisuudesta silloin, kun sitä ei halua vielä täysin tiukasti määritellä? Tässä tapauksessa ideoita tuli paljon, eikä niitä oltu vielä jalostettu sovelluksen mailmaan sopiviksi. Mikä on ohjelmistotuotannon vaihe jossa idea "käsikirjoitetaan" valmiiksi?

### Mites toi teijän prokkis?
Projekti innosti alkuidean kipinästä eteenpäin. Sääli ettei projekteja ole tehty edelleen kehitettäväksi. Uneversity Z:ssä on paljon potentiaalia monen kampuksen valloittamiseen. Toteutus on oltava ehdottoman toimiva ja mielenkiintoinen. Sovelluksen laajentaminen QR-koodein ja AR-tehtävien avulla on kiehtova mahdoliisuus.
Mitä tekisin toisin? Mikäli sovellus olisi alusta alkaen paremmin ideoitu, voisi pelkälle määrittelylle jäädä enemmän aikaa. ideointi vie rutosti aikaa. Onhan  ideoiden heittely hauskaa mutta silloin speksien määrittely on häilyvää ja juosten näpyttelyä.

### Mikä oli vaikein osa dokumentoinnissa? Oliko jotakin mihin ette itse olleet tyytyväisiä?
