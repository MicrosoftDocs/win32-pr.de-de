---
title: Heap
description: Ein Heap verfolgt eine Gruppe von Zuordnungen, die als Einheit freigegeben werden.
ms.assetid: 3a25284a-8f15-42d4-a292-ece28a08fb69
keywords:
- Heap-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5e1651f90b8ad1afca8f85f9dd2e6f10fc7f5c3
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391259"
---
# <a name="heap"></a><span data-ttu-id="f321e-106">Heap</span><span class="sxs-lookup"><span data-stu-id="f321e-106">Heap</span></span>

<span data-ttu-id="f321e-107">Ein Heap verfolgt eine Gruppe von Zuordnungen, die als Einheit freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f321e-107">A heap tracks a group of allocations that are freed as a unit.</span></span>

<span data-ttu-id="f321e-108">Auf diese Weise können Sie komplexe Muster der Zuordnung und Freigabe von Arbeitsspeicher vermeiden, wenn Sie wwsapi verwenden.</span><span class="sxs-lookup"><span data-stu-id="f321e-108">This allows you to avoid complex patterns of allocating and deallocating memory when you use the WWSAPI.</span></span>


<span data-ttu-id="f321e-109">Jeder Nachricht ist ein Heap zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f321e-109">There is a heap associated with every message.</span></span> <span data-ttu-id="f321e-110">Wenn eine Nachricht gesendet wird, oder wenn eine Nachricht empfangen wird, wird der Heap der Nachricht für alle Zuordnungen in Bezug auf die jeweilige Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f321e-110">As a message is being sent, or as a message is being received, the heap of the message is used for any allocations relating to that particular message.</span></span> <span data-ttu-id="f321e-111">Nachdem eine Nachricht gesendet oder empfangen wurde, wird der Heap zurückgesetzt (wodurch alle Zuordnungen bereinigt werden, die mit der jeweiligen Nachricht verknüpft sind).</span><span class="sxs-lookup"><span data-stu-id="f321e-111">After a message is sent or received, the heap is reset (which cleans up any allocations related to the particular message).</span></span>

<span data-ttu-id="f321e-112">Heaps können auch verwendet werden, um Nachrichten Daten getrennt von der Lebensdauer einer Nachricht zu speichern.</span><span class="sxs-lookup"><span data-stu-id="f321e-112">Heaps can also be used to store message data separately from the lifetime of a message.</span></span> <span data-ttu-id="f321e-113">Viele der API-Zulassungs Spezifikation des Heaps, der beim Lesen von Daten verwendet werden soll, ermöglichen eine explizite Kontrolle über die Lebensdauer von gelesenen Daten.</span><span class="sxs-lookup"><span data-stu-id="f321e-113">Many of the API's allow specification of the heap to use when reading data give explicit control over the lifetime of any data read.</span></span>

<span data-ttu-id="f321e-114">Die Zuweisung von Zuordnungen aus einem Heap wird garantiert an mindestens einer 8-Byte-Grenze ausgerichtet.</span><span class="sxs-lookup"><span data-stu-id="f321e-114">Allocations from a heap are guaranteed to be aligned on at least an 8 byte boundary.</span></span>

<span data-ttu-id="f321e-115">Null-Byte Zuordnungen geben einen nicht-NULL-Zeiger zurück.</span><span class="sxs-lookup"><span data-stu-id="f321e-115">Zero byte allocations will return a non-NULL pointer.</span></span>

<span data-ttu-id="f321e-116">In Windows 7 wird ein von HeapCreate zurückgegebener Heap verwendet, um den Arbeitsspeicher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f321e-116">In Windows 7, if PageHeap is enabled, a heap returned from HeapCreate is used to manage the memory.</span></span> <span data-ttu-id="f321e-117">In diesem Fall wird " [**wsalloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) " direkt zu "heapzuzuordnungen" und " [**wsreseethap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) " zu "HeapDestroy" zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="f321e-117">In this case, [**WsAlloc**](/windows/desktop/api/WebServices/nf-webservices-wsalloc) maps directly to HeapAlloc and [**WsResetHeap**](/windows/desktop/api/WebServices/nf-webservices-wsresetheap) maps to HeapDestroy.</span></span>

<span data-ttu-id="f321e-118">Die folgende Enumeration wird mit dem Heap verwendet:</span><span class="sxs-lookup"><span data-stu-id="f321e-118">The following enumeration is used with the heap:</span></span>

-   [<span data-ttu-id="f321e-119">**WS- \_ Heap- \_ Eigenschaften- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="f321e-119">**WS\_HEAP\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_heap_property_id)

<span data-ttu-id="f321e-120">Die folgenden Funktionen werden mit dem Heap verwendet:</span><span class="sxs-lookup"><span data-stu-id="f321e-120">The following functions are used with the heap:</span></span>

-   [<span data-ttu-id="f321e-121">**Wsalloc**</span><span class="sxs-lookup"><span data-stu-id="f321e-121">**WsAlloc**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsalloc)
-   [<span data-ttu-id="f321e-122">**Wscreateheap**</span><span class="sxs-lookup"><span data-stu-id="f321e-122">**WsCreateHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wscreateheap)
-   [<span data-ttu-id="f321e-123">**Wsfreeheap**</span><span class="sxs-lookup"><span data-stu-id="f321e-123">**WsFreeHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsfreeheap)
-   [<span data-ttu-id="f321e-124">**Wsgeder approperty**</span><span class="sxs-lookup"><span data-stu-id="f321e-124">**WsGetHeapProperty**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsgetheapproperty)
-   [<span data-ttu-id="f321e-125">**Wsreabthap**</span><span class="sxs-lookup"><span data-stu-id="f321e-125">**WsResetHeap**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsresetheap)

<span data-ttu-id="f321e-126">Das folgende Handle wird mit dem Heap verwendet:</span><span class="sxs-lookup"><span data-stu-id="f321e-126">The following handle is used with the heap:</span></span>

-   [<span data-ttu-id="f321e-127">WS- \_ Heap</span><span class="sxs-lookup"><span data-stu-id="f321e-127">WS\_HEAP</span></span>](ws-heap.md)

<span data-ttu-id="f321e-128">Die folgenden Strukturen werden mit dem Heap verwendet:</span><span class="sxs-lookup"><span data-stu-id="f321e-128">The following structures are used with the heap:</span></span>

-   [<span data-ttu-id="f321e-129">**Eigenschaften von WS- \_ Heap \_**</span><span class="sxs-lookup"><span data-stu-id="f321e-129">**WS\_HEAP\_PROPERTIES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_properties)
-   [<span data-ttu-id="f321e-130">**WS- \_ Heap- \_ Eigenschaft**</span><span class="sxs-lookup"><span data-stu-id="f321e-130">**WS\_HEAP\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_heap_property)

 

 




