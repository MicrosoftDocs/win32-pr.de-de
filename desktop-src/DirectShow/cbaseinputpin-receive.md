---
description: 'Die Receive-Methode empfängt das nächste Medien Beispiel im Stream. Diese Methode implementiert die IMemInputPin:: Receive-Methode.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: Cbasinput PIN. Receive-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10306d5568ae1754105a4367952cef82f931be99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369952"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="f013f-104">Cbasinput PIN. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="f013f-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="f013f-105">Die- `Receive` Methode empfängt das nächste Medien Beispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="f013f-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="f013f-106">Diese Methode implementiert die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode.</span><span class="sxs-lookup"><span data-stu-id="f013f-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f013f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f013f-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="f013f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f013f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f013f-109">*psample*</span><span class="sxs-lookup"><span data-stu-id="f013f-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f013f-110">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="f013f-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f013f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f013f-111">Return value</span></span>

<span data-ttu-id="f013f-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f013f-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f013f-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="f013f-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="f013f-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f013f-114">Return code</span></span>                                                                                             | <span data-ttu-id="f013f-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f013f-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="f013f-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f013f-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="f013f-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f013f-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="f013f-118"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="f013f-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="f013f-119">PIN wird zurzeit geleert. Das Beispiel wurde zurückgewiesen.</span><span class="sxs-lookup"><span data-stu-id="f013f-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="f013f-120"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="f013f-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="f013f-121">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="f013f-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="f013f-122"><dt>**VFW \_ E \_ invalidmediatype**</dt></span><span class="sxs-lookup"><span data-stu-id="f013f-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="f013f-123">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="f013f-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="f013f-124"><dt>**VFW \_ E \_ Lauf \_ Zeitfehler**</dt></span><span class="sxs-lookup"><span data-stu-id="f013f-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="f013f-125">Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="f013f-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="f013f-126"><dt>**VFW \_ E \_ falscher \_ Zustand**</dt></span><span class="sxs-lookup"><span data-stu-id="f013f-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="f013f-127">Die PIN wurde beendet.</span><span class="sxs-lookup"><span data-stu-id="f013f-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="f013f-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f013f-128">Remarks</span></span>

<span data-ttu-id="f013f-129">Die upstreamausgabepin ruft diese Methode auf, um ein Beispiel an die Eingabe-PIN zu übermitteln</span><span class="sxs-lookup"><span data-stu-id="f013f-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="f013f-130">Die Eingabe-PIN muss eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="f013f-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="f013f-131">Verarbeiten Sie das Beispiel vor der Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="f013f-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="f013f-132">Geben Sie zurück, und verarbeiten Sie das Beispiel in einem Arbeits Thread.</span><span class="sxs-lookup"><span data-stu-id="f013f-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="f013f-133">Ablehnen Sie das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="f013f-133">Reject the sample.</span></span>

<span data-ttu-id="f013f-134">Wenn die PIN einen Arbeits Thread zum Verarbeiten des Beispiels verwendet, fügen Sie dem Beispiel innerhalb dieser Methode einen Verweis Zähler hinzu.</span><span class="sxs-lookup"><span data-stu-id="f013f-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="f013f-135">Nachdem die Methode zurückgegeben wurde, gibt die upstreampin das Beispiel frei.</span><span class="sxs-lookup"><span data-stu-id="f013f-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="f013f-136">Wenn der Verweis Zähler des Beispiels 0 (null) erreicht, wird das Beispiel zur erneuten Verwendung an die Zuweisung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f013f-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="f013f-137">Diese Methode ist synchron und kann blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="f013f-137">This method is synchronous and can block.</span></span> <span data-ttu-id="f013f-138">Wenn die-Methode blockiert werden kann, sollte die [**cbaseinputpin:: receivecanblock**](cbaseinputpin-receivecanblock.md) -Methode der PIN s OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="f013f-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="f013f-139">In der-Basisklasse führt diese Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="f013f-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="f013f-140">Ruft die [**cbaseinputpin:: checkstreaming**](cbaseinputpin-checkstreaming.md) -Methode auf, um zu überprüfen, ob die PIN jetzt Beispiele verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="f013f-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="f013f-141">Wenn die PIN beispielsweise nicht beendet wird, schlägt die Methode fehl.</span><span class="sxs-lookup"><span data-stu-id="f013f-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="f013f-142">Ruft die Beispiel Eigenschaften ab und überprüft, ob sich das Format geändert hat (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="f013f-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="f013f-143">Wenn sich das Format geändert hat, ruft die-Methode die [**cbasepin:: checkmediatype**](cbasepin-checkmediatype.md) -Methode auf, um zu bestimmen, ob das neue Format zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="f013f-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="f013f-144">Wenn das neue Format nicht zulässig ist, ruft die-Methode die [**cbasepin:: EndOf Stream**](cbasepin-endofstream.md) -Methode auf, \_ gibt ein EC errorabort-Ereignis aus und gibt einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="f013f-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="f013f-145">Wenn keine Fehler aufgetreten sind, gibt die Methode "S OK" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="f013f-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="f013f-146">Testen Sie die Formatänderung wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f013f-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="f013f-147">Wenn das Beispiel die [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) -Schnittstelle unterstützt, überprüfen Sie den **dwsampleflags** -Member der [**am \_ SAMPLE2 \_ Properties**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) -Struktur.</span><span class="sxs-lookup"><span data-stu-id="f013f-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="f013f-148">Wenn das "am \_ Sample Sample \_ typechanged"-Flag vorhanden ist, hat sich das Format geändert.</span><span class="sxs-lookup"><span data-stu-id="f013f-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="f013f-149">Wenn das Beispiel **IMediaSample2** nicht unterstützt, müssen Sie andernfalls die [**imediasample:: getmediatype**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f013f-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="f013f-150">Wenn die Methode einen nicht-**null** -Wert zurückgibt, hat sich das Format geändert.</span><span class="sxs-lookup"><span data-stu-id="f013f-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="f013f-151">In der-Basisklasse verarbeitet diese Methode das Beispiel nicht.</span><span class="sxs-lookup"><span data-stu-id="f013f-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="f013f-152">Die abgeleitete Klasse muss diese Methode überschreiben, um die Verarbeitung auszuführen.</span><span class="sxs-lookup"><span data-stu-id="f013f-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="f013f-153">(Was dies bedeutet, hängt vollständig vom Filter ab.) Die abgeleitete Klasse sollte die Basisklassen Methode abrufen, um die zuvor beschriebenen Fehler zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f013f-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="f013f-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f013f-154">Requirements</span></span>



| <span data-ttu-id="f013f-155">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f013f-155">Requirement</span></span> | <span data-ttu-id="f013f-156">Wert</span><span class="sxs-lookup"><span data-stu-id="f013f-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f013f-157">Header</span><span class="sxs-lookup"><span data-stu-id="f013f-157">Header</span></span><br/>  | <dl> <span data-ttu-id="f013f-158"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f013f-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f013f-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f013f-159">Library</span></span><br/> | <dl> <span data-ttu-id="f013f-160">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f013f-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f013f-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f013f-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f013f-162">**Cbaseingeputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f013f-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




