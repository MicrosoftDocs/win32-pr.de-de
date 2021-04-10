---
Description: Im folgenden finden Sie einen kurzen Vergleich der verschiedenen Speicher Belegungs Methoden.
ms.assetid: b6101014-02d2-4b19-aec6-8772a2793d38
title: Vergleichen von Speicher Belegungs Methoden
ms.topic: reference
ms.custom: snippet-project
ms.date: 05/31/2018
ms.openlocfilehash: 541b314c4ff0553ff8812e591c47c87962866bbe
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "103961535"
---
# <a name="comparing-memory-allocation-methods"></a><span data-ttu-id="7a1b3-103">Vergleichen von Speicher Belegungs Methoden</span><span class="sxs-lookup"><span data-stu-id="7a1b3-103">Comparing Memory Allocation Methods</span></span>

<span data-ttu-id="7a1b3-104">Im folgenden finden Sie einen kurzen Vergleich der verschiedenen Speicher Belegungs Methoden:</span><span class="sxs-lookup"><span data-stu-id="7a1b3-104">The following is a brief comparison of the various memory allocation methods:</span></span>

-   [<span data-ttu-id="7a1b3-105">**CoTaskMemAlloc**</span><span class="sxs-lookup"><span data-stu-id="7a1b3-105">**CoTaskMemAlloc**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc)
-   [<span data-ttu-id="7a1b3-106">**GlobalAlloc**</span><span class="sxs-lookup"><span data-stu-id="7a1b3-106">**GlobalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-globalalloc)
-   [<span data-ttu-id="7a1b3-107">**Heapzuweisung**</span><span class="sxs-lookup"><span data-stu-id="7a1b3-107">**HeapAlloc**</span></span>](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc)
-   [<span data-ttu-id="7a1b3-108">**Localzuweisung**</span><span class="sxs-lookup"><span data-stu-id="7a1b3-108">**LocalAlloc**</span></span>](/windows/desktop/api/WinBase/nf-winbase-localalloc)
-   <span data-ttu-id="7a1b3-109">**malloc**</span><span class="sxs-lookup"><span data-stu-id="7a1b3-109">**malloc**</span></span>
-   <span data-ttu-id="7a1b3-110">**new**</span><span class="sxs-lookup"><span data-stu-id="7a1b3-110">**new**</span></span>
-   [<span data-ttu-id="7a1b3-111">**VirtualAlloc**</span><span class="sxs-lookup"><span data-stu-id="7a1b3-111">**VirtualAlloc**</span></span>](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc)

<span data-ttu-id="7a1b3-112">Obwohl die Funktionen [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc)und [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) letztendlich Arbeitsspeicher aus demselben Heap zuweisen, bietet jede Funktion einen etwas anderen Funktions Satz.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-112">Although the [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc), [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc), and [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) functions ultimately allocate memory from the same heap, each provides a slightly different set of functionality.</span></span> <span data-ttu-id="7a1b3-113">**Heapbelegc** kann z. b. angewiesen werden, eine Ausnahme zuzuweisen, wenn der Arbeitsspeicher nicht reserviert werden konnte, eine Funktion, die nicht mit **localbelegc** verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-113">For example, **HeapAlloc** can be instructed to raise an exception if memory could not be allocated, a capability not available with **LocalAlloc**.</span></span> <span data-ttu-id="7a1b3-114">**LocalAlloc** unterstützt die Zuordnung von Handles, die es ermöglichen, dass der zugrunde liegende Speicher durch eine erneute Zuordnung verschoben wird, ohne den Handle-Wert zu ändern. eine Funktion, die mit **HeapAlloc** nicht verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="7a1b3-114">**LocalAlloc** supports allocation of handles which permit the underlying memory to be moved by a reallocation without changing the handle value, a capability not available with **HeapAlloc**.</span></span>

<span data-ttu-id="7a1b3-115">Beginnend mit 32-Bit-Fenstern werden [**Globalzuweisung**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) und [**localzuweisung**](/windows/desktop/api/WinBase/nf-winbase-localalloc) als Wrapper Funktionen implementiert, die [**Heapzuweisung**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) mithilfe eines Handles für den Standard Heap des Prozesses aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-115">Starting with 32-bit Windows, [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) and [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) are implemented as wrapper functions that call [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) using a handle to the process's default heap.</span></span> <span data-ttu-id="7a1b3-116">Daher haben **Globalzuweisung** und **localzuweisung** mehr Aufwand als **Heapzuweisung**.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-116">Therefore, **GlobalAlloc** and **LocalAlloc** have greater overhead than **HeapAlloc**.</span></span>

