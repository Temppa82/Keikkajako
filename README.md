# Lähetejako v1.33

**Tekijä:** Teemu H. Fingerroos

Selainpohjainen työkalu, jolla jaat Pamark-tyyliset lähetteet (PDF) kuljettajien kesken.

## Versio 1.33

- Kartan rakennusnumerovälit hyväksytään oikein: esimerkiksi osoite 19 vastaa kartan rakennusta 15–19.
- Korjaus löytää muun muassa osoitteen Tarvonsalmenkatu 19, 02600 Espoo.
- Väärä talonumero hylätään edelleen, jos se ei kuulu kartan ilmoittamaan numeroväliin.
- Päivityksen ZIP-paketista on jätetty tarpeeton PDF-esimerkkitiedosto pois.

## Versio 1.32

- Osoitehaku käyttää automaattisesti kahta avaimetonta hakupalvelua sekä haluttaessa Maanmittauslaitosta.
- Photon-varahaku löytää myös osoitteita, joita OpenStreetMapin Nominatim-haku ei tunne, kuten Isonniitynkuja 2, 02270 Espoo.
- Tuloksesta tarkistetaan katu, talonumero ja saatavilla oleva postinumero ennen kartalle hyväksymistä.
- Käsin vaihdetulle osoitteelle ei enää jää PDF:stä poimittua vanhaa postinumeroa.
- Myös lähtö- ja loppuosoitteet käyttävät samaa korjattua monivaiheista hakua.
- Vanhat mahdollisesti virheelliset osoitehakutulokset ohitetaan uusilla välimuistiavaimilla.

## Versio 1.31

- Myös ilman karttapistettä jääneet keikat ovat raahattavia.
- Ratkaisematon keikka voidaan pudottaa mihin tahansa optimoitujen keikkojen väliin.
- Käsin sijoitettu keikka säilyttää paikkansa kuljetusnäkymässä ja yhdistetyn PDF:n järjestyksessä.
- Karttapisteetön keikka ohitetaan vain reittiviivan ja kilometrilaskennan osalta.

## Versio 1.30

- Maanmittauslaitoksen valtakunnallinen geokoodaus voidaan ottaa ensisijaiseksi osoitehauksi API-avaimella.
- API-avain syötetään Kuljettajan asetuksiin ja tallennetaan vain käyttäjän omalle laitteelle.
- Maanmittauslaitoksen haku käyttää rakennusosoitteita ja laskennallisia tieosoitteita; OpenStreetMap jää varapalveluksi.

## Versio 1.29

- Osoitehaku kokeilee rakenteisen haun jälkeen enintään kymmenen vapaamuotoista hakutulosta.
- Hakutulos hyväksytään edelleen vain, jos sen postinumero vastaa lähetettä.
- Viimeisenä turvallisena hakuna voidaan käyttää vastaanottajan nimeä oikean postinumeroalueen sisältä.

## Versio 1.28

- Kaikki CARTO-karttatasot on vaihdettu avaimettomaan OpenStreetMap-karttaan.
- API KEY REQUIRED -vesileimat ovat poistuneet kuljettajan ja ajojärjestelijän kartoista.
- OpenStreetMapin tekijämerkintä näkyy jokaisessa kartassa käyttöehtojen mukaisesti.

## Versio 1.27

- Geokoodaus hyväksyy katuosoitteelle vain oikeaan postinumeroon kuuluvan tuloksen.
- Katuosoitetta ei enää korvata virheellisesti postinumeroalueen keskipisteellä.
- Geokoodausvälimuistin versio on vaihdettu, joten vanhat väärät karttaosumat eivät jää käyttöön.

## Versio 1.26

- Sovellus on asennettava PWA puhelimelle ja tietokoneelle.
- Mukana ovat sovelluskuvakkeet, asennuspainike ja paikallinen offline-sovellusrunko.
- Asennus vaatii HTTPS-osoitteen tai localhost-palvelimen; file://-osoitteesta PWA-asennus ei ole selaimissa sallittu.

