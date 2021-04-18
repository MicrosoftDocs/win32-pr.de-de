---
description: 'Die newsegment-Methode benachrichtigt die PIN, dass Medien Beispiele, die nach diesem-aufrufempfang empfangen werden, als Segment gruppiert werden. Implementiert die IPin:: newsegment-Methode.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Cbasepin. newsegment-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365458"
---
# <a name="cbasepinnewsegment-method"></a><span data-ttu-id="1cd14-104">Cbasepin. newsegment-Methode</span><span class="sxs-lookup"><span data-stu-id="1cd14-104">CBasePin.NewSegment method</span></span>

<span data-ttu-id="1cd14-105">Die- `NewSegment` Methode benachrichtigt die PIN, dass nach diesem-aufrufempfang empfangene Medien Beispiele als Segment gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="1cd14-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="1cd14-106">Implementiert die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1cd14-106">Implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cd14-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1cd14-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="1cd14-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1cd14-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cd14-109">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="1cd14-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd14-110">Start Medien Position des Segments in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1cd14-110">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="1cd14-111">*tstopps*</span><span class="sxs-lookup"><span data-stu-id="1cd14-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd14-112">Die endmedien Position des Segments in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="1cd14-112">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="1cd14-113">*drate*</span><span class="sxs-lookup"><span data-stu-id="1cd14-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="1cd14-114">Die Rate, mit der dieses Segment verarbeitet werden soll, als Prozentsatz der ursprünglichen Rate.</span><span class="sxs-lookup"><span data-stu-id="1cd14-114">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cd14-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1cd14-115">Return value</span></span>

<span data-ttu-id="1cd14-116">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="1cd14-116">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cd14-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1cd14-117">Remarks</span></span>

<span data-ttu-id="1cd14-118">Diese Methode legt die Element Variablen [**cbasepin:: m \_ tSTART**](cbasepin-m-tstart.md), [**cbasepin:: m \_ tstoppt**](cbasepin-m-tstop.md)und [**cbasepin:: m \_ drate**](cbasepin-m-drate.md) fest.</span><span class="sxs-lookup"><span data-stu-id="1cd14-118">This method sets the [**CBasePin::m\_tStart**](cbasepin-m-tstart.md), [**CBasePin::m\_tStop**](cbasepin-m-tstop.md), and [**CBasePin::m\_dRate**](cbasepin-m-drate.md) member variables.</span></span> <span data-ttu-id="1cd14-119">Überschreiben Sie diese Methode in der abgeleiteten Klasse, um die Benachrichtigung zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="1cd14-119">In your derived class, override this method to pass the notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="1cd14-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1cd14-120">Requirements</span></span>



| <span data-ttu-id="1cd14-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1cd14-121">Requirement</span></span> | <span data-ttu-id="1cd14-122">Wert</span><span class="sxs-lookup"><span data-stu-id="1cd14-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1cd14-123">Header</span><span class="sxs-lookup"><span data-stu-id="1cd14-123">Header</span></span><br/>  | <dl> <span data-ttu-id="1cd14-124"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1cd14-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1cd14-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1cd14-125">Library</span></span><br/> | <dl> <span data-ttu-id="1cd14-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1cd14-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cd14-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1cd14-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cd14-128">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1cd14-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




