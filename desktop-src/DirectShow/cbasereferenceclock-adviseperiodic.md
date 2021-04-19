---
description: 'Die advianperiodische-Methode erstellt eine regelmäßige anforderungsanforderung. Diese Methode implementiert die IReferenceClock:: advienperiodische-Methode.'
ms.assetid: ddaf0861-df11-4008-8e9c-a0c53929cd3f
title: Cbasereferenceclock. advianperiodische Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.AdvisePeriodic
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a582e05756e8d034e5b2d0a1cd8f7eb569dbb842
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370223"
---
# <a name="cbasereferenceclockadviseperiodic-method"></a><span data-ttu-id="e62d4-104">Cbasereferenceclock. advisperiodische-Methode</span><span class="sxs-lookup"><span data-stu-id="e62d4-104">CBaseReferenceClock.AdvisePeriodic method</span></span>

<span data-ttu-id="e62d4-105">Die- `AdvisePeriodic` Methode erstellt eine regelmäßige anforderungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="e62d4-105">The `AdvisePeriodic` method creates a periodic advise request.</span></span> <span data-ttu-id="e62d4-106">Diese Methode implementiert die [**IReferenceClock:: advienperiodische**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) -Methode.</span><span class="sxs-lookup"><span data-stu-id="e62d4-106">This method implements the [**IReferenceClock::AdvisePeriodic**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-adviseperiodic) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e62d4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e62d4-107">Syntax</span></span>


```C++
HRESULT AdvisePeriodic(
   REFERENCE_TIME StartTime,
   REFERENCE_TIME PeriodTime,
   HSEMAPHORE     hSemaphore,
   DWORD_PTR      *pdwAdviseToken
);
```



## <a name="parameters"></a><span data-ttu-id="e62d4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="e62d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e62d4-109">*StartTime*</span><span class="sxs-lookup"><span data-stu-id="e62d4-109">*StartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e62d4-110">Zeitpunkt der ersten Benachrichtigung in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="e62d4-110">Time of the first notification, in 100-nanosecond units.</span></span> <span data-ttu-id="e62d4-111">Muss größer als 0 (null) und kleiner als die maximale \_ Zeit sein.</span><span class="sxs-lookup"><span data-stu-id="e62d4-111">Must be greater than zero and less than MAX\_TIME.</span></span>

</dd> <dt>

<span data-ttu-id="e62d4-112">*Periodtime*</span><span class="sxs-lookup"><span data-stu-id="e62d4-112">*PeriodTime*</span></span> 
</dt> <dd>

<span data-ttu-id="e62d4-113">Zeit zwischen Benachrichtigungen in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="e62d4-113">Time between notifications, in 100-nanosecond units.</span></span> <span data-ttu-id="e62d4-114">Muss größer sein als Null.</span><span class="sxs-lookup"><span data-stu-id="e62d4-114">Must be greater than zero.</span></span>

</dd> <dt>

<span data-ttu-id="e62d4-115">*hsemaphore*</span><span class="sxs-lookup"><span data-stu-id="e62d4-115">*hSemaphore*</span></span> 
</dt> <dd>

<span data-ttu-id="e62d4-116">Handle für ein Semaphor, das vom Aufrufer erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="e62d4-116">Handle to a semaphore, created by the caller.</span></span>

</dd> <dt>

<span data-ttu-id="e62d4-117">*pdwadvistoken*</span><span class="sxs-lookup"><span data-stu-id="e62d4-117">*pdwAdviseToken*</span></span> 
</dt> <dd>

<span data-ttu-id="e62d4-118">Ein Zeiger auf eine Variable, die einen Bezeichner für die Benachrichtigungs Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="e62d4-118">Pointer to a variable that receives an identifier for the advise request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e62d4-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e62d4-119">Return value</span></span>

<span data-ttu-id="e62d4-120">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e62d4-120">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="e62d4-121">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="e62d4-121">Return code</span></span>                                                                                   | <span data-ttu-id="e62d4-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e62d4-122">Description</span></span>                          |
|-----------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="e62d4-123"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="e62d4-123"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="e62d4-124">Erfolg</span><span class="sxs-lookup"><span data-stu-id="e62d4-124">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="e62d4-125"><dt>**E \_ invalidArg**</dt></span><span class="sxs-lookup"><span data-stu-id="e62d4-125"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="e62d4-126">Ungültige Zeitwerte.</span><span class="sxs-lookup"><span data-stu-id="e62d4-126">Invalid time values</span></span><br/>       |
| <dl> <span data-ttu-id="e62d4-127"><dt>**E \_ outo-Memory**</dt></span><span class="sxs-lookup"><span data-stu-id="e62d4-127"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="e62d4-128">Fehler</span><span class="sxs-lookup"><span data-stu-id="e62d4-128">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="e62d4-129"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="e62d4-129"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="e62d4-130">**Null** -Zeigerargument</span><span class="sxs-lookup"><span data-stu-id="e62d4-130">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e62d4-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e62d4-131">Remarks</span></span>

<span data-ttu-id="e62d4-132">Bei jeder Benachrichtigungs Zeit gibt die Uhr das im *hsemaphore* -Parameter angegebene Semaphor frei.</span><span class="sxs-lookup"><span data-stu-id="e62d4-132">At each notification time, the clock releases the semaphore specified in the *hSemaphore* parameter.</span></span> <span data-ttu-id="e62d4-133">Wenn keine weiteren Benachrichtigungen erforderlich sind, wenden Sie die [**cbasereferenceclock:: unadvi-Methode**](cbasereferenceclock-unadvise.md) an, und übergeben Sie den von diesem-Befehl zurückgegebenen *pdwadvistoken* -Wert.</span><span class="sxs-lookup"><span data-stu-id="e62d4-133">When no further notifications are required, call the [**CBaseReferenceClock::Unadvise**](cbasereferenceclock-unadvise.md) method and pass the *pdwAdviseToken* value returned from this call.</span></span>

## <a name="requirements"></a><span data-ttu-id="e62d4-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e62d4-134">Requirements</span></span>



| <span data-ttu-id="e62d4-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e62d4-135">Requirement</span></span> | <span data-ttu-id="e62d4-136">Wert</span><span class="sxs-lookup"><span data-stu-id="e62d4-136">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e62d4-137">Header</span><span class="sxs-lookup"><span data-stu-id="e62d4-137">Header</span></span><br/>  | <dl> <span data-ttu-id="e62d4-138"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e62d4-138"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e62d4-139">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e62d4-139">Library</span></span><br/> | <dl> <span data-ttu-id="e62d4-140">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e62d4-140"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e62d4-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e62d4-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e62d4-142">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e62d4-142">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




