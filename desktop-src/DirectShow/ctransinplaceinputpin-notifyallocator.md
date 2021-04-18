---
description: 'Die notifyzucator-Methode gibt eine Zuweisung für die Verbindung an. Mit dieser Methode wird die IMemInputPin:: notifyzucator-Methode implementiert.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Ctransinplaceinputpin. notifyzucator-Methode (transip. h)
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
ms.openlocfilehash: 74578243ce780e09d7435f9dd4b70bd9497e1e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357596"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="de8b9-104">Ctransinplaceinputpin. notifyzucator-Methode</span><span class="sxs-lookup"><span data-stu-id="de8b9-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="de8b9-105">Die- `NotifyAllocator` Methode gibt eine Zuweisung für die Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="de8b9-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="de8b9-106">Mit dieser Methode wird die [**IMemInputPin:: notifyzucator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) -Methode implementiert.</span><span class="sxs-lookup"><span data-stu-id="de8b9-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="de8b9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="de8b9-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="de8b9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="de8b9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="de8b9-109">*pallocator*</span><span class="sxs-lookup"><span data-stu-id="de8b9-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="de8b9-110">Ein Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners.</span><span class="sxs-lookup"><span data-stu-id="de8b9-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="de8b9-111">*nur Bread*</span><span class="sxs-lookup"><span data-stu-id="de8b9-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="de8b9-112">Flag, das angibt, ob Beispiele aus dieser Zuweisung schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="de8b9-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="de8b9-113">**True** gibt an, dass die Beispiele schreibgeschützt sind.</span><span class="sxs-lookup"><span data-stu-id="de8b9-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="de8b9-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de8b9-114">Return value</span></span>

<span data-ttu-id="de8b9-115">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de8b9-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="de8b9-116">Mögliche Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="de8b9-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="de8b9-117">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="de8b9-117">Return code</span></span>                                                                               | <span data-ttu-id="de8b9-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de8b9-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="de8b9-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="de8b9-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="de8b9-120">Erfolg</span><span class="sxs-lookup"><span data-stu-id="de8b9-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="de8b9-121"><dt>**E \_ fehlschlagen**</dt></span><span class="sxs-lookup"><span data-stu-id="de8b9-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="de8b9-122">Fehler</span><span class="sxs-lookup"><span data-stu-id="de8b9-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="de8b9-123"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="de8b9-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="de8b9-124">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="de8b9-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="de8b9-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de8b9-125">Remarks</span></span>

<span data-ttu-id="de8b9-126">Der Filter versucht, die gleiche Zuweisung für beide Pin-Verbindungen zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="de8b9-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="de8b9-127">Wenn die Ausgabe-PIN nicht verbunden ist, akzeptiert die Eingabe-PIN automatisch die Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="de8b9-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="de8b9-128">Wenn die Ausgabe-PIN verbunden ist, stellt der Filter erneut eine Verbindung mit der eingabepin her.</span><span class="sxs-lookup"><span data-stu-id="de8b9-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="de8b9-129">An diesem Punkt versucht der Filter erneut, eine einzelne Zuweisung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="de8b9-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="de8b9-130">Wenn die Ausgabe-PIN verbunden ist, akzeptiert die Eingabe-PIN die Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="de8b9-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="de8b9-131">Die Ausgabe-PIN verwendet auch die gleiche Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="de8b9-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="de8b9-132">Er ruft `NotifyAllocator` für die downstreameingabepin auf.</span><span class="sxs-lookup"><span data-stu-id="de8b9-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="de8b9-133">Der vorherige Fall hat die folgende Ausnahme:</span><span class="sxs-lookup"><span data-stu-id="de8b9-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="de8b9-134">Wenn die vorgeschlagene Zuweisung schreibgeschützt ist (d. h., der *bReadOnly* -Parameter ist **true**) und der Filter die Beispiele ändern muss, muss der Filter zwei verschiedene Zuweisungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="de8b9-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="de8b9-135">Wenn der upstreamfilter in diesem Fall vorschlägt, die Zuweisung des downstreamfilters zu verwenden, gibt die Methode E \_ Fail zurück.</span><span class="sxs-lookup"><span data-stu-id="de8b9-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="de8b9-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de8b9-136">Requirements</span></span>



| <span data-ttu-id="de8b9-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de8b9-137">Requirement</span></span> | <span data-ttu-id="de8b9-138">Wert</span><span class="sxs-lookup"><span data-stu-id="de8b9-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de8b9-139">Header</span><span class="sxs-lookup"><span data-stu-id="de8b9-139">Header</span></span><br/>  | <dl> <span data-ttu-id="de8b9-140"><dt>Transip. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de8b9-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="de8b9-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de8b9-141">Library</span></span><br/> | <dl> <span data-ttu-id="de8b9-142">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="de8b9-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de8b9-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de8b9-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de8b9-144">**Ctransinplaceinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="de8b9-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




