# 🌀 AeroFlow — Virtueller 3D-Windkanal

Ein virtueller Windkanal im Browser. Eigene 3D-Modelle laden und die Umströmung
in Echtzeit visualisieren — als CFD-artige Wirbelfäden oder klassische Stromlinien.

**Live:** https://luka2705.github.io/aeroflow/

## Features

- **Modelle laden:** STL, OBJ, GLB/GLTF und BLEND (inkl. Blender 4.5+/5.x) per Drag & Drop
- **Zwei Darstellungen:**
  - 🌀 *Wirbel (CFD)* — tausende Vortex-Filamente: Scherschicht an der Hinterkante,
    Kelvin-Helmholtz-Aufrollen, Mehrskalen-Turbulenz, Färbung nach Vorticity
  - ✦ *Beams* — animierte Stromlinien, gefärbt nach Geschwindigkeit
- **Mesh-genaue Umströmung** über ein Signed-Distance-Field (three-mesh-bvh)
- Druckvisualisierung auf der Oberfläche, Schnittebenen mit Druckfeld,
  grobe Kennwerte (c<sub>w</sub>, Stirnfläche, Luftwiderstand)
- Demo-Objekte: Auto, Flügel, Tropfen, Kugel, Kapsel, Ring

> ⚠️ Keine echte CFD-Simulation — die Strömung ist ein physikalisch motiviertes,
> synthetisches Feld für Anschauung und Ästhetik, kein Rechenwerkzeug.

## Lokal starten

Statische Seite ohne Build-Schritt — einfach einen lokalen Server starten:

```bash
python3 -m http.server 8000
```

und http://localhost:8000 öffnen.

## Tech

Three.js (ES-Module via CDN), three-mesh-bvh, fzstd, js.blend — alles clientseitig.
