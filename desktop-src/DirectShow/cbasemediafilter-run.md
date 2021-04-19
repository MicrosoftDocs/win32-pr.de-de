---
description: 'Die Run-Methode führt das-Objekt aus. Diese Methode implementiert die imediafilter:: Run-Methode.'
ms.assetid: a59180df-46b4-4c23-973f-2931d95ace55
title: Cbasemediafilter. Run-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c4023be7731f9bae60576bc7002010eb0b51823
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369956"
---
# <a name="cbasemediafilterrun-method"></a><span data-ttu-id="9e577-104">Cbasemediafilter. Run-Methode</span><span class="sxs-lookup"><span data-stu-id="9e577-104">CBaseMediaFilter.Run method</span></span>

<span data-ttu-id="9e577-105">Die- `Run` Methode führt das-Objekt aus.</span><span class="sxs-lookup"><span data-stu-id="9e577-105">The `Run` method runs the object.</span></span> <span data-ttu-id="9e577-106">Diese Methode implementiert die [**imediafilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9e577-106">This method implements the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9e577-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9e577-107">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="9e577-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e577-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e577-109">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="9e577-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="9e577-110">Verweis Zeit entsprechend der streamzeit 0.</span><span class="sxs-lookup"><span data-stu-id="9e577-110">Reference time corresponding to stream time 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e577-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e577-111">Return value</span></span>

<span data-ttu-id="9e577-112">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="9e577-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e577-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e577-113">Remarks</span></span>

<span data-ttu-id="9e577-114">Wenn das-Objekt beendet wird, hält diese Methode das-Objekt an, indem die [**cbasemediafilter::P ause**](cbasemediafilter-pause.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="9e577-114">If the object is stopped, this method pauses the object by calling the [**CBaseMediaFilter::Pause**](cbasemediafilter-pause.md) method.</span></span> <span data-ttu-id="9e577-115">Anschließend wird die Variable [**cbasemediafilter:: m \_ State**](cbasemediafilter-m-state.md) Member auf State Running festgelegt \_ .</span><span class="sxs-lookup"><span data-stu-id="9e577-115">It then sets the [**CBaseMediaFilter::m\_State**](cbasemediafilter-m-state.md) member variable to State\_Running.</span></span>

<span data-ttu-id="9e577-116">Die streamzeit wird als aktuelle Verweis Zeit abzüglich *tSTART* berechnet.</span><span class="sxs-lookup"><span data-stu-id="9e577-116">Stream time is calculated as the current reference time minus *tStart*.</span></span> <span data-ttu-id="9e577-117">Ein Medien Beispiel mit einem Zeitstempel von NULL sollte zum Zeitpunkt *tSTART* gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="9e577-117">A media sample with a time stamp of zero should be rendered at time *tStart*.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e577-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e577-118">Requirements</span></span>



| <span data-ttu-id="9e577-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e577-119">Requirement</span></span> | <span data-ttu-id="9e577-120">Wert</span><span class="sxs-lookup"><span data-stu-id="9e577-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e577-121">Header</span><span class="sxs-lookup"><span data-stu-id="9e577-121">Header</span></span><br/>  | <dl> <span data-ttu-id="9e577-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9e577-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9e577-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9e577-123">Library</span></span><br/> | <dl> <span data-ttu-id="9e577-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9e577-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e577-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e577-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e577-126">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9e577-126">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