## Versio 1.25

- Asiakas-soittopainikkeen teksti on nyt Soita.
- Kuljetusnäkymän esikatselu näyttää kokonaiset PDF-sivut täysleveinä.
- Esikatseluikkunan korkeus on noin puoli PDF-sivua ja sisältöä vieritetään pystysuunnassa.
- Monisivuisen PDF:n kaikki sivut voi selata samassa ikkunassa sivunumeroineen.

## Versio 1.24

- Kuljetusnäkymä näyttää vain yhden keikan kerrallaan.
- Nykyisen keikan PDF-esikatselu on jatkuvasti näkyvissä.
- Navigointi-, Kuittaus- ja Varaumat-palkki on suoraan esikatselun alapuolella.
- Vastaanottajan ja asiakkaan puhelinnumerot poimitaan PDF:stä suoriksi soittopainikkeiksi.
- Keikkojen välillä liikutaan Edellinen- ja Seuraava-painikkeilla.

## Versio 1.23

- Korjattu kuljettajan etunimikenttä oikeaan Kuljettajan asetukset -ikkunaan.
- Tallennettu etunimi näkyy Asetukset-painikkeessa, jotta asetuksen voi varmistaa yhdellä silmäyksellä.

## Versio 1.22

- Kuljettajan asetuksiin voi tallentaa etunimen.
- Kuitattujen lähetteiden tiedostonimi muodostetaan etunimestä ja päivämäärästä, esimerkiksi Teemu31082026.pdf.

## Versio 1.21

- Google Maps avataan puhelimessa sovelluslinkillä verkkoversion sijasta.
- Androidissa linkki kohdistetaan varsinaiseen Google Maps -pakettiin Maps Go -version sijasta.
- iPhonessa käytetään Google Mapsin omaa sovellusosoitetta.

## Versio 1.20

- Kuljettaja-näkymässä on Asetukset-valikko navigointisovelluksen valintaan.
- Vaihtoehdot ovat Google Maps, Waze ja Apple Maps; Google Maps on oletus.
- Navigointivalinta muistetaan samalla laitteella.

## Versio 1.19

- Kuljettaja voi tuoda PDF-lähetteet suoraan ZIP-paketista.
- Useita autokohtaisia kansioita sisältävästä ZIP:stä valitaan oma kansio ennen tuontia.
- ZIP puretaan paikallisesti selaimessa.

## Versio 1.18

- Korjattu vastaanottajan kuittauksen ja Varaumat-tekstin sijainti PDF-lähetteessä.
- Kentät tunnistetaan kokonaisista PDF-tekstiriveistä, vaikka otsikko koostuisi useasta tekstipalasta.
- Varasijainnit perustuvat sivun mittoihin eivätkä enää osu alatunnisteeseen.

## Versio 1.17

- Kartan kohdepallot näyttävät vastaanottajan ja osoitteen hiirellä osoitettaessa.
- Valmis reitti voidaan kuitata kuljetukseen ja avata keikkalistaksi ajojärjestyksessä.
- Jokaisella keikalla on navigointi-, kuittaus- ja Varaumat-painikkeet.
- Kuittaus päivämäärineen ja varaumat kirjoitetaan ladattavan PDF:n viimeisen sivun vastaaviin kenttiin.

## Versio 1.16

- Kuljettajan PDF-esikatselussa on muokattava toimitusosoiterivi.
- Käsin tallennettu osoite ohittaa PDF:stä tunnistetun osoitteen reitinoptimoinnissa.

## Versio 1.15

- Kuljettaja-näkymän jokaisella PDF-tiedostolla on osoitteentarkistuksen suurennuslasipainike.
- Esikatselu näyttää PDF:n koko leveyden lähetteen yläreunasta Toimitusohje-kentän alareunaan.
- Esikatselussa voi liikkua edelliseen ja seuraavaan lähetteeseen nuolipainikkeilla tai näppäimistön nuolilla.

