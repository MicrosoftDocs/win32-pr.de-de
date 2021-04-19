---
description: Wenn eine Anwendung die lineclose-Funktion mit einem oder mehreren ausstehenden asynchronen Vorgängen aufruft, kann TAPI den Dienstanbieter anweisen, asynchrone Vorgänge zu beenden, die einem Aufruf zugeordnet sind.
ms.assetid: b26ce074-76dc-4a50-8c17-d3412c336d59
title: Beendigung von asynchronen Vorgängen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8ed2acb0f442e5f4f07427f0e224d7a288087d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349727"
---
# <a name="termination-of-asynchronous-operations"></a>Beendigung von asynchronen Vorgängen

Wenn eine Anwendung die [**lineclose**](/windows/win32/api/tapi/nf-tapi-lineclose) -Funktion mit einem oder mehreren ausstehenden asynchronen Vorgängen aufruft, kann TAPI den Dienstanbieter anweisen, asynchrone Vorgänge zu beenden, die einem Aufruf zugeordnet sind, abhängig davon, ob die Anwendung der alleinige Besitzer des Aufrufs ist und über das einzige Handle für den Aufruf verfügt.

Wenn die Anwendung der alleinige Besitzer eines Aufrufs ist, ruft TAPI [**TSPI \_ linedroponclose**](./tspi-linedroponclose.md) oder [**TSPI \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) (abhängig vom Anbieter) für jeden solchen Aufruf auf. Der Dienstanbieter sollte überprüfen, ob ausstehende, dem Löschvorgang zugeordnete asynchrone Vorgänge vorhanden sind. Wenn ein ausstehender Vorgang vorhanden ist, sollte der Dienstanbieter die entsprechende Aktion durchführen und den Vorgang möglicherweise beenden.

Wenn die Anwendung über das einzige Handle für einen Aufruf verfügt (d. h., es sind keine anderen Besitzer oder Monitore vorhanden), ruft TAPI die [**TSPI \_ lineclosecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) -Funktion auf. Der Dienstanbieter muss diesen Rückruf als absoluten Hinweis in Erwägung gezogen, dass ausstehende asynchrone Vorgänge abgebrochen werden müssen. Der Dienstanbieter muss einen ordnungsgemäßen Abschluss des Aufrufs sicherstellen und die asynchrone [**\_ Vervollständigungs**](/windows/win32/api/tspi/nc-tspi-async_completion) Rückruffunktion für alle ausstehenden asynchronen Vorgänge aufrufen, wobei der \_ Fehlerwert lineerr operationfailed angegeben wird. Wenn TAPI zuvor die [**TSPI \_ linedroponclose**](./tspi-linedroponclose.md) -oder [**TSPI-Funktion \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) aufgerufen hat, wird **TSPI \_ lineclosecall** unmittelbar nach dem zurückkehren des Dienstanbieters aus dem anderen Aufruf aufgerufen. es wird nicht gewartet, bis der asynchrone Vorgang abgeschlossen ist, der der **TSPI- \_ linedrop** -Funktion zugeordnet ist.

Wenn die Anwendung nicht der alleinige Besitzer des Aufrufes ist, ruft TAPI nicht [**TSPI \_ linedroponclose**](./tspi-linedroponclose.md) oder [**TSPI \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)auf. Wenn die Anwendung nicht über das einzige Handle für den-Befehl verfügt, ruft TAPI nicht die [**TSPI \_ lineclosecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) -Funktion auf. Wenn die Anwendung weder der alleinige Besitzer noch der alleinige Besitzer eines Handles für den-Befehl ist, sendet TAPI keine Benachrichtigung an den Dienstanbieter. daher bleiben alle ausstehenden asynchronen Vorgänge intakt. Dies bedeutet, dass solche Anwendungen asynchrone Vorgänge, die Sie gestartet haben, nicht beenden können, indem Sie die [**lineclose**](/windows/win32/api/tapi/nf-tapi-lineclose) -Funktion verwenden. Da jedoch für jeden asynchronen Vorgang die aufrufende Anwendung als Besitzer des Aufrufs fungieren muss, ist die Wahrscheinlichkeit, dass eine Anwendung nicht in der Lage ist, asynchrone Vorgänge zu beenden, sehr selten. Wenn dies der Fall ist, müssen die anderen Besitzer des Aufrufes (s) die Verantwortung für die Disposition der Aufrufe übernehmen.

Wenn TAPI [**TSPI \_ linedroponclose**](./tspi-linedroponclose.md) oder [**TSPI \_ linedrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop)aufruft, muss der Dienstanbieter schließlich eine linecallstate- \_ Leerlauf Nachricht für den zugeordneten Aufruf senden (es sei denn, [**TSPI \_ lineclosecall**](/windows/win32/api/tspi/nf-tspi-tspi_lineclosecall) wird zuerst aufgerufen), damit Monitore des Aufrufs bereinigen können. Wenn der letzte Monitor die [**linedezugecall**](/windows/win32/api/tapi/nf-tapi-linedeallocatecall) -Funktion aufgerufen hat, ruft TAPI die **TSPI \_ lineclosecall** -Funktion auf. alle ausstehenden Vorgänge müssen abgeschlossen oder beendet und der asynchrone [**\_ Abschluss**](/windows/win32/api/tspi/nc-tspi-async_completion) wie zuvor beschrieben aufgerufen werden.

 

 
