# Elektryka od zera

Z wykształcenia jestem fizykiem i mechatronikiem — nie elektrykiem, ale zrobię co mogę, żeby Wasza wiedza była jak najbardziej ugruntowana, jak tylko się da, zanim zaczniecie budować i planować swoją instalację. Wychodzę z założenia, że im większą będziemy mieli świadomość, jak coś działa od środka, tym więcej też będziemy mieli pokory, planując i montując taką instalację.

Nigdy nie zapominajmy, że zarówno niskie stałe napięcie, jak i 230 V może być niebezpieczne! Pierwsze, mimo bycia bagatelizowanym, z powodu wysokich prądów płynących przez przewody, niesie ze sobą ryzyko przegrzań, a nawet pożarów! Wysokie napięcie przy bezpośrednim kontakcie jest śmiertelne — tego chyba wszyscy jesteśmy świadomi.  

Ten rozdział jest wstępem do tematu. Nie ma na celu przedstawić Wam katalogu sprzętu i konkretnych schematów. Tym zajmiemy się dopiero w kolejnym tomie tej książki. 

Jeśli nie wiecie, czym się różni prąd od napięcia, do czego służy falownik w kamperze oraz dlaczego amperogodziny bez woltów za dużo nam nie mówią, to koniecznie przeczytajcie ten rozdział od deski do deski. Najlepiej dwa razy :)

Jeśli czujecie się naprawdę pewni w świecie elektryki, kładliście bądź naprawialiście przydomowe instalacje. Wiecie, czym różni się moc czynna od pozornej, i umiecie policzyć własny bilans energii w watogodzinach — możecie go swobodnie pominąć. 

## Fizyka

Będę starał się opisać zjawiska fizyczne najbardziej obrazowo i najprościej, jak potrafię. To znaczy, że będę stosował uproszczenia, więc nie traktujcie tego rozdziału jako podręcznika. 

### Co to jest prąd?

Prąd elektryczny to uporządkowany ruch ładunków elektrycznych, w praktyce najczęściej elektronów. Płynie w przewodnikach, czyli materiałach, w których elektrony mogą się swobodnie przemieszczać. Przewodników jest wiele, ale skupimy się na metalach, bo to z nich zrobione są przewody w instalacjach elektrycznych.

Metale mają szczególną budowę chemiczną. Każdy atom oddaje elektrony ze swojej ostatniej powłoki do wspólnej puli, tworząc one coś w rodzaju „chmury”, która swobodnie porusza się między atomami. Dopóki na elektrony nic nie oddziałuje z zewnątrz, poruszają się one chaotycznie — w losowych kierunkach. Gdy jednak do końców przewodu przyłożymy napięcie, na elektrony zaczyna działać siła i „chmura” dostaje jeden wspólny kierunek. To właśnie jest prąd.

Ciekawostka: same elektrony wcale nie poruszają się z niesamowitymi prędkościami. W domowej instalacji przemieszczają się o ułamki milimetra na sekundę. Jednakże ich wspólny ruch propaguje się przez cały przewód niemal natychmiast. To jak z rurką pełną wody: naciskasz z jednej strony, a z drugiej woda wypływa natychmiast, choć żadna kropla nie przebyła całej rury :) Analogie z wodą są mocnym uproszczeniem, ale jeszcze będziemy do nich wracać, bo naprawdę dobrze obrazują temat. 

Druga ciekawostka: umownie przyjmuje się, że prąd płynie od plusa do minusa. Ustalono to, zanim odkryto elektron! Elektrony mają ładunek ujemny, więc naprawdę płyną w przeciwną stronę, od minusa (który je odpycha) do plusa (który je przyciąga).

### Jednostki i pojęcia

Najłatwiej zrozumieć te pojęcia znów przez porównanie do ruchu wody w rurach.

#### Napięcie (U), czyli wolt (V)

To „ciśnienie”, które pcha elektrony. Im wyższe napięcie, tym mocniej są popychane. W polskim gniazdku mamy 230 V, w baterii AA 1,5 V, w USB standardowo 5 V (w USB-C nawet do 20 V). Samo napięcie nic jeszcze nie robi, to tylko gotowość do pchania. Bateria w szufladzie tak jak gniazdko „daje” napięcie cały czas, ale prąd nie płynie, bo nie ma zamkniętego obwodu. Tak samo, jak woda pod ciśnieniem z zamkniętym zaworem. Tryśnie natychmiast, jak go odkręcimy. 

#### Natężenie (I), czyli amper (A)

To ilość ładunku, która przepływa przez przekrój przewodu w ciągu sekundy, czyli „ile wody płynie w rurze”. Dla ciekawskich: jeden amper to około 6 trylionów elektronów na sekundę (6,24 · 10¹⁸). Ładowarka telefonu daje 1–3 A, czajnik pobiera około 10 A, a typowy bezpiecznik w mieszkaniu wyłącza obwód przy 16 A. Z tego można wywnioskować, że dziesięć amperów to już jest dość sporo, a 16 A to naprawdę dużo, w szczególności, jeśli chodzi o obciążenie ciągłe. Dla porównania rozrusznik samochodu potrafi pociągnąć z akumulatora kilkaset A, ale trwa to sekundy, a przewody do niego są grube jak palec. To właśnie natężenie, a nie napięcie, decyduje o tym, jak gruby musi być przewód (napięcie decyduje z kolei o grubości izolacji). Dlatego cienki kabel USB wytrzyma 3 A, a do czajnika czy grzejnika potrzebny jest już porządny przewód.

#### Opór (R), czyli om (Ω)

Mówi, jak bardzo materiał „stawia się” przepływowi, czyli „jak wąska jest rura”. Napięcie, natężenie i opór łączy prawo Ohma: I = U / R. Przy tym samym napięciu przez mały opór popłynie duży prąd, przez duży opór mały. Dlatego bezpośrednie połączenie dwóch przewodów pod napięciem (zwarcie) jest groźne: opór spada prawie do zera (łączymy przewodniki), prąd gwałtownie rośnie i przewody się grzeją. 

