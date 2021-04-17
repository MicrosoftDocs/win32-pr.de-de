---
title: Auswählen des Threading Modells
description: Auswählen des Threading Modells
ms.assetid: e8a0286d-1831-454f-8549-1957fd794809
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2f0fdcd327bf05c0019a03ad171d41c1f1d95a1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388708"
---
# <a name="choosing-the-threading-model"></a><span data-ttu-id="bb8ab-103">Auswählen des Threading Modells</span><span class="sxs-lookup"><span data-stu-id="bb8ab-103">Choosing the Threading Model</span></span>

<span data-ttu-id="bb8ab-104">Die Auswahl des Threading Modells für ein Objekt hängt von der Funktion des Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-104">Choosing the threading model for an object depends on the object's function.</span></span> <span data-ttu-id="bb8ab-105">Ein Objekt, das umfangreiche e/a-Vorgänge unterstützt, bietet möglicherweise die Möglichkeit, eine maximale Reaktion an Clients zu ermöglichen, indem Schnittstellen Aufrufe während der e/a-Latenz zugelassen werden</span><span class="sxs-lookup"><span data-stu-id="bb8ab-105">An object that does extensive I/O might support free-threading to provide maximum response to clients by allowing interface calls during I/O latency.</span></span> <span data-ttu-id="bb8ab-106">Auf der anderen Seite kann ein Objekt, das mit dem Benutzer interagiert, das Apartment Threading unterstützen, um eingehende com-Aufrufe mit seinen Fenster Vorgängen zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-106">On the other hand, an object that interacts with the user might support apartment threading to synchronize incoming COM calls with its window operations.</span></span>

<span data-ttu-id="bb8ab-107">Es ist einfacher, Apartment Threading in Single Thread-Apartments zu unterstützen, da com die Synchronisierung pro Rückruf bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-107">It is easier to support apartment threading in single-threaded apartments because COM provides synchronization on a per-call basis.</span></span> <span data-ttu-id="bb8ab-108">Das unterstützen von kostenlosem Threading ist schwieriger, da das Objekt die Synchronisierung implementieren muss. die Reaktion an Clients ist jedoch möglicherweise besser, da die Synchronisierung für kleinere Code Abschnitte implementiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="bb8ab-108">Supporting free-threading is more difficult because the object must implement synchronization; however, response to clients may be better because synchronization can be implemented for smaller sections of code.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bb8ab-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="bb8ab-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb8ab-110">Zugreifen auf Schnittstellen über mehrere Apartments</span><span class="sxs-lookup"><span data-stu-id="bb8ab-110">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="bb8ab-111">Multithread-Apartments</span><span class="sxs-lookup"><span data-stu-id="bb8ab-111">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="bb8ab-112">Threading Probleme im Prozess internen Server</span><span class="sxs-lookup"><span data-stu-id="bb8ab-112">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="bb8ab-113">Prozesse, Threads und Apartments</span><span class="sxs-lookup"><span data-stu-id="bb8ab-113">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="bb8ab-114">Single Thread-und Multithread-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="bb8ab-114">Single-Threaded and Multithreaded Communication</span></span>](single-threaded-and-multithreaded-communication.md)
</dt> <dt>

[<span data-ttu-id="bb8ab-115">Single Thread-Apartments</span><span class="sxs-lookup"><span data-stu-id="bb8ab-115">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




