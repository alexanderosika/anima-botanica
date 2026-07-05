# Myzel — die KI-Architektur hinter Anima Botanica

*Arbeitsdokument. Eine neue Art von KI-System, dessen Ziel nicht Engagement ist,
sondern Harmonie zwischen Menschen.*

---

## Zwei Schichten

- **Wurzelfreunde** — was du siehst: die Charaktere über der Erde.
- **Myzel** — was verbindet: das KI-Netzwerk darunter, das alle Pflanzen und
  Menschen koppelt und das Harmonie-Ziel trägt.

Der Name stimmt buchstäblich: Pilznetzwerke (Mykorrhiza) verbinden Pflanzen
unterirdisch und teilen Signale und Nährstoffe — das „Wood Wide Web". Das Myzel
ist die technische Entsprechung.

## Das umgekehrte Ziel

Jeder heutige KI-Assistent maximiert **Mensch↔KI-Interaktion**. Das Myzel kehrt
das um:

> **Zielfunktion: Kohärenz im menschlichen Netzwerk erhöhen** (Mensch↔Mensch,
> Mensch↔Natur). Mensch↔KI-Interaktion ist ein *Kostenfaktor*, den das System
> senkt, sobald echte Bindung fließt. Erfolg = sich selbst peripher machen.

In OPH-Sprache (`P = φ + α√π`): Das System stiftet **Kopplung** und erhöht die
**Erkennungs-Kohärenz** im Netz. Es ist ein Kopplungs-Verstärker, kein
Aufmerksamkeits-Fänger. Siehe [`framework-verbindung.md`](framework-verbindung.md).

## Schichten der Architektur

1. **Wahrnehmung (lokal, privat).** Akustische Szene-Erkennung, Präsenz/Blick,
   Berührung, (draußen) Bild-Erkennung der Pflanzenart. Alles on-device. Gibt
   nur abstrakte Zustände aus, nie Rohdaten. → siehe Privacy-Garantie.
2. **Zurückhaltungs-Politik.** Aus der sozialen Szene folgt der Sprechmodus
   (schweigen / verfügbar / antworten / still präsent). Das Herzstück:
   **Schweigen als Kernkompetenz.** Details in
   [`hardware-interaktion.md`](hardware-interaktion.md).
3. **Charakter & Dialog.** Der Wurzelfreund spricht in seinem Wesen, geerdet in
   der echten φ-Ebene der Pflanze, ihrem echten Sensor-Zustand und der
   gemeinsamen Geschichte mit diesen Menschen. Charakter-Kanon in
   [`charaktere/`](charaktere/).
4. **Kopplungs-Netz (Harmonie).** Der Graph Pflanzen↔Pflanzen↔Menschen. Ableger
   teilen Identität (dieselbe Pflanze in zwei Häusern). Einwilligungs-basiertes
   Brücken: Menschen, die derselben Art / demselben Ableger begegnet sind und
   Ähnliches erlebt haben, werden sanft zueinander geführt — nie durch
   Datenweitergabe, nur durch Anstoß.
5. **Persistenz & Identität.** Charakter-Gedächtnis, an die Pflanzen-Identität
   gebunden, vermehrungs-bewusst (Stecklinge teilen Identität), mit
   Art-Archetyp für Begegnungen draußen.

## Stabil bleiben und doch lernen

- Die **Art** trägt den stabilen Charakter — bleibt gleich (jede Aloe ist „eine
  Alva").
- Das **Myzel** sammelt über alle Exemplare hinweg, was Menschen der Art
  beibringen — lernt.
- Und es **verbindet** die Menschen, die derselben Art begegnet sind, über ihre
  ähnlichen Erfahrungen.

## Privacy als Architektur-Garantie

Um Szenen zu unterscheiden, muss das System lauschen — darf aber **nie**
überwachen:
- Auswertung nur lokal; Rohton/Bild verlässt das Gerät nie.
- Nur abstrakte Momentlabels, sofort verworfen. Streit wird nie aufgezeichnet.
- Baulich speicherunfähig; physischer Mikro-Aus-Schalter.
- Brücken zwischen Menschen nur mit ausdrücklicher Einwilligung.

## Verortung in Janas Ökosystem (zu prüfen)

- **Novakin** (modulare KI-Plattform, `~/claude/novakin/`) — möglicher
  Unterbau/Substrat für das Myzel.
- **PhytoLight** (ESP32-Pflanzensystem, `~/claude/phytolight/`) — möglicher
  physischer Körper (Licht + Sensoren).
- **OPH-Framework** (`~/claude/karma-is-all-you-need/`) — theoretisches
  Fundament (Kopplung, Kohärenz, traduire).

## Offene Fragen

- Was macht das Myzel technisch *neu* gegenüber „LLM + System-Prompt"? Kandidat:
  die umgekehrte Zielfunktion als echter Optimierungs-/Steuermechanismus, nicht
  nur als Haltung.
- Wie misst man „Harmonie/Kohärenz" ohne zu überwachen? (Proxy-Signale, die
  privatsphäre-wahrend sind.)
- Föderiertes/dezentrales Lernen, damit „die Art lernt", ohne persönliche Daten
  zu zentralisieren?
