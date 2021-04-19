---
title: Informationen zur Windows-Filter Plattform
description: Windows Filtering Platform (WFP) ist eine Plattform für die Verarbeitung von Netzwerk Datenverkehr, die die Schnittstellen für das Filtern von Netzwerk Datenverkehr in Windows XP und Windows Server 2003 ersetzen soll
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ab259eca1da714bbeb8d4ea556e69513f33514c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106339485"
---
# <a name="about-windows-filtering-platform"></a>Informationen zur Windows-Filter Plattform

Windows Filtering Platform (WFP) ist eine Plattform für die Verarbeitung von Netzwerk Datenverkehr, die die Schnittstellen für das Filtern von Netzwerk Datenverkehr in Windows XP und Windows Server 2003 ersetzen soll WFP besteht aus einem Satz von Hooks im Netzwerk Stapel und einer Filter-Engine, die die Interaktion von Netzwerk Stapeln koordiniert.

## <a name="the-wfp-components"></a>Die WFP-Komponenten

### <a name="filter-engine"></a>Filter-Engine

Die zentrale Filterinfrastruktur für mehrere Ebenen, die im Kernel Modus und im Benutzermodus gehostet wird und die mehrere Filtermodule im Netzwerk Subsystem Windows XP und Windows Server 2003 ersetzt.

-   Filtert den Netzwerk Datenverkehr auf jeder Ebene im System über alle Datenfelder, die von einem Shim bereitgestellt werden können.
-   Implementiert die "Callout"-Filter durch Aufrufen von Aufrufen während der Klassifizierung.
-   Gibt Aktionen vom Typ "zulassen" oder "blockieren" für das Shim zurück, von dem es zur Erzwingung aufgerufen wurde.
-   Stellt das zwischen Verfahren zwischen verschiedenen Richtlinien Quellen bereit. Beispielsweise bestimmt die Priorität, wenn eine Anwendung so konfiguriert ist, dass Sie Netzwerk Datenverkehr sichert, aber die lokale Firewall ist so konfiguriert, dass der von der Anwendung gesicherte Datenverkehr verhindert wird.<br/>

### <a name="base-filtering-engine-bfe"></a>Basis Filter-Engine (BFE)

Ein Dienst, der den Betrieb der Windows-Filter Plattform steuert. Sie führt die folgenden Aufgaben aus:

-   Akzeptiert Filter und andere Konfigurationseinstellungen für die Plattform.
-   Meldet den aktuellen Status des Systems, einschließlich der Statistiken.
-   Erzwingt das Sicherheitsmodell für die Annahme der Konfiguration auf der Plattform. Beispielsweise kann ein lokaler Administrator Filter hinzufügen, andere Benutzer können Sie jedoch nur anzeigen.<br/>
-   Die Konfigurationseinstellungen werden auf andere Module im System überfallen. IPSec-Aushandlungs Richtlinien werden z. b. in IKE/AuthIP-Schlüssel-/Verschlüsselungsmodulen geleitet. Filter werden an die Filter-Engine gesendet.<br/>

### <a name="shims"></a>Shims

Kernelmoduskomponenten, die sich zwischen dem Netzwerk Stapel und der Filter-Engine befinden. Shims treffen die Filter Entscheidung, indem die Filter-Engine klassifiziert wird. Im folgenden finden Sie eine Liste der verfügbaren Shims.

-   Anwendungsschicht-Erzwingungs-Shim.
-   Das transportebenenmodul-Shim.
-   Shim des netzwerkebenenmoduls.
-   ICMP-Fehler (Internet Control Message Protocol).
-   Verwerfen Sie das Shim.
-   Stream-Shim.

### <a name="callouts"></a>Aufrufe

Eine Reihe von Funktionen, die von einem Treiber verfügbar gemacht und für spezialisierte Filter verwendet werden. Neben den grundlegenden Aktionen "zulassen" und "blockieren" können durch Aufrufe der eingehende und ausgehende Netzwerk Datenverkehr geändert und gesichert werden. Weitere Informationen zu Legenden aufrufen finden Sie im Thema [Windows-Filterungs Plattform-Callout-Treiber](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) in der Dokumentation zum Windows-Treiberkit (WDK). WFP bietet integrierte Legenden, mit denen die folgenden Aufgaben ausgeführt werden.<br/>

