# System aukcyjny

## Wprowadzenie

Specyfikacja wymagañ funkcjonalnych w ramach informatyzacji procesu sprzeda¿y produktów w oparciu o mechanizm aukcyjny. 

## Procesy biznesowe

---
<a id="bc1"></a>
### BC1: Sprzeda¿ aukcyjna 

**Aktorzy:** [Sprzedaj¹cy](#ac1), [Kupuj¹cy](#ac2)

**Opis:** Proces biznesowy opisuj¹cy sprzeda¿ za pomoc¹ mechanizmu aukcyjnego. |

**Scenariusz g³ówny:**
1. [Sprzedaj¹cy](#ac1) wystawia produkt na aukcjê. ([UC1](#uc1))
2. [Kupuj¹cy](#ac2) oferuje kwotê za produkt wy¿sz¹ od aktualnie najwy¿szej oferty. ([BR1](#br1))
3. [Kupuj¹cy](#ac2) wygrywa aukcjê ([BR2](#br2))
4. [Kupuj¹cy](#ac2) przekazuje nale¿noœæ Sprzedaj¹cemu.
5. [Sprzedaj¹cy](#ac1) przekazuje produkt Kupuj¹cemu.

**Scenariusze alternatywne:** 

2.A. Oferta Kupuj¹cego zosta³a przebita, a [Kupuj¹cy](#ac2) pragnie przebiæ aktualnie najwy¿sz¹ ofertê.
* 2.A.1. PrzejdŸ do kroku 2.

3.A. Czas aukcji up³yn¹³ i [Kupuj¹cy](#ac2) przegra³ aukcjê. ([BR2](#br2))
* 3.A.1. Koniec przypadku u¿ycia.

---

## Aktorzy

<a id="ac1"></a>
### AC1: Sprzedaj¹cy

Osoba oferuj¹ca towar na aukcji.

<a id="ac2"></a>
### AC2: Kupuj¹cy

Osoba chc¹ca zakupiæ produkt na aukcji.


## Przypadki u¿ycia poziomu u¿ytkownika

### Aktorzy i ich cele

[Sprzedaj¹cy](#ac1):
* [UC1](#uc1): Wystawienie produktu na aukcjê
* ...

[Kupuj¹cy](#ac2)
* ...

---
<a id="uc1"></a>
### UC1: Wystawienie produktu na aukcjê

**Aktorzy:** [Sprzedaj¹cy](#ac1)

**Scenariusz g³ówny:**
1. [Sprzedaj¹cy](#ac1) zg³asza do systemu chêæ wystawienia produktu na aukcjê.
2. System prosi o podanie danych produktu i ceny wywo³awczej.
3. [Sprzedaj¹cy](#ac1) podaje dane produktu oraz cenê wywo³awcz¹.
4. System weryfikuje poprawnoœæ danych.
5. System informuje o pomyœlnym wystawieniu produktu na aukcjê.

**Scenariusze alternatywne:** 

4.A. Podano niepoprawne lub niekompletne dane produktu.
* 4.A.1. System informuje o b³êdnie podanych danych.
* 4.A.2. PrzejdŸ do kroku 2.

---

<a id="uc2"></a>
### UC2: ...

**Aktorzy:** [Sprzedaj¹cy](#ac1), [Kupuj¹cy](#ac2), ...

**Scenariusz g³ówny:**
1. ...

**Scenariusze alternatywne:** 

1.A. ...
* 4.A.1. ...

---

## Obiewkty biznesowe (inaczje obiekty dziedzinowe lub informatycjne)

### BO1: Aukcja

Aukcja jest form¹ zawierania transakcji kupna-sprzeda¿y, w której Sprzedaj¹cy okreœla cenê wywo³awcz¹ produktu, natomiast Kupuj¹cy mog¹ oferowaæ w³asn¹ ofertê zakupu ka¿dorazowo proponuj¹c kwotê wy¿sz¹ od aktualnie oferowanej kwoty. Aukcja koñczy siê po up³ywie okreœlonego czasu. Jeœli z³o¿ona zosta³a co najmniej jedna oferta zakupy produkt nabywa ten Kupuj¹cy, który zaproponowa³ najwy¿sz¹ kwotê. 

### BO2: Produkt

Fizyczny lub cyfrowy obiekt, który ma zostaæ sprzedany w ramach aukcji.

## Regu³y biznesowe

<a id="br1"></a>
### BR1: Z³o¿enie oferty

Z³o¿enie oferty wymaga zaproponowania kwoty wy¿szej ni¿ aktualnie oferowana o minimum 1,00 PLN.


<a id="br2"></a>
### BR2: Rozstrzygniêcie aukcji

Aukcjê wygrywa ten z [Kupuj¹cy](#ac2)ch, który w momencie jej zakoñczenia (up³yniêcia czasu) z³o¿y³ najwy¿sz¹ ofertê.

## Macierz CRUDL


| Przypadek u¿ycia                                  | Aukcja | Produkt | ... |
| ------------------------------------------------- | ------ | ------- | --- |
| UC1: Wystawienia produktu na aukcjê               |    C   |    C    | ... |
| ???                                               |  ...   |  ...    | ... |


