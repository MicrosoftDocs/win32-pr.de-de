---
description: Sie erstellen ein Timer-Ereignis, indem Sie eine Instanz von Klassen erstellen, die von der \_ \_ timerinstruction-Klasse in einem beliebigen WMI-Namespace abgeleitet sind.
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: Erstellen eines Zeit Geber Ereignisses mit __TimerInstruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e502678525569dae272edb7b03c0916db25edfd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217964"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>Erstellen eines Timer-Ereignisses mit \_ \_ timerinstruction

Sie erstellen ein Timer-Ereignis, indem Sie eine Instanz von Klassen erstellen, die von der [**\_ \_ timerinstruction**](--timerinstruction.md) -Klasse in einem beliebigen WMI-Namespace abgeleitet sind. WMI generiert dann das Timer-Ereignis zum richtigen Zeitpunkt. Wenn Sie ein Timer-Ereignis aufgrund von Ausfallzeiten übersehen, werden Sie von WMI über das verpasste Ereignis benachrichtigt. WMI unterstützt Zeit Geber Ereignisse aus Gründen der Abwärtskompatibilität und Szenarios, in denen Sie wissen müssen, wie viele Ereignisse Sie seit dem letzten übermittelten Ereignis verpasst haben. Für die meisten Timer-Ereignisse sollten Sie jedoch einen Ereignis Filter für [**Win32 \_ localtime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [**Win32 \_ utcTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)erstellen. Weitere Informationen finden Sie unter [Erstellen eines Zeit Geber Ereignisses mit Win32 \_ localtime oder Win32 \_ utcTime](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).

Im folgenden Verfahren wird beschrieben, wie ein Timer-Ereignis mit \_ \_ timerinstruction erstellt und empfangen wird.

**So erstellen Sie ein Timer-Ereignis mit \_ \_ timerinstruction und empfangen es**

1.  Erstellen Sie eine Instanz der [**\_ \_ absolutetimerinstruction**](--absolutetimerinstruction.md) -Klasse oder der [**\_ \_ intervaltimerinstruction**](--intervaltimerinstruction.md) -Klasse.

    Die Klassen [**\_ \_ absolutetimerinstruction**](--absolutetimerinstruction.md) und [**\_ \_ intervaltimerinstruction**](--intervaltimerinstruction.md) werden von der [**\_ \_ timerinstruction**](--timerinstruction.md) -Klasse abgeleitet, die eine eindeutige, vom Entwickler zugewiesene Zeichenfolge enthält, die den Typ des Timer-Ereignisses identifiziert. Die **\_ \_ timerinstruction** -Klasse enthält außerdem einen Wert, der angibt, ob WMI eine späte Benachrichtigung senden soll, wenn das Timer-Ereignis auftritt, wenn WMI nicht verfügbar ist.

    Verwenden Sie [**\_ \_ absolutetimerinstruction**](--absolutetimerinstruction.md) , um absolute Timer-Ereignisse zu senden, die an einem bestimmten Datum zu einem bestimmten Zeitpunkt auftreten. Verwenden Sie [**\_ \_ intervaltimerinstruction**](--intervaltimerinstruction.md) , um Intervallzeit Geber Ereignisse zu senden, die in regelmäßigen Abständen auftreten.

2.  Legen Sie fest, dass Ihre Anwendung eine [**\_ \_ TimerEvent**](--timerevent.md) -Instanz empfängt.

    Zum Generieren eines Ereignisses erstellt WMI eine Instanz der [**\_ \_ TimerEvent**](--timerevent.md) -Klasse und leitet die Instanz an den Consumer weiter. Die **\_ \_ TimerEvent** -Instanz enthält die timeranweisungs-ID des Consumers. Die-Instanz enthält außerdem einen Wert, der angibt, wie oft WMI die Zeit Geber Ereignis Benachrichtigung während eines beliebigen Intervalls senden soll, wenn WMI den Consumer nicht erreichen kann.

 

 
