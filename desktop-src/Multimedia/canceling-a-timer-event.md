---
title: Abbrechen eines Zeit Geber Ereignisses
description: Abbrechen eines Zeit Geber Ereignisses
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- Multimedia-Timer, Veranstaltungen
- Timer, Ereignisse
- timekillevent-Funktion
- Abbrechen von Zeit Geber Ereignissen
- Multimedia-Timer, Abbrechen von Ereignissen
- Timer, Abbrechen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1380b2868596e0177e806f5df5217bb839abe61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104038953"
---
# <a name="canceling-a-timer-event"></a><span data-ttu-id="4998c-109">Abbrechen eines Zeit Geber Ereignisses</span><span class="sxs-lookup"><span data-stu-id="4998c-109">Canceling a Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="4998c-110">In diesem Thema wird eine veraltete Funktion beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4998c-110">This topic describes an obsolete function.</span></span> <span data-ttu-id="4998c-111">Neue Anwendungen sollten Zeit Geber [**mithilfe der Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) "die Funktion" "von" "erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4998c-111">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="4998c-112">Für jeden periodischen Timer, der durch Aufrufen von [**timesetevent**](/previous-versions//dd757634(v=vs.85))erstellt wird, muss die Anwendung den Timer durch Aufrufen der [**timekillevent**](/previous-versions//dd757630(v=vs.85)) -Funktion abbrechen, bevor Sie den Speicher freigibt, der die Rückruffunktion enthält.</span><span class="sxs-lookup"><span data-stu-id="4998c-112">For every periodic timer creating by calling [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)), the application must cancel the timer by calling the [**timeKillEvent**](/previous-versions//dd757630(v=vs.85)) function before it frees the memory that contains the callback function.</span></span> <span data-ttu-id="4998c-113">Zum Abbrechen eines Zeit Geber Ereignisses wird möglicherweise die folgende Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="4998c-113">To cancel a timer event, it might call the following function.</span></span>


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a><span data-ttu-id="4998c-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4998c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4998c-115">Verwenden von multimeditimern</span><span class="sxs-lookup"><span data-stu-id="4998c-115">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 