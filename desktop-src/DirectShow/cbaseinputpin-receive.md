---
description: 'CBaseInputPin.Receive-Methode: Die Receive-Methode empfängt das nächste Medienbeispiel im Stream. Diese Methode implementiert die IMemInputPin::Receive-Methode.'
ms.assetid: 30fefc7b-7c9c-44cd-b58b-2b275dfa2520
title: CBaseInputPin.Receive-Methode (Amfilter.h)
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
ms.openlocfilehash: 4fe88913ad374923c11cf058a3dc0aa70580411e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099688"
---
# <a name="cbaseinputpinreceive-method"></a><span data-ttu-id="5e394-104">CBaseInputPin.Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="5e394-104">CBaseInputPin.Receive method</span></span>

<span data-ttu-id="5e394-105">Die `Receive` -Methode empfängt das nächste Medienbeispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="5e394-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="5e394-106">Diese Methode implementiert die [**IMemInputPin::Receive-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)</span><span class="sxs-lookup"><span data-stu-id="5e394-106">This method implements the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e394-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e394-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="5e394-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e394-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e394-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="5e394-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="5e394-110">Zeiger auf die [**IMediaSample-Schnittstelle des**](/windows/desktop/api/Strmif/nn-strmif-imediasample) Beispiels.</span><span class="sxs-lookup"><span data-stu-id="5e394-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e394-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5e394-111">Return value</span></span>

<span data-ttu-id="5e394-112">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="5e394-112">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5e394-113">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="5e394-113">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="5e394-114">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="5e394-114">Return code</span></span>                                                                                             | <span data-ttu-id="5e394-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e394-115">Description</span></span>                                                |
|---------------------------------------------------------------------------------------------------------|------------------------------------------------------------|
| <dl> <span data-ttu-id="5e394-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5e394-116"><dt>**S\_OK**</dt></span></span> </dl>                    | <span data-ttu-id="5e394-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="5e394-117">Success.</span></span><br/>                                        |
| <dl> <span data-ttu-id="5e394-118"><dt>**S \_ FALSE**</dt></span><span class="sxs-lookup"><span data-stu-id="5e394-118"><dt>**S\_FALSE**</dt></span></span> </dl>                 | <span data-ttu-id="5e394-119">Pin wird gerade geleert. Das Beispiel wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="5e394-119">Pin is currently flushing; sample was rejected.</span></span><br/> |
| <dl> <span data-ttu-id="5e394-120"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="5e394-120"><dt>**E\_POINTER**</dt></span></span> </dl>               | <span data-ttu-id="5e394-121"> NULL-Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="5e394-121">**NULL** pointer argument.</span></span><br/>                      |
| <dl> <span data-ttu-id="5e394-122"><dt>**VFW \_ E \_ INVALIDMEDIATYPE**</dt></span><span class="sxs-lookup"><span data-stu-id="5e394-122"><dt>**VFW\_E\_INVALIDMEDIATYPE**</dt></span></span> </dl> | <span data-ttu-id="5e394-123">Ungültiger Medientyp.</span><span class="sxs-lookup"><span data-stu-id="5e394-123">Invalid media type.</span></span><br/>                             |
| <dl> <span data-ttu-id="5e394-124"><dt>**VFW \_ \_ E-LAUFZEITFEHLER \_**</dt></span><span class="sxs-lookup"><span data-stu-id="5e394-124"><dt>**VFW\_E\_RUNTIME\_ERROR**</dt></span></span> </dl>   | <span data-ttu-id="5e394-125">Laufzeitfehler.</span><span class="sxs-lookup"><span data-stu-id="5e394-125">A run-time error occurred.</span></span><br/>                      |
| <dl> <span data-ttu-id="5e394-126"><dt>**VFW \_ E \_ WRONG \_ STATE**</dt></span><span class="sxs-lookup"><span data-stu-id="5e394-126"><dt>**VFW\_E\_WRONG\_STATE**</dt></span></span> </dl>     | <span data-ttu-id="5e394-127">Die Stecknadel wird beendet.</span><span class="sxs-lookup"><span data-stu-id="5e394-127">The pin is stopped.</span></span><br/>                             |



 

