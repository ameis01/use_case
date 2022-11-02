# System aukcyjny

## Wprowadzenie

Specyfikacja wymaga� funkcjonalnych w ramach informatyzacji procesu sprzeda�y produkt�w w oparciu o mechanizm aukcyjny. 

## Procesy biznesowe

---
<a id="bc1"></a>
### BC1: Sprzeda� aukcyjna 

**Aktorzy:** [Sprzedaj�cy](#ac1), [Kupuj�cy](#ac2)

**Opis:** Proces biznesowy opisuj�cy sprzeda� za pomoc� mechanizmu aukcyjnego. |

**Scenariusz g��wny:**
1. [Sprzedaj�cy](#ac1) wystawia produkt na aukcj�. ([UC1](#uc1))
2. [Kupuj�cy](#ac2) oferuje kwot� za produkt wy�sz� od aktualnie najwy�szej oferty. ([BR1](#br1))
3. [Kupuj�cy](#ac2) wygrywa aukcj� ([BR2](#br2))
4. [Kupuj�cy](#ac2) przekazuje nale�no�� Sprzedaj�cemu.
5. [Sprzedaj�cy](#ac1) przekazuje produkt Kupuj�cemu.

**Scenariusze alternatywne:** 

2.A. Oferta Kupuj�cego zosta�a przebita, a [Kupuj�cy](#ac2) pragnie przebi� aktualnie najwy�sz� ofert�.
* 2.A.1. Przejd� do kroku 2.

3.A. Czas aukcji up�yn�� i [Kupuj�cy](#ac2) przegra� aukcj�. ([BR2](#br2))
* 3.A.1. Koniec przypadku u�ycia.

---

## Aktorzy

<a id="ac1"></a>
### AC1: Sprzedaj�cy

Osoba oferuj�ca towar na aukcji.

<a id="ac2"></a>
### AC2: Kupuj�cy

Osoba chc�ca zakupi� produkt na aukcji.


## Przypadki u�ycia poziomu u�ytkownika

### Aktorzy i ich cele

[Sprzedaj�cy](#ac1):
* [UC1](#uc1): Wystawienie produktu na aukcj�
* ...

[Kupuj�cy](#ac2)
* ...

---
<a id="uc1"></a>
### UC1: Wystawienie produktu na aukcj�

**Aktorzy:** [Sprzedaj�cy](#ac1)

**Scenariusz g��wny:**
1. [Sprzedaj�cy](#ac1) zg�asza do systemu ch�� wystawienia produktu na aukcj�.
2. System prosi o podanie danych produktu i ceny wywo�awczej.
3. [Sprzedaj�cy](#ac1) podaje dane produktu oraz cen� wywo�awcz�.
4. System weryfikuje poprawno�� danych.
5. System informuje o pomy�lnym wystawieniu produktu na aukcj�.

**Scenariusze alternatywne:** 

4.A. Podano niepoprawne lub niekompletne dane produktu.
* 4.A.1. System informuje o b��dnie podanych danych.
* 4.A.2. Przejd� do kroku 2.

---

<a id="uc2"></a>
### UC2: ...

**Aktorzy:** [Sprzedaj�cy](#ac1), [Kupuj�cy](#ac2), ...

**Scenariusz g��wny:**
1. ...

**Scenariusze alternatywne:** 

1.A. ...
* 4.A.1. ...

---

## Obiewkty biznesowe (inaczje obiekty dziedzinowe lub informatycjne)

### BO1: Aukcja

Aukcja jest form� zawierania transakcji kupna-sprzeda�y, w kt�rej Sprzedaj�cy okre�la cen� wywo�awcz� produktu, natomiast Kupuj�cy mog� oferowa� w�asn� ofert� zakupu ka�dorazowo proponuj�c kwot� wy�sz� od aktualnie oferowanej kwoty. Aukcja ko�czy si� po up�ywie okre�lonego czasu. Je�li z�o�ona zosta�a co najmniej jedna oferta zakupy produkt nabywa ten Kupuj�cy, kt�ry zaproponowa� najwy�sz� kwot�. 

### BO2: Produkt

Fizyczny lub cyfrowy obiekt, kt�ry ma zosta� sprzedany w ramach aukcji.

## Regu�y biznesowe

<a id="br1"></a>
### BR1: Z�o�enie oferty

Z�o�enie oferty wymaga zaproponowania kwoty wy�szej ni� aktualnie oferowana o minimum 1,00 PLN.


<a id="br2"></a>
### BR2: Rozstrzygni�cie aukcji

Aukcj� wygrywa ten z [Kupuj�cy](#ac2)ch, kt�ry w momencie jej zako�czenia (up�yni�cia czasu) z�o�y� najwy�sz� ofert�.

## Macierz CRUDL


| Przypadek u�ycia                                  | Aukcja | Produkt | ... |
| ------------------------------------------------- | ------ | ------- | --- |
| UC1: Wystawienia produktu na aukcj�               |    C   |    C    | ... |
| ???                                               |  ...   |  ...    | ... |


