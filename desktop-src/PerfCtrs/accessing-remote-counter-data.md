---
Beschreibung: um auf die Leistungsdaten auf einem Remote Computer zuzugreifen, muss der Remote Registrierungsdienst auf dem Remote Computer aktiviert sein. Die Datei-und Druckfreigabe Ausnahme muss in den Einstellungen der Windows-Firewall ausgewählt werden. vor Windows Vista: der Remote Registrierungsdienst ist standardmäßig aktiviert.
ms. assetid: 0a6b40b14-18 CC7-4BSD-8315-8b5c12954df8 Title: Zugreifen auf Remote-Datenbankdaten. Topic: article ms. Date: 08/17/2020
---

# <a name="accessing-remote-counter-data"></a>Zugreifen auf Remote-Counter-Daten

So greifen Sie auf die Counter-Daten auf einem Remote Computer zu:

- Der Remote Registrierungsdienst muss auf dem Remote Computer aktiviert sein.
- Die **Datei-und Druckfreigabe** Ausnahme muss in den **Einstellungen der Windows-Firewall** ausgewählt werden.

**Vor Windows Vista:** Der Remote Registrierungsdienst ist standardmäßig aktiviert.

> [!NOTE]
> Zu den Windows-Leistungsindikator-APIs und-Tools gehören eingeschränkte Unterstützung für den Zugriff auf Leistungsindikatoren von anderen Computern über RPC (für V2-Anbieter) und Remote Registrierung (für v1-Anbieter). Diese Unterstützung ist in Bezug auf Authentifizierungs Steuerelemente (Tools und APIs, die sich nur als aktueller Benutzer authentifizieren können) und in Bezug auf die Systemkonfiguration häufig schwer zu verwenden (die erforderlichen Endpunkte und Dienste sind in den meisten Systemen standardmäßig deaktiviert). In vielen Fällen ist es besser, auf die Leistungsindikatoren von Remote Systemen über [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) zuzugreifen, anstatt über die integrierte Remote Zugriffs Unterstützung.