#### Moc (P), czyli wat (W)

Mówi, ile energii urządzenie zużywa w każdej sekundzie. Liczy się prosto: moc = napięcie × natężenie, czyli P = U · I. Czajnik na 230 V pobierający 10 A ma moc 2300 W. Żarówka LED około 10 W, ładowarka telefonu najczęściej około 20 W.

#### Energia (E), czyli dżul (J) i kilowatogodzina (kWh)

Moc mówi, ile energii urządzenie pobiera w każdej sekundzie. Energia to ta moc zsumowana przez cały czas działania: energia = moc × czas. Fizycy liczą ją w dżulach (J), ale dżul jest bardzo małą jednostką niewygodną do praktycznego stosowania, więc na co dzień używamy kilowatogodzin. Jedna kilowatogodzina to urządzenie o mocy 1000 W (czyli jednego kilowata) działające przez godzinę albo urządzenie 100 W przez dziesięć godzin. Czajnik 2300 W gotujący wodę przez trzy minuty zużywa około 2300 W * 3/60 h = 115 Wh, czyli 0,115 kWh. To właśnie za zużyte kilowatogodziny płacimy na rachunku od dostawcy pądu w domu.

##### Pojemność baterii i akumulatorów

W tych samych jednostkach podaje się pojemność baterii i akumulatorów, bo bateria to po prostu magazyn energii. Bateria telefonu mieści około 20 Wh, duży powerbank około 70 Wh.

Kilowatogodzina jest jednostką kompletną: mówi, ile energii jest w magazynie, i nie trzeba do niej nic dodawać. Można wprost porównać akumulator 12 V z akumulatorem 24 V, bo kWh w obu przypadkach oznacza to samo: ilość energii, jaką akumulator może oddać. 

##### Amperogodziny to nie energia

Inaczej jest z amperogodzinami. Amperogodzina (Ah) i miliamperogodzina (mAh) opisują tylko ładunek, czyli ile prądu i przez jaki czas ogniwo może oddać, a nic nie mówią o tym, jak mocno ten prąd jest „popychany” przez napięcie. Dopiero podane razem z napięciem, z jakim akumulator pracuje, dają energię. Sama liczba mAh/Ah bez napięcia nie pozwala niczego porównać.

Przeciętny akumulator samochodowy ma 80 Ah przy 12 V. Duży powerbank do telefonu ma 20 000 mAh.  Producenci umyślnie używają miliamperogodzin, żeby liczba wydawała się większa. Na papierze 20 000 wygląda na więcej niż 80, ale wystarczy postawić oba obok siebie, żeby zwątpić :) Dla praktyki spróbujmy to obliczyć. Standardowy powerbank pracuje z napięciem 3,7 V. 

Akumulator samochodowy: 80 Ah * 12 V = 960 Wh
Duży powerbank do telefonu: 20 000 mAh * 3,7 V = 20 Ah * 3,7 V = 74 Wh

Z obliczeń wyraźnie widać, że akumulator samochodowy przechowuje prawie 1 kWh energii, podczas gdy powerbank do telefonu przechowuje 13 razy mniej.

### Dlaczego przewody się grzeją?

Powyżej pisałem o tym, że elektrony mogą swobodnie poruszać się pomiędzy atomami metalu, a po przyłożeniu napięcia dostają jeden wspólny kierunek. Możemy sobie wyobrazić elektrony lecące pomiędzy twardymi kulami, czyli atomami metalu, z którego zbudowany jest przewód. Od czasu do czasu elektron uderzy w atom, wyhamuje i wprawi go w drgania. A temperatura to nic innego jak miara tego, jak mocno drgają atomy :) Im mocniej drgają, tym cieplejszy jest przewód.

Im więcej elektronów naraz płynie przez przewodnik, tym częściej któryś z nich trafia w atom. Tak więc im większy prąd płynie przez przewód, tym bardziej się on nagrzewa. I to mocno: dwa razy większy prąd to aż cztery razy więcej ciepła. Wynika to wprost ze wzorów, które już znamy. Skoro P = U · I, a z prawa Ohma U = I · R, to moc zamieniana w przewodzie na ciepło wynosi P = I² · R.

Im większą powierzchnię w przekroju poprzecznym ma przewód, czyli im jest on grubszy, tym mniejszy stawia opór. Przez grubszy przewód w każdej sekundzie przepływa tyle samo elektronów, ale mają do dyspozycji szerszą drogę, więc płyną wolniej i uderzają w atomy słabiej. To jak z szerszą rurą, którą ta sama ilość wody płynie spokojniej. Grubszy przewód ma też większą powierzchnię, którą oddaje ciepło do otoczenia.

Dlatego przewody dobiera się pod maksymalny prąd, jaki będzie przez nie przepływał. Tak, żeby były w stanie wystarczająco szybko oddawać ciepło, zanim nagrzeją się na tyle, by stopiła się albo zapaliła izolacja. Standardowy przewód w mieszkaniu, którym płynie do 16 A, ma 2,5 mm² przekroju poprzecznego. Obwody oświetlenia, zabezpieczone bezpiecznikiem 10 A, robi się cieńszym przewodem 1,5 mm².

### Prąd stały i prąd przemienny

Do tej pory pisałem raz o akumulatorze, raz o gniazdku, jakby płynął w nich ten sam prąd. Wszystko, co padło wyżej, czyli napięcie, natężenie, opór, moc i grzanie przewodów, działa w obu przypadkach tak samo. Jednakże pod innymi względami prąd stały i przemienny zdecydowanie się różnią i czas je rozdzielić.

#### Prąd stały (DC)

Skrót DC pochodzi od angielskiego direct current. Elektrony płyną cały czas w jedną stronę, od minusa do plusa. Taki prąd dają baterie, akumulatory, panele słoneczne i gniazda USB. Na urządzeniach oznacza się go skrótem DC albo symbolem ⎓. Wszystko, co magazynuje energię elektryczną, każdy akumulator i bateria działa na prądzie stałym.

