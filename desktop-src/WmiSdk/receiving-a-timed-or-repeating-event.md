---
description: Ein Zeit gesteuerter oder sich wiederholendes Ereignis ist ein Ereignis, das zu einem bestimmten Zeitpunkt oder in regelmäßigen Abständen oder wiederholt auftritt. Ein Ereignis kann z. b. am 2. Dezember 2015 oder einmal wöchentlich um 2:31 Uhr um Mitternacht stattfinden.
ms.assetid: 369bf2d7-8350-4089-8e11-28e2b641f792
ms.tgt_platform: multiple
title: Empfangen eines zeitgesteuerten oder wiederholten Ereignisses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c395f77bdc9295b394fdee3b6d48894e07b09cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215343"
---
# <a name="receiving-a-timed-or-repeating-event"></a>Empfangen eines zeitgesteuerten oder wiederholten Ereignisses

Ein Zeit gesteuerter oder sich wiederholendes Ereignis ist ein Ereignis, das zu einem bestimmten Zeitpunkt oder in regelmäßigen Abständen oder wiederholt auftritt. Ein Ereignis kann z. b. am 2. Dezember 2015 oder einmal wöchentlich um 2:31 Uhr um Mitternacht stattfinden.

In der folgenden Tabelle werden die verschiedenen Klassen aufgelistet, die zum Erstellen eines zeitgesteuerten oder wiederholten Ereignisses verwendet werden.



| Klasse                                                                                            | BESCHREIBUNG                                                                                                                                                                                                         |
|--------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Win32 \_ Localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [ **Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime) | Standard mäßiges Microsoft-Ereignis Modell.<br/> Weitere Informationen finden Sie unter [Erstellen eines Zeit Geber Ereignisses mit Win32 \_ localtime oder Win32 \_ utcTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).<br/> |
| [**\_\_Timerinstruction**](--timerinstruction.md)                                               | Legacy-Technik.<br/> Weitere Informationen finden Sie unter [Erstellen eines Zeit Geber Ereignisses mit \_ timerinstruction](creating-a-timer-event-with---timerinstruction.md).<br/>                                             |



 

Wenn Sie planen, dass ein Task oder ein Auftrag zu einem bestimmten Zeitpunkt oder wiederholt ausgeführt wird, verwenden Sie die [**Win32 \_ ScheduledJob**](/windows/desktop/CIMWin32Prov/win32-scheduledjob) -Klasse und ihre Methoden. Diese Klasse stellt einen Auftrag dar, der mit dem AT-Befehl in einem Befehlsfenster von **Start** und dann **Ausführen** oder über die **geplanten Aufgaben** in der **Systemsteuerung** erstellt wurde.

 

