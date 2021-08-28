---
description: Wenn eine Anwendung die funktion lineClose mit einem oder mehreren ausstehenden asynchronen Vorgängen aufruft, kann TAPI den Dienstanbieter anweisen, asynchrone Vorgänge zu beenden, die einem Aufruf zugeordnet sind.
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: Beendigung asynchroner Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d026754af75743314fbdbf7a2a3c82f9935f9b053f2a7186f095e4f452a0bdd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773000"
---
# <a name="termination-of-asynchronous-operations"></a>Beendigung asynchroner Vorgänge

Wenn eine Anwendung die [**funktion lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) mit einem oder mehreren ausstehenden asynchronen Vorgängen aufruft, kann TAPI den Dienstanbieter anweisen, asynchrone Vorgänge zu beenden, die einem Aufruf zugeordnet sind. Dies hängt davon ab, ob die Anwendung der einzige Besitzer des Aufrufs ist und über das einzige Handle für den Aufruf verfügt.

Wenn die Anwendung der einzige Besitzer eines Aufrufs ist, ruft TAPI [**tspi \_ lineDropOnClose**](./tspi-linedroponclose.md) oder [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (je nach Anbieter) für jeden solchen Aufruf auf. Der Dienstanbieter sollte alle ausstehenden asynchronen Vorgänge überprüfen, die dem gelöschten Aufruf zugeordnet sind. Wenn ein ausstehender Vorgang vorhanden ist, sollte der Dienstanbieter die entsprechende Aktion ergreifen und möglicherweise den laufenden Vorgang beenden.

Wenn die Anwendung über das einzige Handle für einen Aufruf verfügt (d. h., es gibt keine anderen Besitzer oder Monitore), ruft TAPI die [**\_ TSPI-Funktion lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) auf. Der Dienstanbieter muss diesen Aufruf als absoluten Hinweis darauf betrachten, dass ausstehende asynchrone Vorgänge abgebrochen werden müssen. Der Dienstanbieter muss einen ordnungsgemäßen Abschluss des Aufrufs sicherstellen und die [**ASYNC \_ COMPLETION-Rückruffunktion**](/windows/win32/api/tspi/nc-tspi-async_completion) für alle ausstehenden asynchronen Vorgänge aufrufen, wobei der FEHLERWERT LINEERR \_ OPERATIONFAILED angegeben wird. Wenn TAPI zuvor die [**\_ TSPI-Funktion lineDropOnClose**](./tspi-linedroponclose.md) oder [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) aufgerufen hat, ruft sie **TSPI \_ lineCloseCall** sofort auf, nachdem der Dienstanbieter vom anderen Aufruf zurückgegeben wurde. Er wartet nicht auf den Abschluss des asynchronen Vorgangs, der der **TSPI \_ lineDrop-Funktion** zugeordnet ist.

Wenn die Anwendung nicht der einzige Besitzer des Aufrufs ist, ruft TAPI [**tspi \_ lineDropOnClose**](./tspi-linedroponclose.md) oder [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)nicht auf. Wenn die Anwendung nicht über das einzige Handle für den Aufruf verfügt, ruft TAPI die [**\_ TSPI-Funktion lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) nicht auf. Wenn die Anwendung weder der einzige Besitzer noch der einzige Besitzer eines Handles für den Aufruf ist, sendet TAPI keine Benachrichtigung an den Dienstanbieter. Daher bleiben alle ausstehenden asynchronen Vorgänge intakt. Dies bedeutet, dass solche Anwendungen keine asynchronen Vorgänge beenden können, die sie mithilfe der [**funktion lineClose**](/windows/win32/api/tapi/nf-tapi-lineclose) gestartet haben. Da jedoch jeder asynchrone Vorgang erfordert, dass die aufrufende Anwendung besitzer des Aufrufs ist, ist die Wahrscheinlichkeit sehr selten, dass eine Anwendung asynchrone Vorgänge nicht beenden kann. In diesem Fall müssen die anderen Besitzer der Aufrufe die Verantwortung für die Disposition der Aufrufe übernehmen.

Wenn TAPI [**TSPI \_ lineDropOnClose**](./tspi-linedroponclose.md) oder [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)aufruft, muss der Dienstanbieter schließlich eine LINECALLSTATE \_ IDLE-Nachricht für den zugeordneten Aufruf senden (es sei [**denn, TSPI \_ lineCloseCall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) wird zuerst aufgerufen), damit Monitore beim Aufruf bereinigt werden können. Wenn der letzte Monitor die [**Funktion lineDeallocateCall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) aufgerufen hat, ruft TAPI die **\_ TSPI-Funktion lineCloseCall** auf. Alle ausstehenden Vorgänge müssen abgeschlossen oder beendet und [**ASYNC \_ COMPLETION**](/windows/win32/api/tspi/nc-tspi-async_completion) aufgerufen werden, wie weiter oben beschrieben.

 

 