#### Prąd przemienny (AC)

Skrót AC pochodzi od angielskiego alternating current. Tutaj napięcie nieustannie zmienia kierunek, a elektrony, zamiast płynąć przed siebie, kołyszą się w przewodzie tam i z powrotem, praktycznie nie ruszając się z miejsca. Do przekazywania energii to w zupełności wystarcza, tak jak piła ręczna tnie drewno, choć porusza się w obie strony, więc uśredniając stoi w miejscu :) Taki prąd mamy w gniazdku. Oznacza się go skrótem AC albo symbolem ~. 

Potocznie mówi się na niego „prąd zmienny”, ale ściśle rzecz ujmując — to nie to samo. Prąd zmienny to każdy prąd, którego wartość zmienia się w czasie, nawet jeśli płynie cały czas w jedną stronę, na przykład pulsuje. Prąd przemienny to jego szczególny przypadek: zmienia kierunek regularnie i symetrycznie, tyle samo w jedną stronę, co w drugą, więc uśredniając wychodzi zero, dokładnie jak z wyżej wspomnianą piłą :) Każdy prąd przemienny jest więc zmienny, ale nie każdy zmienny jest przemienny. W dalszej części będę trzymał się poprawnej nazwy — czyli „przemienny”.

W Polsce i całej Europie prąd w sieci ma częstotliwość 50 Hz, czyli wykonuje 50 pełnych cykli na sekundę. Pełny cykl to ruch w jedną stronę i z powrotem, więc kierunek zmienia się 100 razy na sekundę.

#### Sinusoida

Napięcie w gniazdku nie przeskakuje gwałtownie między plusem a minusem. Rośnie płynnie do maksimum, płynnie opada do zera, przechodzi na drugą stronę, osiąga tam maksimum i wraca. Wykres tego ruchu to sinusoida. Jest to bezpośredni skutek tego, skąd prąd pochodzi — w elektrowni magnes obraca się wewnątrz cewek, a obrót ze stałą prędkością daje właśnie taki przebieg. 

#### Co właściwie znaczy „230 V”?

Skoro napięcie cały czas się zmienia, to co właściwie znaczy „230 V”? Nie jest to napięcie maksymalne. Nie jest to też średnia, bo średnia z sinusoidy wynosi zero! :) Napięcie jest dodatnie dokładnie tak samo długo, jak ujemne. 230 V to tak zwana „wartość skuteczna”. Definiuje się ją przez skutek, czyli przez ciepło. Prąd przemienny o napięciu skutecznym 230 V nagrzewa grzałkę tak samo, jak nagrzewałby ją prąd stały o napięciu 230 V.

Żeby zobaczyć, skąd bierze się ta liczba, połączmy dwa znane już wzory. Skoro P = U · I, a z prawa Ohma I = U / R, to P = U² / R. Moc grzałki zależy więc od kwadratu napięcia. W szczycie sinusoidy grzałka grzeje z pełną mocą, przy przejściu przez zero przez moment nie grzeje wcale. Kierunek nie ma znaczenia, bo kwadrat liczby ujemnej też jest dodatni, więc grzałka grzeje w obu połowach cyklu.

Gdy uśredni się kwadrat sinusoidy po całym cyklu, wychodzi dokładnie połowa wartości szczytowej. Średnia moc grzałki to zatem połowa jej mocy szczytowej. A skoro moc zależy od kwadratu napięcia, połowie mocy odpowiada napięcie mniejsze nie dwa razy, tylko √2 razy, czyli około 1,41 raza:

napięcie skuteczne = napięcie szczytowe / √2

W drugą stronę: 230 V · 1,41 to około 325 V. Tyle naprawdę wynosi napięcie w gniazdku w szczycie każdego cyklu, zmieniając się od 325 V do - 325 V — 100 razy na sekundę.

W praktyce wynikają z tego dwie rzeczy. Po pierwsze, możemy liczyć po staremu: czajnik 230 V i 10 A ma 2300 W, tak samo przy prądzie przemiennym, jak i przy prądzie stałym. Natężenie 10 A to również wartość skuteczna, a miernik pokazuje właśnie wartości skuteczne. Po drugie, izolacja i elektronika muszą wytrzymać 325 V, a nie 230 V. 

#### Po co w ogóle prąd przemienny?

Powody są dwa i oba bardzo praktyczne.

Pierwszy: taki prąd po prostu wychodzi z elektrowni. Jak pisałem wyżej, prądnica to magnes obracający się wewnątrz cewek, a obrót z natury daje sinusoidę. To najstarszy i do dziś najprostszy znany ludzkości sposób wytwarzania dużych ilości energii elektrycznej. Elektrownie węglowe, gazowe, jądrowe, wodne i wiatrowe różnią się tylko tym, co kręci turbiną: para, woda albo wiatr. Na końcu zawsze jest ta sama obracająca się prądnica. Fotowoltaika, która wytwarza prąd stały bez żadnych ruchomych części, jest na tym tle wynalazkiem bardzo młodym. Na masową skalę stosujemy ją dopiero od kilkunastu lat.

Drugi powód to transformator, czyli urządzenie, które tanio i niemal bez strat zmienia napięcie w górę lub w dół. Działa on tylko na prądzie przemiennym, a zmiana napięcia jest kluczowa przy przesyłaniu energii na duże odległości. Z poprzedniej sekcji wiemy, że ciepło tracone w przewodach rośnie z kwadratem natężenia. Tę samą moc 2300 W można przesłać jako 230 V i 10 A albo jako 23 000 V i 0,1 A. W drugim przypadku prąd jest sto razy mniejszy, więc straty w przewodach są dziesięć tysięcy razy mniejsze.

