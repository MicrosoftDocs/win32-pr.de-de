---
description: Bietet eine Übersicht über die Änderungen an den in Windows 7 eingeführten Windows Jugendschutzfunktionen.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Neuerungen in Windows 7 Jugendschutz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f7b545c6791d286e51ae7a36ed65623d1697a7e742b1ae956e3ef4aaf3425e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951820"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Neuerungen in Windows 7 Jugendschutz

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Übersicht über Änderungen an der Jugendschutzsteuerung für Windows 7

Der Zweck dieses Dokuments besteht darin, einen Überblick über die Änderungen an den in Windows 7 eingeführten Windows Jugendschutzfunktionen zu geben und es Drittanbietern für die Jugendschutzlösung zu ermöglichen, diese Änderungen zu nutzen. In diesem Dokument wird davon ausgegangen, dass Leser mit den Jugendschutzfunktionen für Windows Vista vertraut sind, und es werden nur Änderungen an dieser Funktionalität in Windows 7 widergespiegelt, die für die Entwicklung von Lösungen zur Jugendschutz von Drittanbietern relevant sind. Ein vollständiges Update der MSDN Windows-Dokumentation zur Jugendschutz wird zu einem späteren Zeitpunkt folgen.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Wichtige Entwurfsentscheidungen für Windows 7 Änderungen an der Jugendschutzsteuerung

Änderungen an den in Windows 7 eingeführten Jugendschutzmaßnahmen setzen das übergeordnete Ziel der Förderung der Koexistenz von Lösungen für die Jugendschutz durch Drittanbieter mit der in-box-Funktionalität fort. Die Änderungen sind:

-   Entfernen von Webfilterung und Aktivitätsberichten aus der In-Box-Funktionalität der Jugendschutzfunktionen. Die in der Box enthaltenen Jugendschutzmechanismen bieten grundlegende von Microsoft implementierte Offlineeinschränkungen wie Zeitlimits, Anwendungseinschränkungen und Spieleinschränkungen. Die Webfilterung, Aktivitätsberichterstellung und andere Funktionen können von Microsoft oder Drittanbieterlösungen zur Jugendschutz bereitgestellt werden. Beispielsweise bietet Windows Live Family Safety Lösung Webfilterung, Remoteverwaltung und Aktivitätsüberwachung sowie Kontaktverwaltung für alle Windows Live-Anwendungen.
-   Aktivieren von Lösungen von Drittanbietern, um die Benutzeroberfläche für die Konfiguration des In-Box-Anbieters zu ersetzen, während gleichzeitig die Implementierung von Zeit-, Anwendungs- und Spieleinschränkungen im Feld verwendet wird.
-   Aktivieren der Drittanbieterlösungen, die von einem übergeordneten Oder Wächter (Administratorkonto) auf dem Computer ermittelt und aktiviert werden können.

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Änderungen an Benutzeroberfläche der obersten Ebene in Windows 7

Windows 7 werden die folgenden Änderungen an der Benutzeroberfläche der Systemsteuerung obersten Ebene vorgenommen:

-   Der Abschnitt Zusätzliche Steuerelemente wird eingeführt, in dem Steuerelemente, die zusätzliche Funktionen wie Webfilterung, Aktivitätsberichterstellung usw. bereitstellen, in einem Dropdownlistenfeld ausgewählt werden können. Microsoft oder Drittanbieter müssen ihre Lösungen bei Windows 7 Jugendschutz registrieren, damit sie im Dropdown-Listenfeld Zusätzliche Steuerelemente ausgewählt werden können. Informationen zum Registrieren einer Lösung finden Sie weiter unten in diesem Thema unter Anbieterregistrierung.
-   Das Logobild des aktuell ausgewählten Anbieters wird in der oberen rechten Ecke der Seite angezeigt.
-   Die Kacheln für verwaltete Benutzer können eine Zusammenfassung der Einstellungen der Eltern anzeigen, die vom derzeit ausgewählten Anbieter bereitgestellt werden.

Der derzeit ausgewählte Anbieter kann eine eigene Benutzeroberfläche für Benutzersteuerungsbildschirme für die verwalteten Benutzer verwenden, oder er kann sich für die Verwendung der integrierten WPC-Implementierung dieses Bildschirms entscheiden. Die Implementierung im Feld weist die folgenden Änderungen an ihren Elementen auf:

-   Der Abschnitt zur Aktivitätsberichterstellung wird entfernt.
-   Der Link zum Anzeigen von Aktivitätsberichten wird entfernt.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Übersicht über die API für die Jugendschutzfunktionen: Änderungen an Windows 7

