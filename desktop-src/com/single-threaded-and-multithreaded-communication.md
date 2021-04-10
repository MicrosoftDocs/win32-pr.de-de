---
title: Single-Threaded und Multithread-Kommunikation
description: Single-Threaded und Multithread-Kommunikation
ms.assetid: 8d3a855c-b52d-48bb-9fdf-efbf8005c374
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6470ac398e6ae1c8a645fb076fbbf509d58b579
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309692"
---
# <a name="single-threaded-and-multithreaded-communication"></a><span data-ttu-id="66081-103">Single-Threaded und Multithread-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="66081-103">Single-Threaded and Multithreaded Communication</span></span>

<span data-ttu-id="66081-104">Ein Client oder Server, der sowohl Single Thread-als auch Multithreadapartments unterstützt, verfügt über ein Multithreadapartment, das alle als frei Thread initialisierten Threads und eine oder mehrere Single Thread-Apartments enthält.</span><span class="sxs-lookup"><span data-stu-id="66081-104">A client or server that supports both single-threaded and multithreaded apartments will have one multithreaded apartment, containing all threads initialized as free-threaded, and one or more single-threaded apartments.</span></span> <span data-ttu-id="66081-105">Schnittstellen Zeiger müssen zwischen den Apartments gemarshallt werden, können aber ohne Marshalling in einem Apartment verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66081-105">Interface pointers must be marshaled between apartments but can be used without marshaling within an apartment.</span></span> <span data-ttu-id="66081-106">Aufrufe von Objekten in einem Single Thread-Apartment werden durch com synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="66081-106">Calls to objects in a single-threaded apartment will be synchronized by COM.</span></span> <span data-ttu-id="66081-107">Aufrufe von Objekten im Multithread-Apartment werden nicht durch com synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="66081-107">Calls to objects in the multithreaded apartment will not be synchronized by COM.</span></span>

<span data-ttu-id="66081-108">Alle Informationen zu Single Thread-Apartments gelten für die Threads, die als Apartment Modell gekennzeichnet sind, und alle Informationen zu multithreadwohnungen gelten für alle Threads, die als "frei Thread" gekennzeichnet sind.</span><span class="sxs-lookup"><span data-stu-id="66081-108">All of the information on single-threaded apartments applies to the threads marked as apartment model, and all of the information on multithreaded apartments applies to all of the threads marked as free-threaded.</span></span> <span data-ttu-id="66081-109">Apartment Thread Regeln gelten für die Kommunikation zwischen den Apartments und erfordern, dass Schnittstellen Zeiger zwischen Apartments mit Aufrufen von [**comarshalinterthreadinterfaceinstream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) und [**cogetinterfaceandreleasestream gemarshallt**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream)werden, wie in [Single Thread-Apartments](single-threaded-apartments.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="66081-109">Apartment threading rules apply to inter-apartment communication, requiring that interface pointers be marshaled between apartments with calls to [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) and [**CoGetInterfaceAndReleaseStream**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetinterfaceandreleasestream), as described in [Single-Threaded Apartments](single-threaded-apartments.md).</span></span>

> [!Note]  
> <span data-ttu-id="66081-110">Einige besondere Überlegungen gelten beim Umgang mit Prozess internen Servern.</span><span class="sxs-lookup"><span data-stu-id="66081-110">Some special considerations apply when dealing with in-process servers.</span></span> <span data-ttu-id="66081-111">Weitere Informationen finden Sie unter [Prozess interne Server Threading Probleme](in-process-server-threading-issues.md).</span><span class="sxs-lookup"><span data-stu-id="66081-111">For more information, see [In-Process Server Threading Issues](in-process-server-threading-issues.md).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="66081-112">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="66081-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66081-113">Zugreifen auf Schnittstellen über mehrere Apartments</span><span class="sxs-lookup"><span data-stu-id="66081-113">Accessing Interfaces Across Apartments</span></span>](accessing-interfaces-across-apartments.md)
</dt> <dt>

[<span data-ttu-id="66081-114">Auswählen des Threading Modells</span><span class="sxs-lookup"><span data-stu-id="66081-114">Choosing the Threading Model</span></span>](choosing-the-threading-model.md)
</dt> <dt>

[<span data-ttu-id="66081-115">Multithread-Apartments</span><span class="sxs-lookup"><span data-stu-id="66081-115">Multithreaded Apartments</span></span>](multithreaded-apartments.md)
</dt> <dt>

[<span data-ttu-id="66081-116">Threading Probleme im Prozess internen Server</span><span class="sxs-lookup"><span data-stu-id="66081-116">In-Process Server Threading Issues</span></span>](in-process-server-threading-issues.md)
</dt> <dt>

[<span data-ttu-id="66081-117">Prozesse, Threads und Apartments</span><span class="sxs-lookup"><span data-stu-id="66081-117">Processes, Threads, and Apartments</span></span>](processes--threads--and-apartments.md)
</dt> <dt>

[<span data-ttu-id="66081-118">Single Thread-Apartments</span><span class="sxs-lookup"><span data-stu-id="66081-118">Single-Threaded Apartments</span></span>](single-threaded-apartments.md)
</dt> </dl>

 

 




