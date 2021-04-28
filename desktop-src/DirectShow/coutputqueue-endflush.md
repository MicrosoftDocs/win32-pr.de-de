---
description: 'COutputQueue.EndFlush-Methode: Die EndFlush-Methode beendet einen Leerungsvorgang.'
ms.assetid: 9171a62a-9072-49a3-8e83-f66d7e1483da
title: COutputQueue.EndFlush-Methode (Outputq.h)
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
ms.openlocfilehash: 37701526de66c8cd679f6849703c4eb2a1feb3ee
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099008"
---
# <a name="coutputqueueendflush-method"></a><span data-ttu-id="06448-103">COutputQueue.EndFlush-Methode</span><span class="sxs-lookup"><span data-stu-id="06448-103">COutputQueue.EndFlush method</span></span>

<span data-ttu-id="06448-104">Die `EndFlush` -Methode beendet einen Leerungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="06448-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="06448-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="06448-105">Syntax</span></span>


```C++
void EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="06448-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="06448-106">Parameters</span></span>

<span data-ttu-id="06448-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="06448-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06448-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06448-108">Return value</span></span>

<span data-ttu-id="06448-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="06448-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="06448-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06448-110">Remarks</span></span>

<span data-ttu-id="06448-111">Wenn das Objekt einen Thread verwendet, wartet diese Methode auf das [**Ereignis COutputQueue::m \_ evFlushComplete.**](coutputqueue-m-evflushcomplete.md)</span><span class="sxs-lookup"><span data-stu-id="06448-111">If the object is using a thread, this method waits for the [**COutputQueue::m\_evFlushComplete**](coutputqueue-m-evflushcomplete.md) event.</span></span> <span data-ttu-id="06448-112">Der Thread signalisiert dieses Ereignis, nachdem alle ausstehenden Stichproben frei gegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="06448-112">The thread signals this event after it frees any pending samples.</span></span> <span data-ttu-id="06448-113">Wenn das Objekt keinen Thread verwendet, ruft diese Methode die [**COutputQueue::FreeSamples-Methode**](coutputqueue-freesamples.md) auf.</span><span class="sxs-lookup"><span data-stu-id="06448-113">If the object is not using a thread, this method calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method.</span></span> <span data-ttu-id="06448-114">Anschließend ruft die `EndFlush` -Methode die [**IPin::EndFlush-Methode**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) auf dem Eingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="06448-114">Then the `EndFlush` method calls the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="06448-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06448-115">Requirements</span></span>



| <span data-ttu-id="06448-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06448-116">Requirement</span></span> | <span data-ttu-id="06448-117">Wert</span><span class="sxs-lookup"><span data-stu-id="06448-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06448-118">Header</span><span class="sxs-lookup"><span data-stu-id="06448-118">Header</span></span><br/>  | <dl> <span data-ttu-id="06448-119"><dt>Outputq.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="06448-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="06448-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06448-120">Library</span></span><br/> | <dl> <span data-ttu-id="06448-121"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="06448-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06448-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="06448-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06448-123">**COutputQueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="06448-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




