---
description: Wenn in einem Prozess, der debuggt wird, eine Ausnahme auftritt, benachrichtigt das System den Debugger, indem er die Ausnahme an ihn übergibt. Dies wird als Benachrichtigung über die erste Chance bezeichnet. Das System hält dann alle Threads im debuggten Prozess an.
ms.assetid: 6fdc02ac-9c33-49a8-8614-8b0cc2bf811b
title: Ausnahme Behandlungs Funktionen für das Debuggen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35bca1d031b56a4e7cb208ca93abc9ca0dbdbb7c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860574"
---
# <a name="exception-handling-functions-for-debugging"></a>Ausnahme Behandlungs Funktionen für das Debuggen

Wenn in einem Prozess, der debuggt wird, eine Ausnahme auftritt, benachrichtigt das System den Debugger, indem er die Ausnahme an ihn übergibt. Dies wird als Benachrichtigung über die *erste Chance* bezeichnet. Das System hält dann alle Threads im debuggten Prozess an.

Wenn der Debugger die Ausnahme nicht behandelt, versucht das System, einen entsprechenden Ausnahmehandler zu suchen. Wenn das System keine geeignete finden kann, benachrichtigt das System den Debugger erneut, dass eine Ausnahme aufgetreten ist. Dies wird als *Benachrichtigung der letzten Chance* bezeichnet. Wenn die Ausnahme vom Debugger nach der Benachrichtigung der letzten Chance nicht behandelt wird, beendet das System den Prozess, der debuggt wird.

Weitere Informationen finden Sie unter [Debugger-Ausnahmebehandlung](debugger-exception-handling.md).

 

 