Dzięki temu liniami wysokiego napięcia płynie prąd pod napięciem setek tysięcy woltów. W Polsce główne linie, te na największych słupach, pracują na 400 000 V i 220 000 V. Bliżej miast napięcie obniża się do 110 000 V, potem do kilkunastu tysięcy woltów, najczęściej 15 000 V, i tak energia dociera na osiedla i do wsi. Dopiero transformator stojący kilkaset metrów od domu obniża je do znanych nam 230 V. Dokładniej: wyprowadza trzy fazy po 230 V każda, a „siła”, czyli 400 V, to napięcie mierzone między dwiema fazami. Prądu trójfazowego w kamperach jednak nie będziemy stosować na pewno, więc nie będziemy go tu dokładniej omawiać :)

#### Zamiana jednego prądu w drugi

W kamperze oba rodzaje prądu występują obok siebie. Akumulator i panele słoneczne dają prąd stały, zwykle 12 V. Czajnik elektryczny czy suszarka potrzebują już prądu przemiennego 230 V.

Po podłączeniu do słupka na kempingu dostajemy 230 V prądu przemiennego, którym trzeba naładować akumulator, czyli zamienić go na stały.

Potrzebujemy więc dwóch urządzeń, które zamieniają prąd w przeciwne strony: prostownika i falownika.

##### Prostownik

Prostownik zamienia prąd przemienny na stały. Siedzi w każdej ładowarce telefonu, zasilaczu laptopa i ładowarce akumulatora, bo cała elektronika i wszystkie akumulatory pracują na prądzie stałym.

Prostowanie jest proste, bo załatwia je jeden tani element: dioda. Dioda to elektryczny zawór zwrotny. Przepuszcza prąd w jedną stronę, a w drugą go blokuje. Nie trzeba nią sterować, nie ma w niej nic ruchomego i kosztuje grosze.

Pojedyncza dioda po prostu odcina ujemną połowę sinusoidy, więc połowa energii się marnuje. Dlatego stosuje się cztery diody połączone w tak zwany „mostek”. Taki układ nie odcina ujemnej połowy, tylko ją odwraca. Na wyjściu prąd płynie już zawsze w jedną stronę, ale pulsuje: 100 razy na sekundę rośnie do szczytu i spada do zera. To właśnie przykład prądu zmiennego, który nie jest przemienny :)

Pulsowanie wygładza kondensator, czyli element, który działa jak mały zbiornik wyrównawczy. Napełnia się w szczytach i oddaje ładunek w dołkach. Za nim napięcie jest już prawie równe. Na koniec elektronika obniża je do wartości, której potrzebuje urządzenie, na przykład 5 V dla telefonu albo około 14 V dla akumulatora. Tak, 14 V dla akumulatora nazywanego dwunastowoltowym, to nie pomyłka :) Żeby „wtłoczyć” prąd do akumulatora, ładowarka musi dać napięcie wyższe niż jego własne. Wrócimy do tego przy akumulatorach.

##### Falownik

Falownik, zwany też inwerterem, robi rzecz odwrotną: z prądu stałego z akumulatora wytwarza przemienny 230 V. Potocznie mówi się na niego „przetwornica”. Ściśle biorąc przetwornica to każde urządzenie zmieniające parametry prądu, także takie, które z 12 V robi 5 V do gniazda USB, ale w świecie kamperów „przetwornica” oznacza prawie zawsze falownik.

Zamiana w tę stronę jest dużo trudniejsza. Falownik ma do dyspozycji tylko stałe napięcie z akumulatora i tranzystory, czyli bardzo szybkie wyłączniki. Wyłącznik umie tylko włączyć albo wyłączyć. Nie umie płynnie „trochę przepuszczać”, a sinusoida jest przecież gładka.

Najprostsze rozwiązanie to przełączać plus z minusem 50 razy na sekundę. Wychodzi z tego przebieg prostokątny: napięcie skacze od razu z pełnego plusa na pełny minus. Nieco lepsze falowniki dodają między skokami chwilę przerwy na zerze i powstaje przebieg schodkowy. Sprzedaje się go pod ładnie brzmiącą nazwą „sinus modyfikowany”, choć z sinusoidą ma niewiele wspólnego.

Prawdziwą sinusoidę falownik musi „wyrzeźbić”, a ma do dyspozycji tylko wyłączniki. Stosuje więc sprytną sztuczkę.

Wyobraźcie sobie samochód, w którym pedał gazu ma tylko dwa położenia: gaz do dechy albo nic. Da się takim autem jechać spokojnie 50 km/h? Da się, jeśli będziemy wciskać i puszczać pedał bardzo szybko, kilka razy na sekundę. Im dłuższe wciśnięcia w stosunku do przerw, tym szybciej jedziemy. Szarpania nie poczujemy, bo ciężkie auto ma dużą bezwładność: nie nadąża za pojedynczymi wciśnięciami i je wygładza.

Falownik robi dokładnie to samo. Jego tranzystory włączają się i wyłączają kilkadziesiąt tysięcy razy na sekundę. Gdy napięcie ma być wysokie, włączenia są długie, a przerwy krótkie. Gdy ma być niskie, odwrotnie. Elektronika płynnie zmienia te proporcje w rytmie sinusoidy: coraz dłuższe włączenia, potem coraz krótsze, potem to samo po stronie ujemnej.

Rolę bezwładności ciężkiego auta pełnią elementy wygładzające na wyjściu falownika, podobne do kondensatora — czyli zbiornika wyrównawczego, który poznaliśmy przy prostowniku. Tysiące pojedynczych impulsów zlewają się w nich w jedną gładką falę, taką samą jak w domowym gniazdku.

##### Dlaczego duże falowniki potrzebują 24 V albo 48 V?

Falownik ma jeszcze jedno trudne zadanie. Z 12 V trzeba zrobić napięcie, które w szczycie sięga 325 V, czyli podnieść je ponad dwudziestokrotnie. Energia nie bierze się znikąd, więc po stronie akumulatora płynie odpowiednio większy prąd. Czajnik 2300 W pobiera z gniazdka 10 A, ale falownik ciągnie wtedy z akumulatora 12 V około 200 A.

