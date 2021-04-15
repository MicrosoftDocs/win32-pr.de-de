---
description: Informationen zu VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: Informationen zu VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 911145fda8f2dd63c886530af3d8507c38d8e829
ms.sourcegitcommit: 37f276b5d887a3aad04b1ba86e390dea9d87e591
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2021
ms.locfileid: "104556401"
---
# <a name="about-vds"></a>Informationen zu VDS

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [virtuellen Festplatten Dienstanbieter](virtual-disk-service-portal.md) durch die [Windows-Speicherverwaltungs-API](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)ersetzt.\]

Der Dienst für virtuelle Datenträger ist ein Microsoft Windows-Dienst, der Abfrage-und Konfigurations Vorgänge bei der Anforderung von Endbenutzern, Skripts und Anwendungen ausführt. Der-Dienst erweitert die vorhandenen Speicherfunktionen von Windows Server-Betriebssystemen wie folgt:

-   Stellt eine API für die vorhandenen Funktionen für Volume und Datenträgerverwaltung in Windows bereit.
-   Vereinheitlicht die Volumeverwaltung und die RAID-Verwaltung (Hardware Redundant Array of Independent Disks) unter einer einzigen API.

Die folgenden Speicher Verwaltungsaktivitäten werden von VDS nicht durchgeführt:

-   Verwaltung des Hardware Subsystems, z. b. die Temperaturüberwachung oder die Überwachung von Leistungsstatistiken für Datenträger Arrays.
-   SAN-Fabric-Verwaltung (Storage Area Network), wie z. b. die Zonenverwaltung und Sicherheit von Host-Based Adaptern (HBA).

In den folgenden Abschnitten wird die Architektur von VDS, die Rolle der VDS-Anbieter und die-API beschrieben.

## <a name="service-architecture"></a>Dienstarchitektur

VDS definiert drei Schnittstellen: eine einzelne Schnittstelle zwischen der Anwendungsebene und dem Dienst und zwei Schnittstellen zwischen dem Dienst und den Anbieter Programmen in der Datenschicht. Die folgende Abbildung zeigt die Grenze für die Anwendungs-zu-Dienst-Grenze und die Dienst-zu-Anbieter-Grenze.

![Das Diagramm zeigt die Dienst Architektur, die in den Abschnitten "Anwendungen", "virtueller Datenträger Dienst" und "VDS-Anbieter" unterteilt ist.](images/vdsoverview.png)

Die N-Tier-Architektur ermöglicht VDS das koordinieren mit den Dateisystemfunktionen, das Synchronisieren von Anbieter Aktivitäten und das zwischen Stellen von Anwendungen. VDS besteht zwischen der Anwendung und dem Anbieter und bietet eine einheitliche Funktionalität für Anwendungen, auch wenn einige der zugrunde liegenden Anbieter eine solche Einheitlichkeit aufweisen können.

Der Dienst implementiert allgemeine Funktionen: Formatieren von Volumes, hinzufügen und Entfernen von Laufwerk Buchstaben oder bereitgestellten Ordnern sowie verwalten nicht zugewiesener Datenträger – Datenträger, die keine Partitionsinformationen aufweisen. VDS gibt auch Ereignis Benachrichtigungen an registrierte Anwendungen zurück. Weitere Informationen finden Sie unter [VDS-Benachrichtigungen](vds-notification-model.md).

## <a name="role-of-providers"></a>Rolle von Anbietern

VDS definiert zwei Anbieter Schnittstellen, eine für einen Softwareanbieter und eine für einen Hardware Anbieter. Jeder Anbieter implementiert einen anderen Teil der API, der von VDS definiert wird:

-   Ein *Softwareanbieter* ist ein Host basiertes Programm, das von einem Kernelmodustreiber im Speicher-e/a-Stapel unterstützt wird. Die Anbieter-Kernel-Laufzeit interagiert zum Zeitpunkt der Startzeit mit dem Mount Manager, oder der Plug & Play (PNP) Manager zum Zeitpunkt der Ermittlung, um die einzelnen Datenträger zu beanspruchen. Software Anbieter arbeiten auf Volumes, Datenträgern und Datenträger Partitionen.

    VDS enthält zwei Anbieter Typen. Der Basic-Softwareanbieter verwaltet Basis Datenträger und bietet keine fehlertolerante Bindung. Der dynamische Softwareanbieter verwaltet dynamische Datenträger und bietet ggf. die Fehler Verwaltung. Das Verhalten des Software Anbieters ist mit dem Verhalten von grundlegenden und dynamischen Datenträgern auf dem Host konsistent. Wenn das Betriebssystem eines bestimmten Hosts z. b. fehlertolerante dynamische Datenträger unterstützt, unterstützt VDS auch dieses Verhalten auf dem Host.

