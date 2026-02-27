# Projektdokumentation: WRK-Visualizer
**Projektziel:** Entwicklung einer visuellen Oberfläche (Dashboard/Wrapper) für das Benchmarking-Tool WRK.

---

## 1. Rahmenbedingungen
Das Projekt fokussiert sich auf die Erstellung eines Prototyps innerhalb einer Woche (KW 10), um Performance-Daten grafisch aufzubereiten.

* **Organisationsform:** Matrixorganisation
* **Vorgehensmodell:** SCRUM (Rollen: Oskar/Tobias Master)
* **Technologie-Basis:** JavaScript / TypeScript & Next.js

---

## 2. Systemarchitektur & Techstack
Die Anwendung wird modern und hochverfügbar konzipiert:



* **Frontend/Backend:** Next.js (Fullstack-Framework)
* **Datenbank:** PostgreSQL (verwaltet via Cloudnative-PG in Kubernetes)
* **Infrastruktur:** Containerisierung mittels Docker

---

## 3. Soll-Zustand (Funktionsumfang)
Das Dashboard soll folgende Metriken für mehrere URLs im Vergleich (Benchmark) verarbeiten:

Anforderungen SI 
- Docker Host bereitstellen
- Datenbank bereitstellen (PostgresSQL)
- Proxmox bereitstellen
- Linux Container (Debian 13) bereitstellen
- Netzwerktechnik überprüfen 
- Optional:
  - Kubernetes stack

Anforderungen AE
- next.js framework auf Webserver einrichten
- Datenbank einbinden 
- Dashboard implementieren
- Befehlsausführung auf Dashboard einrichten
- API-Einbindung
- Unit-Test für Ausführung und Berechnung von Metriken


| Metrik | Beschreibung |
| :--- | :--- |
| **Requests per Second** | Anzahl der Anfragen, die pro Sekunde verarbeitet werden. |
| **Throughput** | Datenmenge, die pro Zeiteinheit übertragen wird. |
| **Latency** | Antwortzeit des Servers (Latenz). |
| **Ping** | Grundlegende Erreichbarkeit und Netzwerkverzögerung. |

**Zusatzfunktionen:**
* Visuelle Auswertung (Diagramme)
* Speichern von historischen Ergebnissen in der Datenbank
* Containerisierte Bereitstellung

---

## 4. Zeitplanung (Sprint KW 10)

### Phase 1: Konzeption (Freitag)
* Erstellung des Pflichtenhefts
* Ressourcenplanung & Setup
* Einarbeitung in die WRK-Schnittstellen

### Phase 2: Infrastruktur (Montag)
* Definition der System-Architektur
* Erstellung des Softwareentwurfs
* Initialisierung der Docker-Container

### Phase 3: Entwicklung (Dienstag - Mittwoch)
* **Dienstag:** Backend-Logik & Next.js Integration
* **Mittwoch:** UI/UX Design & Dashboard-Visualisierung

### Phase 4: Abschluss (Donnerstag - Freitag)
* **Donnerstag:** Vorbereitung der Präsentation & Diagrammerstellung
* **Freitag:** Offizielle Projektabgabe

---

## 5. Deployment-Hinweise
Die Datenbank wird in einem Kubernetes-Cluster betrieben. Dabei kommt der **Cloudnative-PG** Operator zum Einsatz, um PostgreSQL-Instanzen nativ in K8s zu managen.