Policzmy to dla kilku mocy, korzystając ze znanego wzoru I = P / U:

| Moc | 12 V | 24 V | 48 V |
| --- | --- | --- | --- |
| 1000 W | 83 A | 42 A | 21 A |
| 2000 W | 167 A | 83 A | 42 A |
| 3000 W | 250 A | 125 A | 63 A |
| 4000 W | 333 A | 167 A | 83 A |

W rzeczywistości prądy są o kilkanaście procent większe, bo falownik ma straty, a napięcie obciążonego akumulatora spada.

Przypomnijmy sobie, że w instalacji domowej 16 A obciążenia ciągłego to już dużo, a ciepło w przewodach rośnie z kwadratem natężenia. Czterokrotnie niższe napięcie oznacza czterokrotnie większy prąd, a to daje szesnaście razy więcej ciepła w tym samym przewodzie. Przy 300 A przewody muszą mieć grubość kciuka, a każde złącze, bezpiecznik i wyłącznik muszą ten prąd wytrzymać godzinami. Jedna źle dokręcona śruba lub zacisk staje się grzałką :/

Jest też drugi, mniej oczywisty kłopot. Każdy przewód zabiera odrobinę napięcia po drodze. Strata pół wolta to przy 12 V aż cztery procent, a przy 48 V tylko jeden procent.

Dlatego w pewnym momencie dokładanie miedzi przestaje mieć sens i producenci po prostu nie oferują dużych mocy na 12 V. 

W praktyce przyjmuje się prostą zasadę. Do około 2500 W wystarcza instalacja 12 V. Między 2500 a 4000 W warto przejść na 24 V. Powyżej zostaje już tylko 48 V. Na tabliczkach falowników zobaczycie te granice jako 3000 i 5000 VA. Czym jest VA i dlaczego ta liczba jest większa niż waty, wyjaśniam w następnej sekcji. 

Wyższe napięcie akumulatora ma swoją cenę, bo lodówki, pompy i oświetlenie w kamperach są budowane na 12 V i trzeba je wtedy zasilać przez dodatkową przetwornicę obniżającą z 24 V czy 48 V do 12 V. Do tego wrócimy przy planowaniu instalacji.

##### Sinus modyfikowany czy pełny sinus?

Grzałce jest wszystko jedno, jaki kształt ma napięcie, byle zgadzała się wartość skuteczna. Inne urządzenia są bardziej wybredne. Silniki i sprężarki na przebiegu schodkowym buczą, grzeją się mocniej i mają mniejszą moc. Część ładowarek, zasilaczy i sprzętu ze sterowaniem elektronicznym działa nieprawidłowo, nie działa wcale albo z czasem się psuje.

„Pełny sinus”, zwany też „czystym sinusem”, oznacza, że falownik daje taki sam gładki przebieg jak gniazdko w domu i można do niego podłączyć wszystko. Takie falowniki są droższe, bo mają bardziej złożoną elektronikę.

### Moc czynna, bierna i pozorna, czyli wat czy VA?

Do tej pory liczyliśmy moc prosto: P = U · I. Dla prądu stałego to zawsze prawda. Dla przemiennego w większości przypadków też, ale pod jednym warunkiem: prąd musi kołysać się dokładnie w rytm napięcia. Gdy napięcie jest w szczycie, prąd też jest w szczycie. Gdy napięcie przechodzi przez zero, prąd również.

Tak zachowują się czajnik, grzejnik i wszystko, co po prostu zamienia prąd na ciepło.

Inaczej jest z urządzeniami, które mają w środku silnik, sprężarkę albo transformator, czyli z lodówką, klimatyzacją, wiertarką czy pompą. Takie urządzenie zachowuje się trochę jak sprężyna. Przez część każdego cyklu przyjmuje energię i na moment ją w sobie magazynuje, a chwilę później oddaje ją z powrotem do źródła. Skutek jest taki, że prąd „spóźnia się” względem napięcia i oba przestają kołysać się w tym samym rytmie.

Najłatwiej zrozumieć to na huśtawce. Jeśli popychamy huśtającego się dokładnie w rytm, czyli zawsze wtedy, gdy huśtawka rusza od nas, cały nasz wysiłek idzie w rozbujanie. Jeśli zaczniemy się spóźniać, przez część czasu będziemy pchać huśtawkę, która leci już w naszą stronę. Wtedy to ona oddaje nam energię i odpycha nasze ręce. Machamy rękami tak samo mocno, jak przedtem, męczymy się tak samo, ale huśtawka buja się słabiej.

Z prądem jest identycznie. Część energii krąży w kółko między falownikiem a urządzeniem i nie robi nic pożytecznego. Prąd płynie w przewodach naprawdę, ale tylko część tego prądu faktycznie coś napędza.
Stąd biorą się trzy rodzaje mocy:

- **Moc czynna (P), w watach (W).** Ta, która faktycznie pracuje: grzeje, kręci, świeci. Tylko ona opróżnia akumulator i tylko za nią płacimy na domowym rachunku.
- **Moc bierna (Q), w warach (var).** Ta, która krąży tam i z powrotem i nic nie robi.
- **Moc pozorna (S), w woltoamperach (VA).** To po prostu napięcie razy cały prąd płynący w przewodzie, bez sprawdzania, ile z niego naprawdę pracuje.

Popularne porównanie to kufel piwa: piwo to moc czynna, piana to moc bierna, a pojemność kufla to moc pozorna. Płacisz za piwo, ale kufel musi pomieścić jedno i drugie. Porównanie kuleje w jednym miejscu: te moce nie dodają się wprost, tylko jak boki trójkąta prostokątnego, czyli S² = P² + Q². Przy 4000 W mocy czynnej i 3000 var biernej moc pozorna wynosi 5000 VA, a nie 7000.

