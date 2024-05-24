# xmlabuse

Ebben a repository-ban olyan tesztfájlokat próbálok összeállítani, amelyek egy XML-t fogadni képes betöltő rendszer teszteléséhez szeretnénk felhasználni egy projekten.

---

- A víruskereső triggerelése

A kiindulási alapot az [EICAR oldaláról letölthető txt tesztfájl](https://www.eicar.org/download-anti-malware-testfile/) képezi.
A txt fájlt a víruskereső "virus - Eicar-Test-Signature" néven ismeri fel.

Cél: olyan tartalmú XML állományok összeállítása, melyek egy backend víruskeresője felismer.

fájlok:

- [x] eicar.txt - az EICAR oldaláról letöltött ártalmatlan próbavírus kódját tartalmazza
- [ ] teszt vírust tartalmazó xml állomány

---

- Az XML parser gyengeségeit kihasználó támadások szimulálása

Szolgáltatásmegtagadást (DoS) eredményezhető problémát okozó ["Billion laughs attack"](https://en.wikipedia.org/wiki/Billion_laughs_attack) tartalmat,
[XXE típusú támadásokat](https://en.wikipedia.org/wiki/XML_external_entity_attack) előidéző fájlok.

Cél: Az XML parser gyengeségeit kihasználó támadások szimulálása, a betöltés mechanizmusát megakasztó, akár script-eket tartalmazó XML állományok összeállítása, melyek egy backend-nél jogosulatlan hozzáférést vagy egyéb problémát okozhatnak, ezek megfelelő kezelésének ellenőrzése.

Megelőzés: [OWASP XML External Entity Prevention Cheat Sheet](https://cheatsheetseries.owasp.org/cheatsheets/XML_External_Entity_Prevention_Cheat_Sheet.html)

fájlok:

- [x] bla-basic.xml - BillionLaughsAttack a Wiki oldalon található kód minta
- [x] OWASP-template_accessing_local_resource.xml - [OWASP](https://en.wikipedia.org/wiki/OWASP) xml injection minta
- [x] OWASP-template_PHP_remote_code_exec.xml - [OWASP](https://en.wikipedia.org/wiki/OWASP) xml injection minta
- [ ]
- [ ]

---

- Nem megfelelően formázott XML-ek (pl lezáratlan).
Cél: Egyéb invalid, fájlok kezelésének ellenőrzése.

fájlok:
- [ ] hibásan formázott XML
- [ ] API POST tartalom (de szintaktikailag helyes XML)

