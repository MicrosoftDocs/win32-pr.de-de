---
title: Schreiben einer Timerrückruffunktion
description: Schreiben einer Timerrückruffunktion
ms.assetid: 85260b6b-42de-43f4-83b7-94edbf660006
keywords:
- Multimedia-Timer, Rückruffunktionen
- Timer, Rückruffunktionen
- Schreiben von Timerrückruffunktionen
- Multimedia-Timer, Schreiben von Rückruffunktionen
- Timer, Schreiben von Rückruffunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b8680fc4d697c33514276276daaa2a4d75577bfbd78fa3caffc7f426ca9d70
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119891780"
---
# <a name="writing-a-timer-callback-function"></a>Schreiben einer Timerrückruffunktion

> [!Note]  
> In diesem Thema wird eine veraltete Funktion beschrieben. Neue Anwendungen sollten die [**CreateTimerQueueTimer-Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) verwenden, um Timer zu erstellen.

 

Die folgende Rückruffunktion, OneShotTimer, macht den Bezeichner für das einzelne Timerereignis ungültig und ruft eine Timerroutine auf, um die anwendungsspezifischen Aufgaben zu verarbeiten. Weitere Informationen finden Sie unter [**TimeProc**](/previous-versions//dd757631(v=vs.85)).


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von Multimedia-Timern](using-multimedia-timers.md)
</dt> </dl>

 

 