<span data-ttu-id="7a1b3-117">Da die verschiedenen Heap Zuordnungen mithilfe verschiedener Mechanismen eine besondere Funktionalität bereitstellen, müssen Sie Arbeitsspeicher mit der richtigen Funktion freigeben.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-117">Because the different heap allocators provide distinctive functionality by using different mechanisms, you must free memory with the correct function.</span></span> <span data-ttu-id="7a1b3-118">Beispielsweise muss der mit [**heapbelegc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) zugeordnete Arbeitsspeicher mit [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) , nicht [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) oder [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree)freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-118">For example, memory allocated with [**HeapAlloc**](/windows/desktop/api/HeapApi/nf-heapapi-heapalloc) must be freed with [**HeapFree**](/windows/desktop/api/HeapApi/nf-heapapi-heapfree) and not [**LocalFree**](/windows/desktop/api/WinBase/nf-winbase-localfree) or [**GlobalFree**](/windows/desktop/api/WinBase/nf-winbase-globalfree).</span></span> <span data-ttu-id="7a1b3-119">Der mit [**globalzuordnungs**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) -oder [**localzugewiesenc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) zugeordnete Arbeitsspeicher muss abgefragt, überprüft und mit der entsprechenden globalen oder lokalen Funktion freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-119">Memory allocated with [**GlobalAlloc**](/windows/desktop/api/WinBase/nf-winbase-globalalloc) or [**LocalAlloc**](/windows/desktop/api/WinBase/nf-winbase-localalloc) must be queried, validated, and released with the corresponding global or local function.</span></span>

<span data-ttu-id="7a1b3-120">Mit der [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) -Funktion können Sie zusätzliche Optionen für die Speicher Belegung angeben.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-120">The [**VirtualAlloc**](/windows/win32/api/memoryapi/nf-memoryapi-virtualalloc) function allows you to specify additional options for memory allocation.</span></span> <span data-ttu-id="7a1b3-121">Die Zuordnungen verwenden jedoch eine Seiten Granularität, sodass die Verwendung von **VirtualAlloc** zu einer höheren Speicherauslastung führen kann.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-121">However, its allocations use a page granularity, so using **VirtualAlloc** can result in higher memory usage.</span></span>

<span data-ttu-id="7a1b3-122">Die **malloc** -Funktion hat den Nachteil, dass Sie von der Laufzeit abhängig ist.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-122">The **malloc** function has the disadvantage of being run-time dependent.</span></span> <span data-ttu-id="7a1b3-123">Der **New** -Operator hat den Nachteil, dass der Compiler abhängig ist und sprachabhängig ist.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-123">The **new** operator has the disadvantage of being compiler dependent and language dependent.</span></span>

<span data-ttu-id="7a1b3-124">Die Funktion " [**cotaskmemzuweisung**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) " hat den Vorteil, dass Sie in C, C++ oder Visual Basic gut funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-124">The [**CoTaskMemAlloc**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemalloc) function has the advantage of working well in either C, C++, or Visual Basic.</span></span> <span data-ttu-id="7a1b3-125">Es ist auch die einzige Möglichkeit, Arbeitsspeicher in einer COM-basierten Anwendung freizugeben, da in der Mitte **cotaskmembelegc** und [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) verwendet werden, um Speicher zu Mars Hallen.</span><span class="sxs-lookup"><span data-stu-id="7a1b3-125">It is also the only way to share memory in a COM-based application, since MIDL uses **CoTaskMemAlloc** and [**CoTaskMemFree**](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) to marshal memory.</span></span>


## <a name="examples"></a><span data-ttu-id="7a1b3-126">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a1b3-126">Examples</span></span>

* [<span data-ttu-id="7a1b3-127">Reservieren und Commit des Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="7a1b3-127">Reserving and Committing Memory</span></span>](./reserving-and-committing-memory.md)

* [<span data-ttu-id="7a1b3-128">AWE-Beispiel</span><span class="sxs-lookup"><span data-stu-id="7a1b3-128">AWE Example</span></span>](./awe-example.md)

## <a name="related-topics"></a><span data-ttu-id="7a1b3-129">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7a1b3-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7a1b3-130">Globale und lokale Funktionen</span><span class="sxs-lookup"><span data-stu-id="7a1b3-130">Global and Local Functions</span></span>](global-and-local-functions.md)
</dt> <dt>

[<span data-ttu-id="7a1b3-131">Heap Funktionen</span><span class="sxs-lookup"><span data-stu-id="7a1b3-131">Heap Functions</span></span>](heap-functions.md)
</dt> <dt>

[<span data-ttu-id="7a1b3-132">Funktionen des virtuellen Arbeitsspeichers</span><span class="sxs-lookup"><span data-stu-id="7a1b3-132">Virtual Memory Functions</span></span>](virtual-memory-functions.md)
</dt> </dl>

 

 