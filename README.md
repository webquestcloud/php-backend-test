# WebQuest.cloud – Symfony Backend Fejlesztői Tesztfeladat

Köszönjük az érdeklődésedet a WebQuest.cloud iránt.

A kiválasztási folyamat részeként egy rövid backend fejlesztési feladatot kérünk a jelentkezőktől. A feladat célja, hogy képet kapjunk arról, hogyan gondolkodsz backend architektúráról, hogyan strukturálod a kódot, illetve mennyire követed a Symfony ökoszisztéma bevett gyakorlatait.

A feladat egy egyszerű REST API megvalósítása egy motor kölcsönző rendszerhez. A projekt megvalósítása során a forráskód nyelve kötelezően angol. A változónevek, propertyk, osztálynevek, endpointok és egyéb kódelemek angol elnevezéseket használjanak.

A projekt története (commit history) legyen követhető. Kérjük ne egyetlen commitban kerüljön feltöltésre a teljes megoldás.

---

## Technológiai elvárások

A megoldásnál az alábbi technológiák használata elvárt:

- PHP 8+
- Symfony (aktuális stabil verzió)
- Doctrine ORM
- REST alapú JSON API
- relációs adatbázis (MySQL / PostgreSQL / SQLite)

Frontend nem szükséges.

---

## Domain

A rendszer két fő entitással dolgozik:

- Motorok
- Foglalások

---

## Motor

A motor entitásnak minimum az alábbi adatokat kell tartalmaznia:

- azonosító
- márka
- modell
- évjárat
- napi bérleti díj
- elérhetőségi állapot

A motorokhoz alapvető CRUD műveletek szükségesek egy REST API-n keresztül.

---

## Foglalás

A foglalás egy adott motorra vonatkozó bérlést reprezentál.

A foglalás legalább az alábbi adatokat tartalmazza:

- azonosító
- a motor hivatkozása
- ügyfél neve
- kezdő dátum
- záró dátum
- teljes ár

A rendszernek lehetővé kell tennie új foglalás létrehozását és a meglévő foglalások lekérdezését.

---

## Üzleti szabály

Egy motor nem foglalható le olyan időintervallumra, amely átfed egy már létező foglalással.

A rendszernek ezt a feltételt minden új foglalás létrehozásakor ellenőriznie kell.

---

## Ár számítás

A foglalás teljes ára automatikusan kerül kiszámításra a motor napi bérleti díja és a foglalás időtartama alapján.

A számítás logikáját a backendnek kell kezelnie.

---

## Validáció

A rendszernek kezelnie kell az alapvető adatvalidációt, például:

- kötelező mezők
- dátum intervallum helyessége
- létező motorra történő hivatkozás
- foglalási ütközések kezelése

---

## Kódszervezés

A megoldásnál fontos szempont a kód szervezettsége és karbantarthatósága.

Külön figyelmet fordítunk arra, hogy:

- mennyire tiszta a projekt struktúrája
- hogyan választod szét a felelősségi köröket
- mennyire követed a Symfony bevett mintáit
- mennyire olvasható és követhető a kód

Nem szükséges túlbonyolított architektúra, de a logika ne kerüljön indokolatlanul kontrollerekbe.

---

## Hibakezelés

Az API-nak megfelelő HTTP válaszokat kell visszaadnia hibás vagy érvénytelen kérések esetén.

---

## Időkeret

A feladat várható megoldási ideje:

2–4 óra

Nem cél, hogy ennél jelentősen több időt tölts vele.

---

## Beküldés

A megoldást egy publikus Git repository formájában kérjük beküldeni.

A repository tartalmazzon egy rövid leírást arról:

- hogyan indítható a projekt
- milyen adatbázist használ
- hogyan tesztelhető az API

---

## Kérdés

A README végén kérjük röviden válaszolj az alábbi kérdésre:

Ha több időd lenne a projektre, milyen irányban fejlesztenéd tovább vagy refaktorálnád?

---

WebQuest.cloud
Engineering Team
