---
description: Die cqueue-Klassen Vorlage implementiert eine einfache, statisch formatierte Warteschlange.
ms.assetid: 5a4f0bcf-24ed-427d-898d-f3ddc6a35b59
title: Cqueue-Klasse (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ceef0d29e0f6f06c30355a47e3274495f17dceb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359715"
---
# <a name="cqueue-class"></a><span data-ttu-id="b51ef-103">Cqueue-Klasse</span><span class="sxs-lookup"><span data-stu-id="b51ef-103">CQueue class</span></span>

<span data-ttu-id="b51ef-104">Die **cqueue** -Klassen Vorlage implementiert eine einfache, statisch formatierte Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="b51ef-104">The **CQueue** class template implements a simple, statically sized queue.</span></span>



| <span data-ttu-id="b51ef-105">Öffentliche Methoden</span><span class="sxs-lookup"><span data-stu-id="b51ef-105">Public Methods</span></span>                                  | <span data-ttu-id="b51ef-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b51ef-106">Description</span></span>                             |
|-------------------------------------------------|-----------------------------------------|
| [<span data-ttu-id="b51ef-107">**Cqueue**</span><span class="sxs-lookup"><span data-stu-id="b51ef-107">**CQueue**</span></span>](cqueue-cqueue.md)                 | <span data-ttu-id="b51ef-108">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="b51ef-108">Constructor method.</span></span>                     |
| [<span data-ttu-id="b51ef-109">**~ Cqueue**</span><span class="sxs-lookup"><span data-stu-id="b51ef-109">**~CQueue**</span></span>](cqueue--cqueue.md)               | <span data-ttu-id="b51ef-110">Dekonstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="b51ef-110">Destructor method.</span></span>                      |
| [<span data-ttu-id="b51ef-111">**Getqueueobject**</span><span class="sxs-lookup"><span data-stu-id="b51ef-111">**GetQueueObject**</span></span>](cqueue-getqueueobject.md) | <span data-ttu-id="b51ef-112">Ruft das nächste Element aus der Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="b51ef-112">Retrieves the next item from the queue.</span></span> |
| [<span data-ttu-id="b51ef-113">**Putqueueobject**</span><span class="sxs-lookup"><span data-stu-id="b51ef-113">**PutQueueObject**</span></span>](cqueue-putqueueobject.md) | <span data-ttu-id="b51ef-114">Fügt ein Element in die Warteschlange ein.</span><span class="sxs-lookup"><span data-stu-id="b51ef-114">Puts an item onto the queue.</span></span>            |



 

## <a name="remarks"></a><span data-ttu-id="b51ef-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b51ef-115">Remarks</span></span>

<span data-ttu-id="b51ef-116">Der Klassenkonstruktor gibt die Größe der Warteschlange an.</span><span class="sxs-lookup"><span data-stu-id="b51ef-116">The class constructor specifies the size of the queue.</span></span> <span data-ttu-id="b51ef-117">Verwenden Sie das [**cqueue::P utqueueobject**](cqueue-putqueueobject.md) , um ein Element in die Warteschlange zu versetzen, und die [**cqueue:: getqueueobject**](cqueue-getqueueobject.md) -Methode, um ein Element aus der Warteschlange zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="b51ef-117">Use the [**CQueue::PutQueueObject**](cqueue-putqueueobject.md) to put an item on the queue, and the [**CQueue::GetQueueObject**](cqueue-getqueueobject.md) method to dequeues an item.</span></span> <span data-ttu-id="b51ef-118">Wenn die Warteschlange voll ist, wird die **putqueueobject** -Methode blockiert, bis ein Element aus der Warteschlange entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b51ef-118">If the queue is full, the **PutQueueObject** method blocks until an item is dequeued.</span></span> <span data-ttu-id="b51ef-119">Wenn die Warteschlange leer ist, wird **getqueueobject** blockiert, bis ein Element in die Warteschlange eingereiht wird.</span><span class="sxs-lookup"><span data-stu-id="b51ef-119">If the queue is empty, the **GetQueueObject** blocks until an item is queued.</span></span> <span data-ttu-id="b51ef-120">Der Template-Parameter gibt den Typ des Elements an.</span><span class="sxs-lookup"><span data-stu-id="b51ef-120">The template parameter specifies the type of item.</span></span> <span data-ttu-id="b51ef-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b51ef-121">For example:</span></span>


```
CQueue<int> number_queue;
number_queue.PutQueueObject(7);
```



<span data-ttu-id="b51ef-122">Die-Klasse verwendet zwei Semaphor zum Steuern von Warteschlangen Vorgängen, eine "Get"-Semaphor und eine "Put"-Semaphor.</span><span class="sxs-lookup"><span data-stu-id="b51ef-122">The class uses two semaphores to control queuing operations, a "get" semaphore and a "put" semaphore.</span></span> <span data-ttu-id="b51ef-123">Die [**getqueueobject**](cqueue-getqueueobject.md) -Methode wartet auf das "Get"-Semaphor (mit der **WaitForSingleObject** -Funktion) und gibt das "Put"-Semaphor frei (mit der **ReleaseSemaphore** -Funktion).</span><span class="sxs-lookup"><span data-stu-id="b51ef-123">The [**GetQueueObject**](cqueue-getqueueobject.md) method waits on the "get" semaphore (using the **WaitForSingleObject** function) and releases the "put" semaphore (using the **ReleaseSemaphore** function).</span></span> <span data-ttu-id="b51ef-124">Die [**putqueueobject**](cqueue-putqueueobject.md) -Methode wartet auf das "Put"-Semaphor und gibt das "Get"-Semaphor frei.</span><span class="sxs-lookup"><span data-stu-id="b51ef-124">The [**PutQueueObject**](cqueue-putqueueobject.md) method waits on the "put" semaphore and releases the "get" semaphore.</span></span> <span data-ttu-id="b51ef-125">Die-Klasse verwendet einen kritischen Abschnitt, um Warteschlangen Vorgänge zwischen mehreren Threads zu serialisieren.</span><span class="sxs-lookup"><span data-stu-id="b51ef-125">The class uses a critical section to serialize queuing operations among multiple threads.</span></span>

## <a name="requirements"></a><span data-ttu-id="b51ef-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b51ef-126">Requirements</span></span>



| <span data-ttu-id="b51ef-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b51ef-127">Requirement</span></span> | <span data-ttu-id="b51ef-128">Wert</span><span class="sxs-lookup"><span data-stu-id="b51ef-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b51ef-129">Header</span><span class="sxs-lookup"><span data-stu-id="b51ef-129">Header</span></span><br/>  | <dl> <span data-ttu-id="b51ef-130"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b51ef-130"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b51ef-131">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b51ef-131">Library</span></span><br/> | <dl> <span data-ttu-id="b51ef-132">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b51ef-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




