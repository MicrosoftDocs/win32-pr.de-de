---
description: Ein Multitasking-Betriebssystem dividiert die verfügbare Prozessorzeit für die Prozesse oder Threads, die es benötigen.
ms.assetid: ac45bef6-f078-40ac-95f4-06bd61ff46c4
title: Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d06c1d8d44f397f06923c793971bcb20f35b2b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345468"
---
# <a name="multitasking"></a><span data-ttu-id="4e359-103">Multitasking</span><span class="sxs-lookup"><span data-stu-id="4e359-103">Multitasking</span></span>

<span data-ttu-id="4e359-104">Ein Multitasking-Betriebssystem dividiert die verfügbare Prozessorzeit für die Prozesse oder Threads, die es benötigen.</span><span class="sxs-lookup"><span data-stu-id="4e359-104">A multitasking operating system divides the available processor time among the processes or threads that need it.</span></span> <span data-ttu-id="4e359-105">Das System ist für ein präemptives Multitasking konzipiert. Er ordnet jedem ausgeführten Thread einen Prozessor *Zeit Slice* zu.</span><span class="sxs-lookup"><span data-stu-id="4e359-105">The system is designed for preemptive multitasking; it allocates a processor *time slice* to each thread it executes.</span></span> <span data-ttu-id="4e359-106">Der aktuell ausgeführte Thread wird angehalten, wenn der Zeit Slice abläuft, sodass ein anderer Thread ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="4e359-106">The currently executing thread is suspended when its time slice elapses, allowing another thread to run.</span></span> <span data-ttu-id="4e359-107">Wenn das System von einem Thread zu einem anderen wechselt, speichert es den Kontext des vorzeitig entfernten Threads und stellt den gespeicherten Kontext des nächsten Threads in der Warteschlange wieder her.</span><span class="sxs-lookup"><span data-stu-id="4e359-107">When the system switches from one thread to another, it saves the context of the preempted thread and restores the saved context of the next thread in the queue.</span></span>

<span data-ttu-id="4e359-108">Die Länge des Zeitsegments hängt vom Betriebssystem und vom Prozessor ab.</span><span class="sxs-lookup"><span data-stu-id="4e359-108">The length of the time slice depends on the operating system and the processor.</span></span> <span data-ttu-id="4e359-109">Da jeder Zeit Slice klein ist (ungefähr 20 Millisekunden), scheinen mehrere Threads gleichzeitig ausgeführt zu werden.</span><span class="sxs-lookup"><span data-stu-id="4e359-109">Because each time slice is small (approximately 20 milliseconds), multiple threads appear to be executing at the same time.</span></span> <span data-ttu-id="4e359-110">Dies ist tatsächlich bei Multiprozessorsystemen der Fall, bei denen die ausführbaren Threads auf die verfügbaren Prozessoren verteilt sind.</span><span class="sxs-lookup"><span data-stu-id="4e359-110">This is actually the case on multiprocessor systems, where the executable threads are distributed among the available processors.</span></span> <span data-ttu-id="4e359-111">Sie müssen jedoch Vorsicht walten lassen, wenn Sie mehrere Threads in einer Anwendung verwenden, da sich die Systemleistung verringern kann, wenn zu viele Threads vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="4e359-111">However, you must use caution when using multiple threads in an application, because system performance can decrease if there are too many threads.</span></span>

<span data-ttu-id="4e359-112">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="4e359-112">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="4e359-113">Vorteile von Multitasking</span><span class="sxs-lookup"><span data-stu-id="4e359-113">Advantages of Multitasking</span></span>](advantages-of-multitasking.md)
-   [<span data-ttu-id="4e359-114">Verwendung von Multitasking</span><span class="sxs-lookup"><span data-stu-id="4e359-114">When to Use Multitasking</span></span>](when-to-use-multitasking.md)
-   [<span data-ttu-id="4e359-115">Überlegungen zum Multitasking</span><span class="sxs-lookup"><span data-stu-id="4e359-115">Multitasking Considerations</span></span>](multitasking-considerations.md)

 

 



