# szamhalo
Számítógépes hálózatok ELTE elmélet

#1. előadás
----------

###Hány réteget különböztet meg az ISO/OSI referencia modell? Sorolja fel őket.
-7 : Fizikai, Adatkapcsolati, Hálózati, Szállítói, Ülés, Megjelenítési, Alkalmazási

###Hány réteget különböztet meg a Tannenbaum-féle hibrid rétegmodell? sorolja fel őket.
-5 : Fizikai, Adatkapcsolati, Hálózati, Szállítói, Alkalmazás

###Mi az "Open System Interconnection Reference Model" (ISO OSI), hogyan specifikáljuk az egyes rétegeket?
(nem teljes)
-Röviden OSI referencia modell, amely egy 7-rétegu standard, koncepcionális modellt definiál kommunikációs hálózatok belso funkcionalitásaihoz ...

###Mi a feladata és mik a főbb funkcionalitásai az ISO OSI modell fizikai rétegének?
-Információt visz át két fizikailag összekötött eszköz között definiálja az eszköz és a fizikai átviteli közeg kapcsolatát. Egy bit kódolásának sémája. Feszültség szintek. Jelek idozítése. Egy bit átvitelének specifikálása

###Mi a feladata és mik a főbb funkcionalitásai az ISO/OSI modell adatkapcsolati rétegének?
-Adatok keretekre tördelésezés: határok a csomagok között. Közeghozzáférés vezérlés (MAC). Per-hop megbízhatóság és folyamvezérlés.Keret küldése két közös médiumra kötött eszköz között.

###Mi a feladata és mik a főbb funkcionalitásai az ISO/OSI modell hálózati rétegének?
-Csomagtovábbítás Útvonalválasztás Csomag fragmentálás kezelése Csomag ütemezés Puffer kezelés.Csomag küldése egy adott végpontnak

###Mi a feladata az ISO/OSI modell ülés (session) rétegének?
-kapcsolat menedzsment: felépítés, fenntarás és bontás munkamenet típusának meghatározása szinkronizációs pont menedzsment (checkpoint), token management, chekpoint beszúrás

###Mik a főbb funkcionalitásai az ISO/OSI modell megjelenítési rétegének?
-Adatkonverzió különbözo reprezentációk között Pl. big endian to little endian Pl. Ascii to Unicode

###Mit jelent a hálózatok esetén az adatok burkolása
-Interfészek definiálják a réteg közi interakciókat, A rétegek csak az alattuk levokre épülnek

###Mit jelent a legjobb szándék (best effort) elv a hálózati kommunikációban?
-ha egy csomag nem éri el a célt, akkor törlodik, az alkalmazás újraküldi ilyen esetekben

###Mit jelent a "Black-box" megközelítés a kapcsolatokra?
-csomaginformációk nem kerülnek megorzésre, nincs folyam-felügyelet

###Mi az a PAN?
-Personal Area Network: Magánhálózat (négyzetméter)

###Mi az a WAN?
-Wide Area Network: nagy kiterjedésu hálózat. pl. kontinens, ország (10-1000km)

###Sorolja fel az internet 5 (előadáson elhangzott) jellemzőjét.
-Rendszerfüggetlenség, nincs központi felügyelet, LAN-ok az építoelemei, globális, szolgáltatásokÉ WWW, e-mail, fájlátvitel

###Definiálja a hálózati sávszélességet?
-Az adat átviteléhez elérheto vagy felhasznált kommunikációs eroforrás mérésére szolgáló mennyiség, amelyet bit per másodpercben szoktak kifejezni.

###Definiálja az átviteli késleltetést.
-Az az idotartam, amely egy csomag összes bitjének az átviteli csatornára tételéhez szükséges.

###Definiálja a propagációs késést.
-Az az idotartam, amely a jelnek szükséges ahhoz, hogy a küldotol megérkezzen a címzetthez.

###Mi a hálózati hoszt?
-Olyan eszköz, amely egy számítógépes hálózattal áll összeköttetésben. Egy hoszt információkat oszthat meg, szolgáltatást és alkalmazásokat biztosíthat a hálózat további csomópontjainak.

###Mi az átviteli csatorna?
-Az a közeg, amelyen a kommunikáció folyik a résztvevo hosztok között. Ez a közeg lehet egy koaxális kábel, a levego, optikai kábel, stb

