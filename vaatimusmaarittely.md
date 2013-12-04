Kansilehti
 
Zombipeli: <Tuotteen kuvaus>"
Tattitiimi Developers
Ryhmän jäsenet: Joonas Schwanck, Velipekka Rahkola, Janne Savela
Päivämäärä
Versiohistoria (jos tarpeen)
 
## 1. Johdanto 
 
### Projektin yleiskuvaus, projektin tausta
Sisätilapaikannukseen perustuva sosiaalinen mobiilizombipeli. Pelissä on kahdenlaisia hahmoja: zombuja ja ihmisiä. Peli toimii samalla tavalla kuin hippa.

### Sovelluksen yleiskuvauksen
 
## 2. Käyttötapaukset (mitä sillä voi tehdä)
 
### Käyttäjäryhmien määrittely

+ ihminen
+ zombi
+ OP
+ kehittäjä
 
### Käyttötapauskaavio(t)

#### ihminen
 + Sisäänkirjautuminen/pelin avaaminen
 + olemassa olevaan peliin liittyminen
 + omien tietojen selaaminen
 + omien tietojen muuttaminen
 + kartan selaaminen
 + kartalla liikkuminen
 + aseen poimiminen
 + aseen käyttäminen vaaratilanteessa
 + zombiksi muuttuminen
 + ryhmänäkymän valitseminen

#### zombi
 + zombi kuolee/peli loppuu
 + pureminen
 + power-uppien poimiminen

#### OP
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
 
### Käyttäjäskenaariot (mallipohjaan perustuen: alkutila, normaali 
eteneminen, lopputila, mikä voi mennä vikaan...)


### Kuvaa yhden (pää)käyttötapauksen kulku vuokaaviona
liite1: käyttäjäskenaario1
 ![liite1](http://users.metropolia.fi/~joonassc/ohjelmistotuotanto/liite1.gif)
 
## 3. Järjestelmäarkkitehtuuri
 
### Korkean abstraktiotason yleiskuvaus
Power-uppeja (zombina) tai aseita (ihmisenä) löytää tiloista joihin on vaikea pääsy tai joihin pääsee vain ajoittain. Esimerkiksi: opehuone, siivouskomero, studio ja muut lukitut tilat. Peliin voisi myöhemmin yhdistää muita tehtäviä. Esimerkiksi kirjastosta voisi vihjeen perusteella löytää kirjan jonka väliin on piilotettu qr-koodi. Tämän "tiedon" tai "avaimen" avulla voisi avata uusia tehtäviä. Skenaariokohtainen päämääränä voisi olla esimerkiksi ulospääsy lukitusta koulusta tai vastalääkkeen kehittäminen.

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
 + 
 
#### power-upit
+ weapon malfunction/out of ammo!
+ hyper zombie: voi syödä seinän läpi
+ flambeeraus: zombi syttyy tuleen:  zombin ulottuvuus kasvaa eli puree pitemmän matkan päästä

### laadulliset vaatimukset (non-functional requirements)
+ kartan on päivityttävä reaaliaikaisesti
+ pelin tapahtumien tulee päivittyä reaaliaikaisesti
 
pohdittavaa
* kuinka taata järjestelmän helppokäyttöisyys?
* kuinka taata järjestelmän luotettavuus? Listaa mahdolliset 
järjestelmävirheet ja kuinka niistä toivutaan
* järjestelmälläsi on paljon käyttäjiä, kuinka taata että 
järjestelmässä on riittävästi tehoja? Millaisia metriikkoja 
käyttäisit?
 
Mitä muita ei-funktionaalisia vaatimuksia olisi syytä kuvata?
### Millaisia metriikkoja käyttäisit, jotta vaatimukset ovat 
riittävän yksiselitteisiä?
 
## 5. Käyttöliittymä
 
### Millaisia näkymiä järjestelmässä on? Miten toiminnallisuuksia niissä 
on?
+ aluksi näytöllä on kirjautumisikkuna jos kyseisen käyttäjän tarvitsee kirjautua erikseen. Muuten mennään suoraan pääikkunaan
+ karttanäkymä on pelin pääikkuna.
+ kartan reunoilla on kuvitettuja nappeja joista pääsee eri valikoihin tai toimintoihin.
+ ase/poweruppivalikko 
+ kaverit/ryhmäikkuna, kavereita voi poistaa/lisätä, myös ryhmäkohtaiset privaattipelit
+ pelivalikko: voi valita pelattavan julkisen skenaarion
+ omat tiedot valikko

### Kuvaile jokainen näkymä ja mihin sitä käytetään 
### Kuvaile siirtymät käyttöliittymänäkymien välillä
 
## 6. Projektin hallinta, reflektio
 
### Listatkaa työhön kuluneet tunnit, so. kuinka monta tuntia dokumentin 
kirjoittamiseen meni aikaa per henkilö.
+ Joonas 4h
+ Velipekka 3,5h
+ Janne 3h

### Kuinka vaikeaa oli arvioida työmäärää, kuinka paljon lopullinen 
työmäärä erosi alustavista arvioista?
### Mitä tekisitte toisin seuraavissa projekteissa? Oliko projektinne 
onnistunut, ostaisitteko oman tuotteenne?
### Mikä oli vaikein osa dokumentoinnissa? Oliko jotakin mihin ette itse 
olleet tyytyväisiä?
