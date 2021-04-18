---
description: Die getprivatetime-Methode ruft die Echt Zeit von der Uhr ab.
ms.assetid: ce9832cb-4b5a-49a1-9a69-d2fb90b3ed2e
title: Cbasereferenceclock. getprivatetime-Methode (Ref. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetPrivateTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 387df10472e4913d33722492bf07601faf08e3ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352101"
---
# <a name="cbasereferenceclockgetprivatetime-method"></a><span data-ttu-id="938a4-103">Cbasereferenceclock. getprivatetime-Methode</span><span class="sxs-lookup"><span data-stu-id="938a4-103">CBaseReferenceClock.GetPrivateTime method</span></span>

<span data-ttu-id="938a4-104">Die- `GetPrivateTime` Methode ruft die Echt Zeit von der Uhr ab.</span><span class="sxs-lookup"><span data-stu-id="938a4-104">The `GetPrivateTime` method retrieves the real time from the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="938a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="938a4-105">Syntax</span></span>


```C++
virtual REFERENCE_TIME GetPrivateTime();
```



## <a name="parameters"></a><span data-ttu-id="938a4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="938a4-106">Parameters</span></span>

<span data-ttu-id="938a4-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="938a4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="938a4-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="938a4-108">Return value</span></span>

<span data-ttu-id="938a4-109">Gibt die aktuelle Uhrzeit in 100-Nanosecond-Einheiten zurück.</span><span class="sxs-lookup"><span data-stu-id="938a4-109">Returns the current clock time, in 100-nanosecond units.</span></span>

## <a name="remarks"></a><span data-ttu-id="938a4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="938a4-110">Remarks</span></span>

<span data-ttu-id="938a4-111">Diese Methode gibt die von der Uhr gemeldete Echt Zeit zurück.</span><span class="sxs-lookup"><span data-stu-id="938a4-111">This method returns the real time reported by the clock.</span></span> <span data-ttu-id="938a4-112">Externe Aufrufer verwenden die [**cbasereferenceclock:: getTime**](cbasereferenceclock-gettime.md) -Methode, die diese Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="938a4-112">External callers use the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method, which calls this method.</span></span> <span data-ttu-id="938a4-113">Anders als bei der **GetTime** -Methode kann die interne Uhr rückwärts gehen.</span><span class="sxs-lookup"><span data-stu-id="938a4-113">Unlike the **GetTime** method, the internal clock is allowed to go backward.</span></span> <span data-ttu-id="938a4-114">Wenn dies der Fall ist, gibt die **GetTime** -Methode weiterhin den Zeitpunkt der letzten Meldung zurück, bis die `GetPrivateTime` Methode abfängt.</span><span class="sxs-lookup"><span data-stu-id="938a4-114">If that happens, the **GetTime** method continues to return the last time that it reported, until the `GetPrivateTime` method catches up.</span></span>

<span data-ttu-id="938a4-115">Diese Methode gibt die Systemzeit zurück.</span><span class="sxs-lookup"><span data-stu-id="938a4-115">This method returns the system time.</span></span> <span data-ttu-id="938a4-116">Überschreiben Sie diese Methode, wenn die Uhr die Zeit aus einer anderen Quelle erhält.</span><span class="sxs-lookup"><span data-stu-id="938a4-116">Override this method if your clock gets the time from another source.</span></span>

## <a name="requirements"></a><span data-ttu-id="938a4-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="938a4-117">Requirements</span></span>



| <span data-ttu-id="938a4-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="938a4-118">Requirement</span></span> | <span data-ttu-id="938a4-119">Wert</span><span class="sxs-lookup"><span data-stu-id="938a4-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="938a4-120">Header</span><span class="sxs-lookup"><span data-stu-id="938a4-120">Header</span></span><br/>  | <dl> <span data-ttu-id="938a4-121"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="938a4-121"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="938a4-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="938a4-122">Library</span></span><br/> | <dl> <span data-ttu-id="938a4-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="938a4-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="938a4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="938a4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="938a4-125">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="938a4-125">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




