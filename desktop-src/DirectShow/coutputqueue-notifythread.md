---
description: Die notifythread-Methode benachrichtigt den Thread, dass die Warteschlange Daten enthält.
ms.assetid: d91cde3f-2876-4fb4-a124-f1460bba2cc9
title: Coutputqueue. notifythread-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.NotifyThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bb5f965bac15e99140955e8ee2519feaadfef85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350777"
---
# <a name="coutputqueuenotifythread-method"></a><span data-ttu-id="be9c5-103">Coutputqueue. notifythread-Methode</span><span class="sxs-lookup"><span data-stu-id="be9c5-103">COutputQueue.NotifyThread method</span></span>

<span data-ttu-id="be9c5-104">Die- `NotifyThread` Methode benachrichtigt den Thread, dass die Warteschlange Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="be9c5-104">The `NotifyThread` method notifies the thread that the queue contains data.</span></span>

## <a name="syntax"></a><span data-ttu-id="be9c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be9c5-105">Syntax</span></span>


```C++
void NotifyThread();
```



## <a name="parameters"></a><span data-ttu-id="be9c5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="be9c5-106">Parameters</span></span>

<span data-ttu-id="be9c5-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="be9c5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="be9c5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be9c5-108">Return value</span></span>

<span data-ttu-id="be9c5-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="be9c5-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="be9c5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be9c5-110">Remarks</span></span>

<span data-ttu-id="be9c5-111">Halten Sie den kritischen Abschnitt vor dem Aufruf dieser Methode.</span><span class="sxs-lookup"><span data-stu-id="be9c5-111">Hold the critical section before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="be9c5-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="be9c5-112">Requirements</span></span>



| <span data-ttu-id="be9c5-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="be9c5-113">Requirement</span></span> | <span data-ttu-id="be9c5-114">Wert</span><span class="sxs-lookup"><span data-stu-id="be9c5-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="be9c5-115">Header</span><span class="sxs-lookup"><span data-stu-id="be9c5-115">Header</span></span><br/>  | <dl> <span data-ttu-id="be9c5-116"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="be9c5-116"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="be9c5-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="be9c5-117">Library</span></span><br/> | <dl> <span data-ttu-id="be9c5-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="be9c5-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="be9c5-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be9c5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be9c5-120">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="be9c5-120">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