-   Ein *Hardware Anbieter* implementiert die Methoden, die zum Verwalten eines Speicher Subsystems verwendet werden – ein Hardware Festplatten Array oder eine Adapterkarte, mit dem logische Datenträger erstellt werden können, die zur Verbesserung der Leistung, der Datenverfügbarkeit oder der Datenwiederherstellung konfiguriert sind. Viele große RAID-CAB-Hersteller haben einen Hardware Anbieter erstellt, der für die Verwendung mit VDS konzipiert ist. Dienstconsumer müssen einen Hardware Anbieter und zugehörige Hardware vom Hersteller erhalten.

    Die Funktionen eines Hardware Anbieters hängen von den Funktionen der zugrunde liegenden Hardware ab. Folglich kann der Grad, in dem die einzelnen Hersteller die API implementieren, variieren. Hersteller können z. b. zusätzliche Methoden zum Optimieren von Konfigurationen, zum Überwachen und zum dynamischen Optimieren der Leistung, zur Automatisierung der Fehler Verwaltung oder zur Bereitstellung anderer nützlicher Funktionen einschließen.

    Hardware Anbieter bieten verschiedene Konfigurationsoptionen, die für die Softwareanbieter nicht verfügbar sind. Besonders erwähnenswert ist das automagingkonfigurationsmodell, das eine Attribut basierte Ansicht des Speichers für jede Anwendung darstellt. Bindungs Hinweise, wie z. b. "überwiegend Lesevorgänge" oder "schnelle Absturz Wiederherstellung erforderlich" ersetzen die Komplexität der Bindung von physischem Speicher in den virtuellen Speicher. Jeder Hardware Anbieter führt eine Block Zuordnung, eine Speicherplatz Zuordnung und eine Bindungstyp Auswahl basierend auf den Hinweisen aus, die von einer Anwendung übermittelt werden. Die Beschreibung des kompletten Hardware Anbieters, einschließlich der Konfigurationsoptionen, finden Sie in der Dokumentation des Subsystem-Herstellers.

## <a name="application-programming-interface"></a>Anwendungsprogrammierschnittstelle

Anwendungen können VDS-Methoden aufrufen, um Host basierte Datenträger, RAID-Speicher oder beides abzufragen und zu konfigurieren. Eine Übersicht über die API finden Sie unter [VDS-Objektmodell](vds-object-model.md).

Typische Anwendungen für VDS lösen Konfigurations Verwaltung und Überwachungsprobleme aus und reichen von dedizierten Speicher Verwaltungssystemen bis hin zu Back-Office-Anwendungen, die eine bessere Kontrolle über die Konfiguration oder Fehler Verwaltung anstreben. Die folgenden Anwendungen verwenden heute VDS:

-   Das Snap-in "Datenträgerverwaltung" konfiguriert und verwaltet Datenträger, die von einem Host Computer gesteuert werden. System Administratoren und Endbenutzer können mit diesem Tool für die Benutzeroberfläche (UI) lokale (oder Remote-) Datenträger und Volumes Abfragen und konfigurieren.
-   Diskpart.exe ist ein Befehlszeilen-Hilfsprogramm, mit dem Datenträger, Volumes und Partitionen konfiguriert und verwaltet werden.
-   Diskraid.exe ist ein Befehlszeilen-Hilfsprogramm, mit dem Hardware-RAID-Subsysteme konfiguriert und verwaltet werden. Dieses Hilfsprogramm kann mit sämtlicher Speicherhardware interagieren, die von einem VDS-Hardware Anbieter begleitet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienst für virtuelle Datenträger](virtual-disk-service-portal.md)
</dt> <dt>

[VDS-Benachrichtigungen](vds-notification-model.md)
</dt> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> </dl>

 

 
