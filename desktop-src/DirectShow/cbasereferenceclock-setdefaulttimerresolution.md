---
description: Die setdefaulttimerresolution-Methode legt die Auflösung des Zeit Gebers der verweisuhr fest.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Cbasereferenceclock. setdefaulttimerresolution-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366873"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a><span data-ttu-id="78b90-103">Cbasereferenceclock. setdefaulttimerresolution-Methode</span><span class="sxs-lookup"><span data-stu-id="78b90-103">CBaseReferenceClock.SetDefaultTimerResolution method</span></span>

<span data-ttu-id="78b90-104">Die `SetDefaultTimerResolution` -Methode legt die Auflösung des Zeit Gebers der verweisuhr fest.</span><span class="sxs-lookup"><span data-stu-id="78b90-104">The `SetDefaultTimerResolution` method sets the resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="78b90-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="78b90-105">Syntax</span></span>


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="78b90-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78b90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78b90-107">*timerresolution*</span><span class="sxs-lookup"><span data-stu-id="78b90-107">*timerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="78b90-108">Minimale Zeit Geber Auflösung in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="78b90-108">Minimum timer resolution, in 100-nanosecond units.</span></span> <span data-ttu-id="78b90-109">Wenn der Wert 0 (null) ist, bricht die Referenzuhr die vorherige Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="78b90-109">If the value is zero, the reference clock cancels its previous request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78b90-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78b90-110">Return value</span></span>

<span data-ttu-id="78b90-111">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78b90-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78b90-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78b90-112">Remarks</span></span>

<span data-ttu-id="78b90-113">Diese Methode implementiert die [**ireferenceclocktimercontrol:: setdefaulttimerresolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) -Methode.</span><span class="sxs-lookup"><span data-stu-id="78b90-113">This method implements the [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="78b90-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78b90-114">Requirements</span></span>



| <span data-ttu-id="78b90-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78b90-115">Requirement</span></span> | <span data-ttu-id="78b90-116">Wert</span><span class="sxs-lookup"><span data-stu-id="78b90-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78b90-117">Header</span><span class="sxs-lookup"><span data-stu-id="78b90-117">Header</span></span><br/>  | <dl> <span data-ttu-id="78b90-118"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78b90-118"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="78b90-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78b90-119">Library</span></span><br/> | <dl> <span data-ttu-id="78b90-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="78b90-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78b90-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78b90-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78b90-122">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="78b90-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




