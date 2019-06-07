# Warsztat ES6 - kalkulatory

## Przygotowanie

Pierwszym etapem było stworzenie środowiska do wykonania zadania - głównie odnosiło się to do zainstalowania npm i webpacka - plikiem wejściowym według założenia miał być `js/app.js`, wyjściowym `js/out.js`.

## Działanie

Warsztat obejmował pracę nad dwoma kalulatorami: binarnym i dziesiętnym.
Kalkulator binarny został już napisany. 
Kolejne działania dotyczyły:

    * Skonfigurowania WebPacka w taki sposób żeby generował style i dołączył do pliku HTML.
    * Połączenia wszystkich plików tak, żeby oba kalkulatory działały poprawnie.
    * Dokończenia kalkulatora dziesiętnego tak, aby dodawał liczby dziesiętne.

**Napisanie kalkulatora dziesiętnego**

1. Stwórzyłam odpowiednie metody oraz konstruktor w klasie `DecCalculator`.

2. W pliku `app.js` zimportowałam odpowiednią klasę oraz stwórzyłam obiekt dla kalkulatora dziesiętnego.

3. W klasie ```DecCalculator``` w konstruktorze jest wywołałam metodę ``` getName()```, która wyświetla nazwę kalkulatora dziesiętnego.

4. **Zmiana liczb** - Nadpisałam metodę `changeNumber()` w klasie `DecCalculator` posługując się  atrybutem **contenteditable** dodałam go do klikniętego elementu (z klasą active) jako atrybut i ustawiłam mu wartość true. Dodtkowo wywołałam na tym elemencie focus().

5. **Nadpisanie metody initEvents()** - Ustawiłam event click na znaku dodawania.
Dodatkowo po kliknięciu w plus wywoła się metoda ```checkNumber()``` oraz ```updateResult()```.

6. **Dodawanie liczb dziesiętnych** - Związane z dodatniem metody `add()`, którą napisałam na podstawie analizy kodu kalkulatora binarnego. 

7. **Zmiana wyniku** - Po kliknięciu w plusa oprócz dodania dwóch liczb jest wywołana jeszcze metoda `updateResult()`. Nadpisałam ją w kalkulatorze dziesiętny - zastosowałam sprawdzanie tablicy `this.resultNumberArray` pobieranie z niej wartości i wstawianie w odpowiednie miejsce w elemencie DOM.


