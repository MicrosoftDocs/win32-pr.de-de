---
description: 'Die getTime-Methode ruft die aktuelle Verweis Zeit ab. Diese Methode implementiert die IReferenceClock:: getTime-Methode.'
ms.assetid: 4e4e5954-b899-4741-8b7c-7bc98a3f0404
title: Cbasereferenceclock. getTime-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a91f0015756d2ccfb545c4039d67434eb6d3c403
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361456"
---
# <a name="cbasereferenceclockgettime-method"></a><span data-ttu-id="67a5c-104">Cbasereferenceclock. getTime-Methode</span><span class="sxs-lookup"><span data-stu-id="67a5c-104">CBaseReferenceClock.GetTime method</span></span>

<span data-ttu-id="67a5c-105">Die- `GetTime` Methode ruft die aktuelle Verweis Zeit ab.</span><span class="sxs-lookup"><span data-stu-id="67a5c-105">The `GetTime` method retrieves the current reference time.</span></span> <span data-ttu-id="67a5c-106">Diese Methode implementiert die [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) -Methode.</span><span class="sxs-lookup"><span data-stu-id="67a5c-106">This method implements the [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="67a5c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="67a5c-107">Syntax</span></span>


```C++
HRESULT GetTime(
   REFERENCE_TIME *pTime
);
```



## <a name="parameters"></a><span data-ttu-id="67a5c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="67a5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67a5c-109">*PTIME*</span><span class="sxs-lookup"><span data-stu-id="67a5c-109">*pTime*</span></span> 
</dt> <dd>

<span data-ttu-id="67a5c-110">Ein Zeiger auf eine Variable, die die aktuelle Uhrzeit in 100-Nanosecond-Einheiten empfängt.</span><span class="sxs-lookup"><span data-stu-id="67a5c-110">Pointer to a variable that receives the current time, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67a5c-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67a5c-111">Return value</span></span>

<span data-ttu-id="67a5c-112">Gibt einen der **HRESULT** -Werte zurück, die in der folgenden Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="67a5c-112">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="67a5c-113">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="67a5c-113">Return code</span></span>                                                                               | <span data-ttu-id="67a5c-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67a5c-114">Description</span></span>                                                 |
|-------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="67a5c-115"><dt>**E- \_ Zeiger**</dt></span><span class="sxs-lookup"><span data-stu-id="67a5c-115"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="67a5c-116">**Null** -Zeigerargument.</span><span class="sxs-lookup"><span data-stu-id="67a5c-116">**NULL** pointer argument.</span></span><br/>                       |
| <dl> <span data-ttu-id="67a5c-117"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="67a5c-117"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="67a5c-118">Die zurückgegebene Uhrzeit ist mit dem vorherigen Wert identisch.</span><span class="sxs-lookup"><span data-stu-id="67a5c-118">Returned time is the same as the previous value.</span></span><br/> |
| <dl> <span data-ttu-id="67a5c-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="67a5c-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="67a5c-120">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="67a5c-120">Success.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="67a5c-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67a5c-121">Remarks</span></span>

<span data-ttu-id="67a5c-122">Diese Methode ruft die [**cbasereferenceclock:: getprivatetime**](cbasereferenceclock-getprivatetime.md) -Methode auf, um die tatsächliche Uhrzeit zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="67a5c-122">This method calls the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method to determine the real clock time.</span></span> <span data-ttu-id="67a5c-123">Wenn die Uhrzeitangabe streng größer als der vorherige Wert ist, `GetTime` verwendet die Uhrzeitangabe und gibt S \_ OK zurück.</span><span class="sxs-lookup"><span data-stu-id="67a5c-123">If the clock time is strictly greater than the previous value, `GetTime` uses the clock time and returns S\_OK.</span></span> <span data-ttu-id="67a5c-124">Andernfalls wird `GetTime` der vorherige Wert von verwendet und S \_ false zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67a5c-124">Otherwise, `GetTime` uses the previous value and returns S\_FALSE.</span></span> <span data-ttu-id="67a5c-125">Daher kann die interne Uhr für einen kurzen Zeitraum rückwärts ausgeführt werden, ohne dass die Bezugszeit rückwärts ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67a5c-125">Therefore, the internal clock can run backward for a short period, without causing the reference time to run backward.</span></span> <span data-ttu-id="67a5c-126">Stattdessen wird die Verweis Zeit mit demselben Wert "Stall", bis die interne Uhr abfängt.</span><span class="sxs-lookup"><span data-stu-id="67a5c-126">Instead, the reference time will "stall" at the same value until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="67a5c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67a5c-127">Requirements</span></span>



| <span data-ttu-id="67a5c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67a5c-128">Requirement</span></span> | <span data-ttu-id="67a5c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="67a5c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67a5c-130">Header</span><span class="sxs-lookup"><span data-stu-id="67a5c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="67a5c-131"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="67a5c-131"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="67a5c-132">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="67a5c-132">Library</span></span><br/> | <dl> <span data-ttu-id="67a5c-133">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="67a5c-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67a5c-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67a5c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67a5c-135">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="67a5c-135">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




