---
description: 'Die setTime-Methode legt die streamzeiten fest, wenn dieses Beispiel beginnen und fertigstellen soll. Diese Methode implementiert die imediasample:: setTime-Methode.'
ms.assetid: cab4907f-eb6f-4444-9b41-1f95a6ecffed
title: Cmediasample. setTime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaSample.SetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935c4f3aa565b291e459d36e067805944b4fd6b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365155"
---
# <a name="cmediasamplesettime-method"></a><span data-ttu-id="26f7d-104">Cmediasample. setTime-Methode</span><span class="sxs-lookup"><span data-stu-id="26f7d-104">CMediaSample.SetTime method</span></span>

<span data-ttu-id="26f7d-105">Die- `SetTime` Methode legt die streamzeiten fest, wenn dieses Beispiel beginnen und fertigstellen soll.</span><span class="sxs-lookup"><span data-stu-id="26f7d-105">The `SetTime` method sets the stream times when this sample should begin and finish.</span></span> <span data-ttu-id="26f7d-106">Diese Methode implementiert die [**imediasample:: setTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="26f7d-106">This method implements the [**IMediaSample::SetTime**](/windows/desktop/api/Strmif/nf-strmif-imediasample-settime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="26f7d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="26f7d-107">Syntax</span></span>


```C++
HRESULT SetTime(
   REFERENCE_TIME *pTimeStart,
   REFERENCE_TIME *pTimeEnd
);
```



## <a name="parameters"></a><span data-ttu-id="26f7d-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="26f7d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26f7d-109">*ptimestart*</span><span class="sxs-lookup"><span data-stu-id="26f7d-109">*pTimeStart*</span></span> 
</dt> <dd>

<span data-ttu-id="26f7d-110">Zeiger auf die streamzeit, zu der das Beispiel beginnt, in 100-Nanosecond-Einheiten oder **null**.</span><span class="sxs-lookup"><span data-stu-id="26f7d-110">Pointer to the stream time at which the sample begins, in 100-nanosecond units, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="26f7d-111">*ptimeend*</span><span class="sxs-lookup"><span data-stu-id="26f7d-111">*pTimeEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="26f7d-112">Zeiger auf die streamzeit, zu der das Beispiel endet, in 100-Nanosecond-Einheiten oder **null**.</span><span class="sxs-lookup"><span data-stu-id="26f7d-112">Pointer to the stream time at which the sample ends, in 100-nanosecond units, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26f7d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="26f7d-113">Return value</span></span>

<span data-ttu-id="26f7d-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="26f7d-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="26f7d-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="26f7d-115">Remarks</span></span>

<span data-ttu-id="26f7d-116">Diese Methode legt die Endelement Variablen [**cmediasample:: m \_ Start**](cmediasample-m-start.md) und [**cmediasample \_ :: m**](cmediasample-m-end.md) fest, mit denen die Zeitstempel angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="26f7d-116">This method sets the [**CMediaSample::m\_Start**](cmediasample-m-start.md) and [**CMediaSample::m\_End**](cmediasample-m-end.md) member variables, which specify the time stamps.</span></span> <span data-ttu-id="26f7d-117">Außerdem wird die Member-Variable [**cmediasample:: m \_ dwFlags**](cmediasample-m-dwflags.md) aktualisiert, die angibt, ob die Zeitstempel gültig sind.</span><span class="sxs-lookup"><span data-stu-id="26f7d-117">It also updates the [**CMediaSample::m\_dwFlags**](cmediasample-m-dwflags.md) member variable, which specifies whether the time stamps are valid.</span></span>

<span data-ttu-id="26f7d-118">Weitere Informationen zu Zeitstempeln finden Sie unter [Zeit und Uhren in DirectShow](time-and-clocks-in-directshow.md).</span><span class="sxs-lookup"><span data-stu-id="26f7d-118">For information about time stamps, see [Time and Clocks in DirectShow](time-and-clocks-in-directshow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="26f7d-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="26f7d-119">Requirements</span></span>



| <span data-ttu-id="26f7d-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="26f7d-120">Requirement</span></span> | <span data-ttu-id="26f7d-121">Wert</span><span class="sxs-lookup"><span data-stu-id="26f7d-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="26f7d-122">Header</span><span class="sxs-lookup"><span data-stu-id="26f7d-122">Header</span></span><br/>  | <dl> <span data-ttu-id="26f7d-123"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="26f7d-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="26f7d-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="26f7d-124">Library</span></span><br/> | <dl> <span data-ttu-id="26f7d-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="26f7d-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26f7d-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26f7d-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26f7d-127">**Cmediasample-Klasse**</span><span class="sxs-lookup"><span data-stu-id="26f7d-127">**CMediaSample Class**</span></span>](cmediasample.md)
</dt> </dl>

 

 




