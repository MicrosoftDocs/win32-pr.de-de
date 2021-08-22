---
title: Informationen Windows Filterplattform
description: Windows Die Filterplattform (WFP) ist eine Plattform zur Verarbeitung von Netzwerkdatenverkehr, die die Netzwerkdatenverkehrsfilterschnittstellen Windows XP und Windows Server 2003 ersetzt.
ms.assetid: 6faad008-b2f6-4f45-89c7-ae98c2f58ce1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01a81f4f67c2f3281a6fa6b5d3220f9e2157643dfd7cf3bac34ea55743024946
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069490"
---
# <a name="about-windows-filtering-platform"></a>Informationen Windows Filterplattform

Windows Die Filterplattform (WFP) ist eine Plattform zur Verarbeitung von Netzwerkdatenverkehr, die die Netzwerkdatenverkehrsfilterschnittstellen Windows XP und Windows Server 2003 ersetzt. WFP besteht aus einem Satz von Hooks in den Netzwerkstapel und einer Filter-Engine, die Netzwerkstapelinteraktionen koordiniert.

## <a name="the-wfp-components"></a>Die WFP-Komponenten

### <a name="filter-engine"></a>Filter-Engine

Die kernbasierte Filterinfrastruktur, die sowohl im Kernelmodus als auch im Benutzermodus gehostet wird und die mehrere Filtermodule im Windows XP- und Windows Server 2003-Netzwerksubsystem ersetzt.

-   Filtert Netzwerkdatenverkehr auf jeder Ebene im System über alle Datenfelder, die ein Shim bereitstellen kann.
-   Implementiert die "Callout"-Filter, indem Während der Klassifizierung Aufrufe aufgerufen werden.
-   Gibt Die Aktionen "Zulassen" oder "Blockieren" an den Shim zurück, der sie zur Erzwingung aufgerufen hat.
-   Ermöglicht die Vermittlung zwischen verschiedenen Richtlinienquellen. Bestimmt z. B. die Priorität, wenn eine Anwendung so konfiguriert ist, dass der damit verbundene Netzwerkdatenverkehr geschützt wird, die lokale Firewall jedoch so konfiguriert ist, dass der durch anwendungen geschützte Datenverkehr verhindert wird.<br/>

### <a name="base-filtering-engine-bfe"></a>Basisfilter-Engine (BFE)

Ein Dienst, der den Betrieb der Windows Filterplattform steuert. Er führt die folgenden Aufgaben aus.

-   Akzeptiert Filter und andere Konfigurationseinstellungen für die Plattform.
-   Meldet den aktuellen Zustand des Systems, einschließlich Statistiken.
-   Erzwingt das Sicherheitsmodell zum Akzeptieren der Konfiguration auf der Plattform. Beispielsweise kann ein lokaler Administrator Filter hinzufügen, aber andere Benutzer können sie nur anzeigen.<br/>
-   Konfiguriert Konfigurationseinstellungen für andere Module im System. Beispielsweise werden IPsec-Aushandlungsrichtlinie zu IKE/AuthIP-Schlüsselmodulen und Filter an die Filter-Engine übergeben.<br/>

### <a name="shims"></a>Shims

Kernelmoduskomponenten, die sich zwischen dem Netzwerkstapel und der Filter-Engine befinden. Shims treffen die Filterentscheidung, indem sie für die Filter-Engine klassifizieren. Im Folgenden finden Sie eine Liste der verfügbaren Shims.

-   ALE-Shim (Application Layer Enforcement).
-   Transport Layer Module shim.
-   Shim des Moduls "Netzwerkebene".
-   Internet Control Message Protocol (ICMP) Error shim.
-   Verwerfen des Shims.
-   Stream-Shim.

### <a name="callouts"></a>Aufrufe

Eine Reihe von Funktionen, die von einem Treiber verfügbar gemacht und für spezielle Filter verwendet werden. Neben den grundlegenden Aktionen "Zulassen" und "Blockieren" können Aufrufe eingehenden und ausgehenden Netzwerkdatenverkehr ändern und schützen. Weitere Informationen zu Callouts finden Sie im Thema [Windows Filtering Platform Callout Drivers](/windows-hardware/drivers/network/windows-filtering-platform-callout-drivers2) in der WDK-Dokumentation (Windows Driver Kit). WFP stellt integrierte Aufrufe bereit, die die folgenden Aufgaben ausführen.<br/>

