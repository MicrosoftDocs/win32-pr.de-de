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
# <a name="debugging-a-running-process"></a><span data-ttu-id="4b6fe-104">Debuggen eines laufenden Prozesses</span><span class="sxs-lookup"><span data-stu-id="4b6fe-104">Debugging a Running Process</span></span>

<span data-ttu-id="4b6fe-105">Zum Debuggen eines Prozesses, der bereits ausgeführt wird, sollte der Debugger [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) mit der Prozess-ID verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b6fe-105">To debug a process that is already running, the debugger should use [**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) with the process identifier.</span></span> <span data-ttu-id="4b6fe-106">Zum Abrufen einer Liste von Prozess bezeichgern verwenden Sie entweder die [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) -oder die [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="4b6fe-106">To retrieve a list of process identifiers, use either the [**EnumProcesses**](/windows/win32/api/psapi/nf-psapi-enumprocesses) or [**Process32First**](/windows/win32/api/tlhelp32/nf-tlhelp32-process32first) function.</span></span>

<span data-ttu-id="4b6fe-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) fügt den Debugger an den aktiven Prozess an.</span><span class="sxs-lookup"><span data-stu-id="4b6fe-107">[**DebugActiveProcess**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocess) attaches the debugger to the active process.</span></span> <span data-ttu-id="4b6fe-108">In diesem Fall kann nur der aktive Prozess gedebuggt werden. die untergeordneten Prozesse sind nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="4b6fe-108">In this case, only the active process can be debugged; its child processes cannot.</span></span> <span data-ttu-id="4b6fe-109">Der Debugger muss über den erforderlichen Zugriff auf den ausführenden Prozess verfügen, um **DebugActiveProcess** verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="4b6fe-109">The debugger must have appropriate access to the executing process to use **DebugActiveProcess**.</span></span> <span data-ttu-id="4b6fe-110">Weitere Informationen zu Zugriffsrechten finden Sie unter [Access Control](../secauthz/access-control.md).</span><span class="sxs-lookup"><span data-stu-id="4b6fe-110">For more information about access rights, see [Access Control](../secauthz/access-control.md).</span></span>

<span data-ttu-id="4b6fe-111">Nachdem der Debugger entweder erstellt oder an den Prozess angefügt wurde, der debuggt werden soll, benachrichtigt das System den Debugger über alle Debugereignisse, die im Prozess auftreten, und, falls angegeben, in allen untergeordneten Prozessen.</span><span class="sxs-lookup"><span data-stu-id="4b6fe-111">After the debugger has either created or attached itself to the process it intends to debug, the system notifies the debugger of all debugging events that occur in the process, and, if specified, in any child processes.</span></span> <span data-ttu-id="4b6fe-112">Weitere Informationen zum Debuggen von Ereignissen finden Sie unter [Debugging-Ereignisse](debugging-events.md).</span><span class="sxs-lookup"><span data-stu-id="4b6fe-112">For more information about debugging events, see [Debugging Events](debugging-events.md).</span></span>

<span data-ttu-id="4b6fe-113">Zum Trennen von dem Prozess, der debuggt wird, sollte der Debugger die [**debugactiveprocessstoppt**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b6fe-113">To detach from the process being debugged, the debugger should use the [**DebugActiveProcessStop**](/windows/win32/api/debugapi/nf-debugapi-debugactiveprocessstop) function.</span></span>

 

 
