---
description: 'Die Run-Methode führt den Filter aus. Diese Methode implementiert die imediafilter:: Run-Methode.'
ms.assetid: fab2cef7-cad1-4933-92a4-5f41cd947c2f
title: Cbasefilter. Run-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0555733f53b4870a43dbcbf36c69061db19490a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351279"
---
# <a name="cbasefilterrun-method"></a><span data-ttu-id="bff44-104">Cbasefilter. Run-Methode</span><span class="sxs-lookup"><span data-stu-id="bff44-104">CBaseFilter.Run method</span></span>

<span data-ttu-id="bff44-105">Die- `Run` Methode führt den Filter aus.</span><span class="sxs-lookup"><span data-stu-id="bff44-105">The `Run` method runs the filter.</span></span> <span data-ttu-id="bff44-106">Diese Methode implementiert die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode.</span><span class="sxs-lookup"><span data-stu-id="bff44-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bff44-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bff44-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="bff44-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bff44-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bff44-109">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="bff44-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="bff44-110">Verweis Zeit entsprechend der streamzeit 0.</span><span class="sxs-lookup"><span data-stu-id="bff44-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bff44-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bff44-111">Return value</span></span>

<span data-ttu-id="bff44-112">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="bff44-112">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="bff44-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bff44-113">Remarks</span></span>

<span data-ttu-id="bff44-114">Wenn der Filter angehalten wurde, hält diese Methode den Filter an, indem er die [**cbasefilter::P ause**](cbasefilter-pause.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="bff44-114">If the filter is stopped, this method pauses the filter by calling the [**CBaseFilter::Pause**](cbasefilter-pause.md) method.</span></span> <span data-ttu-id="bff44-115">Anschließend wird die [**cbasepin:: Run**](cbasepin-run.md) -Methode für jeden verbundenen Pins des Filters aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="bff44-115">It then calls the [**CBasePin::Run**](cbasepin-run.md) method on each of the filter's connected pins.</span></span> <span data-ttu-id="bff44-116">Schließlich wird die [**cbasefilter:: m \_ State**](cbasefilter-m-state.md) Member-Variable auf State Running festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="bff44-116">Finally, it sets the [**CBaseFilter::m\_State**](cbasefilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="bff44-117">Die streamzeit wird als aktuelle Verweis Zeit abzüglich *tSTART* berechnet.</span><span class="sxs-lookup"><span data-stu-id="bff44-117">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="bff44-118">Ein Medien Beispiel mit einem Zeitstempel von NULL sollte zum Zeitpunkt *tSTART* gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="bff44-118">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="bff44-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bff44-119">Requirements</span></span>



| <span data-ttu-id="bff44-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bff44-120">Requirement</span></span> | <span data-ttu-id="bff44-121">Wert</span><span class="sxs-lookup"><span data-stu-id="bff44-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bff44-122">Header</span><span class="sxs-lookup"><span data-stu-id="bff44-122">Header</span></span><br/>  | <dl> <span data-ttu-id="bff44-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bff44-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bff44-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="bff44-124">Library</span></span><br/> | <dl> <span data-ttu-id="bff44-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="bff44-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bff44-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bff44-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bff44-127">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="bff44-127">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




