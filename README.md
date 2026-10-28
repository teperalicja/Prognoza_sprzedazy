# Prognoza tygodniowej sprzedaży sieci sklepów

## O projekcie
Projekt dotyczy prognozowania tygodniowej sprzedaży sieci sklepów. Prognozę przygotowałam dla każdego sklepu i działu na cały 2013 rok, w dwóch wersjach: sprzedaży **bazowej** (bez promocji) i **całkowitej**
(z promocjami, na podstawie zmiennych `MarkDown`). Jakość prognozy oceniłam zarówno dla pojedynczych sklepów i działów, jak i dla łącznej sprzedaży całej firmy.

## Trenowane modele
- Regresja liniowa: prosty model do porównania.
- Random Forest: model oparty na wielu drzewach decyzyjnych.
- XGBoost, sprzedaż bazowa: model bez zmiennych `MarkDown`.
- XGBoost, sprzedaż całkowita: model ze zmiennymi `MarkDown`.

Jako punkt odniesienia użyłam prostej prognozy „tyle, ile w tym samym tygodniu rok temu” (bez trenowania modelu).
Do prognozy na 2013 wybrałam XGBoost, ponieważ uczy się kilka razy szybciej niż Random Forest przy podobnej dokładności.