---
description: Die asynchronousblockoutputpin-Methode blockiert die PIN. Die-Methode gibt möglicherweise zurück, bevor die PIN blockiert wird.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Cdynamicoutputpin. asynchronousblockoutputpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358145"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a><span data-ttu-id="f5589-104">Cdynamicoutputpin. asynchronousblockoutputpin-Methode</span><span class="sxs-lookup"><span data-stu-id="f5589-104">CDynamicOutputPin.AsynchronousBlockOutputPin method</span></span>

<span data-ttu-id="f5589-105">Die- `AsynchronousBlockOutputPin` Methode blockiert die PIN.</span><span class="sxs-lookup"><span data-stu-id="f5589-105">The `AsynchronousBlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="f5589-106">Die-Methode gibt möglicherweise zurück, bevor die PIN blockiert wird.</span><span class="sxs-lookup"><span data-stu-id="f5589-106">The method might return before the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5589-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f5589-107">Syntax</span></span>


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a><span data-ttu-id="f5589-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f5589-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5589-109">*hnotifycallerpinblockedevent*</span><span class="sxs-lookup"><span data-stu-id="f5589-109">*hNotifyCallerPinBlockedEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="f5589-110">Handle für ein Ereignis.</span><span class="sxs-lookup"><span data-stu-id="f5589-110">Handle to an event.</span></span> <span data-ttu-id="f5589-111">Das-Ereignis wird signalisiert, wenn die Ausgabepin blockiert ist, oder, wenn der Aufrufer den Block Vorgang abbricht.</span><span class="sxs-lookup"><span data-stu-id="f5589-111">The event is signaled when the output pin is blocked, or if the caller cancels the block operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5589-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f5589-112">Return value</span></span>

<span data-ttu-id="f5589-113">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="f5589-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="f5589-114">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f5589-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="f5589-115">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="f5589-115">Return code</span></span>                                                                                                                    | <span data-ttu-id="f5589-116">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f5589-116">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="f5589-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f5589-117"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="f5589-118">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="f5589-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="f5589-119"><dt>**VFW \_ E \_ Pin \_ bereits \_ blockiert**</dt></span><span class="sxs-lookup"><span data-stu-id="f5589-119"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="f5589-120">Die PIN ist bereits in einem anderen Thread blockiert.</span><span class="sxs-lookup"><span data-stu-id="f5589-120">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="f5589-121"><dt>**VFW \_ E \_ Pin \_ ist \_ \_ in \_ diesem \_ Thread bereits blockiert.**</dt></span><span class="sxs-lookup"><span data-stu-id="f5589-121"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="f5589-122">Die PIN ist bereits im aufrufenden Thread blockiert.</span><span class="sxs-lookup"><span data-stu-id="f5589-122">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f5589-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f5589-123">Remarks</span></span>

<span data-ttu-id="f5589-124">Diese Methode nicht aus dem streamingthread aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="f5589-124">Do not call this method from the streaming thread.</span></span>

<span data-ttu-id="f5589-125">Wenn kein streamingingthread die PIN verwendet, blockiert diese Methode sofort die PIN.</span><span class="sxs-lookup"><span data-stu-id="f5589-125">If no streaming thread is using the pin, this method immediately blocks the pin.</span></span> <span data-ttu-id="f5589-126">Andernfalls wird der PIN-Status auf "Pending" festgelegt, und es wird zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5589-126">Otherwise, it sets the pin status to "pending" and returns.</span></span> <span data-ttu-id="f5589-127">Wenn der Streamingvorgang abgeschlossen ist, ruft der streamingthread die [**cdynamicoutputpin:: stopusingoutputpin**](cdynamicoutputpin-stopusingoutputpin.md) -Methode auf, die die PIN blockiert und das **hnotifycallerpinblockedevent** -Ereignis signalisiert.</span><span class="sxs-lookup"><span data-stu-id="f5589-127">When the streaming operation completes, the streaming thread calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, which blocks the pin and signals the **hNotifyCallerPinBlockedEvent** event.</span></span> <span data-ttu-id="f5589-128">Um einen ausstehenden Block abzubrechen, rufen Sie die [**cdynamicoutputpin:: unblockoutputpin**](cdynamicoutputpin-unblockoutputpin.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="f5589-128">To cancel a pending block, call the [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5589-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f5589-129">Requirements</span></span>



| <span data-ttu-id="f5589-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f5589-130">Requirement</span></span> | <span data-ttu-id="f5589-131">Wert</span><span class="sxs-lookup"><span data-stu-id="f5589-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5589-132">Header</span><span class="sxs-lookup"><span data-stu-id="f5589-132">Header</span></span><br/>  | <dl> <span data-ttu-id="f5589-133"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f5589-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f5589-134">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f5589-134">Library</span></span><br/> | <dl> <span data-ttu-id="f5589-135">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f5589-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5589-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f5589-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5589-137">**Cdynamicoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f5589-137">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




