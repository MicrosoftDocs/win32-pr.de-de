---
description: Ein Zeit- oder Wiederholungsereignis ist ein Ereignis, das zu einer bestimmten Uhrzeit und einem bestimmten Datum oder wiederholt in regelmäßigen Abständen auftritt. Beispielsweise kann ein Ereignis nur am 2. Dezember 2015 um Mitternacht oder einmal wöchentlich am Dienstag um 14:31 Uhr auftreten.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Empfangen eines Zeit- oder Wiederholungsereignisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45808d9d43ddc7b5370b129e29a4fc268fe09856013599c70bb65187a1c0b918
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118817476"
---
# <a name="receiving-a-timed-or-repeating-event"></a>Empfangen eines Zeit- oder Wiederholungsereignisses

Ein Zeit- oder Wiederholungsereignis ist ein Ereignis, das zu einer bestimmten Uhrzeit und einem bestimmten Datum oder wiederholt in regelmäßigen Abständen auftritt. Beispielsweise kann ein Ereignis nur am 2. Dezember 2015 um Mitternacht oder einmal wöchentlich am Dienstag um 14:31 Uhr auftreten.

In der folgenden Tabelle sind die verschiedenen Klassen aufgeführt, die zum Erstellen eines zeit- oder sich wiederholenden Ereignisses verwendet werden.



| Klasse                                                                                            | Beschreibung                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [ **Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) | Microsoft-Standardereignismodell.<br/> Weitere Informationen finden Sie unter [Creating a Timer Event with Win32 LocalTime or Win32 UTCTime (Erstellen eines Timerereignisses mit \_ Win32 LocalTime oder Win32 \_ UTCTime).](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)<br/> |
| [**\_\_TimerInstruction**](--timerinstruction.md)                                               | Legacy-Technik.<br/> Weitere Informationen finden Sie unter [Erstellen eines Timerereignisses mit \_ TimerInstruction.](creating-a-timer-event-with---timerinstruction.md)<br/>                                             |



 

Wenn Sie eine Aufgabe oder einen Auftrag zu einem bestimmten Zeitpunkt oder wiederholt planen möchten, verwenden Sie die [**Klasse Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) und ihre Methoden. Diese Klasse stellt einen Auftrag dar, der mit dem AT-Befehl in einem Befehlsfenster von **Start** und dann **Ausführen** oder aus den **geplanten Aufgaben** in **Systemsteuerung** erstellt wurde.

 

