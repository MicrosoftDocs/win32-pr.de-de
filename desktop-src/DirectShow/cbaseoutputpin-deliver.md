---
description: Die Deliver-Methode übergibt ein Medien Beispiel an die verbundene Eingabe-PIN.
ms.assetid: b871df84-c69e-42eb-9da9-c25996bf08c3
title: Cbaseoutputpin. Deliver-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.Deliver
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adc603e4cdd1f49e649264d2d82d6df0fb12569
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366864"
---
# <a name="cbaseoutputpindeliver-method"></a><span data-ttu-id="d5d4b-103">Cbaseoutputpin. Deliver-Methode</span><span class="sxs-lookup"><span data-stu-id="d5d4b-103">CBaseOutputPin.Deliver method</span></span>

<span data-ttu-id="d5d4b-104">Die- `Deliver` Methode übermittelt ein Medien Beispiel an die verbundene Eingabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-104">The `Deliver` method delivers a media sample to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5d4b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5d4b-105">Syntax</span></span>


```C++
virtual HRESULT Deliver(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="d5d4b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d5d4b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5d4b-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="d5d4b-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d5d4b-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5d4b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d5d4b-109">Return value</span></span>

<span data-ttu-id="d5d4b-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d5d4b-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-111">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="d5d4b-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="d5d4b-112">Return code</span></span>                                                                                           | <span data-ttu-id="d5d4b-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5d4b-113">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d5d4b-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d5d4b-114"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="d5d4b-115">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-115">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="d5d4b-116"><dt>**VFW \_ E \_ nicht \_ verbunden**</dt></span><span class="sxs-lookup"><span data-stu-id="d5d4b-116"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="d5d4b-117">Die PIN ist nicht verbunden.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-117">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d5d4b-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d5d4b-118">Remarks</span></span>

<span data-ttu-id="d5d4b-119">Diese Methode ruft die [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode für die Eingabe-PIN auf.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-119">This method calls the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method on the input pin.</span></span> <span data-ttu-id="d5d4b-120">**Receive** kann blockieren, wenn die [**IMemInputPin:: receivecanblock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) -Methode S OK zurückgibt \_ .</span><span class="sxs-lookup"><span data-stu-id="d5d4b-120">**Receive** can block if the [**IMemInputPin::ReceiveCanBlock**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivecanblock) method returns S\_OK.</span></span>

<span data-ttu-id="d5d4b-121">Geben Sie das Beispiel nach dem Aufrufen dieser Methode frei.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-121">Release the sample after calling this method.</span></span> <span data-ttu-id="d5d4b-122">Die Eingabe-PIN kann einen Verweis Zähler für das Beispiel enthalten. verwenden Sie daher nicht das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-122">The input pin might hold a reference count on the sample, so do not reuse the sample.</span></span> <span data-ttu-id="d5d4b-123">Rufen Sie immer die [**cbaseoutputpin:: getdeliverybuffer**](cbaseoutputpin-getdeliverybuffer.md) -Methode auf, um ein neues Beispiel zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-123">Always call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain a new sample.</span></span>

<span data-ttu-id="d5d4b-124">Speichern Sie den kritischen Abschnitt des Filters, bevor Sie diese Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-124">Hold the filter's critical section before calling this method.</span></span> <span data-ttu-id="d5d4b-125">Andernfalls wird die PIN während des Methoden Aufrufes möglicherweise getrennt.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-125">Otherwise, the pin might get disconnected during the method call.</span></span> <span data-ttu-id="d5d4b-126">Wenn der Filter einen Arbeits Thread zum Übermitteln von Beispielen verwendet, halten Sie den kritischen Abschnitt gedrückt, wenn der Filter bereit ist, ein Beispiel zu liefern.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-126">If the filter uses a worker thread to deliver samples, hold the critical section when the filter is ready to deliver a sample.</span></span> <span data-ttu-id="d5d4b-127">Andernfalls können Sie den kritischen Abschnitt in der [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) -Methode des Filters speichern, in dem der Filter Beispiele verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-127">Otherwise, you can hold the critical section in the filter's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, where the filter processes samples.</span></span>

<span data-ttu-id="d5d4b-128">Arbeitsthreads können zu einem möglichen Deadlock führen.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-128">Worker threads can create a potential deadlock.</span></span> <span data-ttu-id="d5d4b-129">Wenn der Thread den kritischen Abschnitt enthält, kann er auf eine Zustandsänderung im Filter warten.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-129">When the thread holds the critical section, it might wait on a state change in the filter.</span></span> <span data-ttu-id="d5d4b-130">Gleichzeitig wartet die Zustandsänderung möglicherweise darauf, dass der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-130">At the same time, the state change might be waiting for the thread to complete.</span></span> <span data-ttu-id="d5d4b-131">Um dies zu verhindern, sollte der Code für die Zustandsänderung ein Ereignis signalisieren, das den Thread beendet, und dann auf den Abschluss des Threads warten.</span><span class="sxs-lookup"><span data-stu-id="d5d4b-131">To prevent this, the state-change code should signal an event that terminates the thread, and then wait for the thread to signal completion.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5d4b-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d5d4b-132">Requirements</span></span>



| <span data-ttu-id="d5d4b-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d5d4b-133">Requirement</span></span> | <span data-ttu-id="d5d4b-134">Wert</span><span class="sxs-lookup"><span data-stu-id="d5d4b-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5d4b-135">Header</span><span class="sxs-lookup"><span data-stu-id="d5d4b-135">Header</span></span><br/>  | <dl> <span data-ttu-id="d5d4b-136"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5d4b-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d5d4b-137">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d5d4b-137">Library</span></span><br/> | <dl> <span data-ttu-id="d5d4b-138">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d5d4b-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5d4b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d5d4b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5d4b-140">**Cbaseoutputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d5d4b-140">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




