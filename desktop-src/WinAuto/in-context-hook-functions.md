---
title: In-Context Hook-Funktionen
ms.assetid: bf12bda6-b00e-4fbe-a576-b989aa428b54
description: 'Weitere Informationen finden Sie hier: In-Context Hook-Funktionen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe25bd64234cfbfd92f054565aa7c675328b435
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218493"
---
# <a name="in-context-hook-functions"></a><span data-ttu-id="41115-103">In-Context Hook-Funktionen</span><span class="sxs-lookup"><span data-stu-id="41115-103">In-Context Hook Functions</span></span>

<span data-ttu-id="41115-104">In der folgenden Liste werden die wichtigsten Aspekte der in-context-Hook-Funktionen beschrieben:</span><span class="sxs-lookup"><span data-stu-id="41115-104">The following list outlines the key aspects of in-context hook functions:</span></span>

-   <span data-ttu-id="41115-105">In-context-Hook-Funktionen müssen sich in einer Dynamic Link Library (dll) befinden, die das System dem Adressraum des Servers zuordnet.</span><span class="sxs-lookup"><span data-stu-id="41115-105">In-context hooks functions must be located in a dynamic-link library (DLL) that the system maps into the server's address space.</span></span>
-   <span data-ttu-id="41115-106">In-context-Hook-Funktionen geben den Adressraum mit dem Server frei.</span><span class="sxs-lookup"><span data-stu-id="41115-106">In-context hook functions share the address space with the server.</span></span>
-   <span data-ttu-id="41115-107">Wenn der Server ein Ereignis auslöst, ruft das System eine Hook-Funktion ohne Marshalling auf (Verpacken und Senden von Schnittstellenparametern über Prozess Grenzen hinweg).</span><span class="sxs-lookup"><span data-stu-id="41115-107">When the server triggers an event, the system calls a hook function without marshaling (packaging and sending interface parameters across process boundaries).</span></span>
-   <span data-ttu-id="41115-108">In-context-Hook-Funktionen sind tendenziell sehr schnell und empfangen Ereignis Benachrichtigungen synchron, da kein Marshalling vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="41115-108">In-context hook functions tend to be very fast and receive event notifications synchronously because there is no marshaling.</span></span>
-   <span data-ttu-id="41115-109">Einige Ereignisse werden möglicherweise außerhalb des Prozesses übermittelt, auch wenn Sie anfordern, dass Sie in-Process (mit dem WinEvent \_ InContext-Flag) übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="41115-109">Some events may be delivered out-of-process, even though you request that they be delivered in-process (using the WINEVENT\_INCONTEXT flag).</span></span> <span data-ttu-id="41115-110">Möglicherweise wird diese Situation mit 64-Bit-und 32-Bit-anwendungsinteroperabilitäts Problemen und mit Windows-Konsolen Ereignissen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41115-110">You might see this situation with 64-bit and 32-bit application interoperability issues and with Windows console events.</span></span>

 

 