Der Integrationsmechanismus für Lösungsanbieter von Drittanbietern wurde erweitert, um Folgendes zu ermöglichen:

-   Anbieterregistrierung: Nach der Registrierung kann ein Anbieter im Dropdown-Listenfeld Zusätzliche Steuerelemente auf dem Bildschirm Jugendschutz Systemsteuerung ausgewählt werden.
-   Abfragen des aktuell ausgewählten Anbieters. Eine öffentliche COM-Schnittstelle wird verfügbar gemacht, um diese Funktionalität zu aktivieren.
-   Neu ist auch der Satz von COM-Schnittstellen, die von den Anbietern implementiert werden sollen, um Folgendes zu ermöglichen:
    -   Aktivieren oder Deaktivieren des Anbieters durch WPC bei Auswahl zusätzlicher Steuerelemente durch den Benutzer.
    -   WPC, um die Steuerung an den Anbieter zu übergeben, um die Einstellungen für die Jugendschutzverwaltung verwalteter Benutzer zu konfigurieren.
    -   WPC, um den Anbieter nach der Zusammenfassung der Einstellungen für die Jugendschutzverwaltung eines verwalteten Benutzers abzufragen.

## <a name="third-party-provider-integration"></a>Drittanbieterintegration

### <a name="provider-registration"></a>Anbieterregistrierung

Um einen neuen Anbieter bei Der Jugendschutz zu registrieren, muss ein Registrierungswert in den Anbieterschlüssel von Windows Jugendschutz geschrieben werden. Der Wertname ist eine eindeutige GUID, die zum Identifizieren des Anbieters verwendet wird. Die Wertdaten sind ein Pfad zu einem Registrierungsschlüssel in **HKEY \_ LOCAL \_ MACHINE,** der Anbieterinformationen enthält.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Parental Controls
                  Providers
                     {45D63315-0824-4df4-B8A4-EF137D8810D1} = SOFTWARE\Microsoft\Family Safety\WPC\
```

Am angegebenen Speicherort des Registrierungsschlüssels werden die folgenden Werte erwartet.



| Begriff                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**LogoImage**<br/>         | Ein vollqualifiziertes Pfad zu einer Ressourcenbinärdatei mit einer negativen Ressourcen-ID für das Anbieterlogobild (gespeichert als **IMAGE \_ BITMAP**).<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Displayname**<br/> | Ein vollqualifizierten Pfad zu einer Ressourcenbinärdatei mit einer negativen Ressourcen-ID für den Anbieternamen. **Die Länge von DisplayName** darf 50 Zeichen nicht überschreiten.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**<br/> | Ein vollqualifizierten Pfad zu einer Ressourcenbinärdatei mit einer negativen Ressourcen-ID für die Anbieterbeschreibung. Die Länge der Beschreibung darf 200 Zeichen nicht überschreiten.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**StateCLSID**<br/>     | Die Klassen-ID der Klasse des Anbieters, die IWPCProviderState implementiert.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**ConfigCLSID**<br/> | Die Klassen-ID der Klasse des Anbieters, die IWPCProviderConfig implementiert. **StateCLSID** und **ConfigCLSID** können identisch sein.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**GRSVisible**<br/>     | Ein optionaler **DWORD-Wert** ungleich 0 (null), der angibt, dass Windows Jugendschutz einen Link zum Bildschirm Game Rating System anzeigt, nachdem ein Anbieter als neuer aktueller Anbieter ausgewählt wurde.<br/> |



 

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Family Safety
            WPC
               LogoImage = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40001
               DisplayName = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40002
               Description = C:\Program Files\Windows Live\Family Safety\fssui.rll,-40003
               StateCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               ConfigCLSID = {B4BAAE4D-3D86-4fa9-86F0-CF82C94D8A6A}
               GRSVisible = 0x00000001 (1)
```

Der Systemsteuerung für die Jugendschutzelemente verwendet **LogoImage,** **DisplayName** und **Description,** um die Hauptseite des Systemsteuerung zu ändern, wenn dieser Anbieter ausgewählt wird. Der **StateCLSID-Wert** wird verwendet, wenn der Anbieter aktiviert oder deaktiviert ist. Der **ConfigCLSID-Wert** wird verwendet, wenn die Benutzeroberfläche dynamische Informationen zu jedem Benutzer erhält (dies ist nur der Fall, wenn der Anbieter derzeit ausgewählt ist).

 

 




