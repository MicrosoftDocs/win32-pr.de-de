---
description: Die endflush-Methode beendet einen Löschvorgang.
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: Coutputqueue. endflush-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e18afec866176147c5c75a57fca522c4ebc5fcf6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359663"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="79a0b-103">Coutputqueue. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="79a0b-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="79a0b-104">Die- `EndFlush` Methode beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="79a0b-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="79a0b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="79a0b-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="79a0b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="79a0b-106">Parameters</span></span>

<span data-ttu-id="79a0b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="79a0b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="79a0b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="79a0b-108">Return value</span></span>

<span data-ttu-id="79a0b-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="79a0b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="79a0b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79a0b-110">Remarks</span></span>

<span data-ttu-id="79a0b-111">Wenn das Objekt einen Thread verwendet, wartet diese Methode auf das [**coutputqueue:: m \_ evflushcomplete**](coutputqueue-m-evflushcomplete.md) -Ereignis.</span><span class="sxs-lookup"><span data-stu-id="79a0b-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="79a0b-112">Der Thread signalisiert dieses Ereignis, nachdem alle ausstehenden Stichproben freigegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="79a0b-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="79a0b-113">Wenn das Objekt keinen Thread verwendet, ruft diese Methode die [**coutputqueue:: freesamples**](coutputqueue-freesamples.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="79a0b-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="79a0b-114">Dann ruft die- `EndFlush` Methode die [**IPin:: endflush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="79a0b-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="79a0b-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="79a0b-115">Requirements</span></span>



| <span data-ttu-id="79a0b-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="79a0b-116">Requirement</span></span> | <span data-ttu-id="79a0b-117">Wert</span><span class="sxs-lookup"><span data-stu-id="79a0b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79a0b-118">Header</span><span class="sxs-lookup"><span data-stu-id="79a0b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="79a0b-119"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="79a0b-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="79a0b-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="79a0b-120">Library</span></span><br/> | <dl> <span data-ttu-id="79a0b-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="79a0b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79a0b-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79a0b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79a0b-123">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="79a0b-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




