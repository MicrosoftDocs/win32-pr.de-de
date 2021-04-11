---
description: Jeder Thread verfügt über eine dynamische Priorität.
ms.assetid: bcc6cec7-2d85-4810-98d0-7d99486f4924
title: Prioritäts Steigerungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37f463f30b0abffb24daadb4241ad32c5b51f123
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104216014"
---
# <a name="priority-boosts"></a>Prioritäts Steigerungen

Jeder Thread verfügt über eine *dynamische Priorität*. Dies ist die Priorität, die der Planer verwendet, um zu bestimmen, welcher Thread ausgeführt werden soll. Anfänglich ist die dynamische Priorität eines Threads mit der Basis Priorität identisch. Das System kann die dynamische Priorität erhöhen und verringern, um sicherzustellen, dass Sie reaktionsfähig ist und dass keine Threads zur Prozessorzeit verhungert werden. Das System erhöht die Priorität von Threads mit einer Basis Prioritätsstufe zwischen 16 und 31 nicht. Nur Threads mit einer Basis Priorität zwischen 0 und 15 empfangen dynamische Prioritäts Steigerungen.

Das System erhöht die dynamische Priorität eines Threads, um die Reaktionsfähigkeit wie folgt zu verbessern.

-   Wenn ein Prozess, der die normale \_ Prioritäts \_ Klasse verwendet, in den Vordergrund gestellt wird, erhöht der Planer die Prioritäts Klasse des Prozesses, der dem Vordergrund Fenster zugeordnet ist, sodass er größer als oder gleich der Prioritäts Klasse von Hintergrundprozessen ist. Die Prioritäts Klasse kehrt zur ursprünglichen Einstellung zurück, wenn sich der Prozess nicht mehr im Vordergrund befindet.
-   Wenn ein Fenster Eingaben empfängt, wie z. b. Zeit Geber Nachrichten, Maus Meldungen oder Tastatureingaben, erhöht der Planer die Priorität des Threads, der das Fenster besitzt.
-   Wenn die Warte Bedingungen für einen blockierten Thread erfüllt sind, erhöht der Scheduler die Priorität des Threads. Wenn z. b. ein warte Vorgang mit Datenträger-oder Tastatur-e/a abgeschlossen ist, erhält der Thread eine Prioritäts Erhöhung.

    Sie können das Prioritäts Verstärkungs Feature deaktivieren, indem Sie die Funktion [**setprocesspriorityboost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setprocesspriorityboost) oder [**setthreadpriorityboost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-setthreadpriorityboost) aufrufen. Um zu ermitteln, ob diese Funktion deaktiviert wurde, müssen Sie die [**getprocesspriorityboost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getprocesspriorityboost) -oder [**getthreadpriorityboost**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-getthreadpriorityboost) -Funktion aufrufen.

Nach dem erhöhen der dynamischen Priorität eines Threads reduziert der Planer diese Priorität um eine Ebene, wenn der Thread einen Zeit Slice abschließt, bis der Thread auf seine Basis Priorität zurückfällt. Die dynamische Priorität eines Threads ist nie kleiner als die Basis Priorität.

 

 
