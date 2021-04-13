---
title: Starten eines einzelnen Zeit Geber Ereignisses
description: Starten eines einzelnen Zeit Geber Ereignisses
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- Multimedia-Timer, Veranstaltungen
- Timer, Ereignisse
- Multimedia-Timer, starten von Ereignissen
- Timer, starten von Ereignissen
- timesetevent-Funktion
- Starten von Timer-Ereignissen
- Ereignisse mit nur einem Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c9d0024e3dfa9b0bda79f209abd9b81e89ad11c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104390195"
---
# <a name="starting-a-single-timer-event"></a><span data-ttu-id="6eaf4-110">Starten eines einzelnen Zeit Geber Ereignisses</span><span class="sxs-lookup"><span data-stu-id="6eaf4-110">Starting a Single Timer Event</span></span>

> [!Note]  
> <span data-ttu-id="6eaf4-111">In diesem Thema wird eine veraltete Funktion beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6eaf4-111">This topic describes an obsolete function.</span></span> <span data-ttu-id="6eaf4-112">Neue Anwendungen sollten Zeit Geber [**mithilfe der Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) "die Funktion" "von" "erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6eaf4-112">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="6eaf4-113">Um ein einzelnes Timer-Ereignis zu starten, rufen Sie die [**timesetevent**](/previous-versions//dd757634(v=vs.85)) -Funktion auf, und geben Sie die Zeitspanne vor dem Rückruf, die Auflösung, die Adresse der Rückruffunktion (siehe [**timeproc**](/previous-versions//dd757631(v=vs.85))) und die Benutzerdaten an, die mit der Rückruffunktion bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6eaf4-113">To start a single timer event, call the [**timeSetEvent**](/previous-versions//dd757634(v=vs.85)) function, specifying the amount of time before the callback occurs, the resolution, the address of the callback function (see [**TimeProc**](/previous-versions//dd757631(v=vs.85))), and the user data to supply with the callback function.</span></span> <span data-ttu-id="6eaf4-114">Eine Anwendung kann eine Funktion wie die folgende verwenden, um ein einzelnes Timer-Ereignis zu starten.</span><span class="sxs-lookup"><span data-stu-id="6eaf4-114">An application can use a function like the following to start a single timer event.</span></span>


```C++
UINT SetTimerCallback(NPSEQ npSeq,  // sequencer data
    UINT msInterval)                // event interval
{ 
    npSeq->wTimerID = timeSetEvent(
        msInterval,                    // delay
        wTimerRes,                     // resolution (global variable)
        OneShotCallback,               // callback function
        (DWORD)npSeq,                  // user data
        TIME_ONESHOT );                // single timer event
    if(! npSeq->wTimerID)
        return ERR_TIMER;
    else
        return ERR_NOERROR;
} 

```



<span data-ttu-id="6eaf4-115">Ein Beispiel für die Rückruffunktion oneshotcallback finden Sie unter [Schreiben einer Timer-Rückruffunktion](writing-a-timer-callback-function.md).</span><span class="sxs-lookup"><span data-stu-id="6eaf4-115">For an example of the callback function OneShotCallback, see [Writing a Timer Callback Function](writing-a-timer-callback-function.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6eaf4-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6eaf4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6eaf4-117">Verwenden von multimeditimern</span><span class="sxs-lookup"><span data-stu-id="6eaf4-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 