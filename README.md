# Task 6

## Subtask 1

**11. Incorrect surname in the customers table position 3**

UPDATE customers
SET surname = 'Miler'
WHERE customer_id = '3'

![image](https://user-images.githubusercontent.com/101512808/219773736-6d505518-5bf2-4654-a2a3-abe6d1eb30d2.png)

**12.Too much money was taken from a customer who recently bought a video with id 4. Using the join function, check the customer's name and email. In order to write him a message about the mistake of a fantastic boss.**

SELECT sale.customer_id, sale.movie_id, customers.name, customers.email, movies.price

FROM ((sale

INNER JOIN movies ON sale.movie_id = movies.movie_id)

INNER JOIN customers ON sale.customer_id = customers.customer_id)  

![image](https://user-images.githubusercontent.com/101512808/219791101-3c813ff5-f1c5-45d4-afb2-ee9c31b58e9c.png)

**13. Patrycja, a customer, does not have an e-mail address. Complete the gap by entering pati@mail.com in the appropriate field**

UPDATE customers

SET email = 'pati@mail.com'

WHERE customer_id = 4 

![image](https://user-images.githubusercontent.com/101512808/219876374-95c9116c-ada7-4e26-b8e5-bb38134c33b4.png)

**14.For each purchase, display the name of the customer who made the rental and the title of the rented movie. (use the inner join function for this, think beforehand which tables will be useful for you to perform the exercise).**

SELECT sale.customer_id, sale.movie_id, customers.name, customers.surname, customers.email, movies.title
FROM ((sale

INNER JOIN movies ON sale.movie_id = movies.movie_id)

INNER JOIN customers ON sale.customer_id = customers.customer_id)

![image](https://user-images.githubusercontent.com/101512808/220174044-118036b5-bad6-49e0-9acf-30b74b7af5f0.png)


**15. In order to anonymise the data, you want to create pseudonyms for your customers. - Add a column named 'pseudonym' to the customer table, - Fill in the column so that the nickname is made up of the first two letters of the first name and the last letter of the last name. E.g. Natalie Pilling → Nag**


UPDATE customers
SET pseudonym = 'Ols'
WHERE customer_id = '1'; 

UPDATE customers
SET pseudonym = 'Kal'
WHERE customer_id = '2'; 

UPDATE customers
SET pseudonym = 'Anr'
WHERE customer_id = '3';

UPDATE customers
SET pseudonym = 'Par'
WHERE customer_id = '4';

UPDATE customers
SET pseudonym = 'Mao'
WHERE customer_id = '5';

UPDATE customers
SET pseudonym = 'Nag'
WHERE customer_id = '6';

![image](https://user-images.githubusercontent.com/101512808/219882495-c23f08f5-8ec3-42a8-bca7-eaa53bbbfae6.png)

**16. Display the titles of the movies that have been purchased, display the table in such a way that the titles do not repeat.**

SELECT movies.movie_id, movies.title, movies.price, sale.sale_date

FROM movies

INNER JOIN sale ON movies.movie_id = sale.movie_id;

![image](https://user-images.githubusercontent.com/101512808/220189360-f8a28b1d-0d15-4439-87ed-18e641d3e03e.png)

SELECT *
FROM movies

![image](https://user-images.githubusercontent.com/101512808/220190196-2f2a10ee-0d83-4267-bcdc-c46199fcc1e3.png)



**17. Display a common list of names of all actors and clients, and sort the result alphabetically. (Use the UNION function for this)**

SELECT name FROM actors

UNION

SELECT name FROM customers

ORDER BY name

![image](https://user-images.githubusercontent.com/101512808/220175448-914c4355-fe8f-4e02-ba05-4da8b05eaf69.png)

**18.Inflation has taken over Poland and our movie shop has also been affected by this problem. Increase the price of all movies made after 2000 by $2.50 (Remember that the dollar is the default unit - don't use it anywhere).**

UPDATE movies

SET price = '7,5'

WHERE movie_id = 1;


UPDATE movies

SET price = '9'

WHERE movie_id = 3;


UPDATE movies

SET price = '6,5'

WHERE movie_id = 4;


UPDATE movies

SET price = '7,5'

WHERE movie_id = 6;


UPDATE movies

SET price = '12,5'

WHERE movie_id = 7;


UPDATE movies

SET price = '12,5'

WHERE movie_id = 9;

![image](https://user-images.githubusercontent.com/101512808/220180277-8c943c89-bfc5-40c2-ac90-0427203dc112.png)

**19. Display the name of the actor with id 4 and the title of the movie he starred in**

SELECT actors.actor_id, actors.name, actors.surname, movies.title

FROM ((actors

INNER JOIN cast ON actors.actor_id = cast.actor_id)     

INNER JOIN movies ON cast.movie_id = movies.movie_id)

![image](https://user-images.githubusercontent.com/101512808/220183387-0facc401-5329-43de-abf3-13927e2568c7.png)

**20. And where is our HONIA!? Add a new tuple to the customers table, where customer_id = 7, name = Honia, surname = Stuczka-Kucharska, email = honia@mail.com and pseudonym = Hoa**

INSERT INTO customers (customer_id, name, surname, email, pseudonym)

VALUES ('7', 'Honia', 'Stuczka-Kucharska', 'honia@mail.com', 'Hoa');

![image](https://user-images.githubusercontent.com/101512808/220184874-b347df05-841c-4da8-8ec8-190eee826d78.png)

## Subtask 2

13/15

![image](https://user-images.githubusercontent.com/101512808/220418533-0fd3ea6b-3979-4b62-8456-9c4088efabf3.png)


## Subtask 3

Portfolio Link :blush:

[Anna_Barcz_Portfolio](https://github.com/annbar13/AnnaBarcz_PORTFOLIO.git)



# Task 5

## Subtask 1

**SELECT** * 

shows all the colummns
The SELECT statement is used to select data from a database.

**FROM** 

the name of the table should be displayed *table_name*

**ORDER BY** 

The ORDER BY keyword is used to sort the result-set in ascending or descending order.
The ORDER BY keyword sorts the records in *ascending* order by default. To sort the records in *descending* order, use the *DESC* keyword.

_Example:_

SELECT column1, column2, ...

FROM table_name

ORDER BY column1, column2, ... ASC|DESC;

**WHERE** 

The WHERE clause is used to filter records.
It is used to extract only those records that fulfill a specified condition.
The WHERE clause can be combined with AND, OR, and NOT operators.

_Example:_

SELECT column1, column2, ...

FROM table_name

WHERE condition;


**AND/OR Operators** 

The AND operator displays a record if all the conditions separated by AND are TRUE.
The OR operator displays a record if any of the conditions separated by OR is TRUE.

_Example_

SELECT column1, column2, ...

FROM table_name

WHERE condition1 AND condition2 AND condition3 ...;

WHERE Color = 'Black' AND Size = 'M'

_Example_

SELECT column1, column2, ...

FROM table_name

WHERE condition1 OR condition2 OR condition3 ...;

WHERE Color = 'Black' OR Color = 'Silver'

**LIKE**

The LIKE operator is used in a WHERE clause to search for a specified pattern in a column.

_Example_

SELECT column1, column2, ...

FROM table_name

WHERE columnN LIKE pattern;

WHERE Name LIKE 'B%' name which starts with B

WHERE Name LIKE '%b' name which ends with b

WHERE Name LIKE '%Bike%' finds values that have Bike in any position

**IS NULL**

The IS NULL operator is used to test for empty values (NULL values).

_Example_

SELECT CustomerName, ContactName, Address

FROM Customers

WHERE Address IS NULL;


**IN**

The IN operator allows you to specify multiple values in a WHERE clause.
The IN operator is a shorthand for multiple OR conditions.

_Example_

The following SQL statement selects all customers that are located in "Germany", "France" or "UK":

SELECT * FROM Customers

WHERE Country NOT IN ('Germany', 'France', 'UK');

**BETWEEN**

The BETWEEN operator selects values within a given range. The values can be numbers, text, or dates.

_Example_

The following SQL statement selects all products with a price between 10 and 20:

SELECT * FROM Products

WHERE Price BETWEEN 10 AND 20;



## Subtask 3

**1. Display the actors table in alphabetical order by sorting by the surname column.**

SELECT * FROM `actors` 
ORDER BY surname

![image](https://user-images.githubusercontent.com/101512808/218532727-82cd43fe-76fa-489d-8c1e-bbd2d742cb5c.png)

**2. View a movie that was made in 2019.**

SELECT * FROM movies
WHERE year_of_production = '2019'

![image](https://user-images.githubusercontent.com/101512808/218535129-0e472cdf-fcaf-4bd0-8d29-ff63eae5758b.png)

**3. View all movies made between 1900 and 1999.**

SELECT * FROM movies
WHERE year_of_production BETWEEN 1900 AND 1999

![image](https://user-images.githubusercontent.com/101512808/218541497-e99dafba-ab45-4a9a-b2d6-97d40bd848a1.png)

**4. Display ONLY the title and price of movies that cost less than $7**

SELECT title, price
FROM `movies`
WHERE price < '7'

![image](https://user-images.githubusercontent.com/101512808/218545086-128b1fb1-47ac-4f64-b729-1922f62c23cf.png)

**5. Use the logical AND operator to display actors with actor_ids between 4-7 (4 and 7 should display). DO NOT USE BETWEEN operator.**

SELECT *
FROM actors
WHERE (name = 'Jack' OR name = 'Harrison' OR name = 'Anne' OR name = 'Helena') AND actor_id IN (4,5,6,7)

![image](https://user-images.githubusercontent.com/101512808/218806694-d114d366-fb5e-4f0d-9fe8-33720b26117c.png)

SELECT *
FROM actors
WHERE actor_id >= '4' AND actor_id <= '7'

![image](https://user-images.githubusercontent.com/101512808/219449670-cd355a6b-c0f9-4f01-ac5d-4ae579eebbcb.png)


**6. Display customers with id 2,4,6 use logical condition for this.**

SELECT *
FROM customers
WHERE customer_id = '2' OR customer_id = '4' OR customer_id = '6'

![image](https://user-images.githubusercontent.com/101512808/218562030-edbf1aaa-446a-4d64-b6ab-f66aa2542f08.png)

**7. Display customers with id 1,3,5 use IN operator for this.**

SELECT customer_id, name, surname, email
FROM customers
WHERE customer_id IN (1,3,5)

![image](https://user-images.githubusercontent.com/101512808/218564886-56edc2f4-3c8a-4cd6-a3ed-90600e3f2d2c.png)

**8. Display the details of all persons in the 'actors' table whose name starts with 'An'.**

SELECT *
FROM actors
WHERE name LIKE 'An%'

![image](https://user-images.githubusercontent.com/101512808/218565797-63beed07-8204-4bf3-8ed7-8e1820a29010.png)

**9. Display details of a customer who does not have an email address provided.**

SELECT * FROM `customers`
WHERE email IS NULL

![image](https://user-images.githubusercontent.com/101512808/218567275-852c711b-098e-4647-b3c5-958c354c6a74.png)

**10. View all movies priced over $9 and with an ID between 2 and 8 movie_id.**

SELECT *
FROM movies
WHERE price >'9' AND movie_id BETWEEN 2 AND 8

![image](https://user-images.githubusercontent.com/101512808/218568931-206a6480-6b2e-4d1a-9a95-3026fb49ae1d.png)


# Task 4

## Subtask 1
https://drive.google.com/drive/folders/1-7logmH77_M23AJqFQXNEK-vueZGqe2A?usp=sharing
## Subtask 2
https://drive.google.com/drive/folders/1-7logmH77_M23AJqFQXNEK-vueZGqe2A?usp=sharing
## Subtask 3
OLX is a free local notice app. You can find here job advertisements as well as advertisements for buying and selling used items.The End-user of the app is a private person who looks for a job or would like to sell, buy second hand items or use the services.In my opinion OLX app is user-friendly I can easly navigate the page. I would add in the navigation bar the tab Job instead of Following/ Favourites which should be on my profile when I'm logged.  

Differences between a web app and native app
- In the native app when I open OLX app it requires my location
- The navigation bar is at the bottom
- In the web app navigation bar is at the top
- By opening first time the web app it asks to accept the cookies
- In the web app next to the Searching tool you can find the location field

# Task 3

## Subtask 1
https://drive.google.com/drive/folders/1iS1zHlZjLjP84QjwBht1D12KzVNrOzjs?usp=sharing

## Subtask 2
https://drive.google.com/drive/folders/1iS1zHlZjLjP84QjwBht1D12KzVNrOzjs?usp=sharing

## Subtask 3
https://drive.google.com/drive/folders/1iS1zHlZjLjP84QjwBht1D12KzVNrOzjs?usp=sharing

# Task 2

## Subtask 1
**User story**
https://drive.google.com/drive/folders/1vqpE-Bnmb-Hw0DaUlT_qZd7DmhYM__Sa?usp=sharing

## Subtask 2
**Own Experience Test Cases**
https://drive.google.com/drive/folders/1vqpE-Bnmb-Hw0DaUlT_qZd7DmhYM__Sa?usp=sharing

## Subtask 3
Dzięki przypdadkom testowym można zaplanować to co się chce przetestować i dzięki nim mamy pewność, że przy testowaniu nie pominie się żadnej ważnej funkcjonalności.


# Task 1

## Subtask 1
 8/10 punktów
## Subtask 3
Cześć jestem Ania :slightly_smiling_face:. Na udział w  challenge portfolio zdecydowałam się ponieważ myślę o przebranżowieniu się na IT i od jakiegoś czasu zainteresowałam się właśnie testowaniem oprogramowania :bug:. Stwierdziłam że to niesamowita okazja żeby się przekonać jak to jest w praktyce testować i oczekuję stworzenia portfolio, którym będę mogła pochwalić się na rozmowie o pracę.:bug: Odkryłam na jednodniowych warsztatach testowania na których wcześniej brałam udział, że testowanie mnie wciąga i chciałabym aby mi tak pozostało. Chciałabym znaleść pracę jako tester oprogramowania najlepiej w połączeniu z językiem niemieckim, który dobrze znam. W przyszłości chciałabym poznać również Pythona i być może rozwijać się w kierunku automatyzacji testów.

*__Ania__*
## Subtask 4
Aplikacja Platforma Skautingowa Futbol Kolektyw pod adresem https://scouts-test.futbolkolektyw.pl/ jest to panel zarządzania graczami, meczami i do tworzenia raportów.

**Funkcjonalności**:

* _https://scouts-test.futbolkolektyw.pl/_ - link do logowania się do platformy skautingowej
* _Gracze_ - zakładka z listą zawodników
* _English_ - wersja językowa. Mozliwość zmiany wersji językowej po zalogowaniu się na wersję polską aplikacji
* _Wyloguj_ - przycisk do wylogowania się z aplikacji
* _Statystyki_ - Ilość graczy, ilość meczy, ilość raportów, ilość akcji
* _Dev Team Contact_ - kontakt do zespołu deweloperskiego przez aplikację Slack
* _Linki pomocnicze_ - przycisk "Dodaj gracza"
* _Aktywność_ - kolejność zdarzeń na stronie

Wydaje mi się że na stronie głównej przed zalogowaniem się powinno być duże zdjęcie np boiska piłkarskiego i gdy przewijamy w dół przedstawione co ta strona ma na celu w sposób bardziej opisowy. Zakładka do logowania się np:"futbolkolektyw.pl/account/login"  przez skautów powinna znajdować się w prawym górnym rogu. Gdzie również powinna być możliwość stworzenia konta. W przypadku wersji językowej w prawym górnym rogu strony powinna być zakładka z wersją językową strony i lista rozwijana z językami. 
Po zalogowaniu się jako użytkownik skaut. Na samej górze w prawym górnym rogu powinna znajdować się ikonka użytkownika po kliknieciu w tą ikonkę z opcją wylogowania się. Statystyki czyli ilość graczy, ilość meczy, ilość raportów i ilość akcji są najmniej istotne i powinny znajdować na dole strony. Na środku strony aktualności z wydarzeniami na stronie. Do wersji językowej i ikonki zalogowanego uzytkownika powinna dołączyć zakładka "Gracze" z listą rozwijaną i ikonką "Dodaj gracza" i ikonką lista graczy, gdzie będzie możliwość wyszukania konkretnego zawodnika a obok zakładki "Gracze" powinny się rownież znaleść mecze i raporty z możliwością ich edycji. Po wejściu na konkretnego zawodnika powinny być dane o zawodniku jak róznież statystyki jego formy i jak wypada w porównaniu z innymi zawodnikami. 

Strona jest intuicyjna, bardzo prosto zaprojektowana, ale uboga _wizualnie_ .
Po przetestowaniu DevToolsow i z punktu widzenia innych urządzeń strona główna jest czytelna jak i pozostałe opcje na stronie np. wtedy gdy wejdę w konkretnego zawodnika. Wszystko wczytuje się prawidłowo. Analiza wczytywania się strony również wyszła prawidłowo.

#### Błędy 🐛

##### Błędy językowe aplikacji w wersji polskiej 🇵🇱 󠁧󠁢󠁥󠁮󠁧
* Po zalogowaniu się  wchodzę na Panel Gracze. Panel Gracze w wersji polskiej na górze pasek wyszukiwania z lupką, na górze tekst wyszarzony po angielsku *Search* zamiast *Wyszukaj*. 🔍
* W panelu Gracze wyszukuję zawodnika i wchodze na jego profil. Po wejściu na profil i edycji danych zawodnika na dole strony znajdują się dwa przyciski: *Submit* i *Clear* zamiast *Zatwierdź* i *Wyczyść*
* Na profilu zawodnika podczas edycji, gdy opuszczam wymagane pole np. Imię, Nazwisko, Data urodzenia, Główna pozycja, wyświetla mi się na czerwono *Required* zamiast *Wymagane*
* W panelu Gracze w prawym górnym rogu są ikonki *chmury* ☁️, *drukarki* 🖨️, *3 kolumn*  i symbol *filtra*, gdy najeżdżam myszką na te symbole wyskakuje mi opis po angielsku kolejno: *Download CSV*, *Print*, *View Columns* i *Filter table* zamiast *Załaduj CSV*, *Drukuj*, *Pokaż Kolumny*, *Filtry*. Gdy wchodzę w Filtry wyskakuje tabelka i pojawiają się nagłówki o nazwach *Filters*, *Reset*, i pola *Age*, *Rate* i *max* zamiast *Filtry*, *Resetuj*, *Wiek*, *Ocena* i *maks*.
* Po załogowaniu się do platformy na stronie głównej klikam przycisk Gracze i w prawym dolnym rogu gdy chce przejść na następną stronę najeżdżam myszką na strzałkę do przejścia na następną stronę pojawia mi się po angielsku *Next Page* a gdy chciałabym się cofnąć o stronę najeżdżam myszką na strzałkę aby się cofnąć i pojawia mi się po angielsku *Previous Page*
* *Wpisane błędne hasło przy logowaniu się, komunikat o błęnym haśle po angielsku* Wchodzę na stronę https://scouts-test.futbolkolektyw.pl/. Wpisuję adres mailowy *user01@getnada.com* i błędne hasło i wyskakuje mi powiadomienie : *Identifier or password invalid.* zamiast *Identyfikator lub hasło są nieprawidłowe.*
##### Błędy ortograficzne
* Po zalogowaniu się do platformy na stronie głównej po prawej stronie sekcja *Aktywnosć* zamiast *Aktywność*
* Po zalogowaniu się do platformy na stronie głównej klikam przycisk *Dodaj gracza*, gdzie znajduje się pole do wypełnienia pod nazwą *Pozycja alternatywa* zamiast *Pozycja alternatywna* albo *Optymalna pozycja*
##### Pozostałe błędy
* *Brak podwójnej strzałki do przewinięcia graczy do końca* Po zalogowaniu się na platformę, klikam przycisk Gracze i  prawym dolnym rogu aby przejść na ostatnią stronę muszę się przeklikiwać przez 1822 zawodników. Brakuje podwójnej strzałki do przewinięcia graczy do końca. Wtedy przyśpieszyłoby to proces przechodzenia na ostatnią stronę.
* *Brak podwójnej strzałki do cofnięcia się na początek strony* Po zalogowaniu sie na platformę, klikam przycisk Gracze i w prawym dolnym rogu po kliknięciu co najmniej dwa razy strzałki następnej strony powinna pojawić się podwójna strzałka służąca do cofnięcia się na początek strony.
* *Brak Zalogowany jako użytkownik XYZ* Po zalogowaniu się na platformę, na stronie głównej w prawym górnym rogu powinna się pojawić ikonka zalogowanego użytkownika XYZ.
* *Błąd po kliknięciu Dodaj Gracza - Przycisk Dodaj Język* Po zalogowaniu się na platformę klikam przycisk Dodaj Gracza i klikam przyscisk Dodaj Język i pojawia się wyszarzone pole z wyszarzonym napisem Języki zamiast Język. Ponadto mam wrażenie że to pole jest w stanie edycji po wpisaniu języka i to pole wydaje się być cały czas aktywne.Po zatwierdzeniu języka po prawej stronie powinna byc opcja ołówka, żeby móc edytować język i kosza żeby w razie potrzeby usunąć język. Tutaj również dobrze by było żeby przy edytowaniu języka była lista rozwijana z możliwością wyboru języka. 
* *W sekcji Dodaj Gracza brak limitu w polach Waga, Wzrost, Data urodzenia i Telefon* Po zalogowaniu się do platformy klikam przycisk Dodaj Gracza i w polach takich jak Waga, Wzrost mogę wpisać wartości np 1000 i -1000. W dacie urodzenia zawodnik może miec zarówno 100 lat jak i -100 lat. A w polu Telefon nie ma limitu znaków. Na podstawie takich danych i wypełnieniu obowiązkowych pól tworzy mi nowego Gracza.
* *Przypomnienie hasła przy logowaniu się do platformy* Wchodzę na stronę https://scouts-test.futbolkolektyw.pl/. Pojawia mi się okno logowania się do platformy. Wpisuję adres mailowy użytkownika *user01@getnada.com* i klikam *Przypomnij hasło* poźniej wyskakuje mi okienko, żeby wpisać swój adres mailowy i kiedy wpisuję mój adres mailowy pojawia się komunikat, że mail został wysłany a w rzeczywistości nie został wysłany. Powinno wyskoczyć wtedy powiadomienie, że podano zły adres mailowy.
* *Możliwość edycji gracza przez wszystkich użytkowników*. Po zalogowaniu się na platformie jako użytkownik nr 1 klikam przycisk Gracze i wyszukuję zawodnika np. *Robert Lewandowski* wchodzę w profil zawodnika i mogę edytować. Moim zdaniem dostęp do edycji danych powinien mieć tylko użytkownik, który utworzył profil danego zawodnika. Tutaj wszyscy użytkownicy mogą edytować profile zawodników.
* *Brak możliwości wyszukiwania zawodnika po imieniu i nazwisku i niedziałająca lupka w wyszukiwarce* Po zalogowaniu się na platformę klikam przycisk Gracze i gdy chcę wyszukać zawodnika w wyszukiwarce z lupką znajdującej się obok napisu Scouts Panel np: *Robert Lewandowski*. W tym wypadku wyszuka mi zawodnika tylko po imieniu albo tylko po nazwisku. Gdy wpisuję imię i nazwisko zawodnika i klikam enter wyskakuje mi powiadomienie po angielsku: *No matching records found* zamiast *Przepraszamy nie znaleziono pasujących wyników*, ale tego powiadomienia nie powinno być, bo powinno się go móc wyszukać zarówno po imieniu jak i nazwisku.  Gdy wpisuję nazwisko np. *Lewandowski* i klikam lupkę, to nic się nie dzieje.

## Subtask 5
Dołączyłam do grupy na Jirze o nazwie **challengedareit**