###Mi a fő különbség a csomagkapcsolt és az áramkörkapcsolt hálózatok között?
(tipp, kép alapján Lecture_1.pdf 16.old )
-Csomagkapcsoltnál egy csatornán megy át többféle(minden) csomag, áramkör kapcsoltnál sok csatorna van és ezeket kapcsoljuk áramköri elemekkel egymáshoz.

###Adjon egy valós példát adatok beburkolására (pl. az előadáson látott Internet példa)!
-[ethernet header | IP header | TCP header | HTTP header | WEB PAGE | ethernet tailer]

###Mit értünk Internet homokóra alatt? Miért nehéz az IPv6-ra való átállás?
-Az internet homokóra az egyes rétegekben alkalmazott protokollok számát jelképezni. A hálózati rétegben nagyon kevés van, az IPv4 a legelterjedtebb és minden eszközt át kellene állítani IPv6-ra, hogy megfeleloen muködjön.

###Jellemezze egy mondatban a tűzfalakat, proxykat és NAT dobozokat!
-Absztrakciós rétegek.
  Tuzfal: Alkalmazásréteg fejlécét vizsgálhatja
  Proxyk: Alkalmazás végpontot szimulál
  NAT: Megtöri a végpont végpont elérhetoséget a hálózatban

###A Hálózati réteg funkcióit milyen síkok (planes) mentén csoportosíthatjuk még?
-????

#2.előadás
---------
###Ismertesse a fizikai rétegben a lehetséges átviteli közegek fajtáit!
-optikai kábel, koax kábel, rádiófrekvenciás adó.

###Mit mond ki a Nyquist tétel?
-Zaj mentes csatorna: Maximális adatsebesség = 2H log2 (V) [b/s]

###Mit mond ki a Shannon tétel?
-Zajos csatorna: Maximális adatsebesség = H log2 (1 + S/N) [b/s]

###Soroljon fel 4 különböző vezetékes átviteli közeget!
-sodort érpár, koaxiális kábel, fényvezető szál, ...

###Mit nevezünk frekvenciának? Hogyan jelölik? Mi a mértékegysége?
-Mértékegység: Hz(Hertz), Jele: f. Elektromágneses hullám másodpercenkénti rezgésszáma.

###Mi a hullámhossz?
-Két egymást követő hullámcsúcs (vagy hullámvölgy) közötti távolság. Jele: lambda

###Soroljon fel 3 elektromágneses tartományt a frekvenciáik növekvő sorrendjében!
-Rádió,Mikrohullám,Infravörös,Látható,Ultraibolya,Röntgen,Gamma

###Milyen frekvencia tartomány átvitelére alkalmas a sodort érpár, a koax kábel, az optikai szál?
-sodort: 10^4-10^6
 koax: 10^5-10^9
 optikai: 10^14-10^15

###Soroljon fel 4 vezeték nélküli átviteli közeget!
-rádiófrekvenciás, mikrohullámú, infravörös, látható

###Mi a szimbólumráta és az adatráta? Mi a mértékegységük?
-Szimbólumráta: Elküldött szimbólumok száma mp enként (BAUD). Adatráta: Elküldött bitek száma mp enként (bps).

###Soroljon fel 3 óraszinkronizációs módszert!
-Biphase-Mark,NRZ-L,RZ,NRZI (???)

###Mi az önütemező jel? Mire használható?
- ????????

###Ismertesse az NRZ-L (Non-Return to zero) kódolás szabályait!
-1 -> magas jel, 0-> alacsony jel

###Ismertesse a Manchester kódolás szabályait!
-1 -> átmenet magasról alacsonyra, 0 -> alacsonyról magasra

###Ismertesse az NRZI (Non-return to zero inverted)? Mi a fő probléma ezzel a kódolással?
-1 -> átmenet, 0->marad

###Ismertesse a 4-bit/5-bit módszert? Miért van erre szükség? Hol használjuk?
-NRZI kódolásnál, ha sok a 0 akkor elromlik. Ezért 4bites részeket 5 bitté kódoljuk, nem lehet 1nél több nulla az elején, kettőnél több a végén. Gigabit Ethernet. 80%os veszteség