Stosunek mocy czynnej do pozornej to współczynnik mocy, oznaczany cos φ. Czajnik ma 1, czyli waty i woltoampery są równe. Silniki i sprężarki mają zwykle od 0,6 do 0,8.

Dlaczego falownik w ogóle opisuje się w VA? Bo prąd bierny, choć nie pracuje, naprawdę płynie. Grzeje przewody i elektronikę inwertera dokładnie tak samo, jak prąd czynny, zgodnie z tym, co pisałem w sekcji o grzaniu przewodów. Granicą inwertera jest więc prąd, jaki potrafi przenieść, a to właśnie mówi liczba w VA. Przykład: sprężarka o mocy 1000 W i cos φ = 0,7 zajmuje w falowniku 1000 / 0,7, czyli około 1430 VA. 

W praktyce oznacza to dwie osobne rachuby. Wielkość inwertera dobieramy w VA, bo musi udźwignąć cały prąd. Zużycie energii z akumulatora liczymy w watach, bo tylko moc czynna go opróżnia.

Falownik opisany jako 5000 VA daje realnie około 4000 W mocy czynnej. Samych jednostek nie mam o co winić, ale strasznie nie lubię tego, jak producenci eksponują je na pudełku — tam zawsze ląduje większa liczba, a waty trzeba wyszukać w tabelce drobnym drukiem.

Druga pułapka z tej samej rodziny to moc szczytowa. Silnik w chwili rozruchu pobiera przez ułamek sekundy nawet kilka razy więcej prądu niż w czasie normalnej pracy, więc inwerter musi umieć na moment oddać dużo więcej, niż wynosi jego moc ciągła. To ważny i potrzebny parametr. Część tańszych producentów podaje jednak moc szczytową, dostępną przez ułamek sekundy, tak jakby była mocą znamionową, dostępną godzinami. Papier przyjmie wszystko, więc sprawdzajcie obie liczby.

### Watogodziny na co dzień

W sekcji o energii ustaliliśmy, że amperogodziny bez podanego napięcia nic nie znaczą. Wniosek praktyczny jest jeden: **watogodziny (Wh) to jedyna uczciwa waluta energii w kamperze.** Jeśli ktoś Wam mówi „mam baterię 200 Ah” i nie mówi, przy jakim napięciu, to można zakładać, że to 12 V, ale tak naprawdę jest to niedopowiedzenie. 

Z nieznanego mi powodu nadal większość osób posługuje się amperogodzinami, więc przyda się przelicznik. Bardzo zgrubny możecie przyjąć taki: 1 kWh to około 100 Ah przy 12 V. Dokładny rachunek daje 83 Ah, a przy realnym napięciu instalacji, o którym za chwilę, jeszcze trochę mniej. Setkę łatwo jednak zapamiętać i myli się ona w bezpieczną stronę: kupicie odrobinę za dużo, a nie za mało :)

Nasz własny bank energii to dwie baterie po 5120 Wh w systemie 48 V, czyli łącznie okrągłe 10 kWh. Fizycznie ma on około 200 Ah. Gdyby ktoś się uparł przeliczać to na amperogodziny przy 12 V, wyszłoby niecałe 900 Ah!

### Ile woltów ma instalacja „12 V”?

Przy prostowniku wspomniałem, że akumulator dwunastowoltowy ładuje się napięciem około 14 V. To nie jedyna niespodzianka. W instalacji „12 V” praktycznie nigdy nie ma 12 woltów. Na przewodach jest zwykle około 13,4 V i to napięcie delikatnie się zmienia w zależności od tego, czy bateria się ładuje, czy rozładowuje. „12 V” to tylko nazwa zwyczajowa.

Pierwsza konsekwencja jest drobna. Wrażliwa elektronika nie lubi zmieniającego się napięcia, dlatego laptopa zasilamy w kamperze przez dodatkowy zasilacz, który je stabilizuje, a nie bezpośrednio przewodami z instalacji.

Druga konsekwencja jest poważniejsza i dotyczy pytania, które będziecie sobie zadawać codziennie: ile energii zostało w akumulatorze?

Zacznijmy od tego, że naładowania akumulatora nie da się zmierzyć bezpośrednio. Nie istnieje czujnik, który zajrzy do środka i policzy zgromadzoną energię. Każdy wskaźnik naładowania, w telefonie, w samochodzie elektrycznym i w kamperze, pokazuje wartość wyliczoną pośrednio z czegoś, co zmierzyć się da. Metody są dwie.

Pierwsza to pomiar napięcia. Napięcie akumulatora spada w miarę rozładowania, więc z napięcia można odczytać stan naładowania, a przynajmniej w starych akumulatorach to jako tako działa. Akumulatory LiFePO4 (więcej o nich w tomie o budowie) mają jednak charakterystykę napięcia płaską jak stół – bateria przez większość rozładowania trzyma prawie to samo napięcie, a potem następuje nagłe tąpnięcie. Wskaźnik oparty na napięciu pokazywałby więc przy takim akumulatorze przez cały czas „prawie pełna”, aż do chwili, gdy jest już prawie pusta.

Druga metoda to liczenie wszystkiego, co do akumulatora wpływa i co z niego wypływa. Służy do tego „shunt”, po polsku „bocznik”. W uproszczeniu to bardzo dokładny licznik prądu wpinany przy akumulatorze. Zlicza każdą amperogodzinę w obie strony, tak jak wodomierz liczy wodę. Pamiętacie, że amperogodzina to ładunek? Shunt liczy właśnie ładunek, więc wie, ile go w baterii zostało, niezależnie od napięcia.

W mojej opinii to element niepomijalny. Ma jednak wadę, która wynika wprost z zasady działania. Shunt niczego nie mierzy w akumulatorze, on tylko dodaje i odejmuje. Każdy pomiar prądu ma maleńki błąd, a bardzo małe prądy, takie jak pobór urządzeń w stanie czuwania, potrafią w ogóle umknąć licznikowi. Do tego akumulator nie oddaje dokładnie tyle, ile przyjął, a jego pojemność z wiekiem maleje. Pojedynczo to drobiazgi, ale licznik sumuje je dzień po dniu i po kilku tygodniach wskazanie potrafi rozjechać się z rzeczywistością o kilkanaście procent.

