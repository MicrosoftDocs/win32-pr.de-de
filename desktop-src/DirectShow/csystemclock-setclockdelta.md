---
description: 'Die setclockdelta-Methode passt die Uhrzeit an. Diese Methode implementiert die iamclockadjust:: setclockdelta-Methode.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Csystemclock. setclockdelta-Methode (sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355270"
---
# <a name="csystemclocksetclockdelta-method"></a><span data-ttu-id="3519a-104">Csystemclock. setclockdelta-Methode</span><span class="sxs-lookup"><span data-stu-id="3519a-104">CSystemClock.SetClockDelta method</span></span>

<span data-ttu-id="3519a-105">Die- `SetClockDelta` Methode passt die Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="3519a-105">The `SetClockDelta` method adjusts the clock time.</span></span> <span data-ttu-id="3519a-106">Diese Methode implementiert die [**iamclockadjust:: setclockdelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3519a-106">This method implements the [**IAMClockAdjust::SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3519a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3519a-107">Syntax</span></span>


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a><span data-ttu-id="3519a-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="3519a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3519a-109">*rtdelta*</span><span class="sxs-lookup"><span data-stu-id="3519a-109">*rtDelta*</span></span> 
</dt> <dd>

<span data-ttu-id="3519a-110">Gibt den Betrag an, um den die Uhr als [**Verweis \_ Zeitwert**](reference-time.md) angepasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="3519a-110">Specifies the amount by which to adjust the clock, as a [**REFERENCE\_TIME**](reference-time.md) value.</span></span> <span data-ttu-id="3519a-111">Ein positiver Wert verschiebt die Uhr vorwärts, und ein negativer Wert verschiebt die Uhr nach unten.</span><span class="sxs-lookup"><span data-stu-id="3519a-111">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3519a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3519a-112">Return value</span></span>

<span data-ttu-id="3519a-113">Gibt S \_ OK oder einen **HRESULT** -Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="3519a-113">Returns S\_OK or an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3519a-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3519a-114">Remarks</span></span>

<span data-ttu-id="3519a-115">Diese Methode ruft einfach [**cbasereferenceclock:: settimedelta**](cbasereferenceclock-settimedelta.md)auf.</span><span class="sxs-lookup"><span data-stu-id="3519a-115">This method simply calls [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span></span>

<span data-ttu-id="3519a-116">Die von [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) zurückgegebenen Zeit Werte werden monoton vergrößert.</span><span class="sxs-lookup"><span data-stu-id="3519a-116">The time values returned by [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) are monotonically increasing.</span></span> <span data-ttu-id="3519a-117">Wenn Sie die Uhr wieder festlegen, meldet **GetTime** weiterhin die alte Zeit, bis die interne Uhr abfängt.</span><span class="sxs-lookup"><span data-stu-id="3519a-117">If you set the clock back, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="3519a-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3519a-118">Requirements</span></span>



| <span data-ttu-id="3519a-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3519a-119">Requirement</span></span> | <span data-ttu-id="3519a-120">Wert</span><span class="sxs-lookup"><span data-stu-id="3519a-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3519a-121">Version</span><span class="sxs-lookup"><span data-stu-id="3519a-121">Version</span></span><br/> | <span data-ttu-id="3519a-122">Csystemclock-Klasse</span><span class="sxs-lookup"><span data-stu-id="3519a-122">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="3519a-123">Header</span><span class="sxs-lookup"><span data-stu-id="3519a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3519a-124"><dt>Sysclock. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-124"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3519a-125">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3519a-125">Library</span></span><br/> | <dl> <span data-ttu-id="3519a-126">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3519a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




