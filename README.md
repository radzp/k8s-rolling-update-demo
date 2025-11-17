# k8s-rolling-update-demo

### Krok 1: Utworzenie bazowego Deploymentu

Polecenie to tworzy Deployment (obraz i liczba replik). Użyto obrazu `nginx:1.16`, ponieważ `nginx:1.9` powodował błędy `ImagePullBackOff` we wcześniejszych próbach.

<img width="672" height="80" alt="Zrzut ekranu 2025-11-17 o 7 16 54 PM" src="https://github.com/user-attachments/assets/5bfba32f-d0d2-4b26-8a8c-faa2107755c5" />

### Krok 2: Dodanie etykiety
To polecenie dodaje wymaganą etykietę typ=proxy do obiektu Deploymentu.

<img width="597" height="80" alt="Zrzut ekranu 2025-11-17 o 7 18 05 PM" src="https://github.com/user-attachments/assets/842770d6-2aa0-4142-9441-59576a8d6080" />

### Krok 3: Dodanie Adnotacji

<img width="721" height="85" alt="Zrzut ekranu 2025-11-17 o 7 19 53 PM" src="https://github.com/user-attachments/assets/af6ec5da-4e5d-45ff-8b70-ae07724c3c7c" />

### Krok 4: Ustawienie strategii aktualizacji
Ręczna modyfikacja manifestu Deploymentu

<img width="538" height="81" alt="Zrzut ekranu 2025-11-17 o 7 20 56 PM" src="https://github.com/user-attachments/assets/8cdc83e0-75a7-449b-ac59-9c92d959c333" /> <br>
Zmieniona została część:

```
maxUnavailable: 2
```
### Krok 6: 
Weryfikacja historii

<img width="494" height="127" alt="Zrzut ekranu 2025-11-17 o 7 23 41 PM" src="https://github.com/user-attachments/assets/92553c46-e5d2-4eb2-abd0-788651baf8a9" />


Status zasobów: 

<img width="678" height="281" alt="Zrzut ekranu 2025-11-17 o 7 23 56 PM" src="https://github.com/user-attachments/assets/bb7c9f73-ab05-428a-99f7-70a8fd6d0af6" />

### Krok 7: Wygenerowanie pliku yaml
<img width="643" height="49" alt="Zrzut ekranu 2025-11-17 o 7 25 02 PM" src="https://github.com/user-attachments/assets/008629e3-c255-4dd2-b9f0-9174d13bc0b3" />
