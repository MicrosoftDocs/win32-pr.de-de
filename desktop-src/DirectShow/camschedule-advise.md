---
description: Die Methode "Request" verteilt alle Anforderungen, die für eine angegebene Zeit oder eine frühere Zeit geplant sind.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Camschedule. Empfehlung-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371179"
---
# <a name="camscheduleadvise-method"></a><span data-ttu-id="903ff-103">Camschedule. Empfehlung-Methode</span><span class="sxs-lookup"><span data-stu-id="903ff-103">CAMSchedule.Advise method</span></span>

<span data-ttu-id="903ff-104">Die- `Advise` Methode sendet alle Anforderungen, die für eine angegebene Zeit oder früher geplant sind.</span><span class="sxs-lookup"><span data-stu-id="903ff-104">The `Advise` method dispatches all requests that are scheduled for a specified time or earlier.</span></span>

## <a name="syntax"></a><span data-ttu-id="903ff-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="903ff-105">Syntax</span></span>


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a><span data-ttu-id="903ff-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="903ff-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="903ff-107">*rttime* \[ atur\]</span><span class="sxs-lookup"><span data-stu-id="903ff-107">*rtTime* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="903ff-108">Der-Wert, der die aktuelle Verweis Zeit angibt.</span><span class="sxs-lookup"><span data-stu-id="903ff-108">Value that specifies the current reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="903ff-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="903ff-109">Return value</span></span>

<span data-ttu-id="903ff-110">Gibt den Verweis Zeitpunkt der nächsten geplanten anforderungsanforderung oder die maximale Zeit zurück, \_ Wenn keine Links vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="903ff-110">Returns the reference time of the next scheduled advise request, or MAX\_TIME if there are none left.</span></span>

## <a name="remarks"></a><span data-ttu-id="903ff-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="903ff-111">Remarks</span></span>

<span data-ttu-id="903ff-112">Wenn diese Methode von der Uhr aufgerufen wird, wird die aktuelle Verweis Zeit angegeben.</span><span class="sxs-lookup"><span data-stu-id="903ff-112">When the clock calls this method, it specifies the current reference time.</span></span> <span data-ttu-id="903ff-113">Der Planer bestimmt, welche Anforderungs Anforderungen ggf. abgelaufen sind, und sendet Sie.</span><span class="sxs-lookup"><span data-stu-id="903ff-113">The scheduler determines which advise requests have expired, if any, and dispatches them.</span></span> <span data-ttu-id="903ff-114">Wenn eine One-Shot-Anforderung abläuft, wird Sie vom Scheduler gelöscht.</span><span class="sxs-lookup"><span data-stu-id="903ff-114">If a one-shot request expires, the scheduler deletes it.</span></span> <span data-ttu-id="903ff-115">Wenn eine regelmäßige Anforderung abläuft, plant der Scheduler diese für den nächsten Zeitpunkt der Empfehlung erneut.</span><span class="sxs-lookup"><span data-stu-id="903ff-115">If a periodic request expires, the scheduler re-schedules it for the next advise time.</span></span> <span data-ttu-id="903ff-116">Die-Methode gibt die Zeit der nächsten ausstehenden Anforderung zurück.</span><span class="sxs-lookup"><span data-stu-id="903ff-116">The method returns the time of the next pending request.</span></span>

<span data-ttu-id="903ff-117">Zum Senden einer Benachrichtigungs Anforderung signalisiert der Planer das Ereignis oder die Semaphor, die im *hnotify* -Parameter der Methode " [**camschedule:: addadvisepacket**](camschedule-addadvisepacket.md) " angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="903ff-117">To dispatch an advise request, the scheduler signals the event or semaphore given in the *hNotify* parameter of the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="903ff-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="903ff-118">Requirements</span></span>



| <span data-ttu-id="903ff-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="903ff-119">Requirement</span></span> | <span data-ttu-id="903ff-120">Wert</span><span class="sxs-lookup"><span data-stu-id="903ff-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="903ff-121">Header</span><span class="sxs-lookup"><span data-stu-id="903ff-121">Header</span></span><br/>  | <dl> <span data-ttu-id="903ff-122"><dt>Dsschedule. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="903ff-122"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="903ff-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="903ff-123">Library</span></span><br/> | <dl> <span data-ttu-id="903ff-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="903ff-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="903ff-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="903ff-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="903ff-126">**Camschedule-Klasse**</span><span class="sxs-lookup"><span data-stu-id="903ff-126">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




