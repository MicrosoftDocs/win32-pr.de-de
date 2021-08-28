---
title: Informationen zu Multimediatimern
description: Informationen zu Multimediatimern
ms.assetid: 42101923-3f46-4234-bfcf-a0d06c382fa1
keywords:
- Windows Multimedia, Timer
- Multimedia, Timer
- Multimediaeingabe, Timer
- Multimediatimer, Informationen
- Timer, Informationen
- Multimediatimer, Planen von Ereignissen
- Timer, Planen von Ereignissen
- Planen von Zeitgeberereignissen
- Zeitsteuerung mit hoher Auflösung
- SetTimer-Funktion
- CreateWaitableTimer-Funktion
- WM_TIMER Nachrichten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99b5d899c93f0f292d7ef45e8584ae9e2b5e0e001037c456dcc4900f1c0d3f26
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498210"
---
# <a name="about-multimedia-timers"></a>Informationen zu Multimediatimern

Mit Multimedia-Timerdiensten können Anwendungen Zeitgeberereignisse mit der größtmöglichen Auflösung (oder Genauigkeit) für die Hardwareplattform planen. Mit diesen Multimedia-Timerdiensten können Sie Timerereignisse mit einer höheren Auflösung als andere Timerdienste planen.

Diese Timerdienste sind nützlich für Anwendungen, die eine zeitauflösende Zeitsteuerung mit hoher Auflösung erfordern. Beispielsweise erfordert ein CAB-Sequencer einen Zeitgeber mit hoher Auflösung, da er die Geschwindigkeit von EREIGNISSEN innerhalb einer Auflösung von 1 Millisekunde beibehalten muss.

Anwendungen, die keine Zeitsteuerung mit hoher Auflösung verwenden, sollten die [SetTimer-Funktion](/windows/win32/api/winuser/nf-winuser-settimer) anstelle von Multimedia-Timerdiensten verwenden. Die von **SetTimer** bereitgestellten Timerdienste stellen [WM \_ TIMER-Nachrichten](../winmsg/wm-timer.md) an eine Nachrichtenwarteschlange, während die Multimedia-Timerdienste eine Rückruffunktion aufrufen. Anwendungen, die einen wartebaren Timer benötigen, sollten die [CreateWaitableTimer-Funktion](/windows/win32/api/synchapi/nf-synchapi-createwaitabletimerw) verwenden.

 

 