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
# <a name="starting-a-single-timer-event"></a>Starten eines einzelnen Zeit Geber Ereignisses

> [!Note]  
> In diesem Thema wird eine veraltete Funktion beschrieben. Neue Anwendungen sollten Zeit Geber [**mithilfe der Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) "die Funktion" "von" "erstellt werden.

 

Um ein einzelnes Timer-Ereignis zu starten, rufen Sie die [**timesetevent**](/previous-versions//dd757634(v=vs.85)) -Funktion auf, und geben Sie die Zeitspanne vor dem Rückruf, die Auflösung, die Adresse der Rückruffunktion (siehe [**timeproc**](/previous-versions//dd757631(v=vs.85))) und die Benutzerdaten an, die mit der Rückruffunktion bereitgestellt werden sollen. Eine Anwendung kann eine Funktion wie die folgende verwenden, um ein einzelnes Timer-Ereignis zu starten.


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



Ein Beispiel für die Rückruffunktion oneshotcallback finden Sie unter [Schreiben einer Timer-Rückruffunktion](writing-a-timer-callback-function.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von multimeditimern](using-multimedia-timers.md)
</dt> </dl>

 

 