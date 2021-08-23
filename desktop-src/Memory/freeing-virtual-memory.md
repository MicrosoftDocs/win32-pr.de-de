---
description: Die VirtualFree-Funktion dekommitiert Seiten gemäß den folgenden Regeln und gibt diese frei.
ms.assetid: 8fbd7960-f3f0-4326-ad1d-12b636c0039e
title: Freigeben von virtuellem Arbeitsspeicher
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60c5f78da34573126cfb20d7bc16f803ec603c818a3147f388c9661245d6c408
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869695"
---
# <a name="freeing-virtual-memory"></a>Freigeben von virtuellem Arbeitsspeicher

Die [**VirtualFree-Funktion**](/windows/win32/api/memoryapi/nf-memoryapi-virtualfree) dekommitiert seiten gemäß den folgenden Regeln und gibt diese frei:

-   Dekommitiert eine oder mehrere Seiten, für die ein Commit ausgeführt wurde, und ändert den Zustand der Seiten in reserviert. Durch das Decommiting von Seiten wird der physische Speicher, der den Seiten zugeordnet ist, veröffentlicht, sodass er von jedem Prozess zugeordnet werden kann. Für jeden Block von Seiten, für die ein Commit ausgeführt wurde, kann der Commit aufgehoben werden.
-   Gibt einen Block von einer oder mehreren reservierten Seiten frei und ändert den Zustand der Seiten in "Free". Durch das Freigeben eines Seitenblocks wird der Bereich der reservierten Adressen verfügbar, der vom Prozess zugeordnet werden soll. Reservierte Seiten können nur freigegeben werden, indem der gesamte Block freigegeben wird, der ursprünglich von [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)reserviert wurde.
-   Dekommitiert einen Block von einer oder mehreren Seiten, für die ein Commit ausgeführt wurde, und gibt diesen gleichzeitig frei, und ändert den Zustand der Seiten in "Free". Der angegebene Block muss den gesamten Block enthalten, der ursprünglich von [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)reserviert wurde, und für alle Seiten muss derzeit ein Commit ausgeführt werden.

Nachdem ein Speicherblock freigegeben oder die Freigabe aufgehoben wurde, können Sie nie wieder darauf verweisen. Alle Informationen, die sich möglicherweise in diesem Speicher befinden, sind für immer verloren gegangen. Der Versuch, aus einer kostenlosen Seite zu lesen oder auf eine kostenlose Seite zu schreiben, führt zu einer Zugriffsverletzungsausnahme. Wenn Sie Informationen benötigen, sollten Sie den Arbeitsspeicher, der diese Informationen enthält, nicht freigeben oder freigeben.

Um anzugeben, dass die Daten in einem Speicherbereich nicht mehr von Interesse sind, rufen Sie [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) mit **MEM RESET \_ auf.** Die Seiten werden nicht aus der Auslagerungsdatei gelesen oder in diese geschrieben. Der Speicherblock kann jedoch später wieder verwendet werden.

 

 