## Versio 1.14

- Ajojärjestelijän keikkamäärä tarkoittaa nyt aina fyysisten toimitusosoitteiden määrää.
- PDF-tiedostojen määrää ei näytetä erillisenä keikkamääränä autokorteissa, kartan sivukortissa tai ZIP-yhteenvedossa.
- Suuren **Valitse kartasta** -ikkunan palluran vihjeteksti näyttää EUR-/Teho-lavojen lisäksi osoiteryhmän kokonaispainon.
- Tavallinen jaon kartta näyttää hiirellä osoitettaessa myös keikan painon.

## Versio 1.13

- Automaattijaon ensisijainen tasausmittari on nyt fyysisten pysähdysten määrä.
- Yhden pysähdyksen peruspaino kasvatettiin selvästi tavaramäärää suuremmaksi.
- EUR-/Teho-lavat ja paino vaikuttavat edelleen, mutta vain jaon hienosäätönä.
- Maantieteellinen läheisyys säilyy mukana, mutta se ei enää yhtä helposti ohita selvää eroa keikkamäärissä.
- Jaon jälkeinen automaattinen tasaus tekee tarvittaessa useampia siirtoja ja tavoittelee ensin tasaisia pysähdysmääriä.
- Autokorteissa näytetään erikseen keikkojen/PDF:ien ja fyysisten pysähdysten määrä.

## Versio 1.12

- Ajojärjestelijä jakaa keikat autoille, mutta ei enää muodosta tai optimoi ajojärjestystä.
- Ajojärjestelijän kartasta poistettiin reittinumerot, lähtö-/kotipisteet ja pysähdyksiä yhdistävät reittiviivat.
- Autokorteista poistettiin reittikilometrit, autokohtainen optimointipainike sekä pysähdysten ↑/↓-järjestely.
- **Jaa & optimoi reitit** korvattiin toiminnolla **Jaa keikat autoille**.
- ZIP-viennin yhdistetty tiedosto on nyt `AUTO_lahetteet.pdf`, eikä sen järjestystä esitetä ajojärjestyksenä.
- Kuljettajan oma reittioptimointi, karttavalinta ja käsijärjestys säilyvät ennallaan.

## Versio 1.11

- Ajojärjestelijän tulosalueen alareunaan lisättiin toinen **Valitse kartasta** -painike automaattisen optimoinnin jälkeistä manuaalista hienosäätöä varten.

## Versio 1.10

- Ajojärjestelijä voi valita auton ja avata **Valitse kartasta** -toiminnon omaan suureen ikkunaan.
- Kaikki geokoodatut fyysiset pysähdykset näytetään karttapalluroina, ja koko saman osoitteen PDF-ryhmä valitaan yhdellä napsautuksella.
- Valinnat lukitaan valitulle autolle, joten automaattinen **Jaa & optimoi** säilyttää ne.
- Kartan sivukortti näyttää autokohtaisesti PDF-/keikkamäärän, pysähdykset, EUR- ja Teho-lavat, lavapaikat sekä kapasiteetin.
- Autoa voi vaihtaa myös karttaikkunan sivukortista; kartan zoomaus ja sijainti säilyvät valintojen aikana.
- **Valitse kartasta** -painike on myös Ajojärjestelijä-sivun alareunassa automaattisen optimoinnin vieressä, jotta keikkojen manuaalinen siirtely on helppo avata valmiin jaon jälkeen.

## Versio 1.9

- Kuljettajan karttavalinta avautuu omaan suureen selainikkunaan.
- Kartan keskipiste ja zoomaustaso säilyvät palluroita valittaessa ja valintoja peruttaessa.
- Jos selain estää popup-ikkunan, karttavalinta toimii sivunsisäisenä varavaihtoehtona samalla zoomin säilytyksellä.

