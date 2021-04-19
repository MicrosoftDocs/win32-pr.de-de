---
description: Die Antwortmethode antwortet auf eine Anforderung.
ms.assetid: 90e91b99-6a1c-46a2-b83d-eba483f1832a
title: Camthread. Reply-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Reply
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5e86e0bc0155e527aa11c26531ae5608e6828362
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362091"
---
# <a name="camthreadreply-method"></a><span data-ttu-id="df737-103">Camthread. Reply-Methode</span><span class="sxs-lookup"><span data-stu-id="df737-103">CAMThread.Reply method</span></span>

<span data-ttu-id="df737-104">Die- `Reply` Methode antwortet auf eine-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="df737-104">The `Reply` method replies to a request.</span></span>

## <a name="syntax"></a><span data-ttu-id="df737-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="df737-105">Syntax</span></span>


```C++
void Reply(
   DWORD dw
);
```



## <a name="parameters"></a><span data-ttu-id="df737-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="df737-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df737-107">*dw*</span><span class="sxs-lookup"><span data-stu-id="df737-107">*dw*</span></span> 
</dt> <dd>

<span data-ttu-id="df737-108">Wert, der in der Methode " [**camthread:: callworker**](camthread-callworker.md) " zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="df737-108">Value to return in the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df737-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="df737-109">Return value</span></span>

<span data-ttu-id="df737-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="df737-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df737-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df737-111">Remarks</span></span>

<span data-ttu-id="df737-112">Die callworker-Methode blockiert, bis diese Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="df737-112">The CallWorker method blocks until this method is called.</span></span> <span data-ttu-id="df737-113">Der *DW* -Parameter liefert den Rückgabewert für callworker.</span><span class="sxs-lookup"><span data-stu-id="df737-113">The *dw* parameter supplies the return value for CallWorker.</span></span> <span data-ttu-id="df737-114">Rufen Sie diese Methode in ihrer Thread Prozedur auf, nachdem Sie eine Anforderung abgerufen haben, um den angeforderten Thread freizugeben.</span><span class="sxs-lookup"><span data-stu-id="df737-114">Call this method in your thread procedure after you retrieve a request, to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="df737-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="df737-115">Requirements</span></span>



| <span data-ttu-id="df737-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="df737-116">Requirement</span></span> | <span data-ttu-id="df737-117">Wert</span><span class="sxs-lookup"><span data-stu-id="df737-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df737-118">Header</span><span class="sxs-lookup"><span data-stu-id="df737-118">Header</span></span><br/>  | <dl> <span data-ttu-id="df737-119"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df737-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="df737-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="df737-120">Library</span></span><br/> | <dl> <span data-ttu-id="df737-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="df737-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df737-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df737-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df737-123">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="df737-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




