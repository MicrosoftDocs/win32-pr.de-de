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
# <a name="canceling-a-timer-event"></a>Abbrechen eines Zeit Geber Ereignisses

> [!Note]  
> In diesem Thema wird eine veraltete Funktion beschrieben. Neue Anwendungen sollten Zeit Geber [**mithilfe der Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) "die Funktion" "von" "erstellt werden.

 

Für jeden periodischen Timer, der durch Aufrufen von [**timesetevent**](/previous-versions//dd757634(v=vs.85))erstellt wird, muss die Anwendung den Timer durch Aufrufen der [**timekillevent**](/previous-versions//dd757630(v=vs.85)) -Funktion abbrechen, bevor Sie den Speicher freigibt, der die Rückruffunktion enthält. Zum Abbrechen eines Zeit Geber Ereignisses wird möglicherweise die folgende Funktion aufgerufen.


```C++
void DestroyTimer(NPSEQ npSeq)
{
    if(npSeq->wTimerID) {                // is timer event pending?
        timeKillEvent(npSeq->wTimerID);  // cancel the event
        npSeq->wTimerID = 0;
    }
} 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von multimeditimern](using-multimedia-timers.md)
</dt> </dl>

 

 