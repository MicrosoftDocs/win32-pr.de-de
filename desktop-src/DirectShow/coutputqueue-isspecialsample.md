---
description: Die isspecialsample-Methode bestimmt, ob Daten in der Warteschlange eine Kontroll Nachricht sind.
ms.assetid: 33d9c7a2-3046-45a5-a9f5-8f33a03bbcdd
title: Coutputqueue. isspecialsample-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.IsSpecialSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc57847d6a977c740bbf50bae220a89b0ed6fab1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358284"
---
# <a name="coutputqueueisspecialsample-method"></a><span data-ttu-id="e10aa-103">Coutputqueue. isspecialsample-Methode</span><span class="sxs-lookup"><span data-stu-id="e10aa-103">COutputQueue.IsSpecialSample method</span></span>

<span data-ttu-id="e10aa-104">Die- `IsSpecialSample` Methode bestimmt, ob Daten in der Warteschlange eine Kontroll Meldung sind.</span><span class="sxs-lookup"><span data-stu-id="e10aa-104">The `IsSpecialSample` method determines whether queued data is a control message.</span></span>

## <a name="syntax"></a><span data-ttu-id="e10aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e10aa-105">Syntax</span></span>


```C++
BOOL IsSpecialSample(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="e10aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e10aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e10aa-107">*psample*</span><span class="sxs-lookup"><span data-stu-id="e10aa-107">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e10aa-108">Zeiger auf ein Element in der Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="e10aa-108">Pointer to an item in the queue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e10aa-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e10aa-109">Return value</span></span>

<span data-ttu-id="e10aa-110">Gibt **true** zurück, wenn *psample* eine Steuer Meldung ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="e10aa-110">Returns **TRUE** if *pSample* is a control message, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e10aa-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e10aa-111">Remarks</span></span>

<span data-ttu-id="e10aa-112">Die [**coutputqueue:: queuesample**](coutputqueue-queuesample.md) -Methode kann neben Medien Beispielen auch Steuerungs Meldungen empfangen.</span><span class="sxs-lookup"><span data-stu-id="e10aa-112">The [**COutputQueue::QueueSample**](coutputqueue-queuesample.md) method can receive control messages in addition to media samples.</span></span> <span data-ttu-id="e10aa-113">Eine Kontroll Meldung ist eine definierte Konstante (in einen langen \_ ptr-Typ umgewandelt), die den Thread anweist, eine Aktion auszuführen.</span><span class="sxs-lookup"><span data-stu-id="e10aa-113">A control message is a defined constant (cast to a LONG\_PTR type) that instructs the thread to perform an action.</span></span> <span data-ttu-id="e10aa-114">Steuerungs Meldungen enthalten keine Mediendaten.</span><span class="sxs-lookup"><span data-stu-id="e10aa-114">Control messages do not contain media data.</span></span> <span data-ttu-id="e10aa-115">Weitere Informationen finden Sie unter **coutputqueue:: queuesample**.</span><span class="sxs-lookup"><span data-stu-id="e10aa-115">For more information, see **COutputQueue::QueueSample**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e10aa-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e10aa-116">Requirements</span></span>



| <span data-ttu-id="e10aa-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e10aa-117">Requirement</span></span> | <span data-ttu-id="e10aa-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e10aa-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e10aa-119">Header</span><span class="sxs-lookup"><span data-stu-id="e10aa-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e10aa-120"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e10aa-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e10aa-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e10aa-121">Library</span></span><br/> | <dl> <span data-ttu-id="e10aa-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e10aa-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e10aa-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e10aa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e10aa-124">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e10aa-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




