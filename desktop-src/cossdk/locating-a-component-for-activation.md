---
description: Suchen einer Komponente für die Aktivierung
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Suchen einer Komponente für die Aktivierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51badf0b33f7c133cdea1fa95c859c2f36e282bc748c75c560d57abeead802c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306218"
---
# <a name="locating-a-component-for-activation"></a>Suchen einer Komponente für die Aktivierung

Wenn COM+ die richtige Partition gefunden hat – über den Standardpartitionssatz der Benutzeridentität, einen Partitionsmoniker oder die Partitions-ID im Kontext des Objekts –, muss COM+ dann die richtige Komponente innerhalb dieser Partition finden. Die folgende Abbildung zeigt, wie eine Komponente gefunden und aktiviert wird, wenn sich diese Komponente in einer Partition befindet.

> [!Note]  
> Vor jeder Komponentenaktivierung führt COM+ eine Überprüfung durch, um zu überprüfen, ob die Benutzeridentität, die versucht, die Komponente zu aktivieren, über Zugriffsrechte für den Partitionssatz verfügt, in dem sich die Komponente befindet.

 

![Diagramm, das eine Problembehandlungsstruktur zum Suchen einer Komponente für die Aktivierung zeigt.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

Die obige Abbildung zeigt Folgendes:

-   Wenn sich die aufgerufene Komponente in einer Partition befindet und sich in derselben Anwendung wie die aufrufende Komponente befindet, wird die Komponente unabhängig davon aktiviert, ob die aufgerufene Komponente als öffentlich oder privat markiert ist.
-   Wenn sich die aufgerufene Komponente in einer Partition befindet, aber nicht in derselben Anwendung wie die aufrufende Komponente vorhanden ist, überprüft COM+, ob die Komponente als öffentlich markiert ist. Wenn keine öffentliche Version gefunden wird, durchsucht COM+ die globale Partition, um eine öffentliche Version der Komponente zu finden. Wenn keine öffentliche Version der Komponente in der globalen Partition gefunden wird oder die Benutzeridentität keine Rechte für die Partition hat, schlägt die Aktivierung fehl.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Suchen von Partitionen während der Aktivierung](locating-partitions-during-activation.md)
</dt> </dl>

 

 



