# xmlabuse

Ebben a repository-ban olyan tesztfájlokat próbálok összeállítani, amelyek egy XML-t fogadni képes betöltő rendszer teszteléséhez szeretnénk felhasználni egy projekten.

- A víruskereső triggerelésére a kiindulási alapot az EICAR oldaláról letölthető txt tesztfájl képezi (https://www.eicar.org/download-anti-malware-testfile/).
A txt fájlt a víruskereső "virus - Eicar-Test-Signature" néven ismeri fel.

Cél: olyan tartalmú XML állományok összeállítása, melyek egy backend víruskeresője felismer.

#TODO: fájlok megnevezése feltöltés után

- Invalid XML-eknél a hibás, lezáratlan formátumon kívül az XML parser gyengeségeit kihasználó, 

- Szolgáltatásmegtagadást (DoS) eredményezhető problémát okozó "Billion laughs attack" (https://en.wikipedia.org/wiki/Billion_laughs_attack) tartalmat,

- XXE típusú támadásokat (https://en.wikipedia.org/wiki/XML_external_entity_attack) előidéző fájlok.

Cél: olyan invalid, vagy a betöltés mechanizmusát megaksztó, akár script-eket tartalmazó XML állományok összeállítása, melyek egy backend-nél problémát okozhatnak, ezek a rendszerben megfelelően legyenek kezelve, hogy ne történhessen visszaélés.

#TODO: fájlok megnevezése feltöltés után

- API POST request tartalmú XML-ek betöltése akár a feltöltő rendszerbe fájlként, akár később a kérést a végpontokra megfelelően beállítás után API hívásként felhasználva (a tesztelendő rendszeren jelenleg a JSON még nem scope).

Cél: betöltéskor tartalmilag invalid fájlok (szintaktikailag helyesek) ellenőrzése,  hogy a rendszer hogyan kezeli.

#TODO: fájlok megnevezése feltöltés után
