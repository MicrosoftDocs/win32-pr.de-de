---
description: Die ThreadProc-Methode ruft Beispiele aus der Warteschlange ab und übergibt sie an die eingabepin.
ms.assetid: e5da0a12-c722-4d08-bf84-5e3aa60b64a9
title: Coutputqueue. ThreadProc-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 75e2e6bd7fa05480603f30e68eeaf0487918ae7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367447"
---
# <a name="coutputqueuethreadproc-method"></a><span data-ttu-id="59744-103">Coutputqueue. ThreadProc-Methode</span><span class="sxs-lookup"><span data-stu-id="59744-103">COutputQueue.ThreadProc method</span></span>

<span data-ttu-id="59744-104">Die `ThreadProc` -Methode ruft Beispiele aus der Warteschlange ab und übergibt sie an die eingabepin.</span><span class="sxs-lookup"><span data-stu-id="59744-104">The `ThreadProc` method retrieves samples from the queue and delivers them to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="59744-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="59744-105">Syntax</span></span>


```C++
DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="59744-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="59744-106">Parameters</span></span>

<span data-ttu-id="59744-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="59744-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="59744-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="59744-108">Return value</span></span>

<span data-ttu-id="59744-109">Gibt 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="59744-109">Returns zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="59744-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="59744-110">Remarks</span></span>

<span data-ttu-id="59744-111">Die [**coutputqueue:: initialthread proc**](coutputqueue-initialthreadproc.md) -Methode ruft diese Methode auf, die die Haupt Thread Schleife implementiert.</span><span class="sxs-lookup"><span data-stu-id="59744-111">The [**COutputQueue::InitialThreadProc**](coutputqueue-initialthreadproc.md) method calls this method, which implements the main thread loop.</span></span> <span data-ttu-id="59744-112">Innerhalb der-Schleife führt die-Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="59744-112">Within the loop, the method performs the following steps:</span></span>

1.  <span data-ttu-id="59744-113">Ruft ein Beispiel für die Warteschlange ab.</span><span class="sxs-lookup"><span data-stu-id="59744-113">Retrieves a sample for the queue.</span></span>
2.  <span data-ttu-id="59744-114">Wenn das Beispiel eine Kontroll Meldung ist, führt der Thread die Steuerungs Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="59744-114">If the sample is a control message, the thread executes the control action.</span></span> <span data-ttu-id="59744-115">Andernfalls wird das Beispiel im [**coutputqueue:: m \_ ppsamples**](coutputqueue-m-ppsamples.md) -Array platziert.</span><span class="sxs-lookup"><span data-stu-id="59744-115">Otherwise, it places the sample into the [**COutputQueue::m\_ppSamples**](coutputqueue-m-ppsamples.md) array.</span></span>
3.  <span data-ttu-id="59744-116">Wenn das Array voll ist (oder wenn [**coutputqueue:: m \_ bbatchexact**](coutputqueue-m-bbatchexact.md) den Wert **false** hat), ruft der Thread die [**IMemInputPin:: receivemultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) -Methode auf, um die Beispiele zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="59744-116">When the array is full (or if [**COutputQueue::m\_bBatchExact**](coutputqueue-m-bbatchexact.md) is **FALSE**), the thread calls the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method to deliver the samples.</span></span>
4.  <span data-ttu-id="59744-117">Wenn keine Beispiele in die Warteschlange eingereiht werden, wartet der Thread auf [**coutputqueue:: m \_ hsem**](coutputqueue-m-hsem.md) Semaphore.</span><span class="sxs-lookup"><span data-stu-id="59744-117">If no samples are queued, the thread waits on the [**COutputQueue::m\_hSem**](coutputqueue-m-hsem.md) semaphore.</span></span>

<span data-ttu-id="59744-118">Der Thread wird beendet, wenn die " [**coutputqueue \_ :: m**](coutputqueue-m-bterminate.md) "-Member-Variable " **true**" lautet.</span><span class="sxs-lookup"><span data-stu-id="59744-118">The thread terminates when the [**COutputQueue::m\_bTerminate**](coutputqueue-m-bterminate.md) member variable becomes **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="59744-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="59744-119">Requirements</span></span>



| <span data-ttu-id="59744-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="59744-120">Requirement</span></span> | <span data-ttu-id="59744-121">Wert</span><span class="sxs-lookup"><span data-stu-id="59744-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59744-122">Header</span><span class="sxs-lookup"><span data-stu-id="59744-122">Header</span></span><br/>  | <dl> <span data-ttu-id="59744-123"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="59744-123"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="59744-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="59744-124">Library</span></span><br/> | <dl> <span data-ttu-id="59744-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="59744-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59744-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="59744-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59744-127">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="59744-127">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




