---
beschreibung: Für den Zugriff auf Indikatordaten auf einem Remotecomputer: Auf dem Remotecomputer muss der Remoteregistrierungsdienst aktiviert sein. Die Ausnahme datei- und druckfreigabe muss im Windows Firewall-Einstellungen. Vor der Windows Vista: Der Remoteregistrierungsdienst ist standardmäßig aktiviert.
ms.assetid: 0a6b40b2-6cc7-4bfd-8315-8b5c12954df8 title: Accessing Remote Counter Data ms.topic: article ms.date: 08/17/2020
---

# <a name="accessing-remote-counter-data"></a>Zugreifen auf Remotezählerdaten

So greifen Sie auf Indikatordaten auf einem Remotecomputer zu:

- Auf dem Remotecomputer muss der Remoteregistrierungsdienst aktiviert sein.
- Die **Ausnahme datei- und druckfreigabe** muss in Windows **Firewall** Einstellungen.

**Vor der Windows Vista:** Der Remoteregistrierungsdienst ist standardmäßig aktiviert.

> [!NOTE]
> Windows Leistungsindikator-APIs und -Tools bieten eingeschränkte Unterstützung für den Zugriff auf Leistungsindikatoren von anderen Computern über RPC (für V2-Anbieter) und Remoteregistrierung (für V1-Anbieter). Diese Unterstützung ist häufig schwierig in Bezug auf Authentifizierungssteuerungen (die Tools und APIs können sich nur als aktueller Benutzer authentifizieren) sowie in Bezug auf die Systemkonfiguration (die erforderlichen Endpunkte und Dienste sind auf den meisten Systemen standardmäßig deaktiviert). In vielen Fällen ist es besser, über [WMI](/windows/desktop/WmiSdk/monitoring-performance-data) auf die Leistungsindikatoren von Remotesystemen zu zugreifen, anstatt über die integrierte Remotezugriffsunterstützung.
