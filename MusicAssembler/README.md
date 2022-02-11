# Jeden player, dwa edytory i Mad Pascal
![Music Assembler](https://raw.githubusercontent.com/zbyti/c64portal-article/master/MusicAssembler/data/music_assembler.png)

![Voicetracker 4.0](https://raw.githubusercontent.com/zbyti/c64portal-article/master/MusicAssembler/data/voicetracker.png)

## Trochę historii

W roku 1991 zakupiłem świetny program muzyczny dla **C64**, był to **Voicetracker** w wersji **4.0** i wydaniu dyskowym. Dołączone do niego liczne przykłady powodowały przysłowiowy "opad szczeny". Nie miałem wtedy pojęcia kto jest autorem tym przykładów ale był niezły! Minęło wiele lat zanim dowiedziałem się kto za tym wszystkim stoi.

### Music Assembler

Player (procedura odgrywająca muzykę) i edytor jest autorstwa: Marco [MC](https://csdb.dk/scener/?id=4074) Swagerman i Oscar [OPM](https://csdb.dk/scener/?id=7485) Giesen z grupy  **The Dutch USA-Team**. Powstał jako ukoronowanie wielu prób napisania własnej procedury odgrywającą muzykę na komputerze **C64** i owoc analizy tego jak to robią największe sławy muzycznej sceny lat 80-tych.

Player (według słów jednego z autorów) w momencie powstania był przełomowy pod względem muzycznym, do tego odznaczał się niskim wykorzystaniem zasobów systemowych.

Pierwsze wersje programu **Music Assembler ** były narzędziem "wewnętrznym"  i mogli korzystać z niego tylko zaprzyjaźnieni z autorami programu muzycy. **CSDB** datuje wydanie wersji oznaczonej numerem **1.0** na rok 1989. 

**Music Assembler** w późniejszym czasie był dostępny także komercyjnie, np. w Zachodnich Niemczech, przyniósł chłopakom na tyle wysoki dochód, że zakupili swoje pierwsze 16-bitowce.

Ostatnia wersja programu datuje się na rok 1994 i jest w wersji **1.4**.

### Voicetracker

Paweł [Polonus](https://csdb.dk/scener/?id=823) Sołtysiński to znany koder ze Szczecina na polskiej scenie C64, współredaktor magazynu Kebab za młodu równie arogancki co zdolny a dziś równie milczący co utalentowany - to moja opinia ;)

Polonus w okolicach roku 1989/1990 napotkał ciekawą procedurę odgrywającą muzykę stworzoną przez [Reyna Ouwehanda](https://csdb.dk/scener/?id=8051) będącego wtedy członkiem grupy [Scoop](https://csdb.dk/group/?id=442) stąd błędnie przypisał autorstwo kodu komuś z tej grupy.

Analiza procedury (która początkowo miała być tylko ćwiczeniem programistycznym) doprowadziła go do napisania i wypuszczenia na scenę pierwszego polskiego edytora muzycznego na **C64**  w oparciu o "znalezioną" procedurę i to pomimo niezrozumienia do końca tego co ona "robi" ale jak sam wówczas napisał: on jest programistą a nie muzykiem.

Scena dość szybko zareagował, widząc kod playera praktycznie 1:1 wziętego z Music Assemblera poinformowała Pawła kto jest prawdziwym autorem "pożyczonej" procedury. Paweł przyjął to do wiadomości i poradził krytykom po prostu z tym żyć ;) o czym możemy przeczytać w notce dołączonej do **VT 1.1**.

**Voicetracker** miał bardzo szybki okres deweloperski, od wersji 1.0 do 4.0 upłynęło mniej więcej 1,5 roku. Wersja 3.0 i 4.0 była wydana w Polsce komercyjnie, artykuł o wersji **3.0** oraz reklamę wersji **4.0** mogliśmy spotkać na łamach **64 Plus 4 & Amiga** w roku 1991. Na podziw i uwagę (według mnie) zasługuje fakt, ze aż do wersji 4.0 **Polonus** całą pracę wykonał za pomocą programu monitora, dopier mało znana odsłona 5 programu została zakodowana w **Turbo Assemblerze**. Program był anglojęzyczny i miał ambicję sprzedażowe na zachodzie Europy - nie wiem ostatecznie czy miało to miejsce.

### Reyn Ouwehand

Muzyk który pośrednio zainspirował swoją pracą **Polonusa** jest autorem sporej części "tunes" dołączonych do **VT 4.0**. Dopiero po latach odkryłem, przesłuchując "randomowo" [HVSC](https://www.hvsc.c64.org), że to **Reyn** był odpowiedzialny za jedne z moich pierwszych zachwytów nad możliwościami dźwiękowymi układu [SID](https://pl.wikipedia.org/wiki/MOS_Technology_SID). Ku mojemu zdziwieniu odkryłem, że jako (chyba jedyny) nie komponował on z użyciem **VT** a był dołączony do komercyjnego wydania tego edytora.

Jako, że po latach postanowiłem nauczyć się "jak SID gra" to dla własnej przyjemności postanowiłem zobaczyć ulubione kawałki wczytane do macierzystego **Music Assembler**, a że **MA** wczytywał tylko muzykę pod adres `$C000` szybko okazało się, że potrzebuję ripper **PSID** i procedurę relokującą pod wymagany adres.

## Relokator

Pierwszą czynnością byłą [deasemblacja](https://sjp.pl/deasemblacja) jakiegoś *zaka* napisanego za pomocą **Music Assemblera**, czyli mniej więcej wykonanie pracy jaką **Polonus** wykonał ponad 30 lat temu ale bez aż tak dokładnego zrozumienia.

Efekt można zobaczyć tutaj: [4-Mat AY-Teaser.sid $c000](https://github.com/zbyti/mad-pascal-playground/blob/master/src/c64/music-collection/doc/4mat-ay-c000.txt).

Z mojego punktu widzenia wystarczyła zmiana tylko starszego bajtu playera, nie miałem ambicji pisać czegoś z prawdziwego zdarzenia a tylko na swoje bieżące, poznawcze potrzeby, była to też okazja sprawdzić [PHP](https://www.php.net) jako język skryptowy powłoki :D

Owoc mojej pracy można zobaczyć tutaj: [brzydki kod](https://github.com/zbyti/mad-pascal-playground/blob/master/src/c64/music-collection/assets/converter).

Dzięki powyższym zabiegom dysponuję teraz wersją **MA** z większą liczbą przykładów niż dyskietka zamieszona na **CSDB**. Jeżeli ktoś jest zainteresowany to można ją poprać [stąd](https://github.com/zbyti/c64portal-article/raw/master/MusicAssembler/data/Music%20Assembler%20v1_4%5Bextra%5D.d64). `SHIFT + D` otwiera menu operacji dyskowych.

## Kolekcja

Dysponując już paroma kawałkami **Reyna Ouwehanda** postanowiłem zrobić w ramach "treningu" prostą kolekcję jego *zaków* na **C64** i **Atari 800XL**.

Najszybszym wydał mi się w tej roli [Mad Pascal](https://mads.atari8.info/doc/pl/) i jego bogactwo bibliotek.

Pokrótce opiszę jak wykonać taki program samemu.

### Pakujemy

Wyciągnięte z **PSID** *zaki* warto by spakować, zwłaszcza, że nie oddzielałem kodu playera od danych patternów i instrumentów. W tej roli sprawdził się prosty skrypt:

```
#!/bin/bash
for FILE in *.sid; do ./converter -f $FILE -r c000; done
for FILE in *.rip; do apultra $FILE ../music/${FILE::-4}.apl; done
rm *.rip
```
Jak widzimy najpierw używam wcześniej napisanego *ripper & reloc-atora*, którego dla zmyłki nazwałem `converter`, dalej odbywa się pakowanie do docelowego katalogu i sprzątanie.

### Zasoby

Wytworzone powyżej pliki opisujemy jako **Mad Pascalowe** zasoby:

```
MUSIC_APL_LONDON     rcdata 'music/london_demo.apl'
MUSIC_APL_ART        rcdata 'music/audio_art.apl'
MUSIC_APL_BATMANIA   rcdata 'music/batmania_ii_5.apl'
MUSIC_APL_CONTAXIA   rcdata 'music/contaxia.apl'
MUSIC_APL_DOMINATION rcdata 'music/domination.apl'
MUSIC_APL_FALCON     rcdata 'music/falcon_tn.apl'
MUSIC_APL_FUNCIE     rcdata 'music/funcie.apl'
MUSIC_APL_CHANCE     rcdata 'music/in_chance.apl'
MUSIC_APL_LOVE       rcdata 'music/lessons_in_love.apl'
MUSIC_APL_LILY       rcdata 'music/lily_was_here.apl'
MUSIC_APL_PARTY      rcdata 'music/party_tune.apl'
MUSIC_APL_PIZZA      rcdata 'music/peppered_pizza.apl'
```
w pliku `music.rc`.

### Kodujemy

Całość kodu można znaleźć [tutaj](https://github.com/zbyti/mad-pascal-playground/blob/master/src/c64/music-collection/main.pas), ja tylko objaśnię to co może się wydawać niejasne ;)

```
procedure music_play; assembler; inline;
asm
  sei
  txa \ pha
  jsr M_PLAY
  pla \ tax  
  cli
end;
```
Do wywoływania procedury playera nie skorzystałem z przerwania tylko czekam na określoną linię rastra dlatego aby symulować lepiej przerwanie `IRQ` na czas grania wyłączam przerwania maskowalne, które mogły by zakłócić granie muzyki, wydaje mi się to nadmiarowe ale taką miałem fantazję.

Zrzucanie rejestru `X` gdy korzystam z procedur w języku maszynowym jest przy pracy z **Mad Pascalem** ważne bo wykorzystuje on ten rejestr do swoich mrocznych spraw związanych z programowym stosem itp.

```
procedure prepare_new_music; inline;
begin
  fillbyte(pointer(MUSIC), M_SPACE, 0);
  unapl(pointer(zaks[music_index]), pointer(MUSIC));

  music_init;
end;
```
Za pomocą `fillbyte` czyszczę sobie `4KB` przeznaczone pod rozpakowanie muzyki, wydaje mi się to nadmiarowe bo rozpakowywane *zaki* powinny się nadpisywać, jednak wydawało mi się, że bez tego odgrywane czasem były jakieś bzdety, skoro czyszczenie pamięci załatwiło sprawę to zostało ;)

```
repeat until keypressed;
```
Normalnie w Pascalu `keypressed` informuje, że coś pojawiło się w buforze i zwracana przez tę funkcję wartość "resetowana" jest dopiero przez użycie `readkey`. Na C64 implementacja `keypressed` obywa się bez `readkey` co formalnie jest błędem ale działa w sposób w jaki **JA** się tego spodziewam, więc jest jak jest :-]

### Budujemy

Do zbudowania `PRG` używam prostego skryptu powłoki:

```bash
#!/bin/bash

mp="$HOME/Programs/MadPascal/mp"
mads="$HOME/Programs/mads/mads"
base="$HOME/Programs/MadPascal/base"
name="main"

$mp $name.pas -t c64

if [ -f $name.a65 ]; then
  [ ! -d "output" ] && mkdir output
  mv $name.a65 output/
  $mads output/$name.a65 -x -i:$base -o:output/$name.prg
  exomizer sfx sys -n -t 64 -o bin/collection.prg output/$name.prg
else
  exit 1
fi
```
Jak widzimy wynikowy plik pakuję jeszcze za pomocą **exomizera** aby głównie skompresować puste przestrzenie w pliku.

## The End

Całe repozytorium znajduje się [tutaj](https://github.com/zbyti/mad-pascal-playground/tree/master/src/c64/music-collection) wraz z [binarką](https://github.com/zbyti/mad-pascal-playground/raw/master/src/c64/music-collection/bin/collection.prg).

Dla pasjonatów posiadających komputer Atari 800XL wraz z chipem SID lub jego emulacją kod znajduje się [tutaj](https://github.com/zbyti/mad-pascal-playground/tree/master/src/a8/sid-music-collection).
