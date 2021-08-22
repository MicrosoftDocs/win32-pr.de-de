---
title: Abbrechen eines Timerereignisses
description: Abbrechen eines Timerereignisses
ms.assetid: 4c1be031-e3d5-4d7c-b197-c40c61fc4e2f
keywords:
- Multimediatimer, Ereignisse
- Timer, Ereignisse
- timeKillEvent-Funktion
- Abbrechen von Timerereignissen
- Multimediatimer, Abbrechen von Ereignissen
- Timer, Abbrechen von Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4e9a92a02dca8ffd4723685fc96cdb0f82fc34a0fa2e3481a71a51997c316
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691791"
---
# <a name="canceling-a-timer-event"></a>Abbrechen eines Timerereignisses

> [!Note]  
> In diesem Thema wird eine veraltete Funktion beschrieben. Neue Anwendungen sollten die [**CreateTimerQueueTimer-Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) verwenden, um Timer zu erstellen.

 

Für jeden periodischen Timer, der durch Aufrufen von [**timeSetEvent**](/previous-versions//dd757634(v=vs.85))erstellt wird, muss die Anwendung den Timer abbrechen, indem sie die [**timeKillEvent-Funktion**](/previous-versions//dd757630(v=vs.85)) aufruft, bevor der Arbeitsspeicher freigegeben wird, der die Rückruffunktion enthält. Um ein Timerereignis abzubrechen, wird möglicherweise die folgende Funktion aufgerufen.


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

[Verwenden von Multimediatimern](using-multimedia-timers.md)
</dt> </dl>

 

 