# Przewidywanie cen akcji - metody uczenia maszynowego
Projekt dotyczy analizy oraz prognozowania cen akcji spółki Google (GOOGL) na podstawie danych historycznych z lat 2021–2025. Celem pracy było porównanie klasycznych metod analizy szeregów czasowych z metodami uczenia maszynowego oraz sieciami neuronowymi.

## Dane
Dane giełdowe zostały pobrane z serwisu Yahoo Finance i obejmują dzienne notowania akcji (Open, High, Low, Close, Volume). Na ich podstawie wygenerowano dodatkowe zmienne czasowe, takie jak rok, miesiąc, dzień tygodnia oraz liczba dni od początku szeregu.

## Przetwarzanie danych
W ramach przetwarzania danych wykonano:
- skalowanie zmiennych,
- konwersję danych do postaci numerycznej,
- budowę okien czasowych o długości 30 dni,
- podział danych na zbiór treningowy i testowy (4:1) z zachowaniem kolejności czasowej.

## Zastosowane metody
W projekcie wykorzystano następujące metody:
- średnia krocząca (MA),
- wykładnicza średnia krocząca (EMA),
- regresja liniowa,
- k-najbliższych sąsiadów (KNN),
- las losowy (Random Forest),
- sieć neuronowa LSTM.

## Ocena modeli
Do oceny jakości predykcji wykorzystano następujące miary:
- MSE (Mean Squared Error),
- RMSE (Root Mean Squared Error),
- MAE (Mean Absolute Error).

## Wnioski
Metody klasyczne (MA i EMA) dobrze odwzorowują krótkoterminowe trendy cen. Spośród modeli uczenia maszynowego najlepiej poradziła sobie regresja liniowa, która dobrze uchwyciła ogólny trend i wartości szczytowe. Bardziej złożone modele (KNN, Random Forest oraz LSTM) miały trudności z przewidywaniem gwałtownych zmian cen w końcowej części szeregu czasowego.
