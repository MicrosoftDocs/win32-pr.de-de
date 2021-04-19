---
description: Die newsegment-Methode übergibt ein neues Segment an die eingabepin.
ms.assetid: 53189729-9f47-425e-9df6-faea01dd4482
title: Coutputqueue. newsegment-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e682211a98f4409fda35687160c88b121fa93898
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373828"
---
# <a name="coutputqueuenewsegment-method"></a><span data-ttu-id="62a53-103">Coutputqueue. newsegment-Methode</span><span class="sxs-lookup"><span data-stu-id="62a53-103">COutputQueue.NewSegment method</span></span>

<span data-ttu-id="62a53-104">Die- `NewSegment` Methode übergibt ein neues Segment an die eingabepin.</span><span class="sxs-lookup"><span data-stu-id="62a53-104">The `NewSegment` method delivers a new segment to the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a53-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="62a53-105">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="62a53-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="62a53-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62a53-107">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="62a53-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="62a53-108">Start Medien Position des Segments in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="62a53-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="62a53-109">*tstopps*</span><span class="sxs-lookup"><span data-stu-id="62a53-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="62a53-110">Die endmedien Position des Segments in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="62a53-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="62a53-111">*drate*</span><span class="sxs-lookup"><span data-stu-id="62a53-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="62a53-112">Die Rate, mit der dieses Segment verarbeitet werden soll, als Prozentsatz der ursprünglichen Rate.</span><span class="sxs-lookup"><span data-stu-id="62a53-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62a53-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62a53-113">Return value</span></span>

<span data-ttu-id="62a53-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="62a53-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62a53-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="62a53-115">Remarks</span></span>

<span data-ttu-id="62a53-116">Wenn das Objekt einen Thread verwendet, werden die folgenden Elemente in der angegebenen Reihenfolge in die Warteschlange eingereiht:</span><span class="sxs-lookup"><span data-stu-id="62a53-116">If the object is using a thread, it queues the following items, in order:</span></span>

-   <span data-ttu-id="62a53-117">Eine neue \_ Segment Steuerungs Meldung.</span><span class="sxs-lookup"><span data-stu-id="62a53-117">A NEW\_SEGMENT control message.</span></span>
-   <span data-ttu-id="62a53-118">Die Segment Daten.</span><span class="sxs-lookup"><span data-stu-id="62a53-118">The segment data.</span></span>

<span data-ttu-id="62a53-119">Die neue \_ Segment Nachricht benachrichtigt den Thread, dass das nächste Element in der Warteschlange Segment Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="62a53-119">The NEW\_SEGMENT message notifies the thread that the next item on the queue will contain segment data.</span></span> <span data-ttu-id="62a53-120">Die Segment Daten werden in einer Struktur gebündelt, die wie folgt deklariert wird:</span><span class="sxs-lookup"><span data-stu-id="62a53-120">The segment data is bundled in a structure, declared as follows:</span></span>


```C++
struct NewSegmentPacket {
    REFERENCE_TIME tStart;
    REFERENCE_TIME tStop;
    double dRate;
}; 
```



<span data-ttu-id="62a53-121">Der Thread ruft die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode für die Eingabe-PIN auf, wobei die in der Struktur angegebenen Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62a53-121">The thread calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin, using the data given in the structure.</span></span>

<span data-ttu-id="62a53-122">Wenn das Objekt keinen Thread verwendet, ruft es die [**coutputqueue:: sendanyway**](coutputqueue-sendanyway.md) -Methode auf, um alle ausstehenden Beispiele bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="62a53-122">If the object is not using a thread, it calls the [**COutputQueue::SendAnyway**](coutputqueue-sendanyway.md) method to deliver any pending samples.</span></span> <span data-ttu-id="62a53-123">Anschließend wird **IPin:: newsegment** für die Eingabe-PIN aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="62a53-123">Then it calls **IPin::NewSegment** on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="62a53-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="62a53-124">Requirements</span></span>



| <span data-ttu-id="62a53-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62a53-125">Requirement</span></span> | <span data-ttu-id="62a53-126">Wert</span><span class="sxs-lookup"><span data-stu-id="62a53-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a53-127">Header</span><span class="sxs-lookup"><span data-stu-id="62a53-127">Header</span></span><br/>  | <dl> <span data-ttu-id="62a53-128"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="62a53-128"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="62a53-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="62a53-129">Library</span></span><br/> | <dl> <span data-ttu-id="62a53-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="62a53-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62a53-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62a53-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a53-132">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="62a53-132">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




