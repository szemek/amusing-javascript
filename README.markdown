Instrukcja
===============

Cześć!  
Kod, który tutaj się znajduje jest drobną modyfikacją: https://github.com/kaaes/simple-dom-game  
Pobierz pliki źródłowe na dysk https://github.com/szemek/amusing-javascript/zipball/master  
Rozpakuj archiwum zip i otwórz plik `game_final.js` w swoim ulubionym edytorze, a plik `index.html` otwórz w przeglądarce.

Przed Tobą małe wyzwanie!  

Twoim zadaniem jest zaimplementowanie metody `changeType` dla obiektu `Player` w pliku `game_final.js`.
W okolicach 333 linijki znajdziesz poniższy fragment.

```
Player.prototype.changeType = function(type) {
  // TO IMPLEMENT
};
```

Metoda `changeType` powinna zmienić typ gracza.  
Przykłady:  
`game.activePlayer.changeType("monk")` - aktywny gracz gry jest zamieniony na mnicha

Wskazówki:  
  * `game` jest obiektem gry
  * `game.activePlayer` zwraca aktywnego gracza
  * `game.playersList` zwraca kawałek HTML-a strony, który jest odpowiedzialny za ustawienie graczy na planszy
  * `game.players` zwraca listę obiektów graczy
  * `this` wewnątrz metody `changeType` zwraca aktualny obiekt, dla którego metoda jest wykonywana

Proponowany sposób rozwiązania:  
  1.  Przypisz do zmiennej listę wszystkich graczy.
  2.  W pętli przejdź po wszystkich graczach z listy i znajdź aktualnego (` == this`)
  3.  W HTML-u strony zaktualizuj typ aktualnego gracza, który znajduje się w tagu `li` w atrybucie `class`. Obiekt gracza pod odpowiednim indeksem w tablicy `game.players` odpowiada elementowi `li` w HTML-u strony. `querySelectorAll` i odpowiedni indeks mogą przydać się w realizacji tego punktu.
  4.  Zaktualizuj także pole `type` dla aktualnego obiektu.