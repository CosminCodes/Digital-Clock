<img width="852" height="488" alt="Picture1" src="https://github.com/user-attachments/assets/a93824dd-c42e-482a-94d2-6dee56f9275f" />

# Ceas-digital

Descriere proiect 

Un ceas digital și un calendar cu funcționalitate de alarmă dezvoltat pe microcontrolerul STM32F401 , utilizând RTC DS1307 pentru menținerea timpului. Include o interfață bazată pe un ecran LCD pentru setarea orei, datei și alarmei.
Sistemul oferă o interfață de utilizator bazată pe un ecran LCD, care permite setarea orei, datei și alarmei. Configurările sunt realizate prin intermediul mai multor butoane conectate la microcontroler, folosind un mecanism de întreruperi pentru gestionarea interacțiunilor utilizatorului în timp real.

Printre funcționalitățile sale cheie se numără:

Moduri de ceas configurabile (12h și 24h) cu conversie instantanee între moduri.
Setare și afișare a alarmei și calendarului.
Indicator de alarmă prin intermediul unui LED și buzzer.
Posibilitatea de a opri alarma automat sau manual prin apăsarea unui buton.
Controlul iluminării LCD-ului cu ajutorul unui buton dedicat.


# Schema logica a proiectului 

![image](https://github.com/user-attachments/assets/2b777af2-8a73-43a0-90c1-039d8f2e3c25)

# Configuratia pinilor
![image](https://github.com/user-attachments/assets/46df3eef-f4ba-4854-adc1-e60320a10c51)

# Schema electrica (KiCad)
![image](https://github.com/user-attachments/assets/867463f6-da73-4862-a482-b446b0b28f49)

# Implementare

## Implementarea Butoanelor

Sistemul este controlat și configurat folosind 4 butoane, fiecare având funcționalități diferite.

<p align="center">
	<p align="center">
	<img src="https://github.com/user-attachments/assets/3c2a556e-9490-492c-a20c-004770c42831" width="80%" height="80%">
</p>


### Buton 1: Buton de Configurare RTC

- Acest buton este utilizat pentru a comuta între diferitele interfețe de utilizator de pe LCD pentru setarea ceasului, calendarului și alarmei.
- După finalizarea setării, butonul revine la interfața principală afișată pe LCD.

### Buton 2: Buton Mod Ceas

#### Funcție Principală
- Comută între modurile de afișare 12h și 24h.

#### Funcție Secundară
- Setează statusul am/pm pentru ceas și alarmă în modul 12h.
- Setează ziua săptămânii.

### Buton 3: Buton Control Alarmă

#### Funcție Principală
- Oprește alarma în timpul declanșării.
- Activează/Dezactivează alarma (alarma nu se declanșează când este dezactivată).

#### Funcție Secundară
- Setează valoarea orei pentru ceas și alarmă.
- Setează data calendarului.

### Buton 4: Control Iluminare LCD

#### Funcție Principală
- Activează/Dezactivează iluminarea LCD-ului.

#### Funcție Secundară
- Setează valoarea minutelor pentru ceas și alarmă.
- Setează luna din calendar.

---

## Implementarea Afișajului LCD

### Interfața Principală

Interfața principală afișează următoarele caracteristici:


<p align="center">
	<img src="https://github.com/user-attachments/assets/c6edfdbc-3d6d-4584-9fb1-4c331e95e147" width="45%" height="45%">
</p>

- Mod ceas care afișează fie **'24h>'** în format 24h sau **'am/pm'** în format 12h.
- Ora în format **'hh:mm:ss'**.
- Calendarul în format **'zi dd/mm'**.
- Indicator pentru activare/dezactivare alarmă, afișat ca **'AL>'** când este activat.

### Interfețe Secundare

#### Setare Ceas

- Această interfață permite utilizatorului să seteze valorile pentru ore și minute.
- Dacă modul ceas este 12h, există opțiunea de a comuta între am/pm.




<p align="center">
    <img src="https://github.com/user-attachments/assets/20b6938f-dfc6-4240-975e-0f92e74cbea9" width="45%">
    <img src="https://github.com/user-attachments/assets/b99ab8fb-1fb3-4cf1-8361-5e9da11076c2" width="45%">
</p>


#### Setare Calendar


- Această interfață permite utilizatorului să seteze ziua, data și săptămâna.

<p align="center">
	<img src="https://github.com/user-attachments/assets/a866e6ab-fcab-4c58-9ede-280404e14080" width="45%" height="45%">
</p>

#### Setare Alarmă


- Această interfață permite utilizatorului să seteze valorile pentru ore și minute.
- Dacă modul ceas este 12h, există opțiunea de a comuta între am/pm.
- Reține valorile setate anterior, permițând utilizatorului să știe exact ora la care este setată alarma.

<p align="center">
    <img src="https://github.com/user-attachments/assets/0bd1bec9-e0f5-43c0-824c-b1201ce6652c" width="45%">
    <img src="https://github.com/user-attachments/assets/91f0409d-392c-47a2-87b3-8c9e2d93840e" width="45%">
</p>












