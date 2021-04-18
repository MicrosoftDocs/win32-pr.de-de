---
description: Der Dienst "com+-Warteschlangen Komponenten" unterstützt das Konzept der Partitionen vollständig. Das heißt, wenn eine in einer Warteschlange befindliche Komponente innerhalb einer Partition ausgeführt wird, wird die Nachricht in die Warteschlange eingereiht, und die Komponente wird schließlich innerhalb der Komponenten Partition ausgeführt.
ms.assetid: 08b0f7b5-6c45-4471-9634-1f42fbbf500c
title: Komponenten und Partitionen in der com+-Warteschlange
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 589d7cb7c3e61be8ef53a248f990cde65447cf9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523283"
---
# <a name="com-queued-components-and-partitions"></a>Komponenten und Partitionen in der com+-Warteschlange

Der Dienst "com+-Warteschlangen Komponenten" unterstützt das Konzept der Partitionen vollständig. Das heißt, wenn eine in einer Warteschlange befindliche Komponente innerhalb einer Partition ausgeführt wird, wird die Nachricht in die Warteschlange eingereiht, und die Komponente wird schließlich innerhalb der Partition der Komponente ausgeführt.

## <a name="queue-names-for-partitioned-components"></a>Warteschlangen Namen für partitionierte Komponenten

In der Regel verwendet der Dienst für in der Warteschlange befindliche Komponenten den Anwendungsnamen als Warteschlangen Namen. Dies bedeutet, dass in einem Szenario ohne Partitionen, in dem nur eine Instanz eines Anwendungs namens auf einem Computer vorhanden ist, jeder Anwendungsname eine eigene Nachrichten Warteschlange aufweist.

Wenn jedoch mehrere Instanzen desselben Anwendungs namens auf einem Computer vorhanden sein können, verwendet der Dienst für in der Warteschlange befindliche Komponenten für alle in der Warteschlange befindlichen Komponenten, die denselben Anwendungsnamen haben, dieselbe Warteschlange.

## <a name="activating-queued-components"></a>Aktivieren von Komponenten in der Warteschlange

Die gleichen Regeln, wie die Partitions-ID zum Aktivieren einer nicht in der Warteschlange befindlichen Komponente verwendet wird, gelten für eine in der Warteschlange befindliche Komponente wie folgt:

-   Wenn ein Moniker zum Aktivieren der in der Warteschlange befindlichen Komponente verwendet wird und eine Partitions-ID enthalten ist, wird diese Partitions-ID verwendet, um die Partition zu suchen. Diese Partitions-ID hat Vorrang vor allen Partitions-IDs, die im Kontext für die aktivierte Komponente vorhanden sein könnten.
-   Wenn kein Moniker zum Aktivieren der Komponente verwendet wird, wird die Partitions-ID verwendet, die im Kontext des Objekts verwendet wird.
-   Wenn im Kontext des Objekts keine Partitions-ID vorhanden ist, wird die Standard Zuordnung zwischen Benutzern und Partitionen in Active Directory verwendet.

> [!Note]  
> Wenn ein Server Computer vom Netzwerk getrennt ist und die Zuordnung zwischen Benutzer und Partition geändert wird, während der Server getrennt wird, kann der Partitions Cache eine veraltete Zuordnung zwischen Benutzern und Partitionen enthalten. Dies kann zu einem Aktivierungs Fehler führen, wenn die Zuordnung von Benutzer zu Partition zum Aktivieren einer Komponente verwendet wird.

 

Com+-Ereignisse sind vollständig in Partitionen integriert. Dies bedeutet, dass ein Abonnent einen Verleger abonnieren kann, dessen Anwendung sich innerhalb einer Partition befindet. Um dieses Abonnement zuzulassen, enthält die Auflistung der Abonnenten Klassen zwei Partitions bezogene Eigenschaften – eine Partitions-ID der Ereignisklasse und eine Anwendungs-ID der Ereignisklasse.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einschränkungen beim Anwendungs Entwurf](application-design-restrictions.md)
</dt> <dt>

[Partitions Implementierung](partition-implementation.md)
</dt> <dt>

[Registrieren und Aktivieren von Komponenten in Partitionen](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[Was sind COM+-Partitionen?](what-are-com--partitions-.md)
</dt> </dl>

 

 



