---
description: Gruppieren von Anwendungen in Partitionen
ms.assetid: bdfe2428-9769-4bcb-b74e-a141ba67a67e
title: Gruppieren von Anwendungen in Partitionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28b35c726662d7dbe2cf039678ba5cdb4f94eeea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346461"
---
# <a name="grouping-applications-into-partitions"></a>Gruppieren von Anwendungen in Partitionen

Bei der Entscheidung, wie Anwendungen in Partitionen gruppiert werden sollen, müssen Administratoren bestimmte Regeln und Einschränkungen beachten, einschließlich der folgenden:

-   Eine Anwendung kann in einer oder mehreren Partitionen installiert werden.
-   In einer Anwendung kann nur eine Instanz einer bestimmten Komponente vorhanden sein.

## <a name="public-and-private-components"></a>Öffentliche und private Komponenten

Bei der Entscheidung, wie COM+-Anwendungen gruppiert werden sollen, gibt es weitere Einschränkungen. Diese Einschränkungen beziehen sich auf öffentliche und private Komponenten innerhalb einer Anwendung. Anwendungskomponenten können im Allgemeinen entweder öffentlich oder privat sein. Wenn Sie jedoch Anwendungen in Partitionen gruppieren, sollten Administratoren einige Einschränkungen bei den öffentlichen und privaten Komponenten beachten. In der folgenden Tabelle sind diese Einschränkungen aufgeführt.



| Wenn eine Anwendung:              | Die Komponenten in einer Partition können folgende sein:                                                                                   |
|------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Eine Serveranwendung<br/>    | Öffentlich und privat.<br/>                                                                                           |
| Eine Bibliotheks Anwendung<br/>   | Nur öffentlich. Andernfalls könnte die aufruferanwendung die gleichen Komponenten aufweisen, was zu Mehrdeutigkeit führen würde.<br/> |
| In der globalen Partition<br/> | Nur öffentlich. Dadurch wird die Abwärtskompatibilität sichergestellt.<br/>                                                             |



 

## <a name="application-ids"></a>Anwendungs-IDs

Jede auf einem Computer installierte COM+-Anwendung verfügt über eine eindeutige Anwendungs-ID. Anwendungsnamen müssen jedoch nur innerhalb einer einzelnen Partition und nicht auf dem gesamten Computer eindeutig sein.

In der folgenden Tabelle wird gezeigt, was mit der Anwendungs-ID geschieht, wenn eine Anwendung in eine Partition importiert oder aus einer Partition exportiert wird.



| Wenn eine Anwendung:                                              | Dann die Anwendungs-ID:                    |
|--------------------------------------------------------------------|---------------------------------------------|
| In die globale Partition importiert<br/>                        | Bleibt unverändert<br/>                 |
| Wird in eine andere Partition als die globale Partition importiert.<br/> | Wurde geändert<br/>                       |
| Exportiert<br/>                                                | Ist in der exportierten Datei enthalten.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sammeln von Partitions Metriken](collecting-partition-metrics.md)
</dt> <dt>

[Konfigurieren des Partitions Caches](configuring-the-partition-cache.md)
</dt> <dt>

[Verwalten von lokalen Partitionen](managing-local-partitions.md)
</dt> <dt>

[Verwalten von Partitionen in Active Directory](managing-partitions-within-active-directory.md)
</dt> <dt>

[Festlegen von Administratorrechten für eine Partition](setting-administrative-rights-for-a-partition.md)
</dt> </dl>

 

 




