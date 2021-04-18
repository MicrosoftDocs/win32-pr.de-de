---
description: Streamingthreads und der Filter Graph-Manager
ms.assetid: b490b72a-ab34-46e6-8dc6-a7bb07cfc7b1
title: Streamingthreads und der Filter Graph-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a8c5b8fa972a8118563ae8f9e73d480ac15e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359159"
---
# <a name="streaming-threads-and-the-filter-graph-manager"></a><span data-ttu-id="d38ce-103">Streamingthreads und der Filter Graph-Manager</span><span class="sxs-lookup"><span data-stu-id="d38ce-103">Streaming Threads and the Filter Graph Manager</span></span>

<span data-ttu-id="d38ce-104">Wenn der Filter Graph-Manager das Diagramm stoppt, wartet es, bis alle streamingthreads heruntergefahren sind.</span><span class="sxs-lookup"><span data-stu-id="d38ce-104">When the Filter Graph Manager stops the graph, it waits for all streaming threads to shut down.</span></span> <span data-ttu-id="d38ce-105">Dies hat folgende Auswirkungen auf Filter:</span><span class="sxs-lookup"><span data-stu-id="d38ce-105">This has the following implications for filters:</span></span>

-   <span data-ttu-id="d38ce-106">Ein Filter darf nie Methoden für den Filter Graph-Manager aus einem streamingthread aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d38ce-106">A filter must never call methods on the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="d38ce-107">Der Filter Graph-Manager verwendet einen kritischen Abschnitt, um seine eigenen Vorgänge zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="d38ce-107">The Filter Graph Manager uses a critical section to synchronize its own operations.</span></span> <span data-ttu-id="d38ce-108">Wenn ein streamingingthread versucht, diesen kritischen Abschnitt aufzunehmen, kann dies zu einem Deadlock führen.</span><span class="sxs-lookup"><span data-stu-id="d38ce-108">If a streaming thread tries to hold this critical section, it can cause a deadlock.</span></span> <span data-ttu-id="d38ce-109">Beispiel: angenommen, ein anderer Thread hält das Diagramm an.</span><span class="sxs-lookup"><span data-stu-id="d38ce-109">For example: Suppose that another thread stops the graph.</span></span> <span data-ttu-id="d38ce-110">Dieser Thread nimmt die Filter Diagramm Sperre an und wartet darauf, dass der Filter keine Daten mehr bereit liefert.</span><span class="sxs-lookup"><span data-stu-id="d38ce-110">That thread takes the filter graph lock and waits for your filter to stop delivering data.</span></span> <span data-ttu-id="d38ce-111">Wenn der Filter auf die Sperre wartet, wird er nie beendet, was zu einem Deadlock führt.</span><span class="sxs-lookup"><span data-stu-id="d38ce-111">If your filter is waiting for the lock, it will never stop, causing a deadlock.</span></span>

-   <span data-ttu-id="d38ce-112">Ein Filter muss niemals den Filter Graph-Manager aus einem streamingthread **adressieren** oder **QueryInterface** .</span><span class="sxs-lookup"><span data-stu-id="d38ce-112">A filter must never **AddRef** or **QueryInterface** the Filter Graph Manager from a streaming thread.</span></span>

    <span data-ttu-id="d38ce-113">Wenn der Filter einen Verweis Zähler für den Filter-Graph-Manager (über **adressf** oder **QueryInterface**) enthält, kann er zum letzten Objekt werden, das einen Verweis Zähler enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="d38ce-113">If the filter holds a reference count on the Filter Graph Manager (through **AddRef** or **QueryInterface**), it might become the last object to hold a reference count.</span></span> <span data-ttu-id="d38ce-114">Wenn der Filter die **Freigabe** aufruft, zerstört der Filter Graph-Manager sich selbst.</span><span class="sxs-lookup"><span data-stu-id="d38ce-114">When the filter calls **Release**, the Filter Graph Manager destroys itself.</span></span> <span data-ttu-id="d38ce-115">Innerhalb der Bereinigungs Routine versucht der Filter Graph-Manager, das Diagramm zu beenden, sodass es darauf wartet, dass der streamingthread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d38ce-115">Inside its cleanup routine, the Filter Graph Manager attempts to stop the graph, causing it to wait for the streaming thread to exit.</span></span> <span data-ttu-id="d38ce-116">Er wartet jedoch innerhalb des streamingthreads, sodass der streamingthread nicht beendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d38ce-116">However, it is waiting inside the streaming thread, so the streaming thread cannot exit.</span></span> <span data-ttu-id="d38ce-117">Das Ergebnis ist ein Deadlock.</span><span class="sxs-lookup"><span data-stu-id="d38ce-117">The result is a deadlock.</span></span>

 

 



