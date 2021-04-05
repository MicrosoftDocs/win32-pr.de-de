---
title: Timer-Ereignis Vorgänge
description: Timer-Ereignis Vorgänge
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- Multimedia-Timer, Veranstaltungen
- Timer, Ereignisse
- timesetevent-Funktion
- timekillevent-Funktion
- Starten von Timer-Ereignissen
- Ereignisse mit nur einem Timer
- periodische Timer-Ereignisse
- Abbrechen von Zeit Geber Ereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1d4329a6d6c55e9e8dd6c56fab5d1e3ca938833
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103724800"
---
# <a name="timer-event-operations"></a>Timer-Ereignis Vorgänge

Nachdem Sie die Zeit Geber Auflösung Ihrer Anwendung festgelegt haben, können Sie Timer-Ereignisse mithilfe der [**timesetevent**](/previous-versions//dd757634(v=vs.85)) -Funktion starten. Diese Funktion gibt einen Zeit Geber Bezeichner zurück, der verwendet werden kann, um Zeit Geber Ereignisse anzuhalten oder zu identifizieren. Einer der Parameter der Funktion ist die Adresse einer [**timeproc**](/previous-versions//dd757631(v=vs.85)) -Rückruffunktion, die aufgerufen wird, wenn das Timer-Ereignis stattfindet.

Es gibt zwei Arten von Timer-Ereignissen: *Single* und *periodisch*. Ein einzelnes Timer-Ereignis tritt einmal nach einer angegebenen Anzahl von Millisekunden auf. Jedes Mal, wenn eine angegebene Anzahl von Millisekunden verstrichen ist, tritt ein regelmäßiges Timer-Ereignis auf. Das Intervall zwischen periodischen Ereignissen wird als *Ereignis Verzögerung* bezeichnet. Periodische Timer-Ereignisse mit einer Ereignis Verzögerung von 10 Millisekunden oder weniger belegen einen erheblichen Anteil der CPU-Ressourcen.

Die Beziehung zwischen der Auflösung eines Zeit Geber Ereignisses und der Länge der Ereignis Verzögerung ist in Zeit Geber Ereignissen wichtig. Wenn Sie z. b. eine Auflösung von 5 und eine Ereignis Verzögerung von 100 angeben, benachrichtigen die Timer-Dienste die Rückruffunktion nach einem Intervall zwischen 95 und 105 Millisekunden.

Sie können ein aktives Timer-Ereignis jederzeit mithilfe der [**timekillevent**](/previous-versions//dd757630(v=vs.85)) -Funktion abbrechen. Stellen Sie sicher, dass Sie alle ausstehenden Timer abbrechen, bevor Sie den Speicher freigeben, der die Rückruffunktion enthält.

> [!Note]  
> Der Multimedia-Timer wird in einem eigenen Thread ausgeführt.

 

 

 