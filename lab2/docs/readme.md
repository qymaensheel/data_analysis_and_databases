# Analiza i Bazy Danych
## Bartosz Nieroda


### Projekt dotyczy zaaplikowania protokołu TIER do dostarczonych danych, w moim przypadku billboard.csv

Pierwszym krokiem było pobranie danych oraz utworzenie struktury katalogów zgodnie z wymaganiami protokołu TIER. Opis danych znajduje się w pliku metadata.md.

Kolejnym krokiem było wczytanie ich do pliku jupyter notebook.

Następnie na surowych danych przeprowadziłem dwie operacje: pierwszą z nich jest *melt* przekształcający tabelę do formatu którego wiersz odpowiada notowaniu danej piosenki w danym tygodniu. Bez tej operacji zasada *jeden wiersz - jedna obserwacja* byłaby niespełniona.

Ostatnią operacją było usunięcie wierszy z wartosciami *NaN*: w przypadku mojego datasetu były to rekordy piosenek, które w danych tygodniach nie znajdowały się w rankingu. Operacja usunęła sporo zbędnych wierszy które nie wnosiły żadnych informacji. 

Gotowe dane zapisałem w katalogu *analysis_data* w postaci pliku csv.