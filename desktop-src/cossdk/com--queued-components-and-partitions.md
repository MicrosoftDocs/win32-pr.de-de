---
description: Der COM+-Dienst für Komponenten in der Warteschlange unterstützt das Konzept von Partitionen vollständig. Das heißt, wenn eine Komponente in einer Warteschlange innerhalb einer Partition ausgeführt wird, wird die Nachricht in die Warteschlange gestellt, und die Komponente wird schließlich innerhalb der Komponentenpartition ausgeführt.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Komponenten und Partitionen in der COM+-Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0296119d32eafefd3212ae37e32543b8fd14b884ff6401c16827717a9a6960b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129072"
---
# <a name="com-queued-components-and-partitions"></a>Komponenten und Partitionen in der COM+-Warteschlange

Der COM+-Dienst für Komponenten in der Warteschlange unterstützt das Konzept von Partitionen vollständig. Das heißt, wenn eine Komponente in der Warteschlange innerhalb einer Partition ausgeführt wird, wird die Nachricht in die Warteschlange gestellt, und die Komponente wird schließlich innerhalb der Partition der Komponente ausgeführt.

## <a name="queue-names-for-partitioned-components"></a>Warteschlangennamen für partitionierte Komponenten

Normalerweise verwendet der Dienst für Komponenten in der Warteschlange den Anwendungsnamen als Warteschlangennamen. Dies bedeutet, dass in einem Szenario ohne Partitionen, in dem nur eine Instanz eines Anwendungsnamens auf einem Computer vorhanden ist, jeder Anwendungsname über eine eigene Nachrichtenwarteschlange verfügt.

Bei Partitionen, bei denen mehrere Instanzen desselben Anwendungsnamens auf einem Computer vorhanden sein können, verwendet der Dienst für komponenten in der Warteschlange dieselbe Warteschlange für alle Komponenten in der Warteschlange, die denselben Anwendungsnamen verwenden.

## <a name="activating-queued-components"></a>Aktivieren von Komponenten in der Warteschlange

Die gleichen Regeln für die Verwendung der Partitions-ID zum Aktivieren einer Komponente, die sich nicht in der Warteschlange befindet, gelten wie folgt für eine Komponente in der Warteschlange:

-   Wenn ein Moniker zum Aktivieren der Warteschlangenkomponente verwendet wird und eine Partitions-ID enthalten ist, wird diese Partitions-ID verwendet, um die Partition zu suchen. Diese Partitions-ID hat Vorrang vor allen Partitions-IDs, die möglicherweise im Kontext der zu aktivierenden Komponente vorhanden sind.
-   Wenn kein Moniker zum Aktivieren der Komponente verwendet wird, wird die Partitions-ID verwendet, die sich im Kontext des Objekts befindet.
-   Wenn im Kontext des Objekts keine Partitions-ID vorhanden ist, wird die standardmäßige Zuordnung zwischen Benutzer und Partition in Active Directory verwendet.

> [!Note]  
> Wenn ein Servercomputer vom Netzwerk getrennt ist und die Zuordnung zwischen Benutzer und Partition geändert wird, während der Server getrennt ist, enthält der Partitionscache möglicherweise eine veraltete Zuordnung zwischen Benutzer und Partition. Dies kann zu einem Aktivierungsfehler führen, wenn die Zuordnung von Benutzer zu Partitionssatz der Mechanismus zum Aktivieren einer Komponente ist.

 

COM+-Ereignisse sind vollständig in Partitionen integriert. Dies bedeutet, dass ein Abonnent einen Verleger abonnieren kann, dessen Anwendung sich in einer Partition befindet. Um dieses Abonnement zu ermöglichen, enthält die Abonnentenklassensammlung zwei partitionsbezogene Eigenschaften: eine Ereignisklassenpartitions-ID und eine Ereignisklassenanwendungs-ID.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Anwendungsentwurfseinschränkungen](application-design-restrictions.md)
</dt> <dt>

[Partitionsimplementierung](partition-implementation.md)
</dt> <dt>

[Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Was sind COM+-Partitionen?](what-are-com--partitions-.md)
</dt> </dl>

 

 



