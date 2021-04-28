---
description: 'CBaseFilter.StreamTime-Methode: Die StreamTime-Methode ruft die aktuelle Streamzeit ab.'
ms.assetid: 88a2939d-fb51-49fd-af71-21c99511de43
title: CBaseFilter.StreamTime-Methode (Amfilter.h)
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
ms.openlocfilehash: f3334ac273a733c3f0591b76af7e76460997a199
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120068"
---
# <a name="cbasefilterstreamtime-method"></a><span data-ttu-id="894bc-103">CBaseFilter.StreamTime-Methode</span><span class="sxs-lookup"><span data-stu-id="894bc-103">CBaseFilter.StreamTime method</span></span>

<span data-ttu-id="894bc-104">Die **StreamTime-Methode** ruft die aktuelle Streamzeit ab.</span><span class="sxs-lookup"><span data-stu-id="894bc-104">The **StreamTime** method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="894bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="894bc-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="894bc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="894bc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="894bc-107">*rtStream* \[ Ref\]</span><span class="sxs-lookup"><span data-stu-id="894bc-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="894bc-108">Verweis auf ein [**CRefTime-Objekt,**](creftime.md) das die aktuelle Streamzeit empfängt.</span><span class="sxs-lookup"><span data-stu-id="894bc-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="894bc-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="894bc-109">Return value</span></span>

<span data-ttu-id="894bc-110">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="894bc-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="894bc-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="894bc-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="894bc-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="894bc-112">Return code</span></span>                                                                                      | <span data-ttu-id="894bc-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="894bc-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="894bc-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="894bc-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="894bc-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="894bc-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="894bc-116"><dt>**VFW \_ E \_ NO \_ CLOCK**</dt></span><span class="sxs-lookup"><span data-stu-id="894bc-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="894bc-117">Es ist keine Referenzuhr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="894bc-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="894bc-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="894bc-118">Remarks</span></span>

<span data-ttu-id="894bc-119">Die Streamzeit wird als die aktuelle Referenzzeit (wie durch die Verweisuhr angegeben) abzüglich der Startzeit (angegeben durch [**CBaseFilter::m \_ tStart)**](cbasefilter-m-tstart.md)definiert.</span><span class="sxs-lookup"><span data-stu-id="894bc-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseFilter::m\_tStart**](cbasefilter-m-tstart.md)).</span></span> <span data-ttu-id="894bc-120">Der *Zeitstempel* eines Medienbeispiels gibt die Streamzeit an, zu der es gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="894bc-120">A media sample's *time stamp* specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="894bc-121">Wenn ein Beispiel mit einem Zeitstempel kleiner als die aktuelle Streamzeit noch nicht gerendert wurde, kommt es zu einem späteren Zeitpunkt.</span><span class="sxs-lookup"><span data-stu-id="894bc-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

<span data-ttu-id="894bc-122">Diese Methode ruft die Streamzeit ab, indem [**sie IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) aufruft, um die aktuelle Verweiszeit abzurufen, und subtrahiert dann die anfängliche Startzeit.</span><span class="sxs-lookup"><span data-stu-id="894bc-122">This method gets the stream time by calling [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) to get the current reference time, and then subtracting the initial start time.</span></span>

## <a name="requirements"></a><span data-ttu-id="894bc-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="894bc-123">Requirements</span></span>



| <span data-ttu-id="894bc-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="894bc-124">Requirement</span></span> | <span data-ttu-id="894bc-125">Wert</span><span class="sxs-lookup"><span data-stu-id="894bc-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="894bc-126">Header</span><span class="sxs-lookup"><span data-stu-id="894bc-126">Header</span></span><br/>  | <dl> <span data-ttu-id="894bc-127"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="894bc-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="894bc-128">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="894bc-128">Library</span></span><br/> | <dl> <span data-ttu-id="894bc-129"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="894bc-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="894bc-130">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="894bc-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="894bc-131">Uhrzeit und Uhren in DirectShow</span><span class="sxs-lookup"><span data-stu-id="894bc-131">Time and Clocks in DirectShow</span></span>](time-and-clocks-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="894bc-132">**CBaseFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="894bc-132">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




