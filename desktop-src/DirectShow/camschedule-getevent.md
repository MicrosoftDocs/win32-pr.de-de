---
description: Die GetEvent-Methode ruft ein Ereignis Handle ab, das verwendet wird, um eine Änderung in der nächsten Empfehlung zu signalisieren.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Camschedule. GetEvent-Methode (dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372066"
---
# <a name="camschedulegetevent-method"></a><span data-ttu-id="4f493-103">Camschedule. GetEvent-Methode</span><span class="sxs-lookup"><span data-stu-id="4f493-103">CAMSchedule.GetEvent method</span></span>

<span data-ttu-id="4f493-104">Die- `GetEvent` Methode ruft ein Ereignis Handle ab, das verwendet wird, um eine Änderung in der nächsten Empfehlung zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="4f493-104">The `GetEvent` method retrieves an event handle, which is used to signal a change in the next advise time.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f493-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4f493-105">Syntax</span></span>


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a><span data-ttu-id="4f493-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f493-106">Parameters</span></span>

<span data-ttu-id="4f493-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="4f493-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="4f493-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f493-108">Return value</span></span>

<span data-ttu-id="4f493-109">Gibt ein Handle für ein Ereignis zurück.</span><span class="sxs-lookup"><span data-stu-id="4f493-109">Returns a handle to an event.</span></span>

## <a name="remarks"></a><span data-ttu-id="4f493-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4f493-110">Remarks</span></span>

<span data-ttu-id="4f493-111">Wenn sich die nächste Anforderungszeit geändert hat und eine neue anforderungsanforderung am Anfang der Liste hinzugefügt wird, signalisiert der Scheduler dieses Ereignis.</span><span class="sxs-lookup"><span data-stu-id="4f493-111">If the next advise time changes in other words, if a new advise request is added to the front of the list the scheduler signals this event.</span></span> <span data-ttu-id="4f493-112">Die Uhr sollte die Methode " [**camschedule:: Empfehlung**](camschedule-advise.md) " anrufen, um den nächsten Zeitpunkt der Empfehlung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="4f493-112">The clock should call the [**CAMSchedule::Advise**](camschedule-advise.md) method to determine the next advise time.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f493-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4f493-113">Requirements</span></span>



| <span data-ttu-id="4f493-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4f493-114">Requirement</span></span> | <span data-ttu-id="4f493-115">Wert</span><span class="sxs-lookup"><span data-stu-id="4f493-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f493-116">Header</span><span class="sxs-lookup"><span data-stu-id="4f493-116">Header</span></span><br/>  | <dl> <span data-ttu-id="4f493-117"><dt>Dsschedule. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f493-117"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="4f493-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4f493-118">Library</span></span><br/> | <dl> <span data-ttu-id="4f493-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4f493-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f493-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f493-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f493-121">**Camschedule-Klasse**</span><span class="sxs-lookup"><span data-stu-id="4f493-121">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




