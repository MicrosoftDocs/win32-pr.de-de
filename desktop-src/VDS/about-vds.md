---
description: Informationen zu VDS
ms.assetid: b2f7628c-b567-40a9-9ad7-6c47077af5fb
title: Informationen zu VDS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1215251bf86c3ac4ba9a7a342a483de19653d20a21978715261b87aa7bea31a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603714"
---
# <a name="about-vds"></a>Informationen zu VDS

\[Ab Windows 8 und Windows Server 2012 wird die COM-Schnittstelle des [Virtual Disk Service](virtual-disk-service-portal.md) durch die Windows Storage Verwaltungs-API. [](/previous-versions/windows/desktop/stormgmt/windows-storage-management-api-portal)\]

Virtual Disk Service ist ein Microsoft Windows-Dienst, der Abfrage- und Konfigurationsvorgänge auf Anforderung von Endbenutzern, Skripts und Anwendungen ausführt. Der Dienst erweitert die vorhandenen Speicherfunktionen von Windows Serverbetriebssystemen auf folgende Weise:

-   Stellt eine API für die vorhandenen Volume- und Datenträgerverwaltungsfunktionen in Windows.
-   Vereinheitlicht die Volumeverwaltung und hardwareredundante Raid-Verwaltung (Redundant Array of Independent Disks) unter einer einzelnen API.

VDS führt die folgenden Speicherverwaltungsaktivitäten nicht aus:

-   Verwaltung des Hardwaresubsystems, z. B. Temperaturüberwachung oder Überwachung von Leistungsstatistiken für Datenträgerarrays.
-   Storage San-Fabric-Verwaltung (Area Network), z. B. Host-Based Adapter (HBA) und Sicherheit.

In den folgenden Abschnitten werden die Architektur von VDS, die Rolle von VDS-Anbietern und die API beschrieben.

## <a name="service-architecture"></a>Dienstarchitektur

VDS definiert drei Schnittstellen: eine einzelne Schnittstelle zwischen der Anwendungsschicht und dem Dienst und zwei Schnittstellen zwischen den Diensten und Anbieterprogrammen in der Datenschicht. Die folgende Abbildung zeigt die Anwendungs-zu-Dienst-Grenze und die Grenze zwischen Diensten.

![Diagramm, das die Dienstarchitektur zeigt, die in die Abschnitte "Anwendungen", "Virtual Disk Service" und "VDS-Anbieter" aufgeschlüsselt ist.](images/vdsoverview.png)

Die n-schichtige Architektur ermöglicht VDS die Koordination mit den Dateisystemfunktionen, das Synchronisieren von Anbieteraktivitäten und das Abkoordinieren zwischen Anwendungen. Im Zusammenhang mit der Anwendung und dem Anbieter stellt VDS eine einheitliche Funktionalität für Anwendungen zur Verfügung, auch wenn einige der zugrunde liegenden Anbieter diese Einheitlichkeit möglicherweise nicht haben.

Der Dienst implementiert allgemeine Funktionen: Formatieren von Volumes, Hinzufügen und Entfernen von Laufwerkbuchstaben oder bereitgestellten Ordnern sowie Verwalten nicht zugewiesener Datenträger – Datenträger ohne Partitionsinformationen. VDS gibt auch Ereignisbenachrichtigungen an registrierte Anwendungen zurück. Weitere Informationen finden Sie unter [VDS-Benachrichtigungen.](vds-notification-model.md)

## <a name="role-of-providers"></a>Rolle von Anbietern

VDS definiert zwei Anbieterschnittstellen: eine für einen Softwareanbieter und eine für einen Hardwareanbieter. Jeder Anbieter implementiert einen anderen Teil der durch VDS definierten API:

