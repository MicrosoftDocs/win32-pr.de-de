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
# <a name="multithreaded-services"></a><span data-ttu-id="b107d-103">Multithread-Dienste</span><span class="sxs-lookup"><span data-stu-id="b107d-103">Multithreaded Services</span></span>

<span data-ttu-id="b107d-104">Der Dienststeuerungs-Manager (SCM) steuert einen Dienst, indem er Dienst Steuerungs Ereignisse an die Steuerungs Handlerroutine des dienstanders sendet.</span><span class="sxs-lookup"><span data-stu-id="b107d-104">The service control manager (SCM) controls a service by sending service control events to the service's control handler routine.</span></span> <span data-ttu-id="b107d-105">Der Dienst muss auf rechtzeitige Weise auf Steuerungs Ereignisse reagieren, damit der SCM den Status des Dienstanbieter verfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="b107d-105">The service must respond to control events in a timely manner so that the SCM can keep track of the state of the service.</span></span> <span data-ttu-id="b107d-106">Außerdem muss der Zustand des Dienstanbieter mit der Beschreibung seines Zustands, den der SCM empfängt, identisch sein.</span><span class="sxs-lookup"><span data-stu-id="b107d-106">Also, the state of the service must match the description of its state that the SCM receives.</span></span>

<span data-ttu-id="b107d-107">Aufgrund dieses Kommunikationsmechanismus zwischen einem Dienst und dem SCM müssen Sie bei der Verwendung mehrerer Threads in einem Dienst sorgfältig vorgehen.</span><span class="sxs-lookup"><span data-stu-id="b107d-107">Due to this communication mechanism between a service and the SCM, you must be careful when using multiple threads in a service.</span></span> <span data-ttu-id="b107d-108">Wenn ein Dienst angewiesen wird, vom SCM zu beenden, muss er warten, bis alle Threads beendet werden, bevor er dem SCM berichtet, dass der Dienst beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b107d-108">When a service is instructed to stop by the SCM, it must wait for all the threads to exit before reporting to the SCM that the service is stopped.</span></span> <span data-ttu-id="b107d-109">Andernfalls kann der SCM über den Status des Dienstanbieter verwechselt werden und kann möglicherweise nicht ordnungsgemäß heruntergefahren werden.</span><span class="sxs-lookup"><span data-stu-id="b107d-109">Otherwise, the SCM can become confused about the state of the service and might fail to shut down correctly.</span></span>

<span data-ttu-id="b107d-110">Der SCM muss benachrichtigt werden, dass der Dienst auf das Stop-Steuerungs Ereignis antwortet und dass der Fortschritt beim Beenden des dienstandens erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b107d-110">The SCM needs to be notified that the service is responding to the stop control event and that progress is being made in stopping the service.</span></span> <span data-ttu-id="b107d-111">Der SCM geht davon aus, dass der Dienst Fortschritte macht, wenn der Dienst innerhalb des Zeitpunkts (Wait-Hinweises), der im vorherigen Aufruf von **SetServiceStatus** angegeben wurde, den Status (über [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) antwortet. der Prüfpunkt wird so aktualisiert, dass er größer ist als der im vorherigen Aufruf von **SetServiceStatus** angegebene Prüfpunkt</span><span class="sxs-lookup"><span data-stu-id="b107d-111">The SCM will assume the service is making progress if the service responds (through [**SetServiceStatus**](/windows/desktop/api/Winsvc/nf-winsvc-setservicestatus)) within the time (wait hint) specified in the previous call to **SetServiceStatus**, and the check point is updated to be greater than the checkpoint specified in the previous call to **SetServiceStatus**.</span></span>

<span data-ttu-id="b107d-112">Wenn der Dienst dem SCM meldet, dass der Dienst beendet wurde, bevor alle Threads beendet wurden, ist es möglich, dass der SCM dies als Widerspruch interpretiert.</span><span class="sxs-lookup"><span data-stu-id="b107d-112">If the service reports to the SCM that the service has stopped before all threads have exited, it is possible that the SCM will interpret this as a contradiction.</span></span> <span data-ttu-id="b107d-113">Dies kann zu einem Zustand führen, in dem der Dienst nicht beendet oder neu gestartet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b107d-113">This might result in a state where the service cannot be stopped or restarted.</span></span>

 

 