## Versio 1.8

- Kuljettaja voi valita ajojärjestyksen itse napsauttamalla kartan pysähdyspalluroita.
- Karttavalinnassa viimeisen pisteen voi perua tai koko valinnan aloittaa alusta.
- Nykyisen reittijärjestyksen PDF:t voi yhdistää ja ladata yhtenä tiedostona.

## Versio 1.7

- Kuljettaja voi optimoida omista PDF-lähetteistään yhden päivän reitin.
- Lähtö- ja loppuosoite huomioidaan optimoinnissa; tyhjä loppuosoite tarkoittaa paluuta lähtöpaikkaan.
- Reitti käyttää tieverkkoetäisyyksiä, 2-optia ja siirtoparannusta.
- Saman fyysisen osoitteen PDF:t muodostavat yhden pysähdyksen.
- Tulos näytetään numeroituna pysähdyslistana, kilometrivarauksena ja kartalla.
- Kuljettaja voi muuttaa optimoitua pysähdysjärjestystä raahaamalla rivejä. Numerointi, kilometrimäärä ja kartta päivittyvät heti.
- Kuljettajan kartta hakee OSRM:ltä katuja ja teitä seuraavan reittiviivan. Katkottu suora viiva näytetään vain varatilana, jos tieverkkopalvelu ei vastaa.
- **Valitse ajojärjestys itse** tuo pysähdykset kartalle valittaviksi. Palluroita napsautetaan halutussa ajojärjestyksessä, ja viimeisen valinnan voi perua tai valinnan aloittaa alusta.
- **Yhdistä ja lataa PDF:t** tekee yhden PDF:n nykyisessä reittijärjestyksessä. Reitittämättömät PDF:t lisätään tiedoston loppuun.
- Karttavalinta avautuu omaan suurikokoiseen selainikkunaan. Kartan sijainti ja zoomaustaso säilyvät pistevalintojen, peruutusten ja uudelleenpiirtojen aikana.

## Versio 1.6

- Yläreunassa on selkeä **Ajojärjestelijä / Kuljettaja** -näkymänvalinta.
- Ajojärjestelijä on oletusnäkymä ja sisältää kaikki v1.5:n nykyiset toiminnot.
- Kuljettaja-näkymä on kevyt pohja, johon voidaan seuraavaksi lisätä kuljettajan omat keikat, reitti ja kartta.
- Kuljettaja-näkymässä voi valita tai raahata omat PDF-lähetteet erilliseen tiedostolistaan.
- Kuljettaja voi antaa lähtö- ja loppuosoitteen ja optimoida oman reittinsä tieverkkoetäisyyksillä, 2-optilla ja siirtoparannuksella.
- Optimoitu reitti näytetään numeroituna listana ja kartalla. Saman fyysisen osoitteen PDF:t yhdistetään yhdeksi pysähdykseksi.

## Käyttö

1. Avaa `index.html` selaimessa.
2. Raahaa PDF-lähetteet sovellukseen.
3. Valitse töissä olevat autot ja alueet.
4. Jaa & optimoi reitit.
5. Tarkista jaon kartta ja työmääräpisteet.
6. Lukitse tarvittaessa osoite nykyiselle autolle 🔒.
7. Muokkaa valmista reittijärjestystä ↑ / ↓ -painikkeilla tai optimoi yhden auton reitti uudelleen.
8. Lataa ZIP (kansiot per auto).

## Versio 1.5

### 2-opt + siirtoparannus

- Lähin-naapuri muodostaa vain ensimmäisen reittiehdotuksen.
- Sen jälkeen 2-opt poistaa reitistä turhia ristiinajoja ja paluita.
- Yhden pysähdyksen siirtoparannus täydentää 2-optia pitkissä koukuissa.
- Reitin **kotiosoite/loppupiste vaikuttaa optimointiin jo järjestystä muodostettaessa**.
- Kahdella lastauksella L1 optimoidaan muodossa `lastaus → L1 → lastaus` ja L2 muodossa `lastaus → L2 → koti`.

