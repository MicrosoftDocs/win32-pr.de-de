---
description: Die newsegment-Methode benachrichtigt den Filter, dass nach diesem-Befehl empfangene Medien Beispiele als Segment gruppiert werden.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Ctransformfilter. newsegment-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359705"
---
# <a name="ctransformfilternewsegment-method"></a><span data-ttu-id="2a7b1-103">Ctransformfilter. newsegment-Methode</span><span class="sxs-lookup"><span data-stu-id="2a7b1-103">CTransformFilter.NewSegment method</span></span>

<span data-ttu-id="2a7b1-104">Die- `NewSegment` Methode benachrichtigt den Filter, dass nach diesem-Befehl empfangene Medien Beispiele als Segment gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-104">The `NewSegment` method notifies the filter that media samples received after this call are grouped as a segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a7b1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a7b1-105">Syntax</span></span>


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="2a7b1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a7b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a7b1-107">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="2a7b1-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="2a7b1-108">Die Startzeit des Segments, relativ zur ursprünglichen Quelle.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-108">Start time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="2a7b1-109">*tstopps*</span><span class="sxs-lookup"><span data-stu-id="2a7b1-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="2a7b1-110">Die Endzeit des Segments, relativ zur ursprünglichen Quelle.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-110">Stop time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="2a7b1-111">*drate*</span><span class="sxs-lookup"><span data-stu-id="2a7b1-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="2a7b1-112">Rate, mit der das Segment verarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-112">Rate at which the segment should be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a7b1-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a7b1-113">Return value</span></span>

<span data-ttu-id="2a7b1-114">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a7b1-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2a7b1-115">Remarks</span></span>

<span data-ttu-id="2a7b1-116">Die [**ctransforminputpin:: newsegment**](ctransforminputpin-newsegment.md) -Methode der Eingabe-PIN ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-116">The input pin's [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) method calls this method.</span></span> <span data-ttu-id="2a7b1-117">Diese Methode stellt den-Befehl `NewSegment` an die downstreameingabepin bereit.</span><span class="sxs-lookup"><span data-stu-id="2a7b1-117">This method delivers the `NewSegment` call to the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a7b1-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a7b1-118">Requirements</span></span>



| <span data-ttu-id="2a7b1-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a7b1-119">Requirement</span></span> | <span data-ttu-id="2a7b1-120">Wert</span><span class="sxs-lookup"><span data-stu-id="2a7b1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a7b1-121">Header</span><span class="sxs-lookup"><span data-stu-id="2a7b1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="2a7b1-122"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a7b1-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2a7b1-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="2a7b1-123">Library</span></span><br/> | <dl> <span data-ttu-id="2a7b1-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="2a7b1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a7b1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a7b1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a7b1-126">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="2a7b1-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




