---
description: Die getnextadviantime-Methode ruft den Zeitpunkt der nächsten anforderungsanforderung ab.
ms.assetid: 2a376250-fb39-46d7-a5a8-e3a3143cd209
title: Camschedule. getnextadvitstime-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetNextAdviseTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5894ae98666c9134abd4bce96922a5f28d5919b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366755"
---
# <a name="camschedulegetnextadvisetime-method"></a><span data-ttu-id="aa452-103">Camschedule. getnextadvictime-Methode</span><span class="sxs-lookup"><span data-stu-id="aa452-103">CAMSchedule.GetNextAdviseTime method</span></span>

<span data-ttu-id="aa452-104">Die- `GetNextAdviseTime` Methode ruft den Zeitpunkt der nächsten anforderungsanforderung ab.</span><span class="sxs-lookup"><span data-stu-id="aa452-104">The `GetNextAdviseTime` method retrieves the time of the next advise request.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa452-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa452-105">Syntax</span></span>


```C++
REFERENCE_TIME GetNextAdviseTime();
```



## <a name="parameters"></a><span data-ttu-id="aa452-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa452-106">Parameters</span></span>

<span data-ttu-id="aa452-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="aa452-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa452-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa452-108">Return value</span></span>

<span data-ttu-id="aa452-109">Gibt die Verweis Zeit der nächsten anforderungsanforderung oder die maximale Zeit für die geplante Ausführung von \_ Anforderungen zurück.</span><span class="sxs-lookup"><span data-stu-id="aa452-109">Returns the reference time of the next advise request, or MAX\_TIME no requests are scheduled.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa452-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa452-110">Requirements</span></span>



| <span data-ttu-id="aa452-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa452-111">Requirement</span></span> | <span data-ttu-id="aa452-112">Wert</span><span class="sxs-lookup"><span data-stu-id="aa452-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa452-113">Header</span><span class="sxs-lookup"><span data-stu-id="aa452-113">Header</span></span><br/>  | <dl> <span data-ttu-id="aa452-114"><dt>Dsschedule. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa452-114"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="aa452-115">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa452-115">Library</span></span><br/> | <dl> <span data-ttu-id="aa452-116">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aa452-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa452-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa452-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa452-118">**Camschedule-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aa452-118">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




