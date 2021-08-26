---
title: Starten eines einzelnen Timerereignisses
description: Starten eines einzelnen Timerereignisses
ms.assetid: 56010877-1a02-4a7b-b58c-9f96b169acb2
keywords:
- Multimediatimer, Ereignisse
- Timer, Ereignisse
- Multimediatimer, Startereignisse
- Timer, Startereignisse
- timeSetEvent-Funktion
- Startzeitgeberereignisse
- Einzelne Timerereignisse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dc3a4c69aefe8df3310c8ff974ef7592b435eabccd661bdbeb1ebbf85dc3c9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037170"
---
# <a name="starting-a-single-timer-event"></a>Starten eines einzelnen Timerereignisses

> [!Note]  
> In diesem Thema wird eine veraltete Funktion beschrieben. Neue Anwendungen sollten die [**CreateTimerQueueTimer-Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) verwenden, um Timer zu erstellen.

 

Um ein einzelnes Timerereignis zu starten, rufen Sie die [**timeSetEvent-Funktion**](/previous-versions//dd757634(v=vs.85)) auf. Geben Sie dabei die Zeitspanne vor dem Rückruf, die Auflösung, die Adresse der Rückruffunktion (siehe [**TimeProc)**](/previous-versions//dd757631(v=vs.85))und die Benutzerdaten an, die mit der Rückruffunktion angegeben werden sollen. Eine Anwendung kann eine Funktion wie die folgende verwenden, um ein einzelnes Timerereignis zu starten.


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



Ein Beispiel für die Rückruffunktion OneShotCallback finden Sie unter [Writing a Timer Callback Function](writing-a-timer-callback-function.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Multimediatimern](using-multimedia-timers.md)
</dt> </dl>

 

 