---
description: Zum Debuggen eines Prozesses, der bereits ausgeführt wird, sollte der Debugger DebugActiveProcess mit der Prozess-ID verwenden. Zum Abrufen einer Liste von Prozess bezeichgern verwenden Sie entweder die EnumProcesses-oder die Process32First-Funktion.
ms.assetid: 2662411f-a69a-442b-a177-a27ea025bb01
title: Debuggen eines laufenden Prozesses
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f93d184907bb66a651f04a5e144e40bf5955a672
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125737"
---
# <a name="debugging-a-running-process"></a>Debuggen eines laufenden Prozesses

Zum Debuggen eines Prozesses, der bereits ausgeführt wird, sollte der Debugger [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) mit der Prozess-ID verwenden. Zum Abrufen einer Liste von Prozess bezeichgern verwenden Sie entweder die [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) -oder die [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) -Funktion.

[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) fügt den Debugger an den aktiven Prozess an. In diesem Fall kann nur der aktive Prozess gedebuggt werden. die untergeordneten Prozesse sind nicht möglich. Der Debugger muss über den erforderlichen Zugriff auf den ausführenden Prozess verfügen, um **DebugActiveProcess** verwenden zu können. Weitere Informationen zu Zugriffsrechten finden Sie unter [Access Control](../secauthz/access-control.md).

Nachdem der Debugger entweder erstellt oder an den Prozess angefügt wurde, der debuggt werden soll, benachrichtigt das System den Debugger über alle Debugereignisse, die im Prozess auftreten, und, falls angegeben, in allen untergeordneten Prozessen. Weitere Informationen zum Debuggen von Ereignissen finden Sie unter [Debugging-Ereignisse](debugging-events.md).

Zum Trennen von dem Prozess, der debuggt wird, sollte der Debugger die [**debugactiveprocessstoppt**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) -Funktion verwenden.

 

 
