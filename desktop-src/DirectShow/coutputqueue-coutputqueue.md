---
description: Konstruktormethode.
ms.assetid: 672c0337-0c36-4f53-9125-d02fe8b36b1c
title: Coutputqueue. coutputqueue-Konstruktor (outputq. h)
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
ms.openlocfilehash: de4d8fe0d0a7c3dcf90e67f80a939f6294cb3d5b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361583"
---
# <a name="coutputqueuecoutputqueue-constructor"></a><span data-ttu-id="2a047-103">Coutputqueue. coutputqueue-Konstruktor</span><span class="sxs-lookup"><span data-stu-id="2a047-103">COutputQueue.COutputQueue constructor</span></span>

<span data-ttu-id="2a047-104">Konstruktormethode.</span><span class="sxs-lookup"><span data-stu-id="2a047-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a047-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a047-105">Syntax</span></span>


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



## <a name="parameters"></a><span data-ttu-id="2a047-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a047-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a047-107">*pinputpin*</span><span class="sxs-lookup"><span data-stu-id="2a047-107">*pInputPin*</span></span> 
</dt> <dd>

<span data-ttu-id="2a047-108">Ein Zeiger auf die [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) -Schnittstelle der Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="2a047-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the input pin.</span></span> <span data-ttu-id="2a047-109">Das-Objekt stellt Beispiele für diese PIN bereit.</span><span class="sxs-lookup"><span data-stu-id="2a047-109">The object will deliver samples to this pin.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-110">*PHR*</span><span class="sxs-lookup"><span data-stu-id="2a047-110">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="2a047-111">Zeiger auf einen **HRESULT** -Rückgabecode.</span><span class="sxs-lookup"><span data-stu-id="2a047-111">Pointer to an **HRESULT** return code.</span></span> <span data-ttu-id="2a047-112">Legen Sie \_ vor dem Aufrufen dieser Methode den Wert auf S OK fest.</span><span class="sxs-lookup"><span data-stu-id="2a047-112">Set the value to S\_OK before calling this method.</span></span> <span data-ttu-id="2a047-113">Bei der Rückgabe erhält *PHR* einen Wert, der angibt, ob die Methode erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="2a047-113">On return, *phr* receives a value that indicates the success or failure of the method.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-114">*Bauto*</span><span class="sxs-lookup"><span data-stu-id="2a047-114">*bAuto*</span></span> 
</dt> <dd>

<span data-ttu-id="2a047-115">Flag, das angibt, ob das Objekt entscheidet, wann eine Warteschlange erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a047-115">Flag that specifies whether the object decides when to create a queue.</span></span> <span data-ttu-id="2a047-116">**True** gibt an, dass das Objekt nur dann eine Warteschlange erstellt, wenn die Eingabe-PIN blockiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="2a047-116">If **TRUE**, the object creates a queue only if the input pin might block.</span></span> <span data-ttu-id="2a047-117">Wenn **false**, gibt der *bqueue* -Parameter an, ob eine Warteschlange erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a047-117">If **FALSE**, the *bQueue* parameter specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-118">*bqueue*</span><span class="sxs-lookup"><span data-stu-id="2a047-118">*bQueue*</span></span> 
</dt> <dd>

<span data-ttu-id="2a047-119">Wenn *Bauto* **true** ist, wird dieser Parameter ignoriert.</span><span class="sxs-lookup"><span data-stu-id="2a047-119">If *bAuto* is **TRUE**, this parameter is ignored.</span></span> <span data-ttu-id="2a047-120">Wenn *Bauto* auf **false** festgelegt ist, gibt dieses Flag an, ob eine Warteschlange erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a047-120">If *bAuto* is **FALSE**, this flag specifies whether to create a queue.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-121">*lbatchsize*</span><span class="sxs-lookup"><span data-stu-id="2a047-121">*lBatchSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2a047-122">Maximale Anzahl von Samplings, die in einem Batch geliefert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a047-122">Maximum number of samples to deliver in one batch.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-123">*bbatchexact*</span><span class="sxs-lookup"><span data-stu-id="2a047-123">*bBatchExact*</span></span> 
</dt> <dd>

