---
description: Jeder Thread hat eine dynamische Priorität.
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: Prioritätssteigerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfe04bcd1df27c2456a06d35d83b894243c9871b3799f04bdc3c3df190ef251
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032020"
---
# <a name="priority-boosts"></a>Prioritätssteigerungen

Jeder Thread hat eine *dynamische Priorität.* Dies ist die Priorität, die der Scheduler verwendet, um zu bestimmen, welcher Thread ausgeführt werden soll. Anfänglich ist die dynamische Priorität eines Threads mit der Basispriorität identisch. Das System kann die dynamische Priorität erhöhen und senken, um sicherzustellen, dass es reaktionsfähig ist und dass keine Threads für die Prozessorzeit verhungern. Das System erhöht die Priorität von Threads mit einer Basisprioritätsstufe zwischen 16 und 31 nicht. Nur Threads mit einer Basispriorität zwischen 0 und 15 erhalten dynamische Prioritätssteigerungen.

Das System erhöht die dynamische Priorität eines Threads, um seine Reaktionsfähigkeit wie folgt zu verbessern.

-   Wenn ein Prozess, der NORMAL PRIORITY CLASS verwendet, in den Vordergrund gestellt wird, erhöht der Planer die Prioritätsklasse des Prozesses, der dem Vordergrundfenster zugeordnet ist, sodass er größer oder gleich der Prioritätsklasse von Hintergrundprozessen \_ \_ ist. Die Prioritätsklasse kehrt zur ursprünglichen Einstellung zurück, wenn sich der Prozess nicht mehr im Vordergrund befindet.
-   Wenn ein Fenster Eingaben empfängt, z. B. Timernachrichten, Mausnachrichten oder Tastatureingaben, erhöht der Scheduler die Priorität des Threads, der das Fenster besitzt.
-   Wenn die Wartebedingungen für einen blockierten Thread erfüllt sind, erhöht der Scheduler die Priorität des Threads. Wenn z. B. ein wartevorgang, der dem Datenträger oder der Tastatur-E/A zugeordnet ist, beendet wird, erhält der Thread eine Prioritätssteigerung.

    Sie können das Priority Boosting-Feature deaktivieren, indem Sie die [**Funktion SetProcessPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) oder [**SetThreadPriorityBoost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) aufrufen. Um festzustellen, ob dieses Feature deaktiviert wurde, rufen Sie die [**GetProcessPriorityBoost-**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) oder [**GetThreadPriorityBoost-Funktion**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) auf.

Nachdem die dynamische Priorität eines Threads erhöht wurde, reduziert der Scheduler diese Priorität jedes Mal um eine Ebene, wenn der Thread einen Zeitslice abschneidet, bis der Thread wieder auf seine Basispriorität zurückfällt. Die dynamische Priorität eines Threads ist nie kleiner als die Basispriorität.

 

 
