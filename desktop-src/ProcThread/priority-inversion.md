---
description: Die Inversion der Priorität tritt auf, wenn mindestens zwei Threads mit unterschiedlichen Prioritäten zu planen sind.
ms.assetid: 1cb2f3c9-4641-40d8-892c-768abaf6affb
title: Inversion der Priorität
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79a0f4c9d57000e9e81429ee882e70dc14f63ae4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345458"
---
# <a name="priority-inversion"></a><span data-ttu-id="bcb0e-103">Inversion der Priorität</span><span class="sxs-lookup"><span data-stu-id="bcb0e-103">Priority Inversion</span></span>

<span data-ttu-id="bcb0e-104">Die Inversion der Priorität tritt auf, wenn mindestens zwei Threads mit unterschiedlichen Prioritäten zu planen sind.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-104">Priority inversion occurs when two or more threads with different priorities are in contention to be scheduled.</span></span> <span data-ttu-id="bcb0e-105">Ziehen Sie einen einfachen Fall mit drei Threads in Erwägung: Thread 1, Thread 2 und Thread 3.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-105">Consider a simple case with three threads: thread 1, thread 2, and thread 3.</span></span> <span data-ttu-id="bcb0e-106">Thread 1 hat eine hohe Priorität und ist für die Planung bereit.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-106">Thread 1 is high priority and becomes ready to be scheduled.</span></span> <span data-ttu-id="bcb0e-107">Thread 2, ein Thread mit niedriger Priorität, führt Code in einem kritischen Abschnitt aus.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-107">Thread 2, a low-priority thread, is executing code in a critical section.</span></span> <span data-ttu-id="bcb0e-108">Thread 1, der Thread mit hoher Priorität, wartet auf eine freigegebene Ressource aus Thread 2.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-108">Thread 1, the high-priority thread, begins waiting for a shared resource from thread 2.</span></span> <span data-ttu-id="bcb0e-109">Thread 3 hat mittlere Priorität.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-109">Thread 3 has medium priority.</span></span> <span data-ttu-id="bcb0e-110">Thread 3 empfängt die gesamte Prozessorzeit, da der Thread mit hoher Priorität (Thread 1) auf gemeinsame Ressourcen aus dem Thread mit niedriger Priorität (Thread 2) wartet.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-110">Thread 3 receives all the processor time, because the high-priority thread (thread 1) is waiting for shared resources from the low-priority thread (thread 2).</span></span> <span data-ttu-id="bcb0e-111">Thread 2 verlässt den kritischen Abschnitt nicht, da er nicht die höchste Priorität hat und nicht geplant wird.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-111">Thread 2 will not leave the critical section, because it does not have the highest priority and will not be scheduled.</span></span>

<span data-ttu-id="bcb0e-112">Das Zeit Planungs Modul löst dieses Problem, indem es die Priorität der geeigneten Threads (in diesem Fall die Sperren-Inhaber mit niedriger Priorität) nach dem Zufallsprinzip erhöht.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-112">The scheduler solves this problem by randomly boosting the priority of the ready threads (in this case, the low priority lock-holders).</span></span> <span data-ttu-id="bcb0e-113">Die Threads mit niedriger Priorität laufen lang genug, um den kritischen Abschnitt zu beenden, und der Thread mit hoher Priorität kann in den kritischen Abschnitt wechseln.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-113">The low priority threads run long enough to exit the critical section, and the high-priority thread can enter the critical section.</span></span> <span data-ttu-id="bcb0e-114">Wenn der Thread mit niedriger Priorität nicht genügend CPU-Zeit benötigt, um den kritischen Abschnitt zum ersten Mal zu verlassen, erhält er während der nächsten Zeitplanung eine weitere Chance.</span><span class="sxs-lookup"><span data-stu-id="bcb0e-114">If the low-priority thread does not get enough CPU time to exit the critical section the first time, it will get another chance during the next round of scheduling.</span></span>

 

 



