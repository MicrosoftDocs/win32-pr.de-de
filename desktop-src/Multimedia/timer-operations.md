---
title: Timerereignisvorgänge
description: Timerereignisvorgänge
ms.assetid: a2b75e84-4da8-449f-b02a-4ffc4846eef5
keywords:
- Multimedia-Timer,Ereignisse
- Timer, Ereignisse
- timeSetEvent-Funktion
- timeKillEvent-Funktion
- Starten von Timerereignissen
- Single Timer-Ereignisse
- Periodische Timerereignisse
- Abbrechen von Timerereignissen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e3869015cdde4afe5bd77bb65d39d5ee43aeb4eab65b1f54e7bfd3dadca1a2a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118370820"
---
# <a name="timer-event-operations"></a>Timerereignisvorgänge

Nachdem Sie die Timerauflösung Ihrer Anwendung eingerichtet haben, können Sie Timerereignisse mithilfe der [**timeSetEvent-Funktion**](/previous-versions//dd757634(v=vs.85)) starten. Diese Funktion gibt einen Timerbezeichner zurück, der zum Beenden oder Identifizieren von Timerereignissen verwendet werden kann. Einer der Parameter der Funktion ist die Adresse einer [**TimeProc-Rückruffunktion,**](/previous-versions//dd757631(v=vs.85)) die aufgerufen wird, wenn das Timerereignis stattfindet.

Es gibt zwei Arten von Timerereignissen: *einzelne und* *periodische*. Ein einzelnes Timerereignis tritt einmal nach einer angegebenen Anzahl von Millisekunden auf. Ein periodisches Timerereignis tritt jedes Mal auf, wenn eine angegebene Anzahl von Millisekunden verstreicht. Das Intervall zwischen periodischen Ereignissen wird als *Ereignisverzögerung bezeichnet.* Regelmäßige Timerereignisse mit einer Ereignisverzögerung von 10 Millisekunden oder weniger verbrauchen einen erheblichen Teil der CPU-Ressourcen.

Die Beziehung zwischen der Auflösung eines Timerereignisses und der Länge der Ereignisverzögerung ist in Timerereignissen wichtig. Wenn Sie beispielsweise eine Auflösung von 5 und eine Ereignisverzögerung von 100 angeben, benachrichtigen die Timerdienste die Rückruffunktion nach einem Intervall zwischen 95 und 105 Millisekunden.

Sie können ein aktives Timerereignis jederzeit mithilfe der [**timeKillEvent-Funktion**](/previous-versions//dd757630(v=vs.85)) abbrechen. Stellen Sie sicher, dass Sie alle ausstehenden Timer abbrechen, bevor Sie den Arbeitsspeicher mit der Rückruffunktion frei geben.

> [!Note]  
> Der Multimedia-Timer wird in einem eigenen Thread ausgeführt.

 

 

 