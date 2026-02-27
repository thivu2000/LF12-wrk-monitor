# Pflichtenheft: WRK-Visualizer Dashboard
**Projekt:** Visuelle Oberfläche für das WRK-Benchmarking-Tool  
**Version:** 1.0  
**Datum:** [Datum einfügen]  
**Status:** In Bearbeitung  

---

## 1. Zielbestimmung
Das Projekt "WRK-Visualizer" soll eine benutzerfreundliche Web-Oberfläche (Dashboard) bieten, um das CLI-Tool `wrk` zu steuern und dessen Ergebnisse grafisch aufzubereiten.

### 1.1 Muss-Ziele
* Durchführung von Benchmarks gegen mehrere URLs.
* Visualisierung von RPS, Throughput, Latenz und Ping.
* Speicherung der Ergebnisse in einer PostgreSQL-Datenbank.
* Containerisierung der gesamten Anwendung (Docker).

### 1.2 Wunsch-Ziele
* [Hier weitere Ziele einfügen, z.B. Export als PDF, Vergleich von historischen Daten]

---

## 2. Produkteinsatz
### 2.1 Anwendungsbereiche
Das Tool dient der Performance-Analyse von Web-Services während der Entwicklungs- und Testphase.

### 2.2 Zielgruppen
Entwickler, DevOps-Engineers und QA-Tester.

### 2.3 Betriebsbedingungen
* Lauffähig in Docker-Umgebungen.
* Orchestrierung via Kubernetes (Cloudnative-PG).

---

## 3. Produktfunktionen (Funktionale Anforderungen)
* **F10:** Starten eines WRK-Benchmarks über die Weboberfläche.
* **F20:** Eingabe von Parametern (Dauer, Threads, Connections).
* **F30:** Echtzeit- oder Post-Benchmark-Visualisierung der Daten.
* **F40:** Vergleichsansicht für mehrere Ziel-URLs.
* **F50:** Persistente Speicherung der Testläufe.

---

## 4. Produktdaten (Nicht-funktionale Anforderungen)
* **NF10 (Performance):** Die UI darf während des Benchmarks nicht blockieren.
* **NF20 (Skalierbarkeit):** Unterstützung für Kubernetes-Deployment.
* **NF30 (Usability):** Intuitive Bedienung des Dashboards ohne CLI-Kenntnisse.

---

## 5. Systemarchitektur & Schnittstellen
### 5.1 Software-Architektur
* **Frontend:** Next.js (React)
* **Backend:** Next.js API Routes / Node.js
* **Datenbank:** PostgreSQL

### 5.2 Externe Schnittstellen
* **WRK CLI:** Anbindung des Wrappers an den nativen C-Prozess.
* **Cloudnative-PG:** Schnittstelle zur Datenbank-Orchestrierung.

---

## 6. Benutzeroberfläche (UI-Design)
* [ ] **Dashboard-Ansicht:** Liste der aktiven/vergangenen Tests.
* [ ] **Konfigurations-Panel:** Formular für URL-Eingabe und Header-Einstellungen.
* [ ] **Analyse-View:** Charts (z.B. Chart.js oder Recharts) für Latenzverteilung.

---

## 7. Qualitätsanforderungen
| Produktqualität | Sehr hoch | Hoch | Relevant |
| :--- | :---: | :---: | :---: |
| Zuverlässigkeit | | X | |
| Benutzbarkeit | | X | |
| Performance | X | | |
| Wartbarkeit | | | X |

---

## 8. Abnahmekriterien
* Der Benchmark startet erfolgreich über einen Button-Klick.
* Daten werden korrekt aus dem WRK-Output geparst.
* Die Ergebnisse sind nach einem Refresh der Seite in der Historie sichtbar.

---

## 9. Glossar
* **WRK:** Ein modernes HTTP-Benchmarking-Tool.
* **RPS:** Requests per Second.
* **Cloudnative-PG:** Kubernetes-Operator für PostgreSQL.

## 10. Techstack
