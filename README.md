# Atomkraftwerke

**Eine Fabric-Mod für Minecraft Java Edition, die die Funktionsweise eines Druckwasserreaktors interaktiv und didaktisch vereinfacht simuliert.**

![Status](https://img.shields.io/badge/Status-Planungsphase-lightgrey)
![Minecraft](https://img.shields.io/badge/Minecraft-Version%20offen-lightgrey)
![Loader](https://img.shields.io/badge/Loader-Fabric-blue)
![Java](https://img.shields.io/badge/Java-Version%20offen-lightgrey)
![Lizenz](https://img.shields.io/badge/Lizenz-offen-lightgrey)

<!-- Platzhalter: Build-, Release- und Download-Badges ergänzen, sobald CI und Veröffentlichungen existieren. -->

> [!NOTE]
> Das Projekt befindet sich in der **Planungsphase**. Es gibt noch keinen Quellcode, keinen Build und keine Veröffentlichung. Alle hier beschriebenen Funktionen sind **geplant**, nicht umgesetzt.

---

## Einführung

**Atomkraftwerke** ist eine eigenständige Minecraft-Mod, die ein Kernkraftwerk mit **Druckwasserreaktor (DWR, englisch Pressurized Water Reactor, PWR)** als begehbare, bedienbare Anlage in die Minecraft-Welt bringt. Spieler können eine moderne Leitwarte betreten, auf physischen Bildschirmen den Zustand von Reaktor, Kühlkreisläufen und Generator verfolgen und über Bedienkonsolen in den Betrieb eingreifen, etwa durch das Einfahren der Steuerstäbe oder eine Notabschaltung.

Die Mod entsteht im Rahmen eines **Chemie-Schulprojekts der 9. Klasse** und begleitet ein Minecraft-Video von etwa 2–6 Minuten Länge. Ziel ist es, die Energieumwandlung von der Kernspaltung bis zur elektrischen Energie anschaulich und fachlich korrekt zu erklären.

> [!IMPORTANT]
> Die Simulation ist ein **didaktisches Modell**. Sie ist **kein** ingenieurwissenschaftlich validierter Reaktorsimulator und enthält **keine** realen Bedienungsanleitungen. Alle Zahlenwerte in der Mod sind vereinfacht oder illustrativ.

## Technologie-Stack

| Bereich | Technologie | Stand |
|---|---|---|
| Spiel | Minecraft Java Edition | Version **offen** |
| Mod-Loader | Fabric Loader | Version **offen** |
| Schnittstelle | Fabric API | Version **offen** |
| Sprache | Java | Version **offen** (richtet sich nach der Minecraft-Version) |
| Build | Gradle (mit Fabric Loom) | Version **offen** |
| 3D-Modelle | Blockbench | – |
| Grafische Assets (optional) | ResourcePack.ai | optional |
| Entwicklung | Claude Code mit Claude Opus 5.5 | – |

Die Mod soll **keine verpflichtenden Abhängigkeiten** zu anderen Gameplay- oder Technik-Mods haben. Texturen, Modelle und Sounds werden direkt in der Mod ausgeliefert. Ein zusätzliches Resourcepack ist nicht erforderlich.

## Funktionsübersicht (geplant)

| Bereich | Beschreibung |
|---|---|
| Reaktorsimulation | Vereinfachtes Modell von Kernspaltung, Kettenreaktion, Steuerstäben, Neutronenfluss, Leistung und Temperatur |
| Drei Wasserkreisläufe | Primärkreislauf, Sekundärkreislauf und Kühlkreislauf, im Dampferzeuger thermisch gekoppelt und stofflich getrennt |
| Energieumwandlung | Kernenergie → Wärmeenergie → mechanische Energie → elektrische Energie, mit Wirkungsgrad |
| Physische Bildschirme | Monitore als platzierbare Blöcke, Inhalte direkt in der 3D-Welt gerendert, ohne Klick sofort sichtbar |
| Leitwarte | Bedienkonsolen für Steuerstäbe, Pumpen, Notabschaltung und Alarmquittierung |
| Alarmmanagement | Zentrales System mit den Stufen `NORMAL`, `INFO`, `WARNING`, `CRITICAL` und `SHUTDOWN` |
| Störfallszenarien | Pumpenausfall, Temperaturanstieg, Notabschaltung, Nachzerfallswärme, Wiederherstellung der Kühlung |
| Multiblock-Maschinen | Reaktordruckbehälter, Dampferzeuger, Turbine, Generator und Kühlanlagen aus mehreren Blöcken |
| Multiplayer | Serverautoritative Simulation, alle Spieler sehen dieselben Daten |

### Geplante Bildschirmtypen

1. Reaktorübersicht
2. Reaktorkernüberwachung
3. Primärkreislauf
4. Sekundärkreislauf
5. Turbine und Generator
6. Alarm- und Warnungsübersicht
7. Stromerzeugung

## Visuelle Designphilosophie

Die Mod behält die typische **Minecraft-Ästhetik** bei und stellt darin **realistische, moderne Industrieanlagen** dar: blockbasierte Architektur, technisch plausible Maschinen, eine glaubwürdige Leitwarte mit großen Wandbildschirmen und Bedienplätzen. Science-Fiction-Elemente sind bewusst ausgeschlossen.

Die Bildschirme folgen einem einheitlichen industriellen Designsystem:

| Element | Farbe |
|---|---|
| Hintergrund | Dunkles Anthrazit |
| Panels | Dunkelgrau |
| Akzentfarbe | Kühles Blau |
| Haupttext | Weiß |
| Sekundärtext | Hellgrau |
| Normalbetrieb | Grün |
| Warnungen | Orange |
| Kritische Alarme | Rot |

Vermieden werden übermäßige Farbverläufe, Neon-Effekte, Hologramme und unnötige Animationen.

## Roadmap

| Meilenstein | Inhalt | Status |
|---|---|---|
| **M0** – Projektgrundlage | Fabric-Projekt, Registrierungen, Entwicklungsumgebung | geplant |
| **M1** – Simulationskern | Reaktorzustand, Kernspaltungsmodell, Wärme, Kühlkreisläufe, Energieumwandlung | geplant |
| **M2** – Physische Maschinen | Blöcke, Block Entities, 3D-Modelle, Multiblock-Strukturen | geplant |
| **M3** – Bildschirm-Rendering | Monitorblöcke, World-Space-Rendering, Dashboards, Live-Messwerte | geplant |
| **M4** – Leitwarte | Bedienkonsolen, Interaktionen, Alarmmanagement, Notabschaltung | geplant |
| **M5** – Multiplayer | Serverzustand, Synchronisierung, Speicherung, Multiplayer-Tests | geplant |
| **M6** – Fertigstellung | Optimierung, visuelle Überarbeitung, Tests, Videoproduktion | geplant |

Ziele, Ergebnisse, Abhängigkeiten und Abnahmekriterien je Meilenstein stehen in der [Projektspezifikation](docs/project.md#15-entwicklungs-roadmap).

## Installation

> [!WARNING]
> **Es gibt noch keine Veröffentlichung.** Downloads, Release-Dateien und Installationsanleitungen folgen, sobald eine erste spielbare Version existiert.

Geplanter Ablauf für Spieler (nach der ersten Veröffentlichung):

1. Fabric Loader für die (noch festzulegende) Minecraft-Version installieren.
2. Fabric API in den `mods`-Ordner legen.
3. Die `atomkraftwerke-<version>.jar` in den `mods`-Ordner legen.

Geplanter Ablauf für Entwickler (sobald M0 abgeschlossen ist):

```bash
git clone https://github.com/dimitrilul/atomkraftwerke.git
cd atomkraftwerke
./gradlew build       # Mod bauen
./gradlew runClient   # Entwicklungs-Client starten
```

## Entwicklungsstatus

| Punkt | Stand |
|---|---|
| Projektdokumentation | in Arbeit |
| Fabric-Projekt | nicht angelegt |
| Quellcode | nicht vorhanden |
| Assets (Texturen, Modelle, Sounds) | nicht vorhanden |
| Veröffentlichung | keine |
| Minecraft-/Fabric-Version | **offene Entscheidung** |

Alle offenen technischen Entscheidungen sind in der [Projektspezifikation](docs/project.md#18-offene-technische-entscheidungen) gesammelt.

## Beiträge

Das Projekt ist ein Schulprojekt. Regeln für Beiträge von außen sind **noch nicht festgelegt**.

Für die eigene Entwicklung gilt:

- Änderungen orientieren sich an der [Projektspezifikation](docs/project.md).
- Simulationslogik bleibt unabhängig vom Rendering und wird mit Unit-Tests abgesichert.
- Neue wissenschaftliche Aussagen werden geprüft und vereinfachte Werte als solche gekennzeichnet.

<!-- Platzhalter: CONTRIBUTING-Hinweise ergänzen, falls Beiträge Dritter erwünscht sind. -->

## Lizenz

**Noch offen.** Für dieses Repository wurde noch keine Lizenz festgelegt. Bis dahin gelten die gesetzlichen Standardregeln des Urheberrechts.

<!-- Platzhalter: Lizenz wählen, LICENSE-Datei anlegen und diesen Abschnitt sowie das Lizenz-Badge aktualisieren. -->

## Schulischer und didaktischer Zweck

Diese Mod dient **ausschließlich der schulischen Erklärung** der Funktionsweise eines Kernkraftwerks. Sie vereinfacht reale physikalische und technische Vorgänge stark, verwendet illustrative Zahlenwerte und ersetzt weder Fachliteratur noch reale Reaktorsimulatoren. Sie vermittelt **keine** Anleitungen zum Betrieb realer kerntechnischer Anlagen.

## Dokumentation

Die vollständige technische Spezifikation mit wissenschaftlichen Grundlagen, Simulationsmodell, Architektur, Roadmap und Teststrategie steht in **[docs/project.md](docs/project.md)**.
