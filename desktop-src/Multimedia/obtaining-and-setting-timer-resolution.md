---
title: Abrufen und Festlegen der Zeit Geber Auflösung
description: Abrufen und Festlegen der Zeit Geber Auflösung
ms.assetid: 237a6770-89b9-4922-b9e9-0e0bf3e0c9b6
keywords:
- Multimedia-Timer, Lösung
- Timer, Auflösung
- minimale Zeit Geber Auflösung
- maximale Zeit Geber Auflösung
- Multimedia-Timer, maximale Auflösung
- Timer, maximale Auflösung
- Multimedia-Timer, minimale Auflösung
- Timer, minimale Auflösung
- timegetdevcaps-Funktion
- TimeBeginPeriod-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af5feca59e6fb4c528d6042b00eb7aa23263245c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340423"
---
# <a name="obtaining-and-setting-timer-resolution"></a><span data-ttu-id="be6d4-113">Abrufen und Festlegen der Zeit Geber Auflösung</span><span class="sxs-lookup"><span data-stu-id="be6d4-113">Obtaining and Setting Timer Resolution</span></span>

<span data-ttu-id="be6d4-114">Im folgenden Beispiel wird die Funktion [**timegetdevcaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) aufgerufen, um die minimalen und maximalen Zeit Geber Auflösungen zu ermitteln, die von den Timer-Diensten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="be6d4-114">The following example calls the [**timeGetDevCaps**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetdevcaps) function to determine the minimum and maximum timer resolutions supported by the timer services.</span></span> <span data-ttu-id="be6d4-115">Vor dem Einrichten von Timer-Ereignissen wird im Beispiel die minimale Zeit Geber Auflösung mithilfe der [**TimeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) -Funktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="be6d4-115">Before it sets up any timer events, the example establishes the minimum timer resolution by using the [**timeBeginPeriod**](/windows/desktop/api/TimeAPI/nf-timeapi-timebeginperiod) function.</span></span>


```C++
#define TARGET_RESOLUTION 1         // 1-millisecond target resolution

TIMECAPS tc;
UINT     wTimerRes;

if (timeGetDevCaps(&tc, sizeof(TIMECAPS)) != TIMERR_NOERROR) 
{
    // Error; application can't continue.
}

wTimerRes = min(max(tc.wPeriodMin, TARGET_RESOLUTION), tc.wPeriodMax);
timeBeginPeriod(wTimerRes); 
```



## <a name="related-topics"></a><span data-ttu-id="be6d4-116">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="be6d4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="be6d4-117">Verwenden von multimeditimern</span><span class="sxs-lookup"><span data-stu-id="be6d4-117">Using Multimedia Timers</span></span>](using-multimedia-timers.md)
</dt> </dl>

 

 




