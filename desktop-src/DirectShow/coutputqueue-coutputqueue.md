---
description: 'COutputQueue.COutputQueue-Konstruktor : Konstruktormethode.'
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: COutputQueue.COutputQueue-Konstruktor (Outputq.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.COutputQueue
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 17a795bf4ec33ec904b83f6621fc0bc4f43b4b15
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095328"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="b0f54-103">COutputQueue.COutputQueue-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="b0f54-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="b0f54-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="b0f54-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0f54-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b0f54-105">Syntax</span></span>


```C++
COutputQueue(
   IPin    *pInputPin,
   HRESULT *phr,
   BOOL    bAuto = TRUE,
   BOOL    bQueue = TRUE,
   LONG    lBatchSize = 1,
   BOOL    bBatchExact = FALSE,
   LONG    lListSize = DEFAULTCACHE,
   DWORD   dwPriority = THREAD_PRIORITY_NORMAL
);
```



## <a name="parameters"></a><span data-ttu-id="b0f54-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0f54-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0f54-107">*pInputPin*</span><span class="sxs-lookup"><span data-stu-id="b0f54-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f54-108">Zeiger auf die [**IPin-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ipin) des Eingabepins.</span><span class="sxs-lookup"><span data-stu-id="b0f54-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="b0f54-109">Das -Objekt liefert Beispiele an diesen Pin.</span><span class="sxs-lookup"><span data-stu-id="b0f54-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="b0f54-110">*Phr*</span><span class="sxs-lookup"><span data-stu-id="b0f54-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f54-111">Zeiger auf einen **HRESULT-Rückgabecode.**</span><span class="sxs-lookup"><span data-stu-id="b0f54-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="b0f54-112">Legen Sie den Wert auf S \_ OK fest, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b0f54-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="b0f54-113">Bei der Rückgabe *empfängt phr* einen Wert, der den Erfolg oder Fehler der Methode angibt.</span><span class="sxs-lookup"><span data-stu-id="b0f54-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="b0f54-114">*bAuto*</span><span class="sxs-lookup"><span data-stu-id="b0f54-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f54-115">Flag, das angibt, ob das Objekt entscheidet, wann eine Warteschlange erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0f54-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="b0f54-116">True **gibt an,** dass das -Objekt nur dann eine Warteschlange erstellt, wenn der Eingabepin blockiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b0f54-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="b0f54-117">False **gibt** mit dem *Parameter bQueue* an, ob eine Warteschlange erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0f54-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="b0f54-118">*bQueue*</span><span class="sxs-lookup"><span data-stu-id="b0f54-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f54-119">Wenn *bAuto* **true ist,** wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b0f54-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="b0f54-120">Wenn *bAuto* **FALSE ist,** gibt dieses Flag an, ob eine Warteschlange erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0f54-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="b0f54-121">*lBatchSize*</span><span class="sxs-lookup"><span data-stu-id="b0f54-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f54-122">Maximale Anzahl von Stichproben, die in einem Batch zu liefern sind.</span><span class="sxs-lookup"><span data-stu-id="b0f54-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="b0f54-123">*bBatchExact*</span><span class="sxs-lookup"><span data-stu-id="b0f54-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f54-124">Flag, das angibt, ob genaue Batchgrößen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0f54-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="b0f54-125">True **gibt an,** dass das Objekt auf *lBatchSize-Stichproben* wartet, bevor sie an den Eingabepin zu liefern sind.</span><span class="sxs-lookup"><span data-stu-id="b0f54-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="b0f54-126">False **gibt an,** dass das Objekt Stichproben liefert, während es sie empfängt.</span><span class="sxs-lookup"><span data-stu-id="b0f54-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="b0f54-127">*lListSize*</span><span class="sxs-lookup"><span data-stu-id="b0f54-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f54-128">Cachegröße für die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="b0f54-128">Cache size for the queue.</span></span> <span data-ttu-id="b0f54-129">Der Standardwert DEFAULTCACHE ist eine Konstante, die für die [**CBaseList-Klasse definiert**](cbaselist.md) ist.</span><span class="sxs-lookup"><span data-stu-id="b0f54-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="b0f54-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="b0f54-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="b0f54-131">Priorität des Threads, der Beispiele liefert.</span><span class="sxs-lookup"><span data-stu-id="b0f54-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b0f54-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b0f54-132">Remarks</span></span>

<span data-ttu-id="b0f54-133">Wenn *bAuto* **true ist,** ruft das Objekt die [**IMemInputPin::ReceiveCanBlock-Methode**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) auf dem Downstreampin auf.</span><span class="sxs-lookup"><span data-stu-id="b0f54-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="b0f54-134">Wenn **ReceiveCanBlock** S OK zurückgibt (d. h., der Pin könnte bei \_ [**IMemInputPin::Receive-Aufrufen**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) blockiert werden), erstellt das Objekt einen Thread für die Bereitstellung von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="b0f54-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="b0f54-135">Andernfalls wird kein Thread erstellt.</span><span class="sxs-lookup"><span data-stu-id="b0f54-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="b0f54-136">Wenn *bAuto* **FALSE ist,** bestimmt der Wert *von bQueue,* ob ein Thread erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b0f54-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="b0f54-137">Wenn das -Objekt einen Thread erstellt, wird das Threadhandles der [**Membervariablen COutputQueue::m \_ hThread**](coutputqueue-m-hthread.md) zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="b0f54-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="b0f54-138">Die Threadprozedur [**ist COutputQueue::InitialThreadProc,**](coutputqueue-initialthreadproc.md)und der Threadparameter ist ein Zeiger darauf.</span><span class="sxs-lookup"><span data-stu-id="b0f54-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="b0f54-139">Das -Objekt erstellt auch eine Warteschlange zum Enthalten von Stichproben, die von der [**Membervariablen COutputQueue::m \_ List**](coutputqueue-m-list.md) angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="b0f54-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0f54-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0f54-140">Requirements</span></span>



| <span data-ttu-id="b0f54-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b0f54-141">Requirement</span></span> | <span data-ttu-id="b0f54-142">Wert</span><span class="sxs-lookup"><span data-stu-id="b0f54-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f54-143">Header</span><span class="sxs-lookup"><span data-stu-id="b0f54-143">Header</span></span><br/>  | <dl> <span data-ttu-id="b0f54-144"><dt>Outputq.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="b0f54-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b0f54-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b0f54-145">Library</span></span><br/> | <dl> <span data-ttu-id="b0f54-146"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b0f54-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f54-147">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b0f54-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f54-148">**COutputQueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b0f54-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




