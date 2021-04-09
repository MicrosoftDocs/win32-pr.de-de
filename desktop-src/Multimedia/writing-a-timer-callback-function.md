---
title: Schreiben einer Timer-Rückruffunktion
description: Schreiben einer Timer-Rückruffunktion
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- Multimedia-Timer, Rückruf Funktionen
- Timer, Rückruf Funktionen
- Schreiben von Timer-Rückruf Funktionen
- Multimedia-Timer, Schreiben von Rückruf Funktionen
- Timer, Schreiben von Rückruf Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 609cf2dda455897fb6cae0f3c48252016ba54cb9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103948649"
---
# <a name="writing-a-timer-callback-function"></a><span data-ttu-id="36bcb-108">Schreiben einer Timer-Rückruffunktion</span><span class="sxs-lookup"><span data-stu-id="36bcb-108">Writing a Timer Callback Function</span></span>

> [!Note]  
> <span data-ttu-id="36bcb-109">In diesem Thema wird eine veraltete Funktion beschrieben.</span><span class="sxs-lookup"><span data-stu-id="36bcb-109">This topic describes an obsolete function.</span></span> <span data-ttu-id="36bcb-110">Neue Anwendungen sollten Zeit Geber [**mithilfe der Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) "die Funktion" "von" "erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="36bcb-110">New applications should use the [**CreateTimerQueueTimer**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) function to create timers.</span></span>

 

<span data-ttu-id="36bcb-111">Mit der folgenden Rückruffunktion, oneshottimer, wird der Bezeichner für das einzelne Timer-Ereignis ungültig und eine Zeit Geber Routine aufgerufen, um die anwendungsspezifischen Aufgaben zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="36bcb-111">The following callback function, OneShotTimer, invalidates the identifier for the single timer event and calls a timer routine to handle the application-specific tasks.</span></span> <span data-ttu-id="36bcb-112">Weitere Informationen finden Sie unter [**timeproc**](/previous-versions//dd757631(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="36bcb-112">For more information, see [**TimeProc**](/previous-versions//dd757631(v=vs.85)).</span></span>


```C++
void CALLBACK OneShotTimer(UINT wTimerID, UINT msg, 
    DWORD dwUser, DWORD dw1, DWORD dw2) 
{ 
    NPSEQ npSeq;             // pointer to sequencer data 
    npSeq = (NPSEQ)dwUser;
    npSeq->wTimerID = 0;     // invalidate timer ID (no longer in use)
    TimerRoutine(npSeq);     // handle tasks 
} 
```



## <a name="related-topics"></a><span data-ttu-id="36bcb-113">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36bcb-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36bcb-114">Verwenden von multimeditimern</span><span class="sxs-lookup"><span data-stu-id="36bcb-114">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 