---
description: 'Die Receive-Methode empfängt ein Medien Beispiel, verarbeitet sie und stellt ein Ausgabe Beispiel für den downstreamfilter bereit. Diese Methode überschreibt die ctransformfilter:: Receive-Methode.'
ms.assetid: 35e22a63-471e-4ca8-be3b-d84920cec7cb
title: Cvideotransformfilter. Receive-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: bdc33773a31a7c9ddfd7adb0f3fb20f8fcf6d520
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367048"
---
# <a name="cvideotransformfilterreceive-method"></a><span data-ttu-id="e85da-104">Cvideotransformfilter. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="e85da-104">CVideoTransformFilter.Receive method</span></span>

<span data-ttu-id="e85da-105">Die- `Receive` Methode empfängt ein Medien Beispiel, verarbeitet sie und stellt ein Ausgabe Beispiel für den downstreamfilter bereit.</span><span class="sxs-lookup"><span data-stu-id="e85da-105">The `Receive` method receives a media sample, processes it, and delivers an output sample to the downstream filter.</span></span> <span data-ttu-id="e85da-106">Diese Methode überschreibt die [**ctransformfilter:: Receive**](ctransformfilter-receive.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e85da-106">This method overrides the [**CTransformFilter::Receive**](ctransformfilter-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e85da-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e85da-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="e85da-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e85da-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e85da-109">*psample*</span><span class="sxs-lookup"><span data-stu-id="e85da-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e85da-110">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle für das Eingabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e85da-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface on the input sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e85da-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e85da-111">Return value</span></span>

<span data-ttu-id="e85da-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e85da-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="e85da-113">Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="e85da-113">Possible values include the following:</span></span>



| <span data-ttu-id="e85da-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e85da-114">Return code</span></span>                                                                             | <span data-ttu-id="e85da-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e85da-115">Description</span></span>                                                 |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="e85da-116"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="e85da-116"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="e85da-117">Der upstreamfilter sollte das Senden von Beispielen abbrechen.</span><span class="sxs-lookup"><span data-stu-id="e85da-117">The upstream filter should stop sending samples.</span></span><br/> |
| <dl> <span data-ttu-id="e85da-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e85da-118"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="e85da-119">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="e85da-119">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="e85da-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e85da-120">Remarks</span></span>

<span data-ttu-id="e85da-121">Diese Methode ruft [**cvideotransformfilter:: dendskipframe**](cvideotransformfilter-shouldskipframe.md) auf, um zu bestimmen, ob dieses Beispiel bereitgestellt oder einfach verworfen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e85da-121">This method calls [**CVideoTransformFilter::ShouldSkipFrame**](cvideotransformfilter-shouldskipframe.md) to determine whether it should deliver this sample or simply discard it.</span></span> <span data-ttu-id="e85da-122">Wenn " **dendskipframe** " **false** zurückgibt (was angibt, dass das Beispiel übermittelt werden soll), führt die Methode Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="e85da-122">If **ShouldSkipFrame** returns **FALSE** (indicating the sample should be delivered), the method does the following:</span></span>

1.  <span data-ttu-id="e85da-123">Ruft [**ctransformfilter:: initializeoutputsample**](ctransformfilter-initializeoutputsample.md) auf, um das Ausgabe Beispiel vorzubereiten</span><span class="sxs-lookup"><span data-stu-id="e85da-123">Calls [**CTransformFilter::InitializeOutputSample**](ctransformfilter-initializeoutputsample.md) to prepare the output sample</span></span>
2.  <span data-ttu-id="e85da-124">Ruft [**ctransformfilter:: Transform**](ctransformfilter-transform.md) auf, um das Eingabe Beispiel zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="e85da-124">Calls [**CTransformFilter::Transform**](ctransformfilter-transform.md) to process the input sample.</span></span> <span data-ttu-id="e85da-125">Diese Methode ist rein virtuell und muss in der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e85da-125">This method is pure virtual, and must be implemented in the derived class.</span></span>
3.  <span data-ttu-id="e85da-126">Ruft [**cbaseoutputpin::D eliver**](cbaseoutputpin-deliver.md) auf, um das Ausgabe Beispiel bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e85da-126">Calls [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) to deliver the output sample.</span></span>

<span data-ttu-id="e85da-127">Außerdem prüft diese Methode, ob im Eingabe-oder Ausgabe Beispiel Formatänderungen durch Aufrufen von [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype)durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e85da-127">Also, this method checks for format changes on the input or output sample, by calling [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype).</span></span> <span data-ttu-id="e85da-128">Wenn eine Formatänderung vorliegt, legt die-Methode den Verbindungstyp für die entsprechende PIN fest.</span><span class="sxs-lookup"><span data-stu-id="e85da-128">If there is a format change, the method sets the connection type on the corresponding pin.</span></span> <span data-ttu-id="e85da-129">Bevor der neue Typ festgelegt wird, wird **stopstreaming** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e85da-129">Before it sets the new type, it calls **StopStreaming**.</span></span> <span data-ttu-id="e85da-130">Nachdem der neue Typ festgelegt wurde, wird **startstreaming** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="e85da-130">After it sets the new type, it calls **StartStreaming**.</span></span> <span data-ttu-id="e85da-131">Diese Methoden können von der abgeleiteten Klasse zum Aktualisieren Ihres internen Zustands verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e85da-131">The derived class can use these methods to update its internal state.</span></span> <span data-ttu-id="e85da-132">Die abgeleitete Klasse muss möglicherweise auch das neue Format in der **Transformations** Methode überprüfen.</span><span class="sxs-lookup"><span data-stu-id="e85da-132">The derived class might also need to check for the new format in its **Transform** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e85da-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e85da-133">Requirements</span></span>



| <span data-ttu-id="e85da-134">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e85da-134">Requirement</span></span> | <span data-ttu-id="e85da-135">Wert</span><span class="sxs-lookup"><span data-stu-id="e85da-135">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e85da-136">Header</span><span class="sxs-lookup"><span data-stu-id="e85da-136">Header</span></span><br/>  | <dl> <span data-ttu-id="e85da-137"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e85da-137"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e85da-138">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e85da-138">Library</span></span><br/> | <dl> <span data-ttu-id="e85da-139">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e85da-139"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e85da-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e85da-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e85da-141">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e85da-141">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