Dlatego trzeba go regularnie kalibrować, a nie raz ustawić. Jedyny pewny punkt odniesienia to akumulator naładowany do pełna, bo tylko wtedy wiadomo na pewno, że jest w nim 100%. Porządne liczniki wykrywają ten moment same i wtedy kasują nagromadzony błąd. Warunek jest jeden: bateria musi do tych 100% faktycznie regularnie dochodzić.

I tu zaczyna się kłopot w kamperze. Przy mieszkaniu na stałe, zimą albo przy za małym solarze, bateria potrafi tygodniami krążyć między 30 a 80% i ani razu nie dobić do pełna. Licznik nie ma się wtedy do czego odnieść i z każdym dniem myli się bardziej. Mamy z tym realny problem w naszym systemie. Wniosek praktyczny: co jakiś czas naładujcie baterię do pełna celowo, ze słupka albo podczas długiej jazdy z alternatora, nawet jeśli bieżący bilans energetyczny tego nie wymaga :)

## Ile prądu naprawdę bierze kamper

### Nasze liczby

Teraz trochę praktyki: ile prądu naprawdę zjadają sprzęty w kamperze. Liczby pochodzą z naszych pomiarów, a nie z kart katalogowych. Muszę Was jednak uprzedzić, że jesteśmy dość prądożerni. Mieszkamy i pracujemy w kamperze na stałe, więc nasze zużycie jest wyraźnie wyższe niż w przeciętnym kamperze wakacyjnym. Przy każdej pozycji piszę, co jest u nas niestandardowe.

- **Praca zdalna dwóch osób**, czyli trzy laptopy i dwa duże monitory: około 1 kWh na 8 godzin pracy. To jest ta liczba, przed którą ostrzegał rozdział o filozofii, mówiąc, że monitory są bardzo prądożerne. Niestandardowe są tu właśnie monitory i 3 laptopy (ja pracuje na 2 na raz). Sam jeden laptop ładowany raz dziennie to zwykle około 100 Wh.
- **Lodówka:** około 600 Wh na dobę. Mamy dużą jak na kampera lodówkę domową, zasilaną z 230 V. Typowa kamperowa lodówka kompresorowa na 12 V zużywa mniej więcej połowę tego.
- **Mały serwer smart home**, czyli niewielki komputer w trybie oszczędzania: ledwie około 8 W, ale przez dobę robi z tego około 200 Wh. Jedna trzecia lodówki!
- **Starlink Mini:** teoretycznie do 40 W, realnie około 20 W. Nie włączamy go na 24h, bo najczęściej mamy zasięg sieci komórkowej.
- **Router i kamery:** po kilka watów każde, ale również przez całą dobę.
- **Wentylator dachowy:** od kilku watów na najniższym biegu do kilkudziesięciu na najwyższym.
- **Oświetlenie LED:** kilkanaście do kilkudziesięciu watów, gdy świeci się wszystko naraz. To akurat pozycja, którą ma każdy kamper.
- **Płyta indukcyjna:** łącznie ponad 3 kW. Większość kamperów gotuje na gazie i tej pozycji nie ma wcale.
- **Airfryer:** 2,5 kW. To nasz luksus, a nie standard.
- **Suszarka do włosów:** 2,5 kW. Akurat ona trafia się w wielu kamperach i zdarza się, że to właśnie ona jako urządzenie największej mocy decyduje o mocy falownika ;)
- **Klimatyzacja** (Dometic FreshJet 2200): około 0,9–1,0 kW, kiedy pracuje. W kamperach wakacyjnych klimatyzacja postojowa jest rzadkością i zwykle działa tylko na słupku.
- **Ogrzewanie** (Truma Combi D 6, na diesla): w czasie pracy średnio 30–50 W. Brzmi niewinnie, ale przez mroźną noc robi z tego 300–400 Wh. To więcej, niż w tym samym czasie bierze lodówka. Latem, gdy grzeje tylko wodę, pozycja praktycznie znika.”

### Nocny wyciek

Jest pozycja, o której zapomina prawie każdy, bo powstaje wtedy, kiedy śpimy. Noc wydaje się czasem, w którym kamper nie zużywa nic. Tymczasem wiatrak kręci się dalej, Starlink i router pracują, lodówka pracuje, a falownik pobiera swoje, nawet jeśli nic nie jest do niego podłączone. U nas składa się to na około 1 kWh, czyli około 10% naszego banku, zanim w ogóle wstaniemy z łóżka :/

To klasyczni maratończycy: każde z tych urządzeń bierze niewiele, ale osiem godzin to dużo czasu. Najbardziej boli to zimą, kiedy słabe słońce przez cały dzień może nie oddać nawet tego, co uciekło w nocy.

Swój nocny wyciek zmierzycie bardzo prosto. Zapiszcie wskazanie licznika wieczorem, przed snem, i rano, zaraz po przebudzeniu. Różnica to energia, która uciekła, kiedy nikt niczego nie używał.

Rozwiązaniem jest wyłączać część sprzętów na noc, ale oczywiście nie każde można. My na przykład zawsze na noc wyłączamy Starlinka, nawet jak z niego korzystamy w dzień, ale nie chcemy być totalnie odcięci od internetu oraz zachować lokalną sieć Wi-Fi, więc routera na przykład nie wyłączamy nigdy. 

### Maratończycy i sprinterzy

Energia to moc razy czas, więc w bilansie liczą się obie te rzeczy. Lodówka bierze mało prądu na raz, ale pracuje całą dobę, i dlatego jest jedną z największych pozycji. Suszarka bierze 2,5 kW, ale przez maks pięć minut, co daje około 200 Wh. W watogodzinach maratończyk często bije sprintera :/