### Jaon jälkeinen kartta

- Jokaisella autolla on oma väri.
- Pysähdykset näkyvät kartalla reittinumeroilla.
- Kartta näyttää lastaus-/lähtöpisteen, kodin/reitin lopun ja kahden lastauksen paluun lastauspaikalle.
- Kartan viiva näyttää pysähdysjärjestyksen; kilometrilaskenta käyttää edelleen tieverkkoetäisyyksiä.

### Lukitut keikat

- 🔒 lukitsee koko fyysisen osoitteen nykyiselle autolle.
- Uusi `Jaa & optimoi` ei siirrä lukittua osoitetta toiselle autolle.
- Auton käsin vaihtaminen päivittää myös lukituksen uudelle autolle.
- Käsin siirrettäessä sama fyysinen osoite liikkuu kokonaisena.

### Työmääräpohjainen tasaus

Työmäärä ei perustu enää vain pysähdysten lukumäärään. Työmääräpisteissä huomioidaan:

- yksi fyysinen pysähdys
- EUR-lavat
- Teho-lavat
- kuorman paino (rajatulla vaikutuksella)
- aluekerroin (esim. Helsingin keskustan toimitus saa tavallista suuremman työpainon)

Autokorteissa näkyy auton työmääräpistemäärä ja kaikkien autojen keskiarvo.

### Reitin käsin muokkaus optimoinnin jälkeen

- Jokaisen pysähdyksen vieressä on ↑ / ↓.
- Nuolilla voi muuttaa optimoitua järjestystä käsin.
- Kilometrimäärä ja kartta päivittyvät heti ilman uutta automaattista optimointia.
- Kahdella lastauksella nuolilla järjestetään pysähdyksiä saman lastauksen sisällä.
- `Optimoi tämän auton reitti` palauttaa automaattisen 2-opt-optimoinnin.
- `Optimoi kaikki reitit uudelleen` optimoi koko valmiin jaon uudestaan muuttamatta autojakoa.

## Versio 1.4 – tieverkko ja osoitenormalisointi

- Keikkojen jakopäätökset ja reittijärjestys käyttävät oikeaa ajomatkaa tieverkkoa pitkin.
- Autokohtainen reittikilometrimäärä perustuu tieverkkoon.
- Tieverkkomatriisi lasketaan OSRM-reitityspalvelun avulla.
- Jos tieverkkopalvelu ei vastaa, puuttuvalle välille käytetään varalaskentaa.
- Reitityksessä `12 A` → `12` ja `11-13` → `11`.

## Aiemmat korjaukset

- Sama katuosoite pysyy samalla kuljettajalla myös automaattisessa tasauksessa.
- Manuaalinen siirto laskee reitit, reittinumerot ja lastausjaon uudelleen.
- Pelkkä postinumero ei yhdistä eri asiakkaita samaksi pysähdysryhmäksi.
- Käsin korjatut osoitteet normalisoidaan samalla osoiteparserilla kuin PDF-luku.
- ZIP-vienti säilyttää jakamattomat PDF:t `_EI_SIJOITETTU`-kansiossa ja tarkistaa PDF-määrän ennen vientiä.
- Vastaanottajan katuosoite etsitään ensisijaisesti Vastaanottaja-blokista.
- Moniosaiset kadunnimet kuten `Alvar Aallon katu`, `Hermannin puistotie` ja `Vanha Helsingintie` tunnistetaan.

## Tietoliikenne

PDF-tiedostoja ei lähetetä palvelimelle. Ohjelma käyttää verkkopalveluita osoitteiden geokoodaukseen, karttaruutuihin ja tieverkkoetäisyyksien laskentaan, joten reittijaon tekeminen vaatii internet-yhteyden.
