# Alapfeladat, CR0: Kassza program a JóÁr áruházban

Ebben a repoban 3 file található:
* ProgTech_osszetett_beugro_CR0.pdf: Leírja a feladatot részletesen, példákkal.
* AruhazCR0Tesztek.java: A feladathoz tartozó unit teszteket tartalmazza.
* README.md: Szintén leírja a feladatot, de kevésbé reszletesen.

Az Ön feladata az alapfeladat, azaz a CR0, megoldása! Ez az egész CR-sorozatra épülő gyakorlófeladat kezdőpontja. A következő alfejezet a CR1. A CR1-hez csak akkor kezdjen hozzá, ha a CR0 teljesen kész. Javasoljuk, hogy használja az alfejezet végén lévő egységteszteket. Illetve, használja a hangulatvezérelt kódolás eszközeit a feladat megoldásához! A CR0 szövege itt kezdődik.

Az Ön feladata az lesz, hogy elkészítse a JóÁr áruház kasszarendszerének alapverzióját.

A kasszarendszer központi eleme a következő metódus:
double getKosárÁr(Kosár kosár)

Ez a metódus egy vásárlás végösszegét számítja ki forintban. A visszatérési érték tehát egy szám, amely a vásárlás során fizetendő végső összeget jelenti készpénzes fizetés esetén.

A feladat során az alábbi szabályokat kell figyelembe venni:

A kosár kétféle terméket tartalmazhat:
*	alma, kilogrammban megadva (pl. 1.5 kg),
*	banán, kilogrammban megadva (pl. 3 kg),
*	az egyes termékek többször is benne lehetnek a kosárban, ilyenkor össze kell adni az alma mennyiséget, illetve a banán mennyiséget.

A termékek alapárai a következők:
*	1 kg alma ára 500 Ft.
*	1 kg banán ára 450 Ft.

A JóÁr áruház normál időszakában a következő kedvezmények érvényesek:
*	Legalább 5 kg alma vásárlása esetén 10% kedvezmény az alma összárára.
*	Legalább 20 kg alma vásárlása esetén 15% kedvezmény az alma összárára.
*	Legalább 2 kg banán vásárlása esetén 10% kedvezmény a banán összárára.

Jelenleg a rendszer csak készpénzes fizetést támogat. Készpénzes fizetés esetén a kerekítés szabálya a következő. A végösszeget 5 forintra kell kerekíteni, a következő szabályok szerint:
*	Ha az összeg 0,01–2,49 Ft-ra végződik kerekítés lefelé a legközelebbi 0-ra.
*	Ha az összeg 2,50–4,99 Ft-ra végződik kerekítés felfelé a legközelebbi 5-re.
*	Ha az összeg 5,01–7,49 Ft-ra végződik kerekítés lefelé a legközelebbi 5-re.
*	Ha az összeg 7,50–9,99 Ft-ra végződik kerekítés felfelé a legközelebbi 0-ra.