-   Führen Sie die IPsec-Verarbeitung durch.
-   Passen Sie das Verhalten der zustandsbehafteten Filterung an.
-   Durchführen der Filterung im geschütztem Modus (automatisches Löschen von Paketen, die nicht angefordert wurden).
-   Steuern Der TCP-Auslagerungsvorgang wird gesteuert.
-   Interagieren Sie mit dem Teredo-Dienst.

<br/> Mit der Filter-Engine können sich Aufrufe von Drittanbietern auf jeder kernelmodusbasierten Ebene registrieren.<br/>

### <a name="application-programming-interface"></a>Schnittstelle für die Anwendungsprogrammierung

Eine Reihe von Datentypen und Funktionen, die Entwicklern zum Erstellen und Verwalten von Netzwerkfilteranwendungen zur Verfügung stehen. Diese Datentypen und Funktionen werden in mehrere [API-Sätze](api-sets.md)gruppiert.

## <a name="wfp-features"></a>WFP-Features

-   Stellt eine Paketfilterinfrastruktur bereit, in der unabhängige Softwarehersteller (Independent Software Vendors, ISVs) spezialisierte Filtermodule integrieren können.
-   Funktioniert sowohl mit IPv4 als auch mit IPv6.
-   Ermöglicht die Datenfilterung, -änderung und -einschleusung.
-   Führt die Paket- und Streamverarbeitung aus.
-   Ermöglicht die Aktivierung der Paketfilterung pro Anwendung, pro Benutzer und pro Verbindung zusätzlich zu einer Netzwerkschnittstelle oder pro Port.
-   Bietet Sicherheit zur Startzeit, bis die Basisfilter-Engine (Base Filtering Engine, BFE) gestartet werden kann.
-   Aktiviert zustandsbehaftete Verbindungsfilterung.
-   Verarbeitet sowohl Vor- als auch Post-IPsec-verschlüsselte Daten.
-   Ermöglicht die Integration von IPsec- und Firewallfilterungsrichtlinien.
-   Stellt eine Infrastruktur für die Richtlinienverwaltung bereit, um zu bestimmen, wann bestimmte Filter aktiviert werden sollen. Dies schließt das Vermitteln von in Konflikt stehenden Anforderungen von mehreren Filtern ein, die von verschiedenen Anbietern bereitgestellt werden.
-   Verarbeitet die meisten Paketreassemblys und die Zustandsnachverfolgung.
-   Enthält ein allgemeines Benutzerbenachrichtigungssystem, das Abonnenten über Änderungen am Filtersystem informiert.
-   Implementiert Enumerationsfunktionen, die berichte über den Zustand des Systems.
-   Verwendet Net-Ereignisse, um IPsec-Fehler und Paketverluste aufzuzeichnen.
-   Unterstützt eine [NDF-Hilfsklasse (Network](/windows/desktop/NDF/extensible-helper-classes)Diagnostics Framework).
-   Unterstützt die [Secure Socket-Erweiterungen](/windows/desktop/WinSock/winsock-secure-socket-extensions) für die Winsock-API, die es Netzwerkanwendungen ermöglichen, ihren Datenverkehr durch Konfigurieren von WFP zu schützen.
-   Auf ALE-Ebenen (Application Layer Enforcement) wirkt sich dies minimal auf die Netzwerkleistung aus, indem nur das erste Paket in einer Verbindung verarbeitet wird.
-   Integriert die Hardwareabladung, bei der Kernelmodus-Calloutmodule Hardware verwenden können, um bestimmte Paketüberprüfungen durchzuführen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[WFP-Architektur](windows-filtering-platform-architecture-overview.md)
</dt> <dt>

[WFP-Vorgang](basic-operation.md)
</dt> <dt>

[Anwendungsschichterzwingung (Application Layer Enforcement, ALE)](application-layer-enforcement--ale-.md)
</dt> <dt>

[IPsec-Konfiguration](ipsec-configuration.md)
</dt> <dt>

[WFP-Konfiguration](wfp-configuration.md)
</dt> <dt>

[WFP-Überwachung](wfp-monitoring.md)
</dt> <dt>

[WFP-API](api-sets.md)
</dt> </dl>

 

