---
description: Die Set-Methode signalisiert das-Ereignis.
ms.assetid: dfcb1601-aa65-47f5-ae3c-f13fcd7b1398
title: Camevent. Set-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMEvent.Set
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c9caeed17d42d121ae9263bf6c1fcd011ed573c7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366835"
---
# <a name="cameventset-method"></a><span data-ttu-id="0c01f-103">Camevent. Set-Methode</span><span class="sxs-lookup"><span data-stu-id="0c01f-103">CAMEvent.Set method</span></span>

<span data-ttu-id="0c01f-104">Die- `Set` Methode signalisiert das-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="0c01f-104">The `Set` method signals the event.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c01f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c01f-105">Syntax</span></span>


```C++
void Set();
```



## <a name="parameters"></a><span data-ttu-id="0c01f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c01f-106">Parameters</span></span>

<span data-ttu-id="0c01f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="0c01f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0c01f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0c01f-108">Return value</span></span>

<span data-ttu-id="0c01f-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="0c01f-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c01f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c01f-110">Remarks</span></span>

<span data-ttu-id="0c01f-111">Das Verhalten hängt davon ab, ob es sich bei dem Objekt um ein Auto Reset-Ereignis oder ein manuelles Zurücksetzungs Ereignis handelt:</span><span class="sxs-lookup"><span data-stu-id="0c01f-111">The behavior depends on whether the object is an auto-reset event or a manual-reset event:</span></span>

-   <span data-ttu-id="0c01f-112">**Automatisch zurückgesetzt**: Wenn Threads auf dieses Ereignis warten, wird ein Thread freigegeben, und das Ereignis wird zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0c01f-112">**Auto-reset**: If any threads are waiting on this event, one thread is released and the event is reset.</span></span> <span data-ttu-id="0c01f-113">Wenn keine Threads auf dieses Ereignis warten, bleibt das Ereignis signalisiert.</span><span class="sxs-lookup"><span data-stu-id="0c01f-113">If no threads are waiting on this event, the event remains signaled.</span></span>
-   <span data-ttu-id="0c01f-114">**Manuelles Zurücksetzen**: alle Threads, die auf dieses Ereignis warten, werden freigegeben.</span><span class="sxs-lookup"><span data-stu-id="0c01f-114">**Manual-reset**: All the threads waiting on this event are released.</span></span> <span data-ttu-id="0c01f-115">Das Ereignis bleibt signalisiert.</span><span class="sxs-lookup"><span data-stu-id="0c01f-115">The event remains signaled.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c01f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0c01f-116">Requirements</span></span>



| <span data-ttu-id="0c01f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0c01f-117">Requirement</span></span> | <span data-ttu-id="0c01f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="0c01f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c01f-119">Header</span><span class="sxs-lookup"><span data-stu-id="0c01f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="0c01f-120"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c01f-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="0c01f-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="0c01f-121">Library</span></span><br/> | <dl> <span data-ttu-id="0c01f-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="0c01f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c01f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0c01f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c01f-124">**Camevent-Klasse**</span><span class="sxs-lookup"><span data-stu-id="0c01f-124">**CAMEvent Class**</span></span>](camevent.md)
</dt> </dl>

 

 




