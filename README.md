<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:0f0c29,50:302b63,100:24c6dc&height=200&section=header&text=SeraGlow&fontSize=64&fontColor=ffffff&animation=fadeIn&fontAlignY=38&desc=Foto-Editor%20f%C3%BCr%20Portr%C3%A4ts%20%E2%80%93%20komplett%20lokal&descAlignY=60&descSize=20" width="100%" alt="SeraGlow"/>

![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white)
![React](https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)
![Vite](https://img.shields.io/badge/Vite-646CFF?style=for-the-badge&logo=vite&logoColor=white)
![WebGL2](https://img.shields.io/badge/WebGL2-990000?style=for-the-badge&logo=webgl&logoColor=white)
![CUDA](https://img.shields.io/badge/CUDA-76B900?style=for-the-badge&logo=nvidia&logoColor=white)
![Status](https://img.shields.io/badge/Status-Alpha-24c6dc?style=for-the-badge&labelColor=0f0c29)

*Keine Accounts, kein Abo, keine Cloud-Pflicht.*

</div>

---

> 👀 **Dies ist eine Arbeitsprobe.** Der Quellcode ist nicht öffentlich. Hier steht, was das Projekt kann und wie ich es gebaut habe. Den Code zeige ich gern im Gespräch.

## ✨ Was ist das?

SeraGlow ist ein Foto-Editor für Porträts, gebaut mit **React, Vite und TypeScript**. Alles läuft im Browser: Fotos und Projekte bleiben auf dem Gerät, **nichts wird hochgeladen**. Ich plane, baue und teste es allein.

<div align="center">

<img src="screenshots/editor.jpg" width="49%" alt="Editor mit Werkzeugleiste"/>
<img src="screenshots/hautwerkzeug.jpg" width="49%" alt="Hautwerkzeug mit Reglern"/>

<sub>Das Beispielfoto ist von einem Bildmodell erzeugt, es zeigt keine echte Person.</sub>

</div>

## 🧰 Was kann es?

- **Porträt:** Hautretusche (kantenerhaltend), Strahlen, Schärfe, Verformen per Netz-Warp (WebGL2), Gesichtsteile, Augen, Make-up als Pigment, Haarfarbe
- **Farbe & Licht:** Licht & Farbe, Tonkurve, Farbkanäle, Farbstimmung, Stile, Lichteffekte
- **Bild & Szene:** Zuschneiden, Proportionen, Unschärfe, Hintergrund und Freistellen ohne Farbsaum, Himmel, Objekt entfernen
- **Bereiche:** automatisch wählen (Motiv, Himmel, Haut, Haare, Augen, Lippen, Zähne …) oder selbst malen und gezielt bearbeiten
- **Komfort:** Zoomen, Pinsel, Vergleichen, Rückgängig, automatisches Speichern, Export bis 4096 px

## 🧠 KI, CUDA und viele Bilder

Die Bildverarbeitung läuft im Browser (Canvas, WebGL2, Web Worker). Für schwere Aufgaben gibt es einen **optionalen lokalen KI-Dienst** (Python, CUDA); ohne ihn nutzt die App eingebaute Verfahren.

- **Eigene Modelle mit CUDA trainiert:** kleine Netze für Mund, Brauen, Augen und Himmel, trainiert auf meiner eigenen GPU (RTX 5060 Laptop, 8 GB), mit Dauertraining und Prüfung an echten Fotos
- **Viele Bilder selbst erzeugt:** Beispielbilder und große Teile der Trainingsdaten stammen aus Bildmodellen (SDXL-Lightning), Masken und Paare dazu automatisch gebaut. Echte Fotos nur mit geprüfter Lizenz.
- **Eingebunden:** MediaPipe im Browser, im lokalen Dienst u. a. SAM 2, BiRefNet, Depth Anything V2 (Small), Real-ESRGAN, SCUNet
- **Speicherverwaltung:** Modelle wandern gezielt zwischen Grafikkarte und Arbeitsspeicher, damit 8 GB reichen

## 🔭 Noch offen

Himmel-Erkennung in Randfällen, sehr große Flächen beim Ausbessern, feine Babyhaare bei der Haarfarbe und ein **Video-Editor** (geplant, noch nicht gebaut).

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:24c6dc,50:302b63,100:0f0c29&height=100&section=footer" width="100%" alt=""/>
