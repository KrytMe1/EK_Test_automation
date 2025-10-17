# Tesztautomatizálási kérdések

## Tesztelési alapok (ISTQB-hez kapcsolódó)
<img src="https://www.mindsmapped.com/wp-content/uploads/2016/06/ISTQB.jpg" alt="image" width="300" height="220">

## A tesztelés alapjai:
#### Mi a tesztelés célja? Mi nem az?
A tesztelés célja a szoftverfejlesztésben (de más területeken is) az, hogy hibákat (defekteket) találjunk, és bizonyítékot szerezzünk a rendszer minőségéről, viszont nem cél a 100%-os lefedettség mindenáron vagy a fejlesztők munkájának hibáztatása.
#### Mi a kapcsolat a tesztelés és a hibamegelőzés között?
A tesztelés célja a hibák megtalálása, míg a hibamegelőzés célja azok kialakulásának elkerülése. A tesztelés visszajelzést ad, ami segítheti a hibamegelőzést a jövőben. Mindkettő a minőség javítását szolgálja, de más szakaszban és módon.
#### Miért fontos, hogy a tesztelők függetlenek legyenek a fejlesztőktől?
Azért fontos, mert a független tesztelők objektívebben vizsgálják a rendszert, nem befolyásolja őket az a tudás vagy elfogultság, amit a fejlesztők munkája közben szereztek. Ez növeli a hibák felfedezésének esélyét és a tesztelés megbízhatóságát.
#### Mi a veszélye annak, ha a fejlesztő maga teszteli a saját kódját?
Ha a fejlesztő maga teszteli a saját kódját, akkor fennáll a veszély, hogy:

elfogultság miatt nem veszi észre a hibákat,

csak azokat az eseteket nézi meg, amiket ő maga írt vagy gondolt,

kevésbé alaposan vagy részletesen vizsgálja a kódot,

így a hibák nagy része rejtve maradhat.
#### Mik a tesztelési alapelvek?
A tesztelési alapelvek a szoftvertesztelés irányelvei, amelyek segítenek hatékonyabbá és eredményesebbé tenni a tesztelést. A legfontosabbak:

Tesztelés a hibák jelenlétének kimutatására irányul – nem bizonyítja, hogy nincs hiba, csak hogy vannak-e.

Teljes tesztelés nem lehetséges – nem lehet minden esetet lefedni, ezért prioritásokat kell felállítani.

Korai tesztelés előnyös – minél korábban kezdjük a tesztelést, annál hatékonyabb a hibák felderítése.

Hibák csoportosulnak – a hibák általában koncentráltan jelentkeznek, ezért érdemes a kockázatos területekre fókuszálni.

Nem minden hiba kritikus – egyes hibák kevésbé fontosak, a prioritások alapján kell kezelni.

Tesztelés függ a környezettől – a tesztelés eredménye nagyban függ a környezeti tényezőktől (pl. hardver, szoftver verziók).
#### Mit jelent az „alapvető tesztelési elv”, hogy „a kimerítő tesztelés lehetetlen”?
Az „a kimerítő tesztelés lehetetlen” elv azt jelenti, hogy nem lehet minden lehetséges bemenetet, állapotot és forgatókönyvet végigtesztelni egy szoftverben, mert:

túl sok lehetséges kombináció van,

idő és erőforrás véges,

ezért mindig csak kiválasztott, legfontosabb eseteket lehet tesztelni.

Ezért fontos a tesztelési stratégia és a kockázatok alapján priorizálni.
#### Mit jelent az „alapvető tesztelési elv”, hogy „a hibák halmozódnak”?
Az „a hibák halmozódnak” elv azt jelenti, hogy a hibák nem egyenletesen oszlanak el a szoftverben, hanem általában egy kis részén összpontosulnak. Tehát egyes modulokban vagy funkciókban sok hibát találunk, míg más részek viszonylag hibamentesek. Ez segít a tesztelőknek, hogy a kockázatosabb területekre fókuszáljanak.
#### Mit jelent az „alapvető tesztelési elv”, hogy „a tesztelés a kontextustól függ”?
Az „a tesztelés a kontextustól függ” elv azt jelenti, hogy a tesztelési stratégia, módszerek és eszközök mindig a konkrét projekt, rendszer és környezet sajátosságaihoz igazodnak. Más szavakkal:

