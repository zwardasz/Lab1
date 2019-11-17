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


## ZADANIE 2
W tym miejscu nastepuje uzgodnienie sesji TCP
![obraz9](https://github.com/zwardasz/Lab1/blob/master/uzgodnienie_sesji_tcp_1.png)

A w tym zakończenie sesji. Nie widać flagi [FIN] ponieważ jest ona szyfrowana.
![obraz10](https://github.com/zwardasz/Lab1/blob/master/obraz10.png)

## ZADANIE 3
-niestety nie potrafię zrobić tego zadania

## ZADANIE 4 i 5

Strona jaką wybrałem to www.t-mobile.com
Za pomoca komend `filetype` wpisując w cudzysłowie "salaries" 
![obraz11](https://github.com/zwardasz/Lab1/blob/master/1.1.png)
Możemy znależć między innymi takie informacje jak ta:
![obraz12](https://github.com/zwardasz/Lab1/blob/master/1.2.png)
lub wpisując "bonuses"
![obraz13](https://github.com/zwardasz/Lab1/blob/master/1.3.png)
dostajemy informację o bonusach
![obraz14](https://github.com/zwardasz/Lab1/blob/master/1.4.png)
## ZADANIE 6
Wpisując podobne hasła do domeny pw.edu.pl nie znajdujemy żadnych poufnych danych.
![obraz15](https://github.com/zwardasz/Lab1/blob/master/1.5.png)
## ZADANIE 7
Za pomocą polecenia `whois` systemu operacyjnego Kali Linux identyfikujemy nazwy serwerów Politechniki Warszawskiej
![obraz16](https://github.com/zwardasz/Lab1/blob/master/serwery_pw%20(2).png)

## ZADANIE 8
Znajdujemy serwery DNS domeny `megacorpone.com`
![obraz17](https://github.com/zwardasz/Lab1/blob/master/serwery%20megacorpone%20(2).png)

##ZADANIE 9

