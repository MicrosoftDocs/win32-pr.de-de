---
description: In diesem Thema werden Timer erläutert. Ein Timer ist eine interne Routine, die wiederholt ein angegebenes Intervall in Millisekunden misst.
ms.assetid: vs|winui|~\winui\windowsuserinterface\windowing\timers.htm
title: Timer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fa44be05acc09eafed550a200ed6bc61f79daa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362711"
---
# <a name="timers"></a>Timer

Ein Timer ist eine interne Routine, die wiederholt ein angegebenes Intervall in Millisekunden misst.

### <a name="in-this-section"></a>In diesem Abschnitt



| Name                                   | BESCHREIBUNG                                                                                                               |
|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [Informationen zu Timern](about-timers.md)       | Beschreibt, wie Timer erstellt, identifiziert, festgelegt und gelöscht werden.<br/>                                                     |
| [Verwenden von Timern](using-timers.md)       | Erläutert, wie Timer erstellt und zerstört werden und wie ein Timer verwendet wird, um Maus Eingaben in angegebenen Intervallen abzufangen.<br/> |
| [Timer-Verweis](timer-reference.md) | Enthält die API-Referenz.<br/>                                                                                    |



 

### <a name="timer-functions"></a>Timer-Funktionen



| Name                           | BESCHREIBUNG                                                                                                                                                                                                                                                              |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Killtimer Memberfunktion**](/windows/win32/api/winuser/nf-winuser-killtimer) | Zerstört den angegebenen Timer. <br/>                                                                                                                                                                                                                                |
| [**Ziel**](/windows/win32/api/winuser/nf-winuser-settimer)   | Erstellt einen Timer mit dem angegebenen Timeout Wert.<br/>                                                                                                                                                                                                            |
| [*Timerproc*](/windows/win32/api/winuser/nc-winuser-timerproc)   | Eine Anwendungs definierte Rückruffunktion, die [**WM- \_**](wm-timer.md) Zeit Geber Nachrichten verarbeitet. Der **timerproc** -Typ definiert einen Zeiger auf diese Rückruffunktion. [*Timerproc*](/windows/win32/api/winuser/nc-winuser-timerproc) ist ein Platzhalter für den Namen der Anwendungs definierten Funktion. <br/> |



 

### <a name="timer-notifications"></a>Timer-Benachrichtigungen



| Name                          | BESCHREIBUNG                                                                                                                                                                                     |
|-------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WM- \_ Timer**](wm-timer.md) | Wird in der Meldungs Warteschlange des Installations Threads gepostet, wenn ein Timer abläuft. Die Nachricht wird von der [**GetMessage**](/windows/win32/api/winuser/nf-winuser-getmessage) -Funktion oder der [**Peer Message**](/windows/win32/api/winuser/nf-winuser-peekmessagea) -Funktion gepostet. <br/> |



 

 

 
