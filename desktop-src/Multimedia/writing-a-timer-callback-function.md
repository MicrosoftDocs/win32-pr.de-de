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
# <a name="writing-a-timer-callback-function"></a>Schreiben einer Timer-Rückruffunktion

> [!Note]  
> In diesem Thema wird eine veraltete Funktion beschrieben. Neue Anwendungen sollten Zeit Geber [**mithilfe der Funktion**](/windows/desktop/api/threadpoollegacyapiset/nf-threadpoollegacyapiset-createtimerqueuetimer) "die Funktion" "von" "erstellt werden.

 

Mit der folgenden Rückruffunktion, oneshottimer, wird der Bezeichner für das einzelne Timer-Ereignis ungültig und eine Zeit Geber Routine aufgerufen, um die anwendungsspezifischen Aufgaben zu verarbeiten. Weitere Informationen finden Sie unter [**timeproc**](/previous-versions//dd757631(v=vs.85)).


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

[Verwenden von multimeditimern](using-multimedia-timers.md)
</dt> </dl>

 

 