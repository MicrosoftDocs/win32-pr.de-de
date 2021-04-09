---
title: Überlegungen zur Programmiersprache
description: Beachten Sie beim Entwickeln von Multicast-Gruppen-Manager-Clients die folgenden Richtlinien.
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- Multicast, Überlegungen zur Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856504"
---
# <a name="mgm-programming-considerations"></a><span data-ttu-id="60593-104">Überlegungen zur Programmiersprache</span><span class="sxs-lookup"><span data-stu-id="60593-104">MGM Programming Considerations</span></span>

<span data-ttu-id="60593-105">Beachten Sie beim Entwickeln von Multicast-Gruppen-Manager-Clients die folgenden Richtlinien:</span><span class="sxs-lookup"><span data-stu-id="60593-105">When you are developing multicast group manager clients, observe the following guidelines:</span></span>

-   <span data-ttu-id="60593-106">Funktionsaufrufe müssen innerhalb des routerprozesses erfolgen.</span><span class="sxs-lookup"><span data-stu-id="60593-106">Function calls must be made from within the router process.</span></span> <span data-ttu-id="60593-107">Wenn Funktionen von einem anderen Prozess aufgerufen werden, sind die Ergebnisse nicht gültig. der Client interagiert nicht mit dem Multicast-Gruppen-Manager.</span><span class="sxs-lookup"><span data-stu-id="60593-107">If functions are called from another process, their results will not be valid; the client will not interact with the multicast group manager.</span></span>
-   <span data-ttu-id="60593-108">Clients, die die MGM-API verwenden, müssen eine eigene Fehlerüberprüfung bereitstellen, um sicherzustellen, dass nur gültige Daten an den Multicast Gruppen-Manager übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="60593-108">Clients that use the MGM API must provide their own error checking, ensuring that only valid data is passed to the multicast group manager.</span></span> <span data-ttu-id="60593-109">Von den MGM-Funktionen werden keine ausführlichen Fehlermeldungen zu ungültigen Parametern zurückgegeben. der \_ ungültige \_ Parameter Wert wird ohne Erklärung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="60593-109">MGM functions do not return detailed error messages about invalid parameters; the ERROR\_INVALID\_PARAMETER value is returned without explanation.</span></span>
-   <span data-ttu-id="60593-110">Clients sollten bei der Verwendung von Sperren beim Aufrufen von MGM-Funktionen Vorsicht walten lassen.</span><span class="sxs-lookup"><span data-stu-id="60593-110">Clients should exercise caution in using locks while calling MGM functions.</span></span> <span data-ttu-id="60593-111">Dadurch können Deadlocks verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="60593-111">Doing so can prevent deadlocks.</span></span> <span data-ttu-id="60593-112">Wenn Sie die Funktionen von "MGM" aufrufen, sollten Clients keine Sperren enthalten, die gleichzeitig in einem Rückruf vom Multicast-Gruppen-Manager aufbewahrt werden können.</span><span class="sxs-lookup"><span data-stu-id="60593-112">When calling MGM functions, clients should not hold any locks that might simultaneously be held in a callback from the multicast group manager.</span></span>

 

 




