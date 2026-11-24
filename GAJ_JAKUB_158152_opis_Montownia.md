# Projekt Systemy Operacyjne - Temat 18: Montownia


**Link do repozytorium GitHub:** https://github.com/G4JU5/Montownia


## 1. Opis ogólny środowiska
W hali produkcyjnej (montowni) znajdują się następujące elementy infrastruktury:
* **Magazyn** na podzespoły o pojemności $P$ jednostek.
* **Dwa stanowiska produkcyjne** ($S1$ oraz $S2$).
* **Taśma transportująca** gotowe produkty na rampę załadunkową.
* **Rampa załadunkowa** obsługująca flotę $N$ ciężarówek rozwożących gotowe wyroby do odbiorców.

---

## 2. Magazyn i dostawy podzespołów
* W magazynie o pojemności $P$ jednostek przechowywane są cztery typy podzespołów:
  * **P1** – zajmuje **1** jednostkę magazynową,
  * **P2** – zajmuje **2** jednostki magazynowe,
  * **P3** – zajmuje **3** jednostki magazynowe,
  * **P4** – zajmuje **3** jednostki magazynowe.
* Podzespoły pochodzą z **4 niezależnych źródeł** i są dostarczane w nieokreślonych momentach czasowych.
* Fabryka przyjmuje do magazynu maksymalnie dużo podzespołów, aby zachować płynność produkcji.

---

## 3. Stanowiska montażowe i taśma transportowa
* Pracownicy pobierają podzespoły z magazynu i przenoszą je na stanowiska montażowe:
  * **Stanowisko S1** – składa wyroby z podzespołów **P1, P2 oraz P3**.
  * **Stanowisko S2** – składa wyroby z podzespołów **P2, P3 oraz P4**.
* Gotowe produkty są odkładane przez pracowników ze stanowisk $S1$ i $S2$ na taśmę transportową najszybciej, jak to możliwe.
* **Ograniczenia i zasady działania taśmy transportowej:**
  * Maksymalna liczba produktów na taśmie w danej chwili: **$K$ sztuk**.
  * Maksymalny udźwig taśmy: **$M$ jednostek masy** – niedopuszczalne jest umieszczenie na taśmie np. samych produktów ze stanowiska $S2$ (ponieważ $8K > M$).
  * **Kolejność FIFO:** produkty zjeżdżające z taśmy muszą bezpośrednio trafiać na ciężarówkę dokładnie w takiej kolejności, w jakiej zostały na niej położone.

---

## 4. Rampa i transport ciężarówkami
* Montownia dysponuje łącznie **$N$ ciężarówkami**, z których każda ma ładowność **$L$ jednostek**.
* Ciężarówkę podstawioną na końcu taśmy należy zawsze załadować do pełna (chyba że dyrektor wyda odpowiednie polecenie).
* Po zapełnieniu ciężarówki na jej miejsce natychmiast pojawia się nowa ciężarówka o ładowności $L$ (o ile jest aktualnie dostępna).
* Ciężarówki rozwożą produkty do odbiorców i po losowym czasie $T_i$ wracają do montowni.

---

## 5. Polecenia dyrektora i warunki zakończenia pracy
* **`polecenie_1`** – magazyn kończy pracę.
* **`polecenie_2`** – montownia kończy pracę.
* **`polecenie_3`** – montownia i magazyn kończą pracę jednocześnie; aktualny stan magazynu zostaje zapisany w pliku, a po ponownym uruchomieniu symulacji jest z niego odtwarzany.
* **`polecenie_4`** – ciężarówka stojąca aktualnie przy taśmie może odjechać z montowni z niepełnym ładunkiem.
* **`polecenie_5`** – pracownicy na wskazanym stanowisku montażowym kończą pracę.
* **Zakończenie pracy floty:** ciężarówki kończą pracę po rozwiezieniu wszystkich wyprodukowanych produktów.

---

## 6. Wymagania programistyczne
Należy zaimplementować procedury (procesy) symulujące działanie montowni:
1. **Dyrektor**
2. **Dostawca**
3. **Pracownik** (na stanowiskach montażowych $S1$ i $S2$)
4. **Kierowca ciężarówki**

Raport z przebiegu symulacji (logi) należy zapisać w pliku (lub plikach) tekstowym.
---

