---
description: Zusätzlich zu Partitionen, die eine oder mehrere Anwendungen enthalten, umfasst com+ auch Partitions Sätze, die eine oder mehrere Partitionen enthalten.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Partitionen und Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b08e7b70c4b474e7b7bd949f530fb73973d39c6a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106341134"
---
# <a name="partitions-and-active-directory"></a>Partitionen und Active Directory

Zusätzlich zu Partitionen, die eine oder mehrere Anwendungen enthalten, umfasst com+ auch *Partitions Sätze*, die eine oder mehrere Partitionen enthalten. Die in Active Directory erstellten Partitions Sätze ermöglichen Benutzern in einer Domäne den Zugriff auf COM+-Anwendungen in der gesamten Domäne. Während der Erstellung wird jeder bestimmte Benutzer oder jede Organisationseinheit (OE) einem Partitions Satz zugewiesen oder zugeordnet.

Ein einzelner Benutzer oder eine Organisationseinheit kann auf mehrere Partitionen und deren Anwendungen zugreifen, weil eine 1:1-Korrelation zwischen einer Benutzeridentität oder einer Organisationseinheit und einem Partitions Satz vorliegt. Ohne eine Partition benötigt ein Benutzer oder eine Organisationseinheit mehrere Benutzer Identitäten für den Zugriff auf Anwendungen in verschiedenen Partitionen.

Um den Domänen Benutzern com+-Anwendungen zur Verfügung zu stellen, muss ein Administrator auf dem Domänen Controller, auf dem sich Active Directory befindet, und auf dem Server, auf dem die COM+-Anwendung installiert ist, Aufgaben ausführen

## <a name="on-the-domain-controller"></a>Auf dem Domänen Controller

Der Administrator erstellt zunächst innerhalb Active Directory eine Partition. Das Erstellen einer COM+-Partition erfolgt entweder über das Verwaltungs Tool "Active Directory Benutzer und Computer" oder Programm gesteuert mithilfe der Active Directory Services-Schnittstelle (ADSI).

Nachdem die Partition innerhalb Active Directory erstellt wurde, erstellt der Administrator einen Partitions Satz. Beim Erstellen eines Partitions Satzes definiert der Administrator die Partitionen, die in diesem Satz enthalten sind. Das Erstellen eines COM+-Partitions Satzes erfolgt entweder über das Verwaltungs Tool "Active Directory Benutzer und Computer" oder Programm gesteuert mithilfe der Active Directory Services-Schnittstelle (ADSI).

Schließlich ordnet der Administrator Domänen Benutzer oder Organisationseinheiten (OUs) dem neu erstellten Partitions Satz zu. Dies erfolgt durch Anzeigen der **Eigenschaften** Seite eines Benutzers, zugreifen auf die Registerkarte " **com+-Partitions Sätze** " und Auswählen eines Partitions Satzes aus dem Listenfeld.

## <a name="on-the-com-application-server"></a>Auf dem com+-Anwendungs Server

Der Administrator erstellt eine neue Partition und gibt den gleichen Partitionsnamen und die gleiche Partitions-ID (GUID) wie die der Partition an, die in Active Directory auf dem Domänen Controller erstellt wurde. Dies erfolgt über den **com+** -Ordner "Partitionen" im Verwaltungs Programm "Komponenten Dienste". Um diese Aufgabe zu vereinfachen, ermöglicht das Komponenten Dienst Tool dem Administrator, Active Directory zu durchsuchen, um die gewünschte Partition und ihre GUID auszuwählen.

Wenn die Domänen Partition auf dem Anwendungsserver erstellt wurde, wird die Standard Partition eines Benutzers zur Standard Partition der in der Active Directory festgelegten Partition. Schließlich kann der Administrator die COM+-Anwendung in der neu erstellten Partition auf dem Anwendungsserver installieren.

Weitere Informationen zum Verwalten von Partitionen für den Zugriff durch Domänen Benutzer finden Sie in der Hilfe im Zusammenhang mit dem Verwaltungs Tool "Active Directory-Benutzer und-Computer".

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Zuordnung von Benutzer Identitäten und Organisationseinheiten zu Partitions Sätzen

Benutzer und Organisationseinheiten können einem Partitions Satz zugeordnet werden. Durch die Zuordnung von Organisationseinheiten zu Partitions Sätzen kann ein Administrator mehreren Benutzern gleichzeitig einen Partitions Satz zuordnen, anstatt mehrere Benutzer Identitäten zuzuordnen. Eine einzelne Benutzeridentität oder Organisationseinheit kann nur einem Partitions Satz zugeordnet werden. Im allgemeinen bewirkt die Zuordnung von Benutzer Identitäten oder Organisationseinheiten zu Partitions Sätzen Folgendes:

-   Stellt sicher, dass Anwendungen für die entsprechenden Benutzer in der Domäne verfügbar sind.
-   Unterstützt com+ bei der Bestimmung der Partition, in der sich eine Anwendung befindet.
-   Richtet ein Benutzerrecht für den Zugriff auf eine bestimmte Anwendung ein.

Zum Zuordnen von Partitionen zu Partitions Sätzen in Active Directory und zum Zuordnen von Benutzern und Organisationseinheiten zu diesen Partitions Sätzen verwenden Administratoren die Verwaltungs Tools Active Directory Benutzer und Computer und Komponenten Dienste. Wenn eine Partition innerhalb Active Directory erstellt wird, muss ein Administrator diese Partition lokal auf dem Computer konfigurieren, auf dem die relevante com+-Anwendung installiert werden soll. Diese lokale Konfiguration von Partitionen, die in Active Directory erstellt werden, erfolgt über das Verwaltungs Programmkomponenten Dienste.

Wenn eine Domänen Benutzeridentität keinem Partitions Satz zugeordnet ist, erhält der Benutzer Zugriff durch die Organisationseinheit des Benutzers, der der Partition zugeordnet ist. Wenn die Organisationseinheit des Benutzers keinem Partitions Satz zugeordnet ist, aber die nächsthöchste Organisationseinheit in der Hierarchie diesem Partitions Satz zugeordnet ist, kann der Benutzer auf die Partition zugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standard Partitionen](default-partitions.md)
</dt> <dt>

[Lokale Partitionen](local-partitions.md)
</dt> <dt>

[Partitions Eigenschaften](partition-properties.md)
</dt> <dt>

[Die globale Partition](the-global-partition.md)
</dt> </dl>

 

 