<span data-ttu-id="2a047-124">Flag, das angibt, ob genaue Batch Größen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a047-124">Flag that specifies whether to use exact batch sizes.</span></span> <span data-ttu-id="2a047-125">**True** gibt an, dass das Objekt vor der Übermittlung an die eingabepin auf *lbatchsize* -Beispiele wartet.</span><span class="sxs-lookup"><span data-stu-id="2a047-125">If **TRUE**, the object waits for *lBatchSize* samples before delivering them to the input pin.</span></span> <span data-ttu-id="2a047-126">**False** gibt an, dass das-Objekt beim Empfang von Beispielen Beispiele liefert.</span><span class="sxs-lookup"><span data-stu-id="2a047-126">If **FALSE**, the object delivers samples as it receives them.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-127">*llistsize*</span><span class="sxs-lookup"><span data-stu-id="2a047-127">*lListSize*</span></span> 
</dt> <dd>

<span data-ttu-id="2a047-128">Cache Größe für die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="2a047-128">Cache size for the queue.</span></span> <span data-ttu-id="2a047-129">Der Standardwert, defaultcache, ist eine Konstante, die für die [**cbaselist**](cbaselist.md) -Klasse definiert ist.</span><span class="sxs-lookup"><span data-stu-id="2a047-129">The default value, DEFAULTCACHE, is a constant defined for the [**CBaseList**](cbaselist.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="2a047-130">*dwPriority*</span><span class="sxs-lookup"><span data-stu-id="2a047-130">*dwPriority*</span></span> 
</dt> <dd>

<span data-ttu-id="2a047-131">Priorität des Threads, der Beispiele liefert.</span><span class="sxs-lookup"><span data-stu-id="2a047-131">Priority of the thread that delivers samples.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a047-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a047-132">Remarks</span></span>

<span data-ttu-id="2a047-133">Wenn " *Bauto* " den Wert " **true**" hat, ruft das Objekt die [**IMemInputPin:: receivecanblock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) -Methode für die downstreampin auf.</span><span class="sxs-lookup"><span data-stu-id="2a047-133">If *bAuto* is **TRUE**, the object calls the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method on the downstream pin.</span></span> <span data-ttu-id="2a047-134">Wenn **receivecanblock** S OK zurückgibt \_ (was bedeutet, dass die PIN bei [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -aufrufen blockieren kann), erstellt das Objekt einen Thread zum Bereitstellung von Beispielen.</span><span class="sxs-lookup"><span data-stu-id="2a047-134">If **ReceiveCanBlock** returns S\_OK (meaning the pin might block on [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) calls), the object creates a thread for delivering samples.</span></span> <span data-ttu-id="2a047-135">Andernfalls wird kein Thread erstellt.</span><span class="sxs-lookup"><span data-stu-id="2a047-135">Otherwise, it does not create a thread.</span></span>

<span data-ttu-id="2a047-136">Wenn *Bauto* auf **false** festgelegt ist, bestimmt der Wert von *bqueue* , ob ein Thread erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="2a047-136">If *bAuto* is **FALSE**, the value of *bQueue* determines whether to create a thread.</span></span>

<span data-ttu-id="2a047-137">Wenn das Objekt einen Thread erstellt, wird das Thread Handle der [**coutputqueue:: m \_ hThread**](coutputqueue-m-hthread.md) -Element Variablen zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="2a047-137">If the object creates a thread, it assigns the thread handle to the [**COutputQueue::m\_hThread**](coutputqueue-m-hthread.md) member variable.</span></span> <span data-ttu-id="2a047-138">Die Thread Prozedur ist [**coutputqueue:: initialthread proc**](coutputqueue-initialthreadproc.md), und der Thread Parameter ist ein Zeiger auf dieses.</span><span class="sxs-lookup"><span data-stu-id="2a047-138">The thread procedure is [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md), and the thread parameter is a pointer to this.</span></span> <span data-ttu-id="2a047-139">Das-Objekt erstellt außerdem eine Warteschlange für die Aufnahme von Beispielen, die von der [**coutputqueue:: m \_ List**](coutputqueue-m-list.md) -Element Variable angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="2a047-139">The object also creates a queue for holding samples, which is given by the [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a047-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a047-140">Requirements</span></span>



| <span data-ttu-id="2a047-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a047-141">Requirement</span></span> | <span data-ttu-id="2a047-142">Wert</span><span class="sxs-lookup"><span data-stu-id="2a047-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a047-143">Header</span><span class="sxs-lookup"><span data-stu-id="2a047-143">Header</span></span><br/>  | <dl> <span data-ttu-id="2a047-144"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a047-144"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2a047-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a047-145">Library</span></span><br/> | <dl> <span data-ttu-id="2a047-146">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2a047-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a047-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a047-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a047-148">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2a047-148">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




