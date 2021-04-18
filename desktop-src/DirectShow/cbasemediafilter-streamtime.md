---
description: Die streamtime-Methode ruft die aktuelle streamzeit ab.
ms.assetid: 2e1ff6f1-9815-4ee6-97e8-a5ab5f472b27
title: Cbasemediafilter. streamtime-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.StreamTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 27ccc9c721c97742c09d043af4cca5d287747597
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364437"
---
# <a name="cbasemediafilterstreamtime-method"></a><span data-ttu-id="e767a-103">Cbasemediafilter. streamtime-Methode</span><span class="sxs-lookup"><span data-stu-id="e767a-103">CBaseMediaFilter.StreamTime method</span></span>

<span data-ttu-id="e767a-104">Die- `StreamTime` Methode ruft die aktuelle streamzeit ab.</span><span class="sxs-lookup"><span data-stu-id="e767a-104">The `StreamTime` method retrieves the current stream time.</span></span>

## <a name="syntax"></a><span data-ttu-id="e767a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e767a-105">Syntax</span></span>


```C++
virtual HRESULT StreamTime(
  [ref] CRefTime &rtStream
);
```



## <a name="parameters"></a><span data-ttu-id="e767a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e767a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e767a-107">*rtstream* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="e767a-107">*rtStream* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="e767a-108">Verweis auf ein-Objekt, das die aktuelle [**streamzeit empfängt**](creftime.md) .</span><span class="sxs-lookup"><span data-stu-id="e767a-108">Reference to a [**CRefTime**](creftime.md) object that receives the current stream time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e767a-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e767a-109">Return value</span></span>

<span data-ttu-id="e767a-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e767a-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e767a-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="e767a-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="e767a-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e767a-112">Return code</span></span>                                                                                      | <span data-ttu-id="e767a-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e767a-113">Description</span></span>                                 |
|--------------------------------------------------------------------------------------------------|---------------------------------------------|
| <dl> <span data-ttu-id="e767a-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e767a-114"><dt>**S\_OK**</dt></span></span> </dl>             | <span data-ttu-id="e767a-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e767a-115">Success.</span></span><br/>                         |
| <dl> <span data-ttu-id="e767a-116"><dt>**VFW \_ E \_ No \_ Clock**</dt></span><span class="sxs-lookup"><span data-stu-id="e767a-116"><dt>**VFW\_E\_NO\_CLOCK**</dt></span></span> </dl> | <span data-ttu-id="e767a-117">Es ist keine Referenzuhr verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e767a-117">No reference clock is available.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e767a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e767a-118">Remarks</span></span>

<span data-ttu-id="e767a-119">Die streamzeit wird als aktuelle Bezugszeit (wie durch die verweisuhr angegeben) abzüglich der Startzeit (angegeben durch [**cbasemediafilter:: m \_ tSTART**](cbasemediafilter-m-tstart.md)) definiert.</span><span class="sxs-lookup"><span data-stu-id="e767a-119">Stream time is defined as the current reference time (as given by the reference clock) minus the start time (specified by [**CBaseMediaFilter::m\_tStart**](cbasemediafilter-m-tstart.md)).</span></span> <span data-ttu-id="e767a-120">Der Zeitstempel eines Medien Beispiels gibt die streamzeit an, zu der er gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="e767a-120">A media sample's time stamp specifies the stream time when it should be rendered.</span></span> <span data-ttu-id="e767a-121">Wenn eine Stichprobe mit einem Zeitstempel, der kleiner ist als die aktuelle streamzeit, noch nicht gerendert wurde, wird Sie später angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e767a-121">If a sample with a time stamp less than the current stream time has not yet been rendered, it is late.</span></span>

## <a name="requirements"></a><span data-ttu-id="e767a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e767a-122">Requirements</span></span>



| <span data-ttu-id="e767a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e767a-123">Requirement</span></span> | <span data-ttu-id="e767a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="e767a-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e767a-125">Header</span><span class="sxs-lookup"><span data-stu-id="e767a-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e767a-126"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e767a-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e767a-127">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e767a-127">Library</span></span><br/> | <dl> <span data-ttu-id="e767a-128">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e767a-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e767a-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e767a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e767a-130">**Cbasemediafilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e767a-130">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