-   IPSec-Verarbeitung ausführen.
-   Anpassen des Verhaltens der Zustands behafteten Filterung.
-   Führt die Filterung im Debugmodus aus (Automatisches Löschen von nicht angeforderten Paketen).
-   Steuern Sie die TCP-Chimney-Abladung.
-   Interagieren Sie mit dem Teredo-Dienst.

<br/> Die Filter-Engine ermöglicht das Registrieren von Drittanbieter-Legenden für jede der kernelmodusschichten.<br/>

### <a name="application-programming-interface"></a>Anwendungsprogrammierschnittstelle

Eine Reihe von Datentypen und Funktionen, die Entwicklern zur Erstellung und Verwaltung von Netzwerk Filterungs Anwendungen zur Verfügung stehen. Diese Datentypen und Funktionen sind in mehreren [API-Sätzen](api-sets.md)gruppiert.

## <a name="wfp-features"></a>WFP-Features

-   Bietet eine Paket Filterungs Infrastruktur, in der unabhängige Softwarehersteller (ISVs) spezialisierte Filtermodule einbinden können.
-   Funktioniert sowohl mit IPv4 als auch mit IPv6.
-   Ermöglicht das Filtern, ändern und erneute Einschleusen von Daten.
-   Führt sowohl die Paket-als auch die streamverarbeitung aus.
-   Ermöglicht das Aktivieren der Paketfilterung pro Anwendung, pro Benutzer und pro Verbindung zusätzlich zur Netzwerkschnittstelle oder pro Port.
-   Stellt die Systemstart Zeit Sicherheit bereit, bis die Basis Filter-Engine (BFE) gestartet werden kann.
-   Aktiviert das Filtern Zustands behafteter Verbindungen.
-   Verarbeitet sowohl vorab-als auch Post-verschlüsselte IPSec-verschlüsselte Daten.
-   Ermöglicht die Integration von IPSec-und firewallfilterungs Richtlinien.
-   Stellt eine Richtlinien Verwaltungsinfrastruktur bereit, um zu bestimmen, wann bestimmte Filter aktiviert werden sollen. Dies schließt die unterschiedlichen Anforderungen von mehreren Filtern ein, die von verschiedenen Anbietern bereitgestellt werden.
-   Behandelt die meisten Pakete zur Neuzuweisung und Zustandsüberwachung.
-   Enthält ein generisches Benutzer Benachrichtigungssystem, das Abonnenten über Änderungen am Filtersystem informiert.
-   Implementiert Enumerationsfunktionen, die den Status des Systems melden.
-   Verwendet Net-Ereignisse, um IPsec-Fehler und Paket Abstürze aufzuzeichnen.
-   Unterstützt eine Hilfsprogrammklasse für das Netzwerk Diagnose Framework [(ndf)](/windows/desktop/NDF/extensible-helper-classes).
-   Unterstützt die [Secure Socket-Erweiterungen](/windows/desktop/WinSock/winsock-secure-socket-extensions) für die Winsock-API, mit denen Netzwerkanwendungen den Datenverkehr durch Konfigurieren von WFP sichern können.
-   Bei der Erzwingung der Logik Schicht wirkt sich minimal auf die Netzwerkleistung aus, indem nur das erste Paket in einer Verbindung verarbeitet wird.
-   Integriert die Hardware Auslagerung, bei der kernelmoduscallout-Module Hardware verwenden können, um eine bestimmte Paket Untersuchung auszuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WFP-Architektur](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[WFP-Vorgang](basic-operation.md)
</dt> <dt>

[Durchsetzung der Anwendungsschicht (ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[IPSec-Konfiguration](ipsec-configuration.md)
</dt> <dt>

[WFP-Konfiguration](wfp-configuration.md)
</dt> <dt>

[WFP-Überwachung](wfp-monitoring.md)
</dt> <dt>

[WFP-API](api-sets.md)
</dt> </dl>

 

