# Smart Car Health Monitor

![Project Banner](banner.png) <!-- Poți înlocui cu o imagine relevantă -->

## Descriere

Smart Car Health Monitor este un sistem inteligent construit cu **Raspberry Pi** care monitorizează în timp real starea mașinii prin **OBD-II** și oferă notificări către șofer în caz de valori critice sau anomalii. Sistemul crește siguranța și ajută la prevenirea defecțiunilor, oferind vizualizare live printr-un **dashboard web** sau aplicație mobilă.

---

## Funcționalități

- Citire date de la ECU prin OBD-II (temperatura motor, turație, tensiune baterie, viteza vehiculului etc.)
- Monitorizare continuă a parametrilor critici
- Alertare în timp real prin dashboard și notificări
- Stocare valori istorice pentru analiză și detecție anomalii
- Posibilitate de a detecta tipare anormale în comportamentul mașinii

---

## Componente

**Hardware:**
- Raspberry Pi 4 (sau Pi 3B+/Pi Zero 2 W)  
- Modul OBD-II USB/Bluetooth  
- Breadboard și cabluri jumper  
- Alimentator USB-C 5V/3A  

**Software:**
- Python 3
- Flask / Django pentru dashboard web
- SQLite sau PostgreSQL pentru stocarea datelor
- Biblioteci Python: `pyOBD`, `requests`, `pandas`, `matplotlib` (opțional pentru grafice)  

---

## Arhitectura sistemului

```
Mașină (ECU) --> Modul OBD-II --> Raspberry Pi --> Procesare date + detectie anomalii --> Dashboard Web / Notificări
```

- **Raspberry Pi:** „Creierul” sistemului – colectează, procesează și stochează date.  
- **Modul OBD-II:** „Ochii” – citește datele mașinii.  
- **Dashboard:** „Fața” – afișează valorile, trendurile și alertele către utilizator.  

---

## Instalare

1. Clonați repository-ul:

```bash
git clone https://github.com/username/smart-car-health-monitor.git
cd smart-car-health-monitor
```

2. Instalați dependențele:

```bash
pip install -r requirements.txt
```

3. Conectați modulul OBD-II la Raspberry Pi.  
4. Rulați serverul Flask/Django:

```bash
python app.py
```

5. Accesați dashboard-ul la `http://<IP_PI>:5000`  

---

## Contribuții

Proiectul este open-source și binevenite contribuțiile!  
- Deschideți un **issue** pentru bug-uri sau sugestii.  
- Trimiteți **pull request-uri** pentru funcționalități noi sau îmbunătățiri.

---

## Licență

Acest proiect este licențiat sub **MIT License**.  
Datele OBD-II standard sunt utilizate legal fără licențe speciale.

---

## Contact

Pentru întrebări sau colaborări:  
- Email: example@email.com  
- GitHub: [username](https://github.com/username)
