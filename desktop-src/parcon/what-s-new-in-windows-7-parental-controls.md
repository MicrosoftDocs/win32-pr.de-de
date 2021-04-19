---
description: Bietet einen Überblick über die Änderungen an den in Windows 7 eingeführten Windows-Jugendschutz Steuerelementen.
ms.assetid: 5723fddd-52e2-46a1-a48f-647d479b21d9
title: Neuerungen in Windows 7-Jugend Steuerungs Steuerelementen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8282021c81ee8611fb7206d75f7e6aab48ebf2e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359149"
---
# <a name="whats-new-in-windows-7-parental-controls"></a>Neues in Windows 7-Jugendschutz Steuerelementen

## <a name="overview-of-parental-controls-changes-for-windows-7"></a>Übersicht über Änderungen der Jugend Steuerungs Änderungen für Windows 7

Der Zweck dieses Dokuments besteht darin, einen Überblick über die Änderungen an den in Windows 7 eingeführten in Windows 7 eingeführten Windows-Steuerelementen zu geben und Lösungen für die Lösung von Jugend Steuerungslösungen von Drittanbietern zu ermöglichen, diese Änderungen zu nutzen. In diesem Dokument wird davon ausgegangen, dass die Leser mit Jugendschutz für Windows Vista vertraut sind und nur Änderungen an dieser Funktionalität in Windows 7 widerspiegeln, die für die Entwicklung von Jugendschutz Lösungen von Drittanbietern relevant sind. Ein vollständiges Update der Dokumentation zur MSDN Windows-Jugend Steuerung wird zu einem späteren Zeitpunkt befolgt.

## <a name="key-design-decisions-for-windows-7-parental-control-changes"></a>Wichtige Entwurfsentscheidungen für Änderungen an Jugend Steuerungs Änderungen in Windows 7

Änderungen an den in Windows 7 eingeführten Jugendschutz Maßnahmen setzen das übergeordnete Ziel der herauf Stufung der Koexistenz von Jugend Steuerungslösungen von Drittanbietern mit der in-Box-Funktionalität fort. Die Änderungen sind:

-   Entfernen von Webfiltern und Aktivitäts Berichten aus den in-Box-Steuerelement-Steuerelementen. Die in-Box-Steuerelemente für die Jugendschutz-Steuerelemente bieten wichtige, von Microsoft implementierte Einschränkungen wie Zeitlimits, Anwendungs Einschränkungen und Spiel Einschränkungen. Die Webfilterung, die Aktivitäts Berichterstattung und andere Funktionen können von Microsoft oder von Drittanbietern bereitgestellt werden. Beispielsweise bietet die Windows Live Family Safety-Lösung Webfilterung, Remote Verwaltung und Aktivitäts Überwachung sowie Kontakt Verwaltung für alle Windows Live-Anwendungen.
-   Aktivieren von Drittanbieter Lösungen, um die Konfigurations Benutzeroberfläche des in-Box-Anbieters zu ersetzen und dabei weiterhin auf die in-Box-Implementierung von Zeit-, Anwendungs-und Spiel Einschränkungen zu vertrauen.
-   Das Aktivieren und Aktivieren von Lösungen von Drittanbietern auf dem Computer wird durch ein übergeordnetes Element oder einen Wächter (Administrator Konto) ermöglicht.

## <a name="parental-controls-top-level-user-interface-changes-in-windows-7"></a>Jugend Steuerungs Änderungen der Benutzeroberfläche der obersten Ebene in Windows 7

Windows 7 führt die folgenden Änderungen an der Systemsteuerung auf der obersten Ebene der Jugend Steuerungsebene aus:

-   Der Abschnitt zusätzliche Steuerelemente wird eingeführt, in denen Steuerelemente, die zusätzliche Funktionen bereitstellen, z. b. Webfilterung, Aktivitätsberichte usw., in einem Dropdown-Listenfeld ausgewählt werden können. Anbieter von Microsoft oder Drittanbietern müssen ihre Lösungen mit Windows 7-Jugend Steuerungs Steuerelementen registrieren, damit Sie im Dropdown-Listenfeld zusätzliche Steuerelemente ausgewählt werden können. Weitere Informationen zum Registrieren einer Lösung finden Sie unter Anbieter Registrierung weiter unten in diesem Thema).
-   Das Logo Bild des aktuell ausgewählten Anbieters wird in der oberen rechten Ecke der Seite angezeigt.
-   Die verwalteten Benutzer Kacheln können eine Zusammenfassung der Jugend Einstellungen anzeigen, die vom derzeit ausgewählten Anbieter bereitgestellt werden.

Der aktuell ausgewählte Anbieter kann eine eigene Benutzeroberfläche für Benutzer Steuerelemente für die verwalteten Benutzer verwenden, oder er kann sich darauf verlassen, dass die in-Box-WPC-Implementierung dieses Bildschirms verwendet werden soll. Die in-Box-Implementierung hat die folgenden Änderungen an den Elementen vorgenommen:

