# Task 1
## Subtask 1
###### 8/10 punktów
## Subtask 3
###### Cześć jestem Ania :slightly_smiling_face:. Na udział w  challenge portfolio zdecydowałam się ponieważ myślę o przebranżowieniu się na IT i od jakiegoś czasu zainteresowałam się właśnie testowaniem oprogramowania :bug:. Stwierdziłam że to niesamowita okazja żeby się przekonać jak to jest w praktyce testować i oczekuję stworzenia portfolio, którym będę mogła pochwalić się na rozmowie o pracę.:bug: Odkryłam na jednodniowych warsztatach testowania na których wcześniej brałam udział, że testowanie mnie wciąga i chciałabym aby mi tak pozostało. Chciałabym znaleść pracę jako tester oprogramowania najlepiej w połączeniu z językiem niemieckim, który dobrze znam. W przyszłości chciałabym poznać również Pythona i być może rozwijać się w kierunku automatyzacji testów.
*__Ania__*
## Subtask 4
###### Aplikacja Platforma Skautingowa Futbol Kolektyw pod adresem https://scouts-test.futbolkolektyw.pl/ jest to panel zarządzania graczami, meczami i do tworzenia raportów.
#### Jak działa aplikacja

###### Gdy wchodzimy w link https://scouts-test.futbolkolektyw.pl/ przenosi nas na stronę do logowania. Wpisujemy odpowiednio adres mailowy i hasło i przenosi nas na stronę główną aplikacji.

#### Funkcjonalności:

###### _https://scouts-test.futbolkolektyw.pl/_ - link do logowania się do platformy skautingowej
###### _Gracze_ - zakładka z listą zawodników
###### _English_ - wersja językowa. Mozliwość zmiany wersji językowej po zalogowaniu się na wersję polską aplikacji
###### _Wyloguj_ - przycisk do wylogowania się z aplikacji
###### _Statystyki_ - Ilość graczy, ilość meczy, ilość raportów, ilość akcji
###### _Dev Team Contact_ - kontakt do zespołu deweloperskiego przez aplikację Slack
###### _Linki pomocnicze_ - przycisk "Dodaj gracza"
###### _Aktywność_ - kolejność zdarzeń na stronie

###### Wydaje mi się że na stronie głównej przed zalogowaniem się powinno być duże zdjęcie np boiska piłkarskiego i gdy przewijamy w dół przedstawione co ta strona ma na celu w sposób bardziej opisowy. Zakładka do logowania się np:"futbolkolektyw.pl/account/login"  przez skautów powinna znajdować się w prawym górnym rogu. Gdzie również powinna być możliwość stworzenia konta. W przypadku wersji językowej w prawym górnym rogu strony powinna być zakładka z wersją językową strony i lista rozwijana z językami. 
###### Po zalogowaniu się jako użytkownik skaut. Na samej górze w prawym górnym rogu powinna znajdować się ikonka użytkownika po kliknieciu w tą ikonkę z opcją wylogowania się. Statystyki czyli ilość graczy, ilość meczy, ilość raportów i ilość akcji są najmniej istotne i powinny znajdować na dole strony. Na środku strony aktualności z wydarzeniami na stronie. Do wersji językowej i ikonki zalogowanego uzytkownika powinna dołączyć zakładka "Gracze" z listą rozwijaną i ikonką "Dodaj gracza" i ikonką lista graczy, gdzie będzie możliwość wyszukania konkretnego zawodnika a obok zakładki "Gracze" powinny się rownież znaleść mecze i raporty z możliwością ich edycji. Po wejściu na konkretnego zawodnika powinny być dane o zawodniku jak róznież statystyki jego formy i jak wypada w porównaniu z innymi zawodnikami. 

###### Strona jest intuicyjna, bardzo prosto zaprojektowana, ale uboga _wizualnie_ .
###### Po przetestowaniu DevToolsow i z punktu widzenia innych urządzeń strona główna jest czytelna jak i pozostałe opcje na stronie np. wtedy gdy wejdę w konkretnego zawodnika. Wszystko wczytuje się prawidłowo. Analiza wczytywania się strony również wyszła prawidłowo.

#### Błędy 🐛

