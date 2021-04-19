---
description: Die GetRequest-Methode wartet auf die nächste Anforderung.
ms.assetid: 9f275ee6-cb78-455a-b924-7337c8d2a6dd
title: Camthread. GetRequest-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequest
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 506707bc78583fd9729ad28fb5507b82bee5e670
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359645"
---
# <a name="camthreadgetrequest-method"></a><span data-ttu-id="b04ed-103">Camthread. GetRequest-Methode</span><span class="sxs-lookup"><span data-stu-id="b04ed-103">CAMThread.GetRequest method</span></span>

<span data-ttu-id="b04ed-104">Die- `GetRequest` Methode wartet auf die nächste Anforderung.</span><span class="sxs-lookup"><span data-stu-id="b04ed-104">The `GetRequest` method waits for the next request.</span></span>

## <a name="syntax"></a><span data-ttu-id="b04ed-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b04ed-105">Syntax</span></span>


```C++
DWORD GetRequest();
```



## <a name="parameters"></a><span data-ttu-id="b04ed-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b04ed-106">Parameters</span></span>

<span data-ttu-id="b04ed-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b04ed-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b04ed-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b04ed-108">Return value</span></span>

<span data-ttu-id="b04ed-109">Gibt einen Wert zurück, der von der abgeleiteten Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="b04ed-109">Returns a value that is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="b04ed-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b04ed-110">Remarks</span></span>

<span data-ttu-id="b04ed-111">Diese Methode wird blockiert, bis ein anderer Thread die Methode " [**camthread:: callworker**](camthread-callworker.md) " aufruft.</span><span class="sxs-lookup"><span data-stu-id="b04ed-111">This method blocks until another thread calls the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span> <span data-ttu-id="b04ed-112">Anschließend wird der an callworker übergebenen Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b04ed-112">Then it returns the parameter that was passed to CallWorker.</span></span> <span data-ttu-id="b04ed-113">Ruft die Methode " [**camthread:: Reply**](camthread-reply.md) " auf, um den anfordernden Thread freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b04ed-113">Call the [**CAMThread::Reply**](camthread-reply.md) method to release the requesting thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="b04ed-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b04ed-114">Requirements</span></span>



| <span data-ttu-id="b04ed-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b04ed-115">Requirement</span></span> | <span data-ttu-id="b04ed-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b04ed-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b04ed-117">Header</span><span class="sxs-lookup"><span data-stu-id="b04ed-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b04ed-118"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b04ed-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b04ed-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b04ed-119">Library</span></span><br/> | <dl> <span data-ttu-id="b04ed-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b04ed-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b04ed-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b04ed-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b04ed-122">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b04ed-122">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