### Pobór własny falownika

Najbardziej niedoceniana pozycja w bilansie to pobór własny falownika, czyli prąd, który system zużywa, gdy nic nie robicie. Producenci lubią ten parametr zaniżać: często podają go w trybie oszczędzania, kiedy falownik jest wyłączony i tylko co chwilę sprawdza, czy ktoś czegoś nie podłączył, a nie w normalnej pracy z napięciem na gniazdkach. Realnie włączony falownik bierze około 30 W, a strona produktu potrafi obiecywać 2 W. Policzcie sami: 30 W × 24 h = 720 Wh na dobę! **Włączony i bezczynny falownik potrafi zjeść więcej niż lodówka.**

Kiedy pracuje duży odbiornik, pobór własny ginie w tle. Liczy się wtedy, kiedy nie robicie nic. Mądrym rozwiązaniem jest zaplanowanie takiej instalacji, by 230 V włączać tylko okazjonalnie wtedy, kiedy jest potrzebna. W naszym kamperze, gdyby nie lodówka, moglibyśmy tak robić. 

### Ile prądu da słońce?

Zanim policzymy bilanse, jeszcze jedno szybkie oszacowanie: czego się spodziewać po panelach na dachu. Szczegóły fotowoltaiki zostawiam na tom o budowie, tutaj tylko zgrubny rachunek.

Moc panelu podana na tabliczce, na przykład 400 W, to moc w warunkach idealnych: pełne słońce w zenicie i panel ustawiony dokładnie prostopadle do promieni. Na dachu kampera takie warunki nie zdarzają nigdy. Panel leży płasko, słońce wędruje po niebie, rano i wieczorem świeci pod ostrym kątem, a w upale panel potrafi tracić sprawność z nagrzewania się.

Dlatego nie liczy się godzin dnia, tylko tak zwane godziny pełnego słońca. To pytanie brzmi: gdyby całą energię z dzisiejszego dnia ścisnąć w okres pracy na 100% mocy, ile godzin by to trwało? Rachunek jest wtedy banalny: energia dzienna = moc paneli × liczba godzin pełnego słońca.

Dla Polski wygląda to mniej więcej tak:

| Dzień | Godziny pełnego słońca | Z paneli 400 W |
| --- | --- | --- |
| Bardzo słoneczny, lato | około 5 | około 2 kWh |
| Przeciętny letni | 3–4 | 1,2–1,6 kWh |
| Wiosna i jesień | około 2 | około 0,8 kWh |
| Zima | poniżej 1 | 0,2–0,4 kWh |
| Pochmurny, o każdej porze roku | ułamek powyższych | czasem prawie nic |

Latem panele potrafią dać dziesięć razy więcej niż zimą, więc instalacja, która w lipcu ma nadmiar, w grudniu jest praktycznie niedoładowywana. 

### Dwa profile, dwa zupełnie różne bilanse

**Profil wakacyjny** to lodówka, światła, ładowanie telefonów, pompa wody, żadnej pracy zdalnej, gotowanie na gazie. Taki zestaw zamyka się z grubsza w 1 kWh na dobę, czyli w naszym przeliczniku około 100 Ah przy 12 V. 

Dlatego kampery bardzo często mają akumulator 200 Ah przy 12 V, czyli 2400 Wh. To ponad dwa dni zapasu bez żadnego ładowania. Do tego na dachu 400 W paneli fotowoltaicznych, które w bardzo słoneczny letni dzień potrafią oddać około 2 kWh. To 80–90% całego akumulatora i dwa razy więcej niż dzienne zużycie, więc słoneczne dni z nawiązką nadrabiają pochmurne.

**Profil full-time z pracą zdalną** wygląda u nas tak:

- praca dwóch osób: około 1 kWh,
- lodówka: około 0,6 kWh,
- router, serwer smart home i kamery: około 0,5 kWh,
- noc, czyli ogrzewanie, wiatrak, grzanie wody i falownik: około 0,6 kWh.

Razem około 2,7 kWh na dobę, zanim jeszcze cokolwiek ugotujemy na prądzie. Z gotowaniem na indukcji i w airfryerze robi się z tego około 3,5 kWh, czyli ponad trzy razy więcej niż w profilu wakacyjnym. Dlatego cudze porady elektryczne tak często nie przystają do Waszej sytuacji. Tamten ma inny profil, a nie inną fizykę.

Uwaga na pułapkę, w którą sam wpadłem przy pierwszym liczeniu: nie liczcie niczego podwójnie. Lodówka i router pracują także w nocy, więc jeśli macie je w bilansie jako pozycje całodobowe, nie dodawajcie ich drugi raz do nocnego wycieku.

Sprawdziliśmy ten bilans w praktyce. Nasz bank 10 kWh wystarcza na trzy pełne dni stania bez żadnego ładowania, z pracą i gotowaniem trzech posiłków dziennie na prądzie. W Norwegii w drugim dniu takiego postoju mieliśmy nadal ponad połowę banku :)

Własny rachunek zróbcie teraz. Kartka i trzy kolumny: urządzenie, ile watów, ile godzin na dobę. Wymnóżcie, zsumujcie, dopiszcie 25% zapasu na straty i drobiazgi. 

### Rekomendacja autora

Przeczytajcie ten rozdział jeszcze raz. Serio :) Było tu sporo technikaliów, a warto mieć je w małym palcu, zanim wydacie pierwszą złotówkę na sprzęt. Kto rozumie, czym różni się wat od watogodziny i dlaczego gruby przewód to nie fanaberia, tego nie nabierze ani tabliczka znamionowa, ani sprzedawca.

Zróbcie też swoją kartkę z bilansem, żeby wiedzieć w ogóle, w jakie zapotrzebowanie energetycznie celujecie. 

Konkretnym sprzętem, schematami i montażem zajmiemy się w tomie o budowie!
