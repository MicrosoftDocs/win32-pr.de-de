---
description: In diesem Thema werden Timer erläutert. Ein Timer ist eine interne Routine, die wiederholt ein angegebenes Intervall in Millisekunden misst.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd8eced20e7d8b1eca5ec8a952f10798f92f1650db3c77bca76aca756cdd569
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120110690"
---
# <a name="timers"></a>Timer

Ein Timer ist eine interne Routine, die wiederholt ein angegebenes Intervall in Millisekunden misst.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                   | Beschreibung                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Timern](about-timers.md)       | Beschreibt, wie Timer erstellt, identifiziert, festgelegt und gelöscht werden.<br/>                                                     |
| [Verwenden von Timern](using-timers.md)       | Erläutert das Erstellen und Zerstören von Timern und die Verwendung eines Timers zum Abfangen von Mauseingaben in angegebenen Intervallen.<br/> |
| [Timerreferenz](timer-reference.md) | Enthält die API-Referenz.<br/>                                                                                    |



 

### <a name="timer-functions"></a>Timerfunktionen



| Name                           | Beschreibung                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**KillTimer**](/windows/win32/api/winuser/nf-winuser-killtimer) | Zerstört den angegebenen Timer. <br/>                                                                                                                                                                                                                                |
| [**SetTimer**](/windows/win32/api/winuser/nf-winuser-settimer)   | Erstellt einen Timer mit dem angegebenen Time out-Wert.<br/>                                                                                                                                                                                                            |
| [*TimerProc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | Eine anwendungsdefinierte Rückruffunktion, die [**WM \_ TIMER-Nachrichten**](wm-timer.md) verarbeitet. Der **TIMERPROC-Typ** definiert einen Zeiger auf diese Rückruffunktion. [*TimerProc ist*](/windows/win32/api/winuser/nc-winuser-timerproc) ein Platzhalter für den anwendungsdefinierten Funktionsnamen. <br/> |



 

### <a name="timer-notifications"></a>Timerbenachrichtigungen



| Name                          | Beschreibung                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM \_ TIMER**](wm-timer.md) | Wird an die Nachrichtenwarteschlange des installationsenden Threads gesendet, wenn ein Timer abläuft. Die Nachricht wird von der [**GetMessage-**](/windows/win32/api/winuser/nf-winuser-getmessage) oder [**PeekMessage-Funktion**](/windows/win32/api/winuser/nf-winuser-peekmessagea) gesendet. <br/> |



 

 

 