###Mik a főbb tulajdonságai az alapsávú átvitelnek?
-a digitális jel direkt árammá alakul
 a jel minden frekvencián átvitelre kerül
 átiteli korlátok

###Ismertesse a digitális alapsávú átvitel struktúráját!
-forrás kódolás, csatorna kódolás, fizikai átvitel, médium, dizikai vétel, csatorna dekódolás, forrás dekódolás

###Mik a főbb tulajdonságai a szélessávú átvitelnek?
-Egy széles frekvenciatartományon történik az átvitel
 jel modulálása

###Ismertesse a digitális szélessávú átvitel struktúráját!
-forrás kódolás, csatorna kódolás, fizikai átvitel, médium, fizikai vétel, demoduláció, csatorna dekódolás, forrás dekódolás

###Mi az amplitúdó moduláció?
-a modulálalnadó jelet egy magasabb frekvenciájú jel amplitúdójával kódolunk.

###Mi a frekvencia moduláció?
-egy magas frekvenciájú vivőjel frekvenciáját a szignál jel amplitúdója alapján moduláljuk.

###Mi a fázis moduláció?
-A szignált a szinusz görbe fázisában kódoljuk.

3.előadás
---------
###Ismertesse a médium többszörös használatának 5 módszerét!
-térbeli multiplexálás, frekvencia multiplexálás,hullámhossz multiplexálás, időbeli multiplexálás, CDMA

###Mi a CDMA? Ismertesse a működési algoritmusát.
-multiplexálási módszer, feltételezi, hogy a többszörös jelek összeadódnak. minden bitidőt m darab rövid intervallumra osztunk (chipekre), minden állomáshoz egy m bites kód tartozik, ha 1 et akar küldeni elküldi a saját kódját, ha 0-t akkor elküldi a saját kódjának egyes komplemensét

###Mi az a Walsh mátrix? Mire használható?
-Walsh mátrix sorai és oszlopai kölcsönösen ortogonálisak. ezért használható töredék sorozatok előállítására, állomáskódok a CDMA-ban.

