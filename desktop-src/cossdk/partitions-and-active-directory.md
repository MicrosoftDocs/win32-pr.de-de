---
description: Zusätzlich zu Partitionen, die eine oder mehrere Anwendungen enthalten, enthält COM+ auch Partitionssätze, die eine oder mehrere Partitionen enthalten.
ms.assetid: 0b1a6daa-55e1-4a74-be01-e39473e3c0cc
title: Partitionen und Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 144dde53c6247dcf09dbf9540ce535afb12725822b8e9895f7eb33b569135089
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119462140"
---
# <a name="partitions-and-active-directory"></a>Partitionen und Active Directory

Zusätzlich zu Partitionen, die eine oder mehrere Anwendungen enthalten, enthält COM+ auch Partitionssätze, die eine oder mehrere Partitionen enthalten. Partitionssätze, die in Active Directory erstellt wurden, ermöglichen Benutzern in einer Domäne den Zugriff auf COM+-Anwendungen in der gesamten Domäne. Während der Erstellung wird jeder bestimmte Benutzer oder jede Organisationseinheit (OE) einer Partitionsgruppe zugewiesen oder zugeordnet.

Ein einzelner Benutzer oder eine Organisationseinheit kann auf mehrere Partitionen und deren Anwendungen zugreifen, da eine 1:1-Korrelation zwischen einer Benutzeridentität oder Organisationseinheit und einem Partitionssatz besteht. Ohne einen Partitionssatz benötigt ein Benutzer oder eine Organisationseinheit mehrere Benutzeridentitäten, um auf Anwendungen in verschiedenen Partitionen zugreifen zu können.

Um COM+-Anwendungen für Domänenbenutzer verfügbar zu machen, muss ein Administrator Aufgaben sowohl auf dem Domänencontroller, auf dem sich Active Directory befindet, als auch auf dem Server ausführen, auf dem die COM+-Anwendung installiert ist.

## <a name="on-the-domain-controller"></a>Auf dem Domänencontroller

Der Administrator erstellt zunächst eine Partition in Active Directory. Das Erstellen einer COM+-Partition erfolgt entweder mithilfe des Active Directory-Benutzer und -Computer-Verwaltungstools oder programmgesteuert mithilfe der Active Directory Services Interface (ADSI).

Nachdem die Partition in Active Directory erstellt wurde, erstellt der Administrator einen Partitionssatz. Beim Erstellen eines Partitionssets definiert der Administrator die Partitionen, die in diesem Satz enthalten sind. Das Erstellen eines COM+-Partitionssets erfolgt entweder mithilfe des Active Directory-Benutzer und -Computer-Verwaltungstools oder programmgesteuert mithilfe der Active Directory Services Interface (ADSI).

Schließlich ordnet der Administrator Domänenbenutzer oder Organisationseinheiten (OUs) dem neu erstellten Partitionssatz zu. Dazu wird die Seite Eigenschaften  eines Benutzers angezeigt, auf die Registerkarte **COM+-Partitionssätze** zugreifen und im Listenfeld ein Partitionssatz ausgewählt.

## <a name="on-the-com-application-server"></a>Auf dem COM+-Anwendungsserver

Der Administrator erstellt eine neue Partition und gibt dabei den gleichen Partitionsnamen und die gleiche Partitions-ID (GUID) wie die Partition an, die in Active Directory auf dem Domänencontroller erstellt wurde. Dies erfolgt mithilfe des **Ordners COM+-Partitionen** im Verwaltungstool komponentendienste. Um diese Aufgabe zu vereinfachen, ermöglicht das Tool Komponentendienste dem Administrator das Durchsuchen von Active Directory, um die gewünschte Partition und ihre GUID auszuwählen.

Wenn die Domänenpartition auf dem Anwendungsserver erstellt wurde, wird die Standardpartition eines Benutzers zur Standardpartition des Partitionssets in Active Directory. Schließlich kann der Administrator die COM+-Anwendung in der neu erstellten Partition auf dem Anwendungsserver installieren.

Weitere Informationen zum Verwalten von Partitionen für den Zugriff durch Domänenbenutzer finden Sie in der Hilfe, die dem Active Directory-Benutzer und -Computer zugeordnet ist.

## <a name="mapping-user-identities-and-ous-to-partition-sets"></a>Zuordnen von Benutzeridentitäten und Organisationsgruppen zu Partitionssätzen

Benutzer und Organisationsgruppen können partitionssätzen zugeordnet werden. Durch zuordnen von Organisationsgruppen zu Partitionssätzen kann ein Administrator mehrere Benutzer gleichzeitig einem Partitionssatz zuordnen, anstatt mehrere Benutzeridentitäten zuordnen zu müssen. Eine einzelne Benutzeridentität oder Organisationseinheit kann nur einem Partitionssatz zugeordnet werden. Im Allgemeinen führt die Zuordnung von Benutzeridentitäten oder Organisationsgruppen zu Partitionssätzen folgende Schritte aus:

-   Stellt sicher, dass Anwendungen für die entsprechenden Benutzer in der Domäne verfügbar sind.
-   Unterstützt COM+ bei der Bestimmung der Partition, in der sich eine Anwendung befindet.
-   Legt das Recht eines Benutzers fest, auf eine bestimmte Anwendung zu zugreifen.

Zum Zuordnen von Partitionen zu Partitionssätzen in Active Directory und zum Zuordnen von Benutzern und Organisationsgruppen zu diesen Partitionssätzen verwenden Administratoren die verwaltungstools Active Directory-Benutzer und -Computer und Komponentendienste. Wenn eine Partition in Active Directory erstellt wird, muss ein Administrator diese Partition lokal auf dem Computer konfigurieren, auf dem die entsprechende COM+-Anwendung installiert werden soll. Diese lokale Konfiguration von Partitionen, die in Active Directory erstellt werden, erfolgt über das Verwaltungstool komponentendienste.

Wenn eine Domänenbenutzeridentität nicht einem Partitionssatz zugeordnet ist, erhält der Benutzer Zugriff von der Organisationseinheit des Benutzers, die der Partition zugeordnet ist. Wenn die Organisationseinheit des Benutzers nicht einem Partitionssatz zugeordnet ist, aber die nächste höchste Organisationseinheit in der Hierarchie diesem Partitionssatz zugeordnet ist, kann der Benutzer auf die Partition zugreifen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Standardpartitionen](default-partitions.md)
</dt> <dt>

[Lokale Partitionen](local-partitions.md)
</dt> <dt>

[Partitionseigenschaften](partition-properties.md)
</dt> <dt>

[Die globale Partition](the-global-partition.md)
</dt> </dl>

 

 