-   Der Abschnitt Aktivitäts Berichterstellung wurde entfernt.
-   Der Link zum Anzeigen von Aktivitäts Berichten wird entfernt.

## <a name="parental-controls-api-overview-windows-7-changes"></a>Übersicht über die Eltern Steuerungs-API: Änderungen in Windows 7

Der Integrationsmechanismus für Drittanbieter Lösungsanbieter wurde erweitert, um Folgendes zu ermöglichen:

-   Anbieterregistrierung: Bei der Registrierung wird ein Anbieter im Dropdown-Listenfeld zusätzliche Steuerelemente auf dem Bildschirm "Eltern Steuerelemente" in der Systemsteuerung ausgewählt.
-   Abfragen des aktuell ausgewählten Anbieters. Eine öffentliche com-Schnittstelle wird verfügbar gemacht, um diese Funktionalität zu aktivieren.
-   Außerdem ist New der Satz von COM-Schnittstellen, die von den Anbietern implementiert werden müssen, um Folgendes zuzulassen:
    -   Aktivieren oder Deaktivieren des Anbieters durch WPC bei der Benutzer Auswahl zusätzlicher Steuerelemente.
    -   WPC, um die Steuerung an den Anbieter zu übergeben, um die Jugend Steuerungseinstellungen der verwalteten Benutzer zu konfigurieren.
    -   WPC, um den Anbieter für die Zusammenfassung der Jugend Steuerungseinstellungen der verwalteten Benutzer abzufragen.

## <a name="third-party-provider-integration"></a>Integration von Drittanbieter-Anbietern

### <a name="provider-registration"></a>Anbieter Registrierung

Um einen neuen Anbieter mit Jugend Steuerungs Steuerelementen zu registrieren, muss ein Registrierungs Wert in den Anbieter Schlüssel der Windows-Jugend Steuerelemente geschrieben werden. Der Wertname ist eine eindeutige GUID, die zum Identifizieren des Anbieters verwendet wird. Bei den Wertdaten handelt es sich um einen Pfad zu einem Registrierungsschlüssel auf dem **lokalen HKEY- \_ \_ Computer** , der Anbieter Informationen enthält.

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
| <span id="LogoImage"></span><span id="logoimage"></span><span id="LOGOIMAGE"></span>**Abbild**<br/>         | Ein voll qualifizierter Pfad zu einer Ressourcen Binärdatei mit einer negativen Ressourcen-ID für das Anbieter Logo Image (gespeichert **als \_ bildbitmap**).<br/>                                                        |
| <span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Display Name**<br/> | Ein voll qualifizierter Pfad zu einer Ressourcen Binärdatei mit einer negativen Ressourcen-ID für den Anbieter Namen. **Display Name** darf nicht länger als 50 Zeichen sein.<br/>                                       |
| <span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**<br/> | Ein voll qualifizierter Pfad zu einer Ressourcen Binärdatei mit einer negativen Ressourcen-ID für die Anbieter Beschreibung. Die Beschreibungs Länge darf nicht länger als 200 Zeichen sein.<br/>                               |
| <span id="StateCLSID"></span><span id="stateclsid"></span><span id="STATECLSID"></span>**Status-sid**<br/>     | Die Klassen-ID der Klasse des Anbieters, die iwpcproviderstate implementiert.<br/>                                                                                                                     |
| <span id="ConfigCLSID"></span><span id="configclsid"></span><span id="CONFIGCLSID"></span>**Configclsid**<br/> | Die Klassen-ID der Klasse des Anbieters, die iwpcproviderconfig implementiert. Die Werte für " **Status-sid** " und " **configclsid** " können identisch sein.<br/>                                                               |
| <span id="GRSVisible"></span><span id="grsvisible"></span><span id="GRSVISIBLE"></span>**Grsvisible**<br/>     | Ein optionaler **DWORD** -Wert ungleich 0 (null), der angibt, dass die Windows-Eltern Steuerelemente einen Link zum Bildschirm für die Spiel Bewertungssysteme anzeigen, nachdem ein Anbieter als neuer aktueller Anbieter ausgewählt wurde<br/> |



 

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

In der Systemsteuerung für die Jugendschutz Einstellungen werden das **Abbild**, **Display Name** und die **Beschreibung** verwendet, um die Hauptseite der Systemsteuerung für Eltern Steuerelemente zu ändern, wenn dieser Anbieter ausgewählt wird. Der Wert " **Status** " wird verwendet, wenn der Anbieter aktiviert oder deaktiviert ist. Der **configclsid** -Wert wird verwendet, wenn die Benutzeroberfläche dynamische Informationen zu den einzelnen Benutzern erhält (Dies ist nur der Fall, wenn der Anbieter derzeit ausgewählt ist).

 

 




