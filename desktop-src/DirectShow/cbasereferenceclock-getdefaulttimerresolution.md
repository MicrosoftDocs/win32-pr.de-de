---
description: Die getdefaulttimerresolution-Methode gibt die aktuelle Auflösung des Zeit Gebers der verweisuhr zurück.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Cbasereferenceclock. getdefaulttimerresolution-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352986"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a><span data-ttu-id="d48c2-103">Cbasereferenceclock. getdefaulttimerresolution-Methode</span><span class="sxs-lookup"><span data-stu-id="d48c2-103">CBaseReferenceClock.GetDefaultTimerResolution method</span></span>

<span data-ttu-id="d48c2-104">Die `GetDefaultTimerResolution` -Methode gibt die aktuelle Auflösung des Zeit Gebers der verweisuhr zurück.</span><span class="sxs-lookup"><span data-stu-id="d48c2-104">The `GetDefaultTimerResolution` method returns the current resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d48c2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d48c2-105">Syntax</span></span>


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="d48c2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d48c2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d48c2-107">*ptimerresolution*</span><span class="sxs-lookup"><span data-stu-id="d48c2-107">*pTimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="d48c2-108">Empfängt die angeforderte Zeit Geber Auflösung in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="d48c2-108">Receives the requested timer resolution, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d48c2-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d48c2-109">Return value</span></span>

<span data-ttu-id="d48c2-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d48c2-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d48c2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d48c2-111">Remarks</span></span>

<span data-ttu-id="d48c2-112">Diese Methode implementiert die [**ireferenceclocktimercontrol:: getdefaulttimerresolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) -Methode.</span><span class="sxs-lookup"><span data-stu-id="d48c2-112">This method implements the [**IReferenceClockTimerControl::GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d48c2-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d48c2-113">Requirements</span></span>



| <span data-ttu-id="d48c2-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d48c2-114">Requirement</span></span> | <span data-ttu-id="d48c2-115">Wert</span><span class="sxs-lookup"><span data-stu-id="d48c2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d48c2-116">Header</span><span class="sxs-lookup"><span data-stu-id="d48c2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="d48c2-117"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d48c2-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d48c2-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d48c2-118">Library</span></span><br/> | <dl> <span data-ttu-id="d48c2-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d48c2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d48c2-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d48c2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d48c2-121">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d48c2-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