## <a name="remarks"></a><span data-ttu-id="5e394-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5e394-128">Remarks</span></span>

<span data-ttu-id="5e394-129">Der Upstreamausgabepin ruft diese Methode auf, um ein Beispiel an den Eingabepin zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="5e394-129">The upstream output pin calls this method to deliver a sample to the input pin.</span></span> <span data-ttu-id="5e394-130">Der Eingabepin muss einen der folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="5e394-130">The input pin must do one of the following:</span></span>

-   <span data-ttu-id="5e394-131">Verarbeiten Sie das Beispiel vor der Rückgabe.</span><span class="sxs-lookup"><span data-stu-id="5e394-131">Process the sample before returning.</span></span>
-   <span data-ttu-id="5e394-132">Gibt zurück und verarbeitet das Beispiel in einem Arbeitsthread.</span><span class="sxs-lookup"><span data-stu-id="5e394-132">Return, and process the sample in a worker thread.</span></span>
-   <span data-ttu-id="5e394-133">Lehnt das Beispiel ab.</span><span class="sxs-lookup"><span data-stu-id="5e394-133">Reject the sample.</span></span>

<span data-ttu-id="5e394-134">Wenn der Pin einen Arbeitsthread zum Verarbeiten des Beispiels verwendet, fügen Sie dem Beispiel innerhalb dieser Methode einen Verweiszähler hinzu.</span><span class="sxs-lookup"><span data-stu-id="5e394-134">If the pin uses a worker thread to process the sample, add a reference count to the sample inside this method.</span></span> <span data-ttu-id="5e394-135">Nachdem die Methode zurückgegeben wurde, gibt der Upstream-Pin das Beispiel frei.</span><span class="sxs-lookup"><span data-stu-id="5e394-135">After the method returns, the upstream pin releases the sample.</span></span> <span data-ttu-id="5e394-136">Wenn der Verweiszähler der Stichprobe 0 (null) erreicht, kehrt das Beispiel zur erneuten Verwendung zur Zuweisung zurück.</span><span class="sxs-lookup"><span data-stu-id="5e394-136">When the sample's reference count reaches zero, the sample returns to the allocator for re-use.</span></span>

<span data-ttu-id="5e394-137">Diese Methode ist synchron und kann blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="5e394-137">This method is synchronous and can block.</span></span> <span data-ttu-id="5e394-138">Wenn die -Methode blockiert werden kann, sollte die [**CBaseInputPin::ReceiveCanBlock-Methode**](cbaseinputpin-receivecanblock.md) des Pins S \_ OK zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="5e394-138">If the method might block, the pin's [**CBaseInputPin::ReceiveCanBlock**](cbaseinputpin-receivecanblock.md) method should return S\_OK.</span></span>

<span data-ttu-id="5e394-139">In der Basisklasse führt diese Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="5e394-139">In the base class, this method performs the following steps:</span></span>

1.  <span data-ttu-id="5e394-140">Ruft die [**CBaseInputPin::CheckStreaming-Methode**](cbaseinputpin-checkstreaming.md) auf, um zu überprüfen, ob der Pin jetzt Beispiele verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="5e394-140">Calls the [**CBaseInputPin::CheckStreaming**](cbaseinputpin-checkstreaming.md) method to verify that the pin can process samples now.</span></span> <span data-ttu-id="5e394-141">Wenn dies beispielsweise nicht dere ist, schlägt die -Methode fehl, wenn die Stecknadel beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5e394-141">If it cannot for example, if the pin is stopped the method fails.</span></span>
2.  <span data-ttu-id="5e394-142">Ruft die Beispieleigenschaften ab und überprüft, ob sich das Format geändert hat (siehe unten).</span><span class="sxs-lookup"><span data-stu-id="5e394-142">Retrieves the sample properties and checks whether the format has changed (see below).</span></span>
3.  <span data-ttu-id="5e394-143">Wenn sich das Format geändert hat, ruft die -Methode die [**CBasePin::CheckMediaType-Methode**](cbasepin-checkmediatype.md) auf, um zu bestimmen, ob das neue Format akzeptabel ist.</span><span class="sxs-lookup"><span data-stu-id="5e394-143">If the format has changed, the method calls the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to determine whether the new format is acceptable.</span></span>
4.  <span data-ttu-id="5e394-144">Wenn das neue Format nicht akzeptabel ist, ruft die -Methode die [**CBasePin::EndOfStream-Methode**](cbasepin-endofstream.md) auf, sendet ein EC \_ ERRORABORT-Ereignis und gibt einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="5e394-144">If the new format is not acceptable, the method calls the [**CBasePin::EndOfStream**](cbasepin-endofstream.md) method, posts an EC\_ERRORABORT event, and returns an error code.</span></span>
5.  <span data-ttu-id="5e394-145">Wenn keine Fehler aufgetreten sind, gibt die Methode S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="5e394-145">Assuming there were no errors, the method returns S\_OK.</span></span>

