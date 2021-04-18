---
description: Die streamtime-Methode ruft die aktuelle streamzeit ab.
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: Cbasefilter. streamtime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f4370758eb4ab15a9e53a5157550ee2129783c7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354735"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="9a215-103">Cbasefilter. streamtime-Methode</span><span class="sxs-lookup"><span data-stu-id="9a215-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="9a215-104">Die **streamtime** -Methode ruft die aktuelle streamzeit ab.</span><span class="sxs-lookup"><span data-stu-id="9a215-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a215-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a215-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="9a215-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a215-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9a215-107">*rtstream* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="9a215-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="9a215-108">Verweis auf ein-Objekt, das die aktuelle [**streamzeit empfängt**](creftime.md) .</span><span class="sxs-lookup"><span data-stu-id="9a215-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9a215-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9a215-109">Return value</span></span>

<span data-ttu-id="9a215-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9a215-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="9a215-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="9a215-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="9a215-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="9a215-112">Return code</span></span>                                                                                      | <span data-ttu-id="9a215-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a215-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="9a215-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9a215-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="9a215-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="9a215-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="9a215-116"><dt>**VFW \_ E \_ No \_ Clock**</dt></span><span class="sxs-lookup"><span data-stu-id="9a215-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="9a215-117">Es ist keine Referenzuhr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9a215-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9a215-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9a215-118">Remarks</span></span>

<span data-ttu-id="9a215-119">Die streamzeit wird als aktuelle Verweis Zeit (wie durch die verweisuhr angegeben) abzüglich der Startzeit (angegeben durch [**cbasefilter:: m \_ tSTART**](cbasefilter-m-tstart.md)) definiert.</span><span class="sxs-lookup"><span data-stu-id="9a215-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="9a215-120">Der *Zeitstempel* eines Medien Beispiels gibt die streamzeit an, zu der er gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9a215-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="9a215-121">Wenn eine Stichprobe mit einem Zeitstempel, der kleiner ist als die aktuelle streamzeit, noch nicht gerendert wurde, wird Sie später angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a215-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="9a215-122">Diese Methode ruft die streamzeit ab, indem [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aufgerufen wird, um die aktuelle Verweis Zeit zu erhalten, und anschließend wird die anfängliche Startzeit subtrahieren.</span><span class="sxs-lookup"><span data-stu-id="9a215-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a215-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9a215-123">Requirements</span></span>



| <span data-ttu-id="9a215-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9a215-124">Requirement</span></span> | <span data-ttu-id="9a215-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9a215-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a215-126">Header</span><span class="sxs-lookup"><span data-stu-id="9a215-126">Header</span></span><br/>  | <dl> <span data-ttu-id="9a215-127"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a215-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9a215-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9a215-128">Library</span></span><br/> | <dl> <span data-ttu-id="9a215-129">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9a215-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a215-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a215-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a215-131">Uhrzeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="9a215-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="9a215-132">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9a215-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




