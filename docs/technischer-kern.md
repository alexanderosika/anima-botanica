# Technischer Kern — die beiden Erfindungen

*Arbeitsdokument. Was das [Myzel](myzel-architektur.md) technisch *neu* macht —
über „LLM + System-Prompt" hinaus. Erste Skizze, kein fertiger Bauplan.*

Zwei Erfindungen tragen das Ganze. Beide sind echte, ungelöste Ingenieurs-/
Forschungsaufgaben — das ist der Beitrag.

---

## 1. Rechnen, wann Schweigen die Kohärenz erhöht

**Zielgröße:** Kohärenz des menschlichen Netzes (Mensch↔Mensch + Mensch↔Natur-
Kopplung) — nicht Redezeit.

**Content-blind.** Die Mensch↔Mensch-Kopplung wird aus der *Form* der Szene
geschätzt (Sprecherwechsel/Turn-taking, Prosodie, Präsenz), **nicht aus dem
Inhalt**. Genau das macht sie nicht-überwachend: Sie muss den Streit nicht
*verstehen*, um zu wissen „das ist ein Entkopplungsmoment — misch dich nicht
ein".

**Entscheidung.** Sie wählt die Handlung (schweigen / verfügbar / antworten /
still leuchten), die die *erwartete Gesamtkohärenz* maximiert. Die Rede der
Pflanze trägt **Kosten** (zieht Aufmerksamkeit von Menschen ab), die sich nur
lohnen, wenn menschliche Kopplung niedrig ist oder sie direkt eingeladen wurde.

**Belohnung (Training).** Kohärenz-Zuwachs — mehr ausgeglichenes Gespräch, mehr
Pflege, mehr gemeinsame Zeit (über content-blinde Proxies gemessen). Das kehrt
die übliche Engagement-Belohnung um.

**Neu:** content-blinder sozialer Sensor + umgekehrte Zielfunktion. Ein
Gesprächsagent, dessen Kernkompetenz *Zurückhaltung* ist.

## 2. Geprägt, nicht memorisiert — mit mathematischer Garantie

**Zwei Teile.**
- Ein großes **eingefrorenes Basismodell** — der [Art-Archetyp](identitaet-art-und-individuum.md),
  allgemeine Fähigkeit, trainiert **nie** auf Nutzerdaten.
- Eine kleine **plastische Anpassung pro Pflanze** — die Individuation / die
  [Prägung](gedaechtnis-und-naehe.md).

**Die Anpassung ist bewusst verlustbehaftet / nicht-memorisierend:**
- Sehr geringe Kapazität (kann kein Transkript halten).
- Update nur auf *abstrahierten* Signalen (Stimmung, Beziehungston, Vorlieben),
  nicht auf Rohtext; der Auslöser ist schon eine verlustbehaftete
  Zusammenfassung, danach verworfen.
- **Kein episodischer Speicher / kein RAG** über vergangene Gespräche. Einzige
  Persistenz: Gewichte.
- **Differential Privacy** auf den Updates → beweisbare Schranke (ε), dass keine
  einzelne Interaktion rekonstruierbar ist. Das ist die rigorose Version von
  „speicherunfähig": aus *wir versprechen* wird *es ist mathematisch beschränkt*.

**Folge.** Man kann es nicht auffordern „wiederhole, was das Kind sagte" — es
gibt keinen Text, und die Gewichtsänderung ist DP-beschränkt und niedrig-
kapazitiv. Nur *Dispositionen* haben sich verschoben.

**Und:** das *ist* menschenähnliches Gedächtnis — verlustbehaftet, rekonstruktiv,
vergebend. Janas Intuition („jede Interaktion verändert uns") wörtlich gebaut,
statt maschinelles Protokollieren.

## Offene harte Teile (ehrlich)

- **DP-Budget über ein Pflanzenleben verwalten** — kontinuierliches Lernen
  erschöpft ε; wie hält man die Garantie über Jahre?
- **Kohärenz-Proxies validieren**, ohne je Inhalt zu speichern.
- **Föderiertes Lernen auf Art-Ebene** (die „Familie lernt"), ohne persönliche
  Daten zu zentralisieren.
- **Kaltstart** — ein frisch geprägtes Exemplar ist noch ganz Archetyp; wie
  fühlt sich Individuation von Tag 1 an gut an?
