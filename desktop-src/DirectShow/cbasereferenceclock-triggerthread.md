---
description: Die triggerthread-Methode aktiviert den Arbeits Thread, der die Planung verarbeitet.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Cbasereferenceclock. triggerthread-Methode (refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369235"
---
# <a name="cbasereferenceclocktriggerthread-method"></a><span data-ttu-id="53f81-103">Cbasereferenceclock. triggerthread-Methode</span><span class="sxs-lookup"><span data-stu-id="53f81-103">CBaseReferenceClock.TriggerThread method</span></span>

<span data-ttu-id="53f81-104">Die- `TriggerThread` Methode aktiviert den Arbeits Thread, der die Planung verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="53f81-104">The `TriggerThread` method wakes up the worker thread that handles scheduling.</span></span>

## <a name="syntax"></a><span data-ttu-id="53f81-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="53f81-105">Syntax</span></span>


```C++
void TriggerThread();
```



## <a name="parameters"></a><span data-ttu-id="53f81-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="53f81-106">Parameters</span></span>

<span data-ttu-id="53f81-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="53f81-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="53f81-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="53f81-108">Return value</span></span>

<span data-ttu-id="53f81-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="53f81-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f81-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53f81-110">Remarks</span></span>

<span data-ttu-id="53f81-111">Die Uhr verwendet einen Arbeits Thread, der die Methode " [**camschedule:: Empfehlung**](camschedule-advise.md) " zu den entsprechenden Zeitpunkten aufruft.</span><span class="sxs-lookup"><span data-stu-id="53f81-111">The clock uses a worker thread that calls the [**CAMSchedule::Advise**](camschedule-advise.md) method at appropriate times.</span></span> <span data-ttu-id="53f81-112">Von der abgeleiteten Klasse kann aufgerufen `TriggerThread` werden, um den Thread zu reaktivieren.</span><span class="sxs-lookup"><span data-stu-id="53f81-112">The derived class can call `TriggerThread` to wake up the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f81-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="53f81-113">Requirements</span></span>



| <span data-ttu-id="53f81-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="53f81-114">Requirement</span></span> | <span data-ttu-id="53f81-115">Wert</span><span class="sxs-lookup"><span data-stu-id="53f81-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="53f81-116">Header</span><span class="sxs-lookup"><span data-stu-id="53f81-116">Header</span></span><br/>  | <dl> <span data-ttu-id="53f81-117"><dt>Ref. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="53f81-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="53f81-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="53f81-118">Library</span></span><br/> | <dl> <span data-ttu-id="53f81-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="53f81-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f81-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="53f81-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f81-121">**Cbasereferenceclock-Klasse**</span><span class="sxs-lookup"><span data-stu-id="53f81-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




