---
description: Hinweise zur Fehlerbehebung
ms.assetid: e87ad3bd-07ae-4b9d-b465-2ce4688bdd83
title: Hinweise zur Fehlerbehebung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c0280702c7ce2131d1252ec75b8bee4be231e29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358968"
---
# <a name="troubleshooting-tips"></a><span data-ttu-id="269a7-103">Hinweise zur Fehlerbehebung</span><span class="sxs-lookup"><span data-stu-id="269a7-103">Troubleshooting Tips</span></span>

<span data-ttu-id="269a7-104">Die folgenden Tipps helfen Ihnen, Deadlocks oder Abstürze in ihrer DirectShow-Anwendung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="269a7-104">This following tips will help you to avoid deadlocks or crashes in your DirectShow application.</span></span>

<span data-ttu-id="269a7-105">**Globale Objekte**</span><span class="sxs-lookup"><span data-stu-id="269a7-105">**Global Objects**</span></span>

<span data-ttu-id="269a7-106">Ein globales C++-Objekt sollte keine DirectShow-Objekte in seiner Konstruktormethode erstellen oder in seiner dededemethode freigeben.</span><span class="sxs-lookup"><span data-stu-id="269a7-106">A global C++ object should not create DirectShow objects in its constructor method or release them in its destructor method.</span></span> <span data-ttu-id="269a7-107">Dies kann aus folgendem Grund bewirken, dass die Anwendung unbegrenzt blockiert wird:</span><span class="sxs-lookup"><span data-stu-id="269a7-107">Doing so can cause the application to block indefinitely, for the following reason:</span></span>

<span data-ttu-id="269a7-108">Threads können nicht innerhalb einer DLL-Einstiegspunkt Funktion beendet werden.</span><span class="sxs-lookup"><span data-stu-id="269a7-108">Threads cannot exit while inside a DLL's entry-point function.</span></span> <span data-ttu-id="269a7-109">Kernel 32 enthält eine globale Prozess Sperre während der Einstiegspunkt Funktion, und die Sperre verhindert, dass der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="269a7-109">Kernel 32 holds a global process lock during the entry-point function, and the lock prevents the thread from exiting.</span></span> <span data-ttu-id="269a7-110">Da einige DirectShow-Objekte über Threads verfügen, können Sie blockieren, wenn Sie von innerhalb einer DLL-Einstiegspunkt Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="269a7-110">Because some DirectShow objects own threads, they can block if released from inside a DLL entry-point function.</span></span> <span data-ttu-id="269a7-111">Wenn eine Anwendung über ein globales C++-Objekt verfügt, ruft die C-Lauf Zeit-dll den Dekonstruktor des Objekts auf, wenn die DLL entladen wird.</span><span class="sxs-lookup"><span data-stu-id="269a7-111">If an application has a global C++ object, the C runtime DLL calls the object's destructor when the DLL is unloaded.</span></span> <span data-ttu-id="269a7-112">Wenn der Dekonstruktor DirectShow-Objekte freigibt, kann dies als Ergebnis blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="269a7-112">If the destructor releases DirectShow objects, it can block as a result.</span></span>

<span data-ttu-id="269a7-113">Aus ähnlichen Gründen sollte eine DLL DirectShow-Objekte nicht in der Einstiegspunkt Routine erstellen oder freigeben.</span><span class="sxs-lookup"><span data-stu-id="269a7-113">For similar reasons, a DLL should not create or release DirectShow objects in its entry point routine.</span></span>

<span data-ttu-id="269a7-114">**Freigeben von Schnittstellen**</span><span class="sxs-lookup"><span data-stu-id="269a7-114">**Releasing Interfaces**</span></span>

<span data-ttu-id="269a7-115">Sie sollten alle DirectShow-Schnittstellen Zeiger freigeben, während die Anwendung weiterhin Nachrichten verarbeitet, bevor die Nachrichten Schleife beendet wird.</span><span class="sxs-lookup"><span data-stu-id="269a7-115">You should release all DirectShow interface pointers while your application is still processing messages, before it exits the message loop.</span></span> <span data-ttu-id="269a7-116">Andernfalls werden möglicherweise verschiedene Bestätigungen angezeigt, da einige DirectShow-Objekte Nachrichten während ihrer Bereinigungs Routinen senden.</span><span class="sxs-lookup"><span data-stu-id="269a7-116">Otherwise, you might see various asserts, because some DirectShow objects send messages during their clean-up routines.</span></span>

<span data-ttu-id="269a7-117">(Wenn Sie die ATL **CWindowImpl** -Klasse verwenden, sollten Sie nicht warten, bis **onfinalmessage** die Schnittstellen freigibt.</span><span class="sxs-lookup"><span data-stu-id="269a7-117">(As a corollary, if you are using the ATL **CWindowImpl** class, do not wait until **OnFinalMessage** to free the interfaces.</span></span> <span data-ttu-id="269a7-118">Verwenden Sie Sie stattdessen, wenn Sie die Meldung zum Schließen der WM verarbeiten \_ .)</span><span class="sxs-lookup"><span data-stu-id="269a7-118">Instead, free them when you handle the WM\_CLOSE message.)</span></span>

<span data-ttu-id="269a7-119">**Verweis Zähler**</span><span class="sxs-lookup"><span data-stu-id="269a7-119">**Reference Counts**</span></span>

<span data-ttu-id="269a7-120">Wenn die Debugversion von Quartz.dll entladen wird, wird überprüft, ob DirectShow-Objekte über Verweis Zähler verfügen, die nicht freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="269a7-120">When the debug version of Quartz.dll unloads, it checks whether any DirectShow objects have reference counts that were not released.</span></span> <span data-ttu-id="269a7-121">Wenn dies der Fall ist, wird eine-Behauptung ausgelöst:</span><span class="sxs-lookup"><span data-stu-id="269a7-121">If so, it throws an assertion:</span></span>


```C++
g_cFGObjects == 0 
```



<span data-ttu-id="269a7-122">Wenn diese Aussage fehlschlägt, bedeutet dies, dass Ihre Anwendung einen Verweis Zähler kompromittiert hat.</span><span class="sxs-lookup"><span data-stu-id="269a7-122">When this assertion fails, it means your application has leaked a reference count.</span></span> <span data-ttu-id="269a7-123">Überprüfen Sie den Code, und stellen Sie sicher, dass alle Schnittstellen Zeiger freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="269a7-123">Review your code and make sure that you release all interface pointers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="269a7-124">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="269a7-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="269a7-125">Debuggen in DirectShow</span><span class="sxs-lookup"><span data-stu-id="269a7-125">Debugging in DirectShow</span></span>](debugging-in-directshow.md)
</dt> </dl>

 

 