<span data-ttu-id="5e394-146">Testen Sie wie folgt, um eine Formatänderung zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="5e394-146">Test for a format change as follows:</span></span>

-   <span data-ttu-id="5e394-147">Wenn das Beispiel die [**IMediaSample2-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) unterstützt, überprüfen Sie den **dwSampleFlags-Member** der [**AM \_ SAMPLE2 \_ PROPERTIES-Struktur.**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties)</span><span class="sxs-lookup"><span data-stu-id="5e394-147">If the sample supports the [**IMediaSample2**](/windows/desktop/api/Strmif/nn-strmif-imediasample2) interface, check the **dwSampleFlags** member of the [**AM\_SAMPLE2\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-am_sample2_properties) structure.</span></span> <span data-ttu-id="5e394-148">Wenn das \_ AM SAMPLE \_ TYPECHANGED-Flag vorhanden ist, wurde das Format geändert.</span><span class="sxs-lookup"><span data-stu-id="5e394-148">If the AM\_SAMPLE\_TYPECHANGED flag is present, the format has changed.</span></span>
-   <span data-ttu-id="5e394-149">Wenn das Beispiel **IMediaSample2** nicht unterstützt, rufen Sie andernfalls die [**IMediaSample::GetMediaType-Methode**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) auf.</span><span class="sxs-lookup"><span data-stu-id="5e394-149">Otherwise, if the sample does not support **IMediaSample2**, call the [**IMediaSample::GetMediaType**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getmediatype) method.</span></span> <span data-ttu-id="5e394-150">Wenn die Methode einen Wert ungleich **NULL** zurückgibt, wurde das Format geändert.</span><span class="sxs-lookup"><span data-stu-id="5e394-150">If the method returns a non-**NULL** value, the format has changed.</span></span>

<span data-ttu-id="5e394-151">In der Basisklasse verarbeitet diese Methode das Beispiel nicht.</span><span class="sxs-lookup"><span data-stu-id="5e394-151">In the base class, this method does not process the sample.</span></span> <span data-ttu-id="5e394-152">Die abgeleitete Klasse muss diese Methode überschreiben, um die Verarbeitung durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="5e394-152">The derived class must override this method to perform the processing.</span></span> <span data-ttu-id="5e394-153">(Dies hängt vollständig vom Filter ab.) Die abgeleitete Klasse sollte die Basisklassenmethode aufrufen, um nach den zuvor beschriebenen Fehlern zu suchen.</span><span class="sxs-lookup"><span data-stu-id="5e394-153">(What this entails depends entirely on the filter.) The derived class should call the base-class method, to check for the errors described previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="5e394-154">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e394-154">Requirements</span></span>



| <span data-ttu-id="5e394-155">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5e394-155">Requirement</span></span> | <span data-ttu-id="5e394-156">Wert</span><span class="sxs-lookup"><span data-stu-id="5e394-156">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5e394-157">Header</span><span class="sxs-lookup"><span data-stu-id="5e394-157">Header</span></span><br/>  | <dl> <span data-ttu-id="5e394-158"><dt>Amfilter.h (streams.h einschließen)</dt></span><span class="sxs-lookup"><span data-stu-id="5e394-158"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5e394-159">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="5e394-159">Library</span></span><br/> | <dl> <span data-ttu-id="5e394-160"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="5e394-160"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5e394-161">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="5e394-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e394-162">**CBaseInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="5e394-162">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