egy üzleti alkalmazás tesztelése más megközelítést igényel, mint egy beágyazott rendszeré,

a célok, kockázatok, felhasználók, technológia mind befolyásolják, hogyan és mit tesztelünk.

Tehát nincs „egy mindenre jó” tesztelési módszer, mindig a helyzethez kell igazítani.


## 2. Tesztelés a szoftverfejlesztés életciklusán át
#### Mik a tesztszintek, és mi a különbség köztük?
A tesztszintek:

Egységteszt: Kis kódrészek tesztelése, fejlesztők végzik.

Integrációs teszt: Modulok együttműködésének tesztelése.

Rendszerteszt: Az egész rendszer tesztelése, független tesztelők végzik.

Elfogadási teszt: Felhasználók tesztelik, hogy megfelel-e az üzleti igényeknek.

Különbség: a tesztelés terjedelme és célja változik, valamint hogy ki végzi.
#### Miért nem érdemes mindig ugyanazokat a teszteseteket futtatni (regressziós torzítás)?
Nem érdemes mindig ugyanazokat a teszteseteket futtatni, mert így **átlátszóvá, unalmassá válik a tesztelés**, és **elfogultság (regressziós torzítás)** alakulhat ki: a tesztelők hajlamosak csak az ismert hibákra koncentrálni, így új vagy rejtett hibák könnyen elkerülhetik a figyelmet. Ez csökkenti a tesztelés hatékonyságát és a szoftver minőségét.
#### Mi az egységtesztelés (unit testing)? Ki felelős az egységtesztek írásáért?
Az egységtesztelés a szoftver legkisebb részeinek (pl. függvények, metódusok) különálló tesztelése, hogy meggyőződjünk azok helyes működéséről.

Az egységtesztek írásáért elsősorban a fejlesztők felelősek.
#### Mi a különbség a verifikáció és a validáció között?
A verifikáció azt ellenőrzi, hogy a termék megfelelően készült-e el a specifikáció szerint („Jól csináljuk-e a dolgot?”).

A validáció pedig azt vizsgálja, hogy a termék megfelel-e a felhasználói igényeknek és elvárásoknak („Jót csinálunk-e?”).
#### Mik a tesztelési típusok, és mi a különbség köztük?
Tesztelési típusok:

* **Funkcionális:** a rendszer funkcióit ellenőrzi, hogy jól működnek-e.
* **Nem-funkcionális:** a rendszer tulajdonságait vizsgálja (pl. teljesítmény, biztonság).

Különbség: mit tesztelünk (funkció vagy jellemző).
#### Mi a különbség a fehér doboz, szürke doboz és fekete doboz tesztelés között?
* **Fehér doboz tesztelés:** A tesztelő ismeri a belső kódot és működést, belső logikát vizsgál.
* **Fekete doboz tesztelés:** Csak a bemeneteket és kimeneteket ismeri, belső működés rejtett.
* **Szürke doboz tesztelés:** Részben ismeri a belső működést, részben külső nézőpontból tesztel.
Különbség a belső ismeretek mértékében van.
#### Mi a különbség a felhasználói elfogadási teszt (UAT) és a rendszerteszt között?
Rendszerteszt: Az egész kész rendszert tesztelik, hogy megfelel-e a követelményeknek, általában független tesztelők végzik.

Felhasználói elfogadási teszt (UAT): A végfelhasználók vagy megrendelők végzik, hogy ellenőrizzék, a rendszer megfelel-e az üzleti igényeknek és használatra kész-e.

Különbség: a célközönség és a fókusz (technikai megfelelés vs. üzleti elfogadás).
#### Mi a különbség a statikus és dinamikus tesztelés között?
Statikus tesztelés: Kód vagy dokumentum elemzése futtatás nélkül (pl. kódreview, analízis).

Dinamikus tesztelés: A szoftver futtatása tesztesetekkel, hogy működés közben vizsgáljuk.

Különbség: futtatjuk-e a szoftvert vagy sem.