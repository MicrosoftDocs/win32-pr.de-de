---
description: Die settimedelta-Methode passt die interne Uhrzeit an.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Cbasereferenceclock. settimedelta-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367778"
---
# <a name="cbasereferenceclocksettimedelta-method"></a><span data-ttu-id="cc4f1-103">Cbasereferenceclock. settimedelta-Methode</span><span class="sxs-lookup"><span data-stu-id="cc4f1-103">CBaseReferenceClock.SetTimeDelta method</span></span>

<span data-ttu-id="cc4f1-104">Die- `SetTimeDelta` Methode passt die interne Uhrzeit an.</span><span class="sxs-lookup"><span data-stu-id="cc4f1-104">The `SetTimeDelta` method adjusts the internal clock time.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc4f1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cc4f1-105">Syntax</span></span>


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a><span data-ttu-id="cc4f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cc4f1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc4f1-107">*Timedelta* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="cc4f1-107">*TimeDelta* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="cc4f1-108">Der Wert für die Anpassung der Uhrzeitangabe in 100-Nanosecond-Einheiten.</span><span class="sxs-lookup"><span data-stu-id="cc4f1-108">Amount to adjust the clock time, in 100-nanosecond units.</span></span> <span data-ttu-id="cc4f1-109">Ein positiver Wert verschiebt die Uhr vorwärts, und ein negativer Wert verschiebt die Uhr nach unten.</span><span class="sxs-lookup"><span data-stu-id="cc4f1-109">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc4f1-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cc4f1-110">Return value</span></span>

<span data-ttu-id="cc4f1-111">Gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="cc4f1-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cc4f1-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cc4f1-112">Remarks</span></span>

<span data-ttu-id="cc4f1-113">Diese Methode kann von der abgeleiteten Klasse verwendet werden, um die interne Uhr anzupassen, wenn Sie von dem Gerät abweicht, das Zeit Steuerungsinformationen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cc4f1-113">The derived class can use this method to adjust the internal clock, if it drifts from the device that is providing timing information.</span></span>

<span data-ttu-id="cc4f1-114">Die [**cbasereferenceclock:: getTime**](cbasereferenceclock-gettime.md) -Methode gibt keine abnehmenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cc4f1-114">The [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method never returns decreasing values.</span></span> <span data-ttu-id="cc4f1-115">Wenn Sie die Uhr rückwärts anpassen, gibt **GetTime** den vorherigen Wert zurück, bis die Uhr diesen Wert wieder erreicht.</span><span class="sxs-lookup"><span data-stu-id="cc4f1-115">If you adjust the clock backward, **GetTime** returns the previous value until the clock reaches that value again.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc4f1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cc4f1-116">Requirements</span></span>



| <span data-ttu-id="cc4f1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cc4f1-117">Requirement</span></span> | <span data-ttu-id="cc4f1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="cc4f1-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cc4f1-119">Header</span><span class="sxs-lookup"><span data-stu-id="cc4f1-119">Header</span></span><br/>  | <dl> <span data-ttu-id="cc4f1-120"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4f1-120"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cc4f1-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="cc4f1-121">Library</span></span><br/> | <dl> <span data-ttu-id="cc4f1-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="cc4f1-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc4f1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cc4f1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc4f1-124">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="cc4f1-124">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




