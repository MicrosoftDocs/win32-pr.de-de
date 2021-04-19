---
description: Die startusingoutputpin-Methode erhält Zugriff auf die PIN für einen Streamingvorgang.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Cdynamicoutputpin. startusingoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359772"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a><span data-ttu-id="14296-103">Cdynamicoutputpin. startusingoutputpin-Methode</span><span class="sxs-lookup"><span data-stu-id="14296-103">CDynamicOutputPin.StartUsingOutputPin method</span></span>

<span data-ttu-id="14296-104">Die `StartUsingOutputPin` Methode erhält Zugriff auf die PIN für einen Streamingvorgang.</span><span class="sxs-lookup"><span data-stu-id="14296-104">The `StartUsingOutputPin` method obtains access to the pin for a streaming operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="14296-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="14296-105">Syntax</span></span>


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="14296-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="14296-106">Parameters</span></span>

<span data-ttu-id="14296-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="14296-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="14296-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="14296-108">Return value</span></span>

<span data-ttu-id="14296-109">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="14296-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="14296-110">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="14296-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="14296-111">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="14296-111">Return code</span></span>                                                                                           | <span data-ttu-id="14296-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14296-112">Description</span></span>                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="14296-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="14296-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="14296-114">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="14296-114">Success.</span></span><br/>                                               |
| <dl> <span data-ttu-id="14296-115"><dt>**E \_ unerwartet**</dt></span><span class="sxs-lookup"><span data-stu-id="14296-115"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>          | <span data-ttu-id="14296-116">Unerwarteter Fehler.</span><span class="sxs-lookup"><span data-stu-id="14296-116">Unexpected error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="14296-117"><dt>**VFW \_ E \_ Status \_ geändert**</dt></span><span class="sxs-lookup"><span data-stu-id="14296-117"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="14296-118">Der Filter wurde beendet, oder die PIN wurde mit dem leeren begonnen.</span><span class="sxs-lookup"><span data-stu-id="14296-118">The filter was stopped, or the pin has begun flushing.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="14296-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="14296-119">Remarks</span></span>

<span data-ttu-id="14296-120">Rufen Sie diese Methode auf, bevor Sie Methoden aufrufen, die Daten an die verbundene Eingabe-PIN übermitteln oder den Medientyp der Verbindung ändern.</span><span class="sxs-lookup"><span data-stu-id="14296-120">Call this method before calling any methods that deliver data to the connected input pin or that change the connection's media type.</span></span> <span data-ttu-id="14296-121">Diese Regel gilt z. b. für die folgenden Methoden:</span><span class="sxs-lookup"><span data-stu-id="14296-121">For example, this rule applies to the following methods:</span></span>

