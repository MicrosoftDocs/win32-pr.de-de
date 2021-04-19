---
description: Die delivernewsegment-Methode übergibt eine Benachrichtigung über einen neuen Segment an die verbundene Eingabe-PIN.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Cbaseoutputpin. delivernewsegment-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361448"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a><span data-ttu-id="638ed-103">Cbaseoutputpin. delivernewsegment-Methode</span><span class="sxs-lookup"><span data-stu-id="638ed-103">CBaseOutputPin.DeliverNewSegment method</span></span>

<span data-ttu-id="638ed-104">Die `DeliverNewSegment` -Methode übergibt eine Benachrichtigung über einen neuen Segment an die verbundene Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="638ed-104">The `DeliverNewSegment` method delivers a new-segment notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="638ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="638ed-105">Syntax</span></span>


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="638ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="638ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="638ed-107">*tSTART*</span><span class="sxs-lookup"><span data-stu-id="638ed-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="638ed-108">Start Medien Position des Segments in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="638ed-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="638ed-109">*tstopps*</span><span class="sxs-lookup"><span data-stu-id="638ed-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="638ed-110">Die endmedien Position des Segments in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="638ed-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="638ed-111">*drate*</span><span class="sxs-lookup"><span data-stu-id="638ed-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="638ed-112">Die Rate, mit der dieses Segment verarbeitet werden soll, als Prozentsatz der ursprünglichen Rate.</span><span class="sxs-lookup"><span data-stu-id="638ed-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="638ed-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="638ed-113">Return value</span></span>

<span data-ttu-id="638ed-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="638ed-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="638ed-115">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="638ed-115">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="638ed-116">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="638ed-116">Return code</span></span>                                                                                           | <span data-ttu-id="638ed-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="638ed-117">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="638ed-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="638ed-118"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="638ed-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="638ed-119">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="638ed-120"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="638ed-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="638ed-121">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="638ed-121">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="638ed-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="638ed-122">Remarks</span></span>

<span data-ttu-id="638ed-123">Diese Methode ruft die [**IPin:: newsegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="638ed-123">This method calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="638ed-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="638ed-124">Requirements</span></span>



| <span data-ttu-id="638ed-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="638ed-125">Requirement</span></span> | <span data-ttu-id="638ed-126">Wert</span><span class="sxs-lookup"><span data-stu-id="638ed-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="638ed-127">Header</span><span class="sxs-lookup"><span data-stu-id="638ed-127">Header</span></span><br/>  | <dl> <span data-ttu-id="638ed-128"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="638ed-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="638ed-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="638ed-129">Library</span></span><br/> | <dl> <span data-ttu-id="638ed-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="638ed-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="638ed-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="638ed-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="638ed-132">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="638ed-132">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




