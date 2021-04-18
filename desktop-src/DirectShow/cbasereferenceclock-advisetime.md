---
description: 'Die adviantime-Methode erstellt eine One-Shot-anforderungsanforderung. Diese Methode implementiert die IReferenceClock:: adviabtime-Methode.'
ms.assetid: 4849a04d-35f2-4a24-bf5d-f20e541f5e99
title: Cbasereferenceclock. adviantime-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 326fc5e0939803ab66e0466fbf32351387977019
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372158"
---
# <a name="cbasereferenceclockadvisetime-method"></a><span data-ttu-id="ff239-104">Cbasereferenceclock. advientime-Methode</span><span class="sxs-lookup"><span data-stu-id="ff239-104">CBaseReferenceClock.AdviseTime method</span></span>

<span data-ttu-id="ff239-105">Die `AdviseTime` -Methode erstellt eine One-Shot-anforderungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="ff239-105">The `AdviseTime` method creates a one-shot advise request.</span></span> <span data-ttu-id="ff239-106">Diese Methode implementiert die [**IReferenceClock:: adviabtime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ff239-106">This method implements the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ff239-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff239-107">Syntax</span></span>


```C++
HRESULT AdviseTime(
   REFERENCE_TIME baseTime,
   REFERENCE_TIME streamTime,
   HEVENT         hEvent,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="ff239-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ff239-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff239-109">*baseTime*</span><span class="sxs-lookup"><span data-stu-id="ff239-109">*baseTime*</span></span> 
</dt> <dd>

<span data-ttu-id="ff239-110">Basis Verweis Zeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="ff239-110">Base reference time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="ff239-111">*streamtime*</span><span class="sxs-lookup"><span data-stu-id="ff239-111">*streamTime*</span></span> 
</dt> <dd>

<span data-ttu-id="ff239-112">Streamoffset Zeit in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="ff239-112">Stream offset time, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="ff239-113">*hevent*</span><span class="sxs-lookup"><span data-stu-id="ff239-113">*hEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="ff239-114">Handle für ein Ereignis, das vom Aufrufer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="ff239-114">Handle to an event, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="ff239-115">*pdwadvistoken*</span><span class="sxs-lookup"><span data-stu-id="ff239-115">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="ff239-116">Ein Zeiger auf eine Variable, die einen Bezeichner für die Benachrichtigungs Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="ff239-116">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff239-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ff239-117">Return value</span></span>

<span data-ttu-id="ff239-118">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="ff239-118">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="ff239-119">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ff239-119">Return code</span></span>                                                                                   | <span data-ttu-id="ff239-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ff239-120">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="ff239-121"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ff239-121"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="ff239-122">Erfolg</span><span class="sxs-lookup"><span data-stu-id="ff239-122">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="ff239-123"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="ff239-123"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="ff239-124">Ungültige Zeitwerte.</span><span class="sxs-lookup"><span data-stu-id="ff239-124">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="ff239-125"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="ff239-125"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="ff239-126">Fehler</span><span class="sxs-lookup"><span data-stu-id="ff239-126">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="ff239-127"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="ff239-127"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="ff239-128">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="ff239-128">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ff239-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ff239-129">Remarks</span></span>

<span data-ttu-id="ff239-130">Diese Methode erstellt eine One-Shot-anforderungsanforderung für die Referenzzeit *baseTime*  +  *streamtime*.</span><span class="sxs-lookup"><span data-stu-id="ff239-130">This method creates a one-shot advise request for the reference time *baseTime* + *streamTime*.</span></span> <span data-ttu-id="ff239-131">Die Summe muss größer als 0 (null) und kleiner als \_ die maximale Zeit sein, oder die Methode gibt E \_ invalidArg zurück.</span><span class="sxs-lookup"><span data-stu-id="ff239-131">The sum must be greater than zero and less than MAX\_TIME, or the method returns E\_INVALIDARG.</span></span> <span data-ttu-id="ff239-132">Die Uhr signalisiert zum angeforderten Zeitpunkt das Ereignis, das im *hevent* -Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="ff239-132">At the requested time, the clock signals the event specified in the *hEvent* parameter.</span></span>

<span data-ttu-id="ff239-133">Um die Benachrichtigung abzubrechen, bevor die Zeit erreicht ist, rufen Sie die [**cbasereferenceclock:: unadvi-Methode**](cbasereferenceclock-unadvise.md) auf, und übergeben Sie den von diesem Aufruf zurückgegebenen *pdwadvistoken* -Wert.</span><span class="sxs-lookup"><span data-stu-id="ff239-133">To cancel the notification before the time is reached, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span> <span data-ttu-id="ff239-134">Nachdem die Benachrichtigung erfolgt ist, wird Sie von der Uhr automatisch gelöscht. Daher ist es nicht erforderlich, die **Empfehlung "nicht empfohlen**" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ff239-134">After the notification has occurred, the clock automatically clears it, so it is not necessary to call **Unadvise**.</span></span> <span data-ttu-id="ff239-135">Dies ist jedoch kein Fehler.</span><span class="sxs-lookup"><span data-stu-id="ff239-135">However, it is not an error to do so.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff239-136">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ff239-136">Requirements</span></span>



| <span data-ttu-id="ff239-137">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ff239-137">Requirement</span></span> | <span data-ttu-id="ff239-138">Wert</span><span class="sxs-lookup"><span data-stu-id="ff239-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ff239-139">Header</span><span class="sxs-lookup"><span data-stu-id="ff239-139">Header</span></span><br/>  | <dl> <span data-ttu-id="ff239-140"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ff239-140"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ff239-141">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ff239-141">Library</span></span><br/> | <dl> <span data-ttu-id="ff239-142">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ff239-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff239-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ff239-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff239-144">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ff239-144">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




