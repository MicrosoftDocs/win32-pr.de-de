---
description: Die CheckRequest-Methode überprüft, ob eine Anforderung vorhanden ist, ohne zu blockieren.
ms.assetid: 46d0840e-a304-41e3-9016-9f35e404cd30
title: Camthread. CheckRequest-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.CheckRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5a004e0f5303cf6702c03e78c292a6a2d832a489
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361503"
---
# <a name="camthreadcheckrequest-method"></a><span data-ttu-id="9727f-103">Camthread. CheckRequest-Methode</span><span class="sxs-lookup"><span data-stu-id="9727f-103">CAMThread.CheckRequest method</span></span>

<span data-ttu-id="9727f-104">Die- `CheckRequest` Methode überprüft, ob eine Anforderung vorhanden ist, ohne zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="9727f-104">The `CheckRequest` method checks if there is a request, without blocking.</span></span>

## <a name="syntax"></a><span data-ttu-id="9727f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9727f-105">Syntax</span></span>


```C++
BOOL CheckRequest(
   DWORD *pParam
);
```



## <a name="parameters"></a><span data-ttu-id="9727f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9727f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9727f-107">*pParam*</span><span class="sxs-lookup"><span data-stu-id="9727f-107">*pParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9727f-108">Ein Zeiger auf eine Variable, die den Wert empfängt, der beim letzten Aufruf der Methode " [**camthread:: callworker**](camthread-callworker.md) " übermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="9727f-108">Pointer to a variable that receives the value passed in the last call to the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9727f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9727f-109">Return value</span></span>

<span data-ttu-id="9727f-110">Gibt **true** zurück, wenn eine ausstehende Anforderung vorhanden ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9727f-110">Returns **TRUE** if there is a pending request, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9727f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9727f-111">Remarks</span></span>

<span data-ttu-id="9727f-112">Diese Methode ist eine nicht blockierende Version der [**camthread:: GetRequest**](camthread-getrequest.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9727f-112">This method is a non-blocking version of the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span>

<span data-ttu-id="9727f-113">Wenn ein anderer Thread auf einen Aufruf von callworker wartet, ruft diese Methode den Anforderungs Parameter ab und gibt **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="9727f-113">If another thread is waiting on a call to CallWorker, this method retrieves the request parameter and returns **TRUE**.</span></span> <span data-ttu-id="9727f-114">Andernfalls wird **false** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9727f-114">Otherwise, it returns **FALSE**.</span></span> <span data-ttu-id="9727f-115">Wenn die Methode **true** zurückgibt, wird die Methode " [**camthread:: Reply**](camthread-reply.md) " aufgerufen, um den anfordernden Thread freizugeben.</span><span class="sxs-lookup"><span data-stu-id="9727f-115">If the method returns **TRUE**, call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="9727f-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9727f-116">Requirements</span></span>



| <span data-ttu-id="9727f-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9727f-117">Requirement</span></span> | <span data-ttu-id="9727f-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9727f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9727f-119">Header</span><span class="sxs-lookup"><span data-stu-id="9727f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="9727f-120"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9727f-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9727f-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9727f-121">Library</span></span><br/> | <dl> <span data-ttu-id="9727f-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9727f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9727f-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9727f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9727f-124">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9727f-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