-   Ein *Softwareanbieter ist* ein hostbasiertes Programm, das von einem Kernelmodustreiber im Speicher-E/A-Stapel unterstützt wird. Die Anbieter-Kernel-Runtime interagiert zum Zeitpunkt der Ermittlung mit dem Bereitstellungs-Manager oder dem Plug & Play-Manager (PnP), um die einzelnen Datenträger zu beanspruchen. Softwareanbieter arbeiten mit Volumes, Datenträgern und Datenträgerpartitionen.

    VDS umfasst zwei Anbietertypen. Der Basic-Softwareanbieter verwaltet Basisdatenträger und bietet keine fehlertolerante Bindung. Der dynamische Softwareanbieter verwaltet dynamische Datenträger und bietet ggf. Fehlerverwaltung. Das Verhalten des Softwareanbieters ist konsistent mit dem Verhalten von basisbasierten und dynamischen Datenträgern auf dem Host. Wenn das Betriebssystem eines bestimmten Hosts beispielsweise fehlertolerante dynamische Datenträger unterstützt, unterstützt VDS dieses Verhalten auch auf dem Host.

-   Ein *Hardwareanbieter* implementiert die Methoden, die zum Verwalten eines Speichersubsystems verwendet werden– ein Hardwaredatenträgerarray oder eine Adapterkarte, die die Erstellung logischer Datenträger ermöglicht, die zur Verbesserung der Leistung, Datenverfügbarkeit oder Datenwiederherstellung konfiguriert sind. Viele große RAID-Schränkhersteller haben einen Hardwareanbieter erstellt, der für die Verwendung mit VDS entwickelt wurde. Dienstverbraucher müssen einen Hardwareanbieter und die zugehörige Hardware vom Hersteller beziehen.

    Die Funktionen eines Hardwareanbieters hängen von den Funktionen der zugrunde liegenden Hardware ab. Daher kann der Grad, in dem jeder Hersteller die API implementiert, variieren. Hersteller können beispielsweise zusätzliche Methoden zum Optimieren von Konfigurationen, überwachen und dynamisch optimieren, die Fehlerverwaltung automatisieren oder andere nützliche Funktionen bereitstellen.

    Hardwareanbieter bieten mehrere Konfigurationsoptionen, die den Softwareanbietern nicht zur Verfügung stehen. Am wichtigsten ist das automagic-Konfigurationsmodell, das jeder Anwendung eine attributbasierte Ansicht des Speichers bietet. Bindungshinweise wie "größtenteils Lese- oder schnelle Absturzwiederherstellung erforderlich" ersetzen die Komplexität der Bindung von physischem Speicher an den virtuellen Speicher. Jeder Hardwareanbieter führt die Zuordnung des Umfangs, die Speicherplatzzuordnung und die Bindungstypauswahl basierend auf den Hinweisen aus, die von einer Anwendung übermittelt werden. Die vollständige Beschreibung des Hardwareanbieters, einschließlich der Konfigurationsoptionen, finden Sie in der Dokumentation, die vom Subsystemhersteller bereitgestellt wird.

## <a name="application-programming-interface"></a>Anwendungsprogrammierschnittstelle

Anwendungen können VDS-Methoden aufrufen, um hostbasierte Datenträger, RAID-Speicher oder beides zu abfragen und zu konfigurieren. Eine Übersicht über die API finden Sie unter [VDS-Objektmodell.](vds-object-model.md)

Typische Anwendungen für VDS lösen Konfigurationsverwaltungs- und Überwachungsprobleme und reichen von dedizierten Speicherverwaltungssystemen bis hin zu Back-Office-Anwendungen, die eine bessere Kontrolle über die Konfiguration oder Fehlerverwaltung suchen. Die folgenden Anwendungen verwenden VDS noch heute:

-   Das Datenträgerverwaltungs-Snap-In konfiguriert und verwaltet Datenträger, die von einem Hostcomputer gesteuert werden. Systemadministratoren und Endbenutzer können lokale Datenträger und Volumes (oder Remotedatenträger) mit diesem Benutzeroberflächentool abfragen und konfigurieren.
-   Diskpart.exe ist ein Befehlszeilenprogramm, das Datenträger, Volumes und Partitionen konfiguriert und verwaltet.
-   Diskraid.exe ist ein Befehlszeilenprogramm, das HARDWARE-RAID-Subsysteme konfiguriert und verwaltet. Dieses Hilfsprogramm kann mit jeder Speicherhardware interagieren, die von einem VDS-Hardwareanbieter begleitet wird.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Dienst für virtuelle Datenträger](virtual-disk-service-portal.md)
</dt> <dt>

[VDS-Benachrichtigungen](vds-notification-model.md)
</dt> <dt>

[VDS-Objektmodell](vds-object-model.md)
</dt> </dl>

 

 
