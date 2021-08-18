---
description: Der Dienststeuerungs-Manager (Service Control Manager, SCM) steuert einen Dienst, indem Dienststeuerungsereignisse an die Dienststeuerungshandlerroutine gesendet werden.
ms.assetid: 86e04b43-5f6f-409e-ac18-d7efada4d3d3
title: Multithreaddienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32b4b51f740e0a3773115b9048ec34619910936f1531fba1260740df28873b67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003728"
---
# <a name="multithreaded-services"></a>Multithreaddienste

Der Dienststeuerungs-Manager (Service Control Manager, SCM) steuert einen Dienst, indem Dienststeuerungsereignisse an die Steuerungshandlerroutine des Diensts gesendet werden. Der Dienst muss rechtzeitig auf Steuerungsereignisse reagieren, damit der SCM den Zustand des Diensts nachverfolgen kann. Außerdem muss der Zustand des Diensts mit der Beschreibung des Zustands übereinstimmen, den der SCM empfängt.

Aufgrund dieses Kommunikationsmechanismus zwischen einem Dienst und dem SCM müssen Sie vorsichtig sein, wenn Sie mehrere Threads in einem Dienst verwenden. Wenn ein Dienst angewiesen wird, vom SCM anzuhalten, muss er warten, bis alle Threads beendet werden, bevor an den SCM gemeldet wird, dass der Dienst beendet wird. Andernfalls kann der SCM über den Status des Diensts verwechselt werden und kann möglicherweise nicht ordnungsgemäß heruntergefahren werden.

Der SCM muss benachrichtigt werden, dass der Dienst auf das Beendigungssteuerungsereignis antwortet und dass der Fortschritt beim Beenden des Diensts erfolgt. Der SCM geht davon aus, dass der Dienst [](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)Fortschritte macht, wenn der Dienst innerhalb der im vorherigen Aufruf von **SetServiceStatus** angegebenen Zeit (Wartezeithinweis) antwortet und der Prüfpunkt aktualisiert wird, sodass er größer als der im vorherigen Aufruf von **SetServiceStatus** angegebene Prüfpunkt ist.

Wenn der Dienst an den SCM meldet, dass der Dienst beendet wurde, bevor alle Threads beendet wurden, interpretiert der SCM dies möglicherweise als Einenfall. Dies kann zu einem Zustand führen, in dem der Dienst nicht beendet oder neu gestartet werden kann.

 

 



