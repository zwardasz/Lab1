# Lab1
## Moduł 1: Kali Linux | Wprowadzenie do testów penetracyjncych - rekonesans
### Zbigniew Wardaszka numer albumu 303729

## ZADANIE 1

Na początku pobieramy stronę za pomocą polecenia `wget`
![obraz1](https://github.com/zwardasz/Lab1/blob/master/obraz1.png)

Następnie poleceniem `grep` wyodrębniamy wszystkie wiersze zawierające ciąg "href=" (te wiersze zawierają adres URL)
![obraz2](https://github.com/zwardasz/Lab1/blob/master/obraz2.png)

Następnie wyodrębniamy nazwy domen przycinając wiersze przy użyciu polecenia `cut` z separatorem "/" na trzecim polu.
![obraz3](https://github.com/zwardasz/Lab1/blob/master/obraz3.png)

Kolejnym krokiem jest wyodbrębnienie wierszy posidających kropkę.
![obraz4](https://github.com/zwardasz/Lab1/blob/master/obraz4.png)

Następnie czyścimy je używając polecenia `cut` do pierwszej kolumny
![obraz5](https://github.com/zwardasz/Lab1/blob/master/obraz5.png)

Aby zlikwidować powtarzające się adresy (duplikaty) używamy polecenia `sort` z opcją _unique_ `-u`.
![obraz6](https://github.com/zwardasz/Lab1/blob/master/obraz6.png)

Teraz zapisujemy to w postaci listy.
![obraz7](https://github.com/zwardasz/Lab1/blob/master/obraz7.png)

Następnie za pomocą pętli `for` i polecenia `host` dla każdej domeny w pliku tekstowych znajdujemy odpowiedni adres IP.
![obraz7](https://github.com/zwardasz/Lab1/blob/master/obraz7.png)

Ostatnim krokiem jest wyodręnienie adresów IP za pomocą poleceia `grep`. Szukamy wyrażenia `"has address"`, a następnie wycinamy i sortujemy dane wyjściowe.
![obraz8](https://github.com/zwardasz/Lab1/blob/master/obraz8.png)
