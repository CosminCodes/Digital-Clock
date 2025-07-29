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

<img width="1446" height="658" alt="image" src="https://github.com/user-attachments/assets/c7cb1e24-67f0-4719-a63d-f6af3cfeb3ad" />


# Configuratia pinilor
<img width="868" height="782" alt="image" src="https://github.com/user-attachments/assets/a1ca6284-a841-4025-9106-84fd4c3ed8a1" />


# Schema electrica (KiCad)
<img width="1500" height="1077" alt="image" src="https://github.com/user-attachments/assets/c01e69ce-3b35-45cb-98a2-1ae9131a2458" />


# Implementare

## Implementarea Butoanelor

Sistemul este controlat și configurat folosind 4 butoane, fiecare având funcționalități diferite.

<p align="center">
	<p align="center">
	<img width="872" height="627" alt="image" src="https://github.com/user-attachments/assets/2e7323ac-47e1-4d02-897d-b0c9bc51bbcd" />

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
	<img width="617" height="250" alt="image" src="https://github.com/user-attachments/assets/98278efa-b259-40d6-b312-f561d82094c2" />

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
    <img width="556" height="231" alt="image" src="https://github.com/user-attachments/assets/2be5aab0-0d89-4c68-877a-274cc46fc9fe" />
    <img width="575" height="236" alt="image" src="https://github.com/user-attachments/assets/2479f97c-b9e1-4034-8a53-dff59a4a0b57" />
</p>


#### Setare Calendar


- Această interfață permite utilizatorului să seteze ziua, data și săptămâna.

<p align="center">
	<img width="533" height="225" alt="image" src="https://github.com/user-attachments/assets/693d2567-247b-483b-b46d-2f7e6b9831df" />
</p>

#### Setare Alarmă


- Această interfață permite utilizatorului să seteze valorile pentru ore și minute.
- Dacă modul ceas este 12h, există opțiunea de a comuta între am/pm.
- Reține valorile setate anterior, permițând utilizatorului să știe exact ora la care este setată alarma.

<p align="center">
    <img width="614" height="272" alt="image" src="https://github.com/user-attachments/assets/6ead5d83-ba3b-4bd8-8e3c-1417c0a1dc66" />
    <img width="614" height="272" alt="image" src="https://github.com/user-attachments/assets/c70614f7-e4bf-48c7-a3c2-ca2c45ab4be8" />
</p>












