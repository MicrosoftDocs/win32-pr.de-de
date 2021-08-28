---
description: Sie erstellen ein Timerereignis, indem Sie eine Instanz von Klassen erstellen, die von der \_ \_ TimerInstruction-Klasse in einem beliebigen WMI-Namespace abgeleitet werden.
ms.assetid: 3df2a75a-5231-40d7-ae9d-a7a735fbf316
ms.tgt_platform: multiple
title: Erstellen eines Timerereignisses mit __TimerInstruction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31cb943419a255846fbde4e17e357f8ce199824085d542d8ad300fb7e301fa3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030670"
---
# <a name="creating-a-timer-event-with-__timerinstruction"></a>Erstellen eines Timerereignisses mit \_ \_ TimerInstruction

Sie erstellen ein Timerereignis, indem Sie eine Instanz von Klassen erstellen, die von der [**\_ \_ TimerInstruction-Klasse**](--timerinstruction.md) in einem beliebigen WMI-Namespace abgeleitet werden. WMI generiert dann das Timerereignis zum entsprechenden Zeitpunkt. Wenn Sie aufgrund von Computerausfällen ein Timerereignis übersehen, benachrichtigt WMI Sie über das verpasste Ereignis. WMI unterstützt Timerereignisse aus Gründen der Abwärtskompatibilität und für Szenarien, in denen Sie wissen müssen, wie viele Ereignisse seit dem letzten übermittelten Ereignis verpasst wurden. Für die meisten Timerereignisse sollten Sie jedoch einen Ereignisfilter für [**Win32 \_ LocalTime**](/previous-versions/windows/desktop/wmitimepprov/win32-localtime) oder [**Win32 \_ UTCTime**](/previous-versions/windows/desktop/wmitimepprov/win32-utctime)erstellen. Weitere Informationen finden Sie unter [Creating a Timer Event with Win32 LocalTime or Win32 UTCTime (Erstellen eines Timerereignisses mit \_ Win32 LocalTime oder Win32 \_ UTCTime).](creating-a-timer-event-with-win32-localtime-or-win32-utctime.md)

Das folgende Verfahren beschreibt das Erstellen und Empfangen eines Timerereignisses mit \_ \_ TimerInstruction.

**So erstellen und empfangen Sie ein Timerereignis mit \_ \_ TimerInstruction**

1.  Erstellen Sie eine Instanz der [**\_ \_ Klassen AbsoluteTimerInstruction**](--absolutetimerinstruction.md) oder [**\_ \_ IntervalTimerInstruction.**](--intervaltimerinstruction.md)

    Die Klassen [**\_ \_ AbsoluteTimerInstruction**](--absolutetimerinstruction.md) und [**\_ \_ IntervalTimerInstruction**](--intervaltimerinstruction.md) werden von der [**\_ \_ TimerInstruction-Klasse**](--timerinstruction.md) abgeleitet, die eine eindeutige vom Entwickler zugewiesene Zeichenfolge enthält, die den Typ des Timerereignisses identifiziert. Die **\_ \_ TimerInstruction-Klasse** enthält auch einen Wert, der angibt, ob WMI eine Benachrichtigung senden soll, wenn das Timerereignis auftritt, wenn WMI nicht verfügbar ist.

    Verwenden Sie [**\_ \_ AbsoluteTimerInstruction,**](--absolutetimerinstruction.md) um absolute Timerereignisse zu senden, die zu einem bestimmten Zeitpunkt an einem bestimmten Datum auftreten. Verwenden Sie [**\_ \_ IntervalTimerInstruction,**](--intervaltimerinstruction.md) um Intervalltimerereignisse zu senden, die in regelmäßigen Abständen auftreten.

2.  Legen Sie ihre Anwendung so fest, dass sie eine [**\_ \_ TimerEvent-Instanz empfängt.**](--timerevent.md)

    Um ein Ereignis zu generieren, erstellt WMI eine Instanz der [**\_ \_ TimerEvent-Klasse**](--timerevent.md) und leitet die Instanz an Ihren Consumer weiter. Die **\_ \_ TimerEvent-Instanz** enthält den Timeranweisungsbezeichner des Consumers. Die -Instanz enthält auch einen -Wert, der angibt, wie oft WMI die Timerereignisbenachrichtigung in einem beliebigen Intervall senden soll, wenn WMI den Consumer nicht erreichen kann.

 

 
