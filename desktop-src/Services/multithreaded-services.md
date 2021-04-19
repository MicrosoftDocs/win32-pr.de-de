---
description: Der Dienststeuerungs-Manager (SCM) steuert einen Dienst, indem er Dienst Steuerungs Ereignisse an die Dienstkontroll-Handlerroutine sendet.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Multithread-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5795a170f912050d115537407fcb491305a35ba3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369763"
---
# <a name="multithreaded-services"></a>Multithread-Dienste

Der Dienststeuerungs-Manager (SCM) steuert einen Dienst, indem er Dienst Steuerungs Ereignisse an die Steuerungs Handlerroutine des dienstanders sendet. Der Dienst muss auf rechtzeitige Weise auf Steuerungs Ereignisse reagieren, damit der SCM den Status des Dienstanbieter verfolgen kann. Außerdem muss der Zustand des Dienstanbieter mit der Beschreibung seines Zustands, den der SCM empfängt, identisch sein.

Aufgrund dieses Kommunikationsmechanismus zwischen einem Dienst und dem SCM müssen Sie bei der Verwendung mehrerer Threads in einem Dienst sorgfältig vorgehen. Wenn ein Dienst angewiesen wird, vom SCM zu beenden, muss er warten, bis alle Threads beendet werden, bevor er dem SCM berichtet, dass der Dienst beendet wird. Andernfalls kann der SCM über den Status des Dienstanbieter verwechselt werden und kann möglicherweise nicht ordnungsgemäß heruntergefahren werden.

Der SCM muss benachrichtigt werden, dass der Dienst auf das Stop-Steuerungs Ereignis antwortet und dass der Fortschritt beim Beenden des dienstandens erfolgt. Der SCM geht davon aus, dass der Dienst Fortschritte macht, wenn der Dienst innerhalb des Zeitpunkts (Wait-Hinweises), der im vorherigen Aufruf von **SetServiceStatus** angegeben wurde, den Status (über [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) antwortet. der Prüfpunkt wird so aktualisiert, dass er größer ist als der im vorherigen Aufruf von **SetServiceStatus** angegebene Prüfpunkt

Wenn der Dienst dem SCM meldet, dass der Dienst beendet wurde, bevor alle Threads beendet wurden, ist es möglich, dass der SCM dies als Widerspruch interpretiert. Dies kann zu einem Zustand führen, in dem der Dienst nicht beendet oder neu gestartet werden kann.

 

 