##### Błędy językowe aplikacji w wersji polskiej 🇵🇱 󠁧󠁢󠁥󠁮󠁧󠁿:ENGLISH:
###### - Po zalogowaniu się  wchodzę na Panel Gracze. Panel Gracze w wersji polskiej na górze pasek wyszukiwania z lupką, na górze tekst wyszarzony po angielsku *Search* zamiast *Wyszukaj*. 🔍
###### - W panelu Gracze wyszukuję zawodnika i wchodze na jego profil. Po wejściu na profil i edycji danych zawodnika na dole strony znajdują się dwa przyciski: *Submit* i *Clear* zamiast *Zatwierdź* i *Wyczyść*
###### - Na profilu zawodnika podczas edycji, gdy opuszczam wymagane pole np. Imię, Nazwisko, Data urodzenia, Główna pozycja, wyświetla mi się na czerwono *Required* zamiast *Wymagane*
###### - W panelu Gracze w prawym górnym rogu są ikonki *chmury* ☁️, *drukarki* 🖨️, *3 kolumn*  i symbol *filtra*, gdy najeżdżam myszką na te symbole wyskakuje mi opis po angielsku kolejno: *Download CSV*, *Print*, *View Columns* i *Filter table* zamiast *Załaduj CSV*, *Drukuj*, *Pokaż Kolumny*, *Filtry*. Gdy wchodzę w Filtry wyskakuje tabelka i pojawiają się nagłówki o nazwach *Filters*, *Reset*, i pola *Age*, *Rate* i *max* zamiast *Filtry*, *Resetuj*, *Wiek*, *Ocena* i *maks*.
###### - Po załogowaniu się do platformy na stronie głównej klikam przycisk Gracze i w prawym dolnym rogu gdy chce przejść na następną stronę najeżdżam myszką na strzałkę do przejścia na następną stronę pojawia mi się po angielsku *Next Page* a gdy chciałabym się cofnąć o stronę najeżdżam myszką na strzałkę aby się cofnąć i pojawia mi się po angielsku *Previous Page*
##### Błędy ortograficzne
###### - Po zalogowaniu się do platformy na stronie głównej po prawej stronie sekcja *Aktywnosć* zamiast *Aktywność*
###### - Po zalogowaniu się do platformy na stronie głównej klikam przycisk *Dodaj gracza*, gdzie znajduje się pole do wypełnienia pod nazwą *Pozycja alternatywa* zamiast *Pozycja alternatywna* albo *Optymalna pozycja*
##### Pozostałe błędy
###### - *Brak podwójnej strzałki do przewinięcia graczy do końca* Po zalogowaniu się na platformę, klikam przycisk Gracze i  prawym dolnym rogu aby przejść na ostatnią stronę muszę się przeklikiwać przez 1822 zawodników. Brakuje podwójnej strzałki do przewinięcia graczy do końca. Wtedy przyśpieszyłoby to proces przechodzenia na ostatnią stronę.
###### - *Brak podwójnej strzałki do cofnięcia się na początek strony* Po zalogowaniu sie na platformę, klikam przycisk Gracze i w prawym dolnym rogu po kliknięciu co najmniej dwa razy strzałki następnej strony powinna pojawić się podwójna strzałka służąca do cofnięcia się na początek strony.
###### - *Brak Zalogowany jako użytkownik XYZ* Po zalogowaniu się na platformę, na stronie głównej w prawym górnym rogu powinna się pojawić ikonka zalogowanego użytkownika XYZ.
###### - *Błąd po kliknięciu Dodaj Gracza - Przycisk Dodaj Język* Po zalogowaniu się na platformę klikam przycisk Dodaj Gracza i klikam przyscisk Dodaj Język i pojawia się wyszarzone pole z wyszarzonym napisem Języki zamiast Język. Ponadto mam wrażenie że to pole jest w stanie edycji po wpisaniu języka i to pole wydaje się być cały czas aktywne.Po zatwierdzeniu języka po prawej stronie powinna byc opcja ołówka, żeby móc edytować język i kosza żeby w razie potrzeby usunąć język. Tutaj również dobrze by było żeby przy edytowaniu języka była lista rozwijana z możliwością wyboru języka. 
###### - *W sekcji Dodaj Gracza brak limitu w polach Waga, Wzrost, Wiek i Telefon* 

## Subtask 5
###### Dołączyłam do grupy na Jirze o nazwie challengedareit