-   [<span data-ttu-id="14296-122">**Cdynamicoutputpin:: changeoutputformat**</span><span class="sxs-lookup"><span data-stu-id="14296-122">**CDynamicOutputPin::ChangeOutputFormat**</span></span>](cdynamicoutputpin-changeoutputformat.md)
-   [<span data-ttu-id="14296-123">**Cdynamicoutputpin:: changemediatype**</span><span class="sxs-lookup"><span data-stu-id="14296-123">**CDynamicOutputPin::ChangeMediaType**</span></span>](cdynamicoutputpin-changemediatype.md)
-   [<span data-ttu-id="14296-124">**Cdynamicoutputpin::D ynamikreconnect**</span><span class="sxs-lookup"><span data-stu-id="14296-124">**CDynamicOutputPin::DynamicReconnect**</span></span>](cdynamicoutputpin-dynamicreconnect.md)
-   [<span data-ttu-id="14296-125">**Cbaseoutputpin::D eliver**</span><span class="sxs-lookup"><span data-stu-id="14296-125">**CBaseOutputPin::Deliver**</span></span>](cbaseoutputpin-deliver.md)
-   [<span data-ttu-id="14296-126">**Cbaseoutputpin::D eliverendof Stream**</span><span class="sxs-lookup"><span data-stu-id="14296-126">**CBaseOutputPin::DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md)
-   [<span data-ttu-id="14296-127">**Cbaseoutputpin::D elivernewsegment**</span><span class="sxs-lookup"><span data-stu-id="14296-127">**CBaseOutputPin::DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)
-   [<span data-ttu-id="14296-128">**IMemInputPin:: Receive**</span><span class="sxs-lookup"><span data-stu-id="14296-128">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="14296-129">**IMemInputPin:: receivemultiple**</span><span class="sxs-lookup"><span data-stu-id="14296-129">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="14296-130">**IPin:: EndOf Stream**</span><span class="sxs-lookup"><span data-stu-id="14296-130">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="14296-131">**IPin:: newsegment**</span><span class="sxs-lookup"><span data-stu-id="14296-131">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

<span data-ttu-id="14296-132">Anschließend können Sie die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode aufrufen, um den Zugriff auf die PIN freizugeben.</span><span class="sxs-lookup"><span data-stu-id="14296-132">Afterward, call the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method to release the access to the pin.</span></span>

<span data-ttu-id="14296-133">Wenn die PIN blockiert ist, `StartUsingOutputPin` wartet darauf, dass die Blockierung der PIN aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="14296-133">If the pin is blocked, `StartUsingOutputPin` waits for the pin to become unblocked.</span></span> <span data-ttu-id="14296-134">Wenn der Filter während der Wartezeit der Methode angehalten wird, gibt die Methode sofort VFW \_ E \_ State \_ Changed zurück.</span><span class="sxs-lookup"><span data-stu-id="14296-134">If the filter stops while the method is waiting, the method immediately returns VFW\_E\_STATE\_CHANGED.</span></span> <span data-ttu-id="14296-135">Die PIN behält, wie oft `StartUsingOutputPin` ohne einen entsprechenden Aufruf von **stopusingoutputpin** aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="14296-135">The pin maintains a count of how many times `StartUsingOutputPin` has been called without a corresponding call to **StopUsingOutputPin**.</span></span> <span data-ttu-id="14296-136">Wenn ein anderer Thread versucht, die PIN zu blockieren, während diese Anzahl ungleich NULL ist, legt die PIN ihren Blockierungs Status auf "Ausstehend" fest.</span><span class="sxs-lookup"><span data-stu-id="14296-136">If another thread tries to block the pin while this count is non-zero, the pin sets its blocking status to "pending."</span></span> <span data-ttu-id="14296-137">Die PIN wird blockiert, sobald alle Streamingvorgänge abgeschlossen sind, und zwar im letzten Rückruf von **stopusingoutputpin**.</span><span class="sxs-lookup"><span data-stu-id="14296-137">The pin becomes blocked once all of the streaming operations have completed, in the final call to **StopUsingOutputPin**.</span></span>

<span data-ttu-id="14296-138">Wenn Sie diese Methode aufrufen, dürfen Sie nicht den Abschnitt " [**cdynamicoutputpin:: m \_ blockstatuelock**](cdynamicoutputpin-m-blockstatelock.md) Critical" speichern.</span><span class="sxs-lookup"><span data-stu-id="14296-138">Do not hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section when you call this method.</span></span> <span data-ttu-id="14296-139">Andernfalls kann, wenn die PIN blockiert ist, nie die Blockierung aufgehoben werden, was zu einem Deadlock führt.</span><span class="sxs-lookup"><span data-stu-id="14296-139">Otherwise, if the pin is blocked, it can never become unblocked, causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="14296-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="14296-140">Requirements</span></span>



| <span data-ttu-id="14296-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="14296-141">Requirement</span></span> | <span data-ttu-id="14296-142">Wert</span><span class="sxs-lookup"><span data-stu-id="14296-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="14296-143">Header</span><span class="sxs-lookup"><span data-stu-id="14296-143">Header</span></span><br/>  | <dl> <span data-ttu-id="14296-144"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="14296-144"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="14296-145">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="14296-145">Library</span></span><br/> | <dl> <span data-ttu-id="14296-146">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="14296-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="14296-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14296-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14296-148">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="14296-148">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




