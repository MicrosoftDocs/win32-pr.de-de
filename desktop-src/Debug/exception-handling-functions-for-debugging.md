---
description: Wenn eine Ausnahme in einem Prozess auftritt, der gerade gedebuggt wird, benachrichtigt das System den Debugger, indem die Ausnahme an ihn übergeben wird. Dies wird als Benachrichtigung der ersten Chance bezeichnet. Das System setzt dann alle Threads im Prozess an, der gedebuggt wird.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Ausnahmebehandlungsfunktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab4542b6e1d3ad2699b3cb43d15e327d26156760980188555b1a4bf9c68e9a7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119573170"
---
# <a name="exception-handling-functions-for-debugging"></a>Ausnahmebehandlungsfunktionen für das Debuggen

Wenn eine Ausnahme in einem Prozess auftritt, der gerade gedebuggt wird, benachrichtigt das System den Debugger, indem die Ausnahme an ihn übergeben wird. Dies wird als *Erste-Chance-Benachrichtigung bezeichnet.* Das System setzt dann alle Threads im Prozess an, der gedebuggt wird.

Wenn der Debugger die Ausnahme nicht behandelt, versucht das System, einen geeigneten Ausnahmehandler zu finden. Wenn das System keine geeignete finden kann, benachrichtigt das System den Debugger erneut, dass eine Ausnahme aufgetreten ist. Dies wird als Benachrichtigung *mit letzter Chance bezeichnet.* Wenn der Debugger die Ausnahme nach der Benachrichtigung der letzten Chance nicht behandelt, beendet das System den debuggten Prozess.

Weitere Informationen finden Sie unter [Ausnahmebehandlung für Debugger.](debugger-exception-handling.md)

 

 



