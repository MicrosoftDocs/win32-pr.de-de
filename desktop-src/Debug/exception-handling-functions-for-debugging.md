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
# <a name="exception-handling-functions-for-debugging"></a><span data-ttu-id="1a108-105">Ausnahme Behandlungs Funktionen für das Debuggen</span><span class="sxs-lookup"><span data-stu-id="1a108-105">Exception Handling Functions for Debugging</span></span>

<span data-ttu-id="1a108-106">Wenn in einem Prozess, der debuggt wird, eine Ausnahme auftritt, benachrichtigt das System den Debugger, indem er die Ausnahme an ihn übergibt.</span><span class="sxs-lookup"><span data-stu-id="1a108-106">When an exception occurs in a process that is being debugged, the system notifies the debugger by passing the exception to it.</span></span> <span data-ttu-id="1a108-107">Dies wird als Benachrichtigung über die *erste Chance* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1a108-107">This is known as *first-chance notification*.</span></span> <span data-ttu-id="1a108-108">Das System hält dann alle Threads im debuggten Prozess an.</span><span class="sxs-lookup"><span data-stu-id="1a108-108">The system then suspends all threads in the process being debugged.</span></span>

<span data-ttu-id="1a108-109">Wenn der Debugger die Ausnahme nicht behandelt, versucht das System, einen entsprechenden Ausnahmehandler zu suchen.</span><span class="sxs-lookup"><span data-stu-id="1a108-109">If the debugger does not handle the exception, the system attempts to locate an appropriate exception handler.</span></span> <span data-ttu-id="1a108-110">Wenn das System keine geeignete finden kann, benachrichtigt das System den Debugger erneut, dass eine Ausnahme aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="1a108-110">If the system cannot locate an appropriate one, the system again notifies the debugger that an exception has occurred.</span></span> <span data-ttu-id="1a108-111">Dies wird als *Benachrichtigung der letzten Chance* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1a108-111">This is known as *last-chance notification*.</span></span> <span data-ttu-id="1a108-112">Wenn die Ausnahme vom Debugger nach der Benachrichtigung der letzten Chance nicht behandelt wird, beendet das System den Prozess, der debuggt wird.</span><span class="sxs-lookup"><span data-stu-id="1a108-112">If the debugger does not handle the exception after the last-chance notification, the system terminates the process being debugged.</span></span>

<span data-ttu-id="1a108-113">Weitere Informationen finden Sie unter [Debugger-Ausnahmebehandlung](debugger-exception-handling.md).</span><span class="sxs-lookup"><span data-stu-id="1a108-113">For more information, see [Debugger Exception Handling](debugger-exception-handling.md).</span></span>

 

 



