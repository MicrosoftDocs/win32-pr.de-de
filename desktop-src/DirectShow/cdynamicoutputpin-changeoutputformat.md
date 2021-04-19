---
description: Mit der changeoutputformat-Methode wird der Medientyp für die Verbindung dynamisch geändert, und es werden neue Segmentinformationen bereitstellt.
ms.assetid: d1204ca0-a489-48a0-8fe5-3ade04f51c93
title: Cdynamicoutputpin. changeoutputformat-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.ChangeOutputFormat
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57421b2fd9624d9798037151a5656343e386a497
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367201"
---
# <a name="cdynamicoutputpinchangeoutputformat-method"></a><span data-ttu-id="16f2b-103">Cdynamicoutputpin. changeoutputformat-Methode</span><span class="sxs-lookup"><span data-stu-id="16f2b-103">CDynamicOutputPin.ChangeOutputFormat method</span></span>

<span data-ttu-id="16f2b-104">Mit der `ChangeOutputFormat` -Methode wird der Medientyp für die Verbindung dynamisch geändert, und es werden neue Segmentinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="16f2b-104">The `ChangeOutputFormat` method dynamically changes the media type for the connection, and delivers new segment information.</span></span> <span data-ttu-id="16f2b-105">Die Änderung kann auftreten, während das Filter Diagramm ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16f2b-105">The change can occur while the filter graph is running.</span></span> <span data-ttu-id="16f2b-106">Nachdem diese Methode aufgerufen wurde, können keine Beispiele mit dem alten Medientyp übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="16f2b-106">Once this method is called, samples with the old media type cannot be delivered.</span></span> <span data-ttu-id="16f2b-107">Der Aufrufer muss sicherstellen, dass keine alten Beispiele ausstehend sind.</span><span class="sxs-lookup"><span data-stu-id="16f2b-107">The caller must ensure that no old samples are pending.</span></span>

## <a name="syntax"></a><span data-ttu-id="16f2b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="16f2b-108">Syntax</span></span>


```C++
HRESULT ChangeOutputFormat(
   const AM_MEDIA_TYPE  *pmt,
         REFERENCE_TIME tSegmentStart,
         REFERENCE_TIME tSegmentStop,
         double         dSegmentRate
);
```



## <a name="parameters"></a><span data-ttu-id="16f2b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="16f2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16f2b-110">*PMT*</span><span class="sxs-lookup"><span data-stu-id="16f2b-110">*pmt*</span></span> 
</dt> <dd>

<span data-ttu-id="16f2b-111">Zeiger auf eine [**am \_ - \_ Medientyp**](/windows/win32/api/strmif/ns-strmif-am_media_type) Struktur, die den Medientyp angibt.</span><span class="sxs-lookup"><span data-stu-id="16f2b-111">Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.</span></span>

</dd> <dt>

<span data-ttu-id="16f2b-112">*tsegmentstart*</span><span class="sxs-lookup"><span data-stu-id="16f2b-112">*tSegmentStart*</span></span> 
</dt> <dd>

<span data-ttu-id="16f2b-113">Die Startzeit des Segments.</span><span class="sxs-lookup"><span data-stu-id="16f2b-113">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="16f2b-114">*tsegmentbeendet*</span><span class="sxs-lookup"><span data-stu-id="16f2b-114">*tSegmentStop*</span></span> 
</dt> <dd>

<span data-ttu-id="16f2b-115">Die Endzeit des Segments.</span><span class="sxs-lookup"><span data-stu-id="16f2b-115">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="16f2b-116">*dsegmentrate*</span><span class="sxs-lookup"><span data-stu-id="16f2b-116">*dSegmentRate*</span></span> 
</dt> <dd>

<span data-ttu-id="16f2b-117">Segment Rate.</span><span class="sxs-lookup"><span data-stu-id="16f2b-117">Segment rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16f2b-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="16f2b-118">Return value</span></span>

<span data-ttu-id="16f2b-119">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="16f2b-119">Returns an **HRESULT** value.</span></span> <span data-ttu-id="16f2b-120">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="16f2b-120">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="16f2b-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="16f2b-121">Return code</span></span>                                                                                           | <span data-ttu-id="16f2b-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="16f2b-122">Description</span></span>                                                                                                                              |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="16f2b-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="16f2b-123"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="16f2b-124">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="16f2b-124">Success.</span></span><br/>                                                                                                                      |
| <dl> <span data-ttu-id="16f2b-125"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="16f2b-125"><dt>**E\_FAIL**</dt></span></span> </dl>                | <span data-ttu-id="16f2b-126">Fehler.</span><span class="sxs-lookup"><span data-stu-id="16f2b-126">Failure.</span></span> <span data-ttu-id="16f2b-127">Möglicherweise hat der besitzende Filter [**cdynamicoutputpin:: setconfiginfo**](cdynamicoutputpin-setconfiginfo.md)nicht aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="16f2b-127">Possibly the owning filter did not call [**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md).</span></span><br/> |
| <dl> <span data-ttu-id="16f2b-128"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="16f2b-128"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="16f2b-129">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="16f2b-129">The pin is not connected.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="16f2b-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="16f2b-130">Remarks</span></span>

<span data-ttu-id="16f2b-131">Diese Methode ändert den Formattyp, während der Filter ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="16f2b-131">This method changes the format type while the filter is running.</span></span> <span data-ttu-id="16f2b-132">Wenn die downstreampin das neue Format annimmt, ist keine erneute Verbindung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="16f2b-132">If the downstream pin accepts the new format, no reconnection is necessary.</span></span> <span data-ttu-id="16f2b-133">Andernfalls versucht die Methode, die PIN erneut zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="16f2b-133">Otherwise, the method attempts to reconnect the pin.</span></span> <span data-ttu-id="16f2b-134">Wenn die-Methode das Format erfolgreich ändert, werden die neuen Segmentinformationen übermittelt.</span><span class="sxs-lookup"><span data-stu-id="16f2b-134">If the method successfully changes the format, it delivers the new segment information.</span></span> <span data-ttu-id="16f2b-135">Diese Methode ruft die [**cdynamicoutputpin:: changemediatype**](cdynamicoutputpin-changemediatype.md) -Methode auf, um die Formatänderung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="16f2b-135">This method calls the [**CDynamicOutputPin::ChangeMediaType**](cdynamicoutputpin-changemediatype.md) method to perform the format change.</span></span>

<span data-ttu-id="16f2b-136">Sie müssen die [**cdynamicoutputpin:: startusingoutputpin**](cdynamicoutputpin-startusingoutputpin.md) -Methode aufrufen, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="16f2b-136">You must call the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="16f2b-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="16f2b-137">Requirements</span></span>



| <span data-ttu-id="16f2b-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="16f2b-138">Requirement</span></span> | <span data-ttu-id="16f2b-139">Wert</span><span class="sxs-lookup"><span data-stu-id="16f2b-139">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f2b-140">Header</span><span class="sxs-lookup"><span data-stu-id="16f2b-140">Header</span></span><br/>  | <dl> <span data-ttu-id="16f2b-141"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="16f2b-141"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="16f2b-142">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="16f2b-142">Library</span></span><br/> | <dl> <span data-ttu-id="16f2b-143">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="16f2b-143"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16f2b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="16f2b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16f2b-145">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="16f2b-145">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