###Hogyan áll elő a H(2^k)-nal jelölt Walsh mátrix?
|H(2^(k-1)   H(2^(k-1)|
|H(2^(k-1)  -H(2^(k-1)| = minden k eleme N >=2 re H(2^k)

###Melyek az adatkapcsolati réteg legfontosabb feladatai?
-átviteli hibák kezelése,adatforgalom szabályozása,jól definiált szolgálati interfész biztosítása a hálózati rétegnek

###Milyen módszereket ismer a keretezésre az adatkapcsolati rétegben?
-bájt alapú(karakterszámlálás, bájtbeszúrás), bit alapú(bit beszúrás), óra alapú(sonet)

###Hogyan működik a karakterszámlálás?
-a keretben lévő karakterek megadása fejlécben,a vevő ebből tudja a keret végét

###Hogyan működik a karakterbeszúrás (bájt beszúrás)?
-speciális flag bájt jelzi a keret elejét és végét, ha a keretben van flag akkor azt egy speciális esc bájttal jelezzük, az esc bájtot is esccel jelezzük.

###Hogyan működik a bitbeszúrás?
-van egy speciális bitminta : 01111110. ezzel kezdjük és fejezzük be a kereteket, közben minden 5. 1es után egy 0-t szúrúnk be.

###Hogyan működik az óra alapú keretezés (pl. SONET)?
-A keret méretei rögzítettek, 810 bájt után újabb keret kezdő mintázat keresése.
 A fizikai részhez tartozik: A bitek NRZ kódolással kerülnek átvitelre Payload egy speciális 127-bites mintával van XOR kódolva.

###Mit tud mondani a bájt beszúrás és a bit beszúrás hatékonyságáról legrosszabb esetben?
-bitbeszúrás: max 20% teljesítmény csökkenés
 bájtbeszúrás: duplázódik legrosszabb esetben.

###Definiálja a csoportos bithibát adott védelmi övezet (m) mellett!
-Az átviteli csatornán fogadott bitek egy olyan folytonos sorozata, amelynek az első és utolsó szimbóluma hibás, és nem létezik ezen két szimbólummal határolt részsorozatban olyan m hosszú részsorozat, amelyet helyesen fogadtunk volna a hiba burst-ön belül. A definícióban használt m paramétert védelmi övezetnek (guard band) nevezzük.

###Mi az egyszerű bithiba definiciója?
-Az adategység 1 bitje nulláról egyre avagy egyről nullára változik.

###Definiálja egy tetszőleges S kódkönyv Hamming távolságát?
-Az olyan bitpozíciók számát, amelyeken a két kódszóban különböző bitek állnak, a két kódszó Hamming távolságának nevezzük.
 Jelölés: d(x,y)
 Legyen S egyenlő hosszú bitszavak halmaza, ekkor S Hamming távolsága az alábbi: d(S) = min d(x,y) x,y eleme S x!=y

###Mi az a Hamming korlát?
-A kódszavak (k-1)/2 sugarú környezeteiben található bitszavak egymással diszjunkt halmazainak uniója legfeljebb az n-hosszú bitszavak halmazát adhatja ki

###Mi a kódráta és a kód távolság? Milyen a rátája és távolsága egy jó kódkönyvnek?
-kód ráta: Rs = log2|S|/n
 kód távolság: DELTAs = d(s)/n
 A jó kódoknak a rátája és a távolsága is nagy.

###Milyen összefüggés ismeretes egy tetszőleges kódkönyv, a Hamming távolsága és hibajavitási képessége között?
-d bit hiba javításához a megengedett keretek halmazában legalább 2d+1 Hamming távolság szükséges.

###Milyen összefüggés ismeretes egy tetszőleges kódkönyv, a Hamming távolsága és hibafelismerő képessége között?
-d bit hiba felismeréséhez a megengedett keretek halmazában legalább d+1 Hamming távolság szükséges.

###Mikor érdemes hibajelző kódot és mikor hibajavító kódot használni?
-(?) ha kevés bithiba léphet fel, és ez minél kisebb burstot okoz akkor érdemes hibajavítót, egyébként hibajelzőt-> eldobni és újrakérni a hibás részeket.

###Hogyan működik a Hamming kód (több paritásos módszer)?
-a kódszó bitjeit megszámozzuk, kettő egészhatványai sorszámú bitek paritásbitek, maradék helyek az üzenet bitjei, mindegyik paritás bit a bitek valamilyen csoportjának paritását állítja be

###Mi a redundancia szerepe a hibafelügyeletben?
-a redundáns bitek tudják jelezni vagy akár javítani a hibákat a kódban. a hamming távolságos összefüggések alapján.

4. előadás
----------
###Mi a CRC? Mire használható?
-A crc egy ellenőrző összeg, hibák felismerésére használják.

###Ismertesse a CRC-t használó algoritmus 4 lépését!
-G generátor polinom, foka r (küldő, és vevő is ismeri).
 1. r darab nullát fűzünk a keret alacsony helyiértékű végéhez.
 2. elosztjuk a bitsorozatot a G-hez tartozó bitsorozattal modulo 2.
 3. kivonjuk a maradékot modulo 2 vel. Az eredmény az ellenőrző összeggel ellátott továbbítandó keret (T).
 4. a vevő a T+E polinomnak megfelelő sorozatot kapja, ahol E a hiba polinom. Ezt elosztja G-vel.
 Ha a maradék 0 akkor nem volt hiba*.

###Mikor nem ismeri fel a hibát a vevő oldal?
-ha a hiba a kontrollösszeg többszöröse.

###CRC esetén mit lehet mondani hibajelző képességéről, ha a generátor polinom x+1 többszöröse?
-Egy r ellenőrző bittel ellátott polinom-kód minden legfeljebb r hosszúságú csoportos hibát jelezni tud.

###Mutassa be röviden a korlátozás nélküli szimplex protokollt!
-küldő végtelen ciklusban küldi kifele a kereteket folyamatosan,a vevő kezdetben várakozik az első keret megérkezésére, keret érkezésekor a hardver puffer tartalmát változóba teszi és az adatrészt továbbküldi a hálózati rétegnek

###Mutassa be röviden a szimplex megáll-és-vár protokollt!
-küldő egyesével küldi kereteket és addig nem küld újat, még nem kap nyugtát a vevőtől. a vevő kezdetben várakozik az első keret megérkezésére, keret érkezésekor a hardver puffer tartalmát változóba teszi és az adatrészt továbbküldi a hálózati rétegnek, végül nyugtázza a keretet.

###Mutassa be röviden a szimplex protokollt zajos csatorna esetén
-küldő egyesével küldi kereteket és addig nem küld újat, még nem kap nyugtát a vevőtől egy megadott határidőn belül, ha a határidő lejár, akkor ismételten elküldi az aktuális keretet.vevő kezdetben várakozik az első keret megérkezésére, keret érkezésekor a hardver puffer tartalmát változóba teszi, leellenőrzi a kontroll összeget, ha nincs hiba, az adatrészt továbbküldi a hálózati rétegnek, végül nyugtázza a keretet. Ha hiba van, akkor eldobja a keretet és nem nyugtáz.

###Mutassa be röviden a csúszóablak protokollt!
-Egyszerre több keretet is küldhetünk, a fogadó n keretnek megfelelő helyet foglal le ide várja a kereteket. A keret pozíciója adja meg a keret címkéjét. A keret nyugtázója tartalmazza a következőnek várt keret sorozatszámát, a hibás keretet és a nem megfelelő sorrendűt eldobjuk.

###Mit neveznek adási ablaknak?
-A küldő nyilvántartja a küldhető sorozatszámok halmazát (csúszó ablak esetén)

###Mit neveznek vételi ablaknak?
-A fogadó nyilvántartja a fogadható sorozatszámok halmazát (csúszóablak)

###Mi a visszalépés N-nel stratégia lényege?
-Az összes hibás keret utáni keretet eldobja és nyugtát sem küld róluk. Mikor az adónak lejár az időzítője, akkor újraküldi az összes nyugtázatlan keretet, kezdve a sérült vagy elveszett kerettel, így megfelelő sorrendben fognak tovább érkezni a keretek.

###Mi a szelektív ismétléses stratégia lényege?
-A hibás kereteket eldobja, de a jó kereteket a hibás után puffereli. Mikor az adónak lejár az időzítője, akkor a legrégebbi nyugtázatlan keretet küldi el újra.

###Mely 3 dolgot biztosítja a PPP protokoll?
1. keretezési módszer
2. kapcsoaltvezérlő protokoll vonalak felélesztésére,tesztelésére, elengedésére
3. hálózati réteg protokolljától független mód a hálózati réteg opcióinak megbeszélésére

###A csatorna kiosztásra mik a legelterjedtebb módszerek?
-statikus (TDM, FDM),
 dinamikus (verseny vagy ütközés alapú: ALOHA, CSMA, CSMA/CD,
           verseny- illetve ütközés-mentes: bittérkép, bináris visszaszámlálás,
           korlátozott versenyes: adaptív fa)

###Röviden mutassa be a frekvenciaosztásos nyalábolás módszerét!
-a felhasználók különböző frekvencián adnak, az állomások nem zavarják egymást
  előnyös ha fix számú felhasználó van, nagy forgalmi igényekkel
  nem hatékony löketszerű forgalom esetén

###Röviden mutassa be az időosztásos nyalábolás módszerét!
-a felhasználók különböző időszeletekben adnak, nem zavarják egymást. nem hatékony löketszerű forgalom esetén

###A csatorna modellben mit nevezünk ütközésnek?
-Ha két keret egy időben kerül átvitelre, akkor átlapolódnak, és az eredményül kapott jel értelmezhetetlenné válik. Ezt nevezzük ütközésnek.

###Írja le a folytonos és a diszkrét időmodell lényegét!
-Folytonos: Mindegyik állomás tetszőleges időpontban megkezdheti a küldésre kész keretének sugárzását.
 Diszkrét: Az időt diszkrét résekre osztjuk. Keret továbbítás csak időrés elején lehetséges. Az időrés lehet üres, sikeres vagy ütközéses

###Mit jelent a vivőjel érzékelési (Carrier Sensing) képesség?
-az állomások vizsgálják-e a csatorna foglaltságát a küldés előtt vagy nem

###Hogyan működik az egyszerű ALOHA protokoll?
-Ha van elküldendő adat, akkor elküldi.A fogadók minden csomagot nyugtáznak.Nincs nyugta = ütközés, véletlen ideig vár, majd újraküld

###Mit jelent a keretidő az ALOHA protokoll esetén?
-feldolgozási, átviteli és propagációs idő

###Mennyi az Aloha protokoll esetén az áteresztőképesség (átvitel) a terhelés függvényében?
 S = G*e^(-2G)
 S: azt jelöli, hogy egy keretidő alatt átlagosan hány keret jut át sikeresen;
 G: azt jelöli, hogy egy keretidő alatt átlagosan hány keretet küldenek az állomások összesen

###Mit nevezünk sebezhetőségi időnek?
-Az az időtartam, amely alatt ha másik keret is elküldésre kerül, akkor az aktuális keret sérül.

5. előadás
----------
###Hogyan működik a réselt ALOHA protokoll?
-A csatornát azonos időrésekre bontjuk, melyek hossza pont egy keret átviteléhez szükséges idő. Átvitel csak az időrések határán lehetséges

###Mennyi a réselt Aloha protokoll esetén az áteresztőképesség a terhelés függvényében?
 S = G*e^(-G) azaz a sebezhetőségi idő a felére csökkent

###Hogyan működik az 1-perzisztens CSMA protokoll?
-Keret leadása előtt belehallgat a csatornába:
 a. Ha foglalt, akkor addig vár, amíg fel nem szabadul. Szabad csatorna esetén azonnal küld. (perzisztens)
 b. Ha szabad, akkor küld.
 Ha ütközés történik, akkor az állomás véletlen hosszú ideig vár, majd újrakezdi a keret leadását.

###Hogyan működik a nem-perzisztens CSMA protokoll?
-Keret leadása előtt belehallgat a csatornába:
 a. Ha foglalt, akkor véletlen ideig vár (nem figyeli a forgalmat), majd kezdi előröl a küldési algoritmust. (nem-perzisztens)
 b. Ha szabad, akkor küld.
 Ha ütközés történik, akkor az állomás véletlen hosszú ideig vár, majd újrakezdi a keret leadását.

###Hogyan működik a p-perzisztens CSMA protokoll?
-Adás kész állapotban az állomás belehallgat a csatornába:
 a. Ha foglalt, akkor vár a következő időrésig, majd megismétli az algoritmust.
 b. Ha szabad, akkor p valószínűséggel küld, illetve 1-p valószínűséggel visszalép a szándékától a következő időrésig. Előlről.
 Ha ütközés, újrakezdi random idő után.

###Hogyan működik a CSMA/CD protokoll? (CD -> Collision Detection: ütközés érzékelés)
-Ütközés érzékelés esetén meg lehessen szakítani az adást. Minden állomás küldés közben megfigyeli a csatornát, ha ütközést tapasztalna, akkor megszakítja az adást, és véletlen ideig várakozik, majd újra elkezdi leadni a keretét.

###Hogyan működik az alapvető bittérkép eljárás?
-i-edik állomás az i-edik versengési időrésben jelzi küldési szándékát adatszórással
 a versengési időszak végére minden állomás ismeri a küldőket
 a küldés a sorszámok szerinti sorrendben történik

###Hogyan működik a bináris visszaszámlálás protokoll?
-Minden állomás azonos hosszú bináris azonosítóval rendelkezik.
 A forgalmazni kívánó állomás elkezdi a bináris címét bitenként elküldeni a legnagyobb helyi értékű bittel kezdve. Az azonos pozíciójú bitek logikai VAGY kapcsolatba lépnek ütközés esetén. Ha az állomás nullát küld, de egyet hall vissza, akkor feladja a küldési szándékát, mert van nála nagyobb azonosítóval rendelkező küldő

###Mi a korlátozott versenyes protokollok célja?
-Ötvözni a versenyhelyzetes és ütközésmentes protokollok jó tulajdonságait

###Hogyan működik az adaptív fabejárási protokoll?
-0-adik időrésben mindenki küldhet.
 Ha ütközés történik, akkor megkezdődik a fa mélységi bejárása.
 A rések a fa egyes csomópontjaihoz vannak rendelve.
 Ütközéskor rekurzívan az adott csomópont bal illetve jobb gyerekcsomópontjánál folytatódik a keresés.
 Ha egy bitrés kihasználatlan marad, vagy pontosan egy állomás küld, akkor a szóban forgó csomópont keresése befejeződik.

###Mi a repeater, és mire használják?
-Analóg eszköz, mely két kábelszegmenshez csatlakozik. Felerősíti a jelet és továbbítja. (fizikai réteg)

###Mi az elosztó (Hub) és mire használják?
-több bemenettel rendelkezik; a beérkező keretet minden vonalon továbbítja; ha két keret egyszerre érkezik, ütközni fognak; általában nem erősíti a jelet (fizikai réteg)
###Mi a bridge (híd), és mire használják?
-Az adatkapcsolati rétegben működő eszköz, amely LAN-ok összekapcsolását végzi.
 A bejövő keretet csak a megfelelő LAN-hoz továbbítja (forgalomirányítás az adatkapcsolati rétegben).
 A portok külön ütközési tartományt képeznek és különböző sebességű hálózatokhoz csatlakozhatnak.
 Pufferelést, csomagfeldolgozást végez, továbbító táblázatot (forwarding table) tart karban.

###Mi a "backward learning" (Címek tanulása) lényege?
-A hidak használják ezt a módszert a keretek továbbításához használt táblázatuk feltöltésére. Ha egy keret érkezik hozzájuk, megnézik a forráscímet (feladót) és "megtanulják", hogy az melyik porton érhető el (ahonnan a keret jött), és ezt bejegyzik a táblázatukba.

###Ismertesse a feszítőfa protokoll (STP) lépéseit?
- ...

6. előadás
----------
Mi a forgalomirányító algoritmusok definiciója?
Mi a statikus (nem adaptív) forgalomirányító algoritmusok fő jellemzője?
Mi az adaptív forgalomirányító algoritmusok fő jellemzője?
Mit mond ki az optimalitási elv (forgalomirányítás esetén)?
Mi a távolságvektor (distance vector) alapú forgalomirányítás lényege?
Magyarázza el a végtelenig számolás problémáját!
Mik a link-state (kapcsolatállapot) alapú forgalomirányítás megvalósításának lépései?
Hasonlítsa össze a távolságvektor alapú és a link-state (kapcsolatállapot) alapú forgalomirányítást.
Mi a hierarchikus forgalomirányítás lényege?
Mit nevezünk adatszórásnak vagy broadcasting-nak?
Sorolja fel az adatszórás megvalósítási lehetőségeit.
Mi a többcélú forgalomirányítás lényege?
Mi a visszairányú továbbítás (reverse path forwarding) lényege?
Mit nevezünk többesküldésnek vagy multicasting-nak?
Mire szolgál a DF bit az IPv4 fejlécében?
Mire szolgál a MF bit az IPv4 fejlécében?
Mire szolgál az azonosító (azonosítás) az IPv4 fejlécében?
Mire szolgál a darabeltolás (fragment offset) az IPv4 fejlécében?
Mire szolgál az élettartam (TTL) mező az IPv4 fejlécében?
Mi az IPv4 cím és hogyan ábrázoljuk?
Milyen IP cím osztályokat ismer? Jelemezze ezeket!
Milyen speciális IPv4 címek léteznek?
Mi az alhálózati maszk és mire szolgál?

7.előadás:
----------
Mi az a NAT doboz és mire szolgál?
Mi az az MTU és mire szolgál?
Hogyan működik az MTU felderítés?
Hogyan ÉS hol történik az fragmentált/darabolt IP csomagok helyreállítása?
Mi az IPv6 cím és hogyan ábrázoljuk?
Mi a localhost IPv6 esetén?
Soroljon fel két olyan lehetőséget (az EA-on látott 4-ből), melyet az IPv6 támogat, de az IPv4 esetén nem találkoztunk vele?
Mi gátolja az IPv6-ra való átállást?
Hogyan oldható meg az IPv6 csomagok átvitele IPv4 hálózat felett?
Mire szolgál az ICMP protokoll?
Mi lehet a hatása egy ICMP forráslefojtás csomagnak?
Mire szolgál az ARP és hogyan működik?
Mire szolgál a RARP és hogyan működik?
Mi az a DHCP és hogyan működik?
Milyen lehetőségeket támogat a DHCP?
Mi DHCP esetén a cím bérlés?
Mi az AS (Autonóm rendszer)?
Miért van szükségünk AS-ekre?
Mi azonosít egy AS-t?
Milyen routing megoldást/protokollt alakalmaz a BGP?
Hogyan működik az útvonalvektor protokoll?
Mit értünk az alatt, hogy minden AS saját útválasztási politikát alkalmazhat?
Sorolja fel az IGP, iBGP és eBGP szerepét?
Mikor mondjuk két AS-ről, hogy azok össze vannak kötve?
Adjon meg 3 példát forgalomirányítási korlátozásra AS-ek közötti routing esetén.
Mit nevez a BGP csonka hálózatnak?
Mit nevez a BGP többszörösen bekötött hálózatnak?Mit nevez a BGP tranzit hálózatnak?
Mire szolgál és hogyan működik a VPN (virtuális magánhálózat)?

8.előadás:
----------
Mire szolgál a TCP protokoll? Mik a főbb jellemzői?
Mire szolgál az UDP protokoll? Mik a főbb jellemzői?
Hogyan történik egy TCP kapcsolat felépítése? Mik a lépései?
Hogyan történik egy TCP kapcsolat lezárása?
Mit mondhatunk a TCP átviteléről az ablak és az RTT függvényében?
Mit jelent az RTO, és hol használják?
Hogyan történik az RTT becslés az eredeti TCP esetén?
Mit mondhatunk TCP esetén a hibadetektálásról?
Mi a fogadó által felajánlott ablakméret (wnd)?
Mit jelent, ha a fogadó wnd=0-át küld?
Mit nevezünk folyamvezérlésnek?
Mit nevezünk torlódásnak TCP esetén?
Mi a TCP Nagle algoritmus működési alapelve?
Mi a TCP Karn algoritmusa? A kapcsolódó problémát is ismertesse!
Vázolja a TCP Incast problémát!


9.előadás: (TCP folyt.)
----------
Mi az a torlódási ablak? Mire szolgál?
Mi az a "slow start" TCP esetén?
Mi az AIMD TCP Tahoe esetén?
Mi a gyors újraküldéss TCP RENO esetén?
Mit jelenthet az ha három nyugta-duplikátum érkezik egymás után?
Mi a gyors visszaállítás TCP Reno esetén?
Mivel több a TCP NewReno? Mi a problémája az alkalmazott megoldásnak?
Mi a probléma nagy késleltetés-sávszélesség szorzatú hálózatok esetén?
Mely TCP variánsok használatosak napjainkban?
Hogyan működik a Compound TCP?
Hogyan működik a CUBIC TCP?
Mik a TCP problémái kis folyamok esetén?
Mik a TCP problémái vezetéknélküli hálózatok esetén?
Mi a DoS támadás? Miért probléma ez TCP esetén?

10.előadás:
-----------
Mit nevezünk munkamenetnek az ISO/OSI referencia modellben?
Mit tud a DNS tartománynevek (körzetnevek) rendszeréről?
Mik azok a TLD-k? Adjon meg 4 példát.
Mik azok a DNS erőforrás rekordok? Mit tárolnak (1-2 példa)?
Mit tud a (DNS) zónákról?
A névfeloldásnál mit neveznek iteratív lekérdezésnek? Mik a jellemzői?
A névfeloldásnál mit neveznek rekurzív lekérdezésnek? Mik a jellemzői?
Írja le a lokális névszerverek legfőbb jellemzőit!
Mit jelent DNS esetén a cache? Mire jó?
Ismertesse egy HTML oldal lekérésének 5 lépését!
Mit nevezünk statikus weboldalnak?
Mit nevezünk dinamikus weboldalnak?
Mi az a PLT? Mit mérünk vele?
Mik azok a párhuzamos és perzisztens kapcsolatok?
Hogyan működik a cache "HTTP esetén"?
Mire jó egy HTTP proxy? Hogyan működik?
Mi a CDN? Milyen problémát old meg? Hogyan valsítja ezt meg?
Mik a p2p hálózatok legfontosabb jellemzői?
Mi a szerepe egy peer-nek egy p2p hálózatban?
Mik egy torrent letöltésének lépései (4 lépés)?
Mit nevezünk choke peer-nek?
Mi az a seed peer?

