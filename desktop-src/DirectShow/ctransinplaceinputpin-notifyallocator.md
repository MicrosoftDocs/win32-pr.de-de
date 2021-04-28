---
description: 'CTransInPlaceInputPin.NotifyAllocator-Methode: Die NotifyAllocator-Methode gibt eine Zuweisung für die Verbindung an. Diese Methode implementiert die IMemInputPin::NotifyAllocator-Methode.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: CTransInPlaceInputPin.NotifyAllocator-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca15be5dc1893a393e6052832cc7522f27355eeb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094748"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="7099f-104">CTransInPlaceInputPin.NotifyAllocator-Methode</span><span class="sxs-lookup"><span data-stu-id="7099f-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="7099f-105">Die `NotifyAllocator` -Methode gibt eine Zuweisung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="7099f-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="7099f-106">Diese Methode implementiert die [**IMemInputPin::NotifyAllocator-Methode.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)</span><span class="sxs-lookup"><span data-stu-id="7099f-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="7099f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="7099f-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="7099f-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="7099f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7099f-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="7099f-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="7099f-110">Zeiger auf die [**IMemAllocator-Schnittstelle der Zuweisung.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)</span><span class="sxs-lookup"><span data-stu-id="7099f-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="7099f-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="7099f-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="7099f-112">Flag, das angibt, ob Beispiele aus dieser Zuweisung schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="7099f-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="7099f-113">True **gibt an,** dass Beispiele schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="7099f-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7099f-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7099f-114">Return value</span></span>

<span data-ttu-id="7099f-115">Gibt einen **HRESULT-Wert** zurück.</span><span class="sxs-lookup"><span data-stu-id="7099f-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7099f-116">Mögliche Werte sind die in der folgenden Tabelle gezeigten Werte.</span><span class="sxs-lookup"><span data-stu-id="7099f-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7099f-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="7099f-117">Return code</span></span>                                                                               | <span data-ttu-id="7099f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7099f-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="7099f-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7099f-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="7099f-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="7099f-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="7099f-121"><dt>**E \_ FAIL**</dt></span><span class="sxs-lookup"><span data-stu-id="7099f-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="7099f-122">Fehler</span><span class="sxs-lookup"><span data-stu-id="7099f-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="7099f-123"><dt>**\_E-ZEIGER**</dt></span><span class="sxs-lookup"><span data-stu-id="7099f-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="7099f-124">**NULL-Zeigerargument**</span><span class="sxs-lookup"><span data-stu-id="7099f-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7099f-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7099f-125">Remarks</span></span>

<span data-ttu-id="7099f-126">Der Filter versucht, dieselbe Zuweisung für beide Pinverbindungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7099f-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="7099f-127">Wenn der Ausgabepin nicht verbunden ist, akzeptiert der Eingabepin automatisch die Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="7099f-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="7099f-128">Wenn der Ausgabepin verbunden ist, verbindet der Filter den Eingabepin erneut.</span><span class="sxs-lookup"><span data-stu-id="7099f-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="7099f-129">An diesem Punkt versucht der Filter erneut, eine einzelne Zuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7099f-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="7099f-130">Wenn der Ausgabepin verbunden ist, akzeptiert der Eingabepin die Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="7099f-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="7099f-131">Der Ausgabepin verwendet auch die gleiche Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="7099f-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="7099f-132">Er ruft `NotifyAllocator` auf dem nachgeschalteten Eingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="7099f-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="7099f-133">Der vorherige Fall weist die folgende Ausnahme auf:</span><span class="sxs-lookup"><span data-stu-id="7099f-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="7099f-134">Wenn die vorgeschlagene Zuweisung schreibgeschützt ist (d. h., der *bReadOnly-Parameter* ist **TRUE),** und der Filter die Stichproben ändern muss, muss der Filter zwei verschiedene Zuweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="7099f-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="7099f-135">Wenn der Upstreamfilter in diesem Fall die Verwendung der Zuweisung des Downstreamfilters vorschlägt, gibt die Methode E \_ FAIL zurück.</span><span class="sxs-lookup"><span data-stu-id="7099f-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="7099f-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7099f-136">Requirements</span></span>



| <span data-ttu-id="7099f-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7099f-137">Requirement</span></span> | <span data-ttu-id="7099f-138">Wert</span><span class="sxs-lookup"><span data-stu-id="7099f-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7099f-139">Header</span><span class="sxs-lookup"><span data-stu-id="7099f-139">Header</span></span><br/>  | <dl> <span data-ttu-id="7099f-140"><dt>Transip.h (include Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="7099f-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7099f-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7099f-141">Library</span></span><br/> | <dl> <span data-ttu-id="7099f-142"><dt>Strmbase.lib (Verkaufsbuilds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7099f-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7099f-143">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7099f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7099f-144">**CTransInPlaceInputPin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7099f-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




