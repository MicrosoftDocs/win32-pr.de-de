---
description: 'Die getrequesthandle-Methode ruft ein Handle für das Ereignis ab, das von der camthread:: callworker-Methode signalisiert wird.'
ms.assetid: 6e4496ae-a635-4b55-ae7a-31748f21068b
title: Camthread. getrequesthandle-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.GetRequestHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 051a6a3e3daed1dae6df3bdbb42e36f07b852d85
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358676"
---
# <a name="camthreadgetrequesthandle-method"></a><span data-ttu-id="6e3c7-103">Camthread. getrequesthandle-Methode</span><span class="sxs-lookup"><span data-stu-id="6e3c7-103">CAMThread.GetRequestHandle method</span></span>

<span data-ttu-id="6e3c7-104">Die- `GetRequestHandle` Methode ruft ein Handle für das-Ereignis ab, das von der [**camthread:: callworker**](camthread-callworker.md) -Methode signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-104">The `GetRequestHandle` method retrieves a handle to the event that is signaled by the [**CAMThread::CallWorker**](camthread-callworker.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e3c7-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6e3c7-105">Syntax</span></span>


```C++
HANDLE GetRequestHandle() const;
```



## <a name="parameters"></a><span data-ttu-id="6e3c7-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6e3c7-106">Parameters</span></span>

<span data-ttu-id="6e3c7-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6e3c7-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6e3c7-108">Return value</span></span>

<span data-ttu-id="6e3c7-109">Gibt ein Ereignis Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-109">Returns an event handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e3c7-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6e3c7-110">Remarks</span></span>

<span data-ttu-id="6e3c7-111">Die Klasse "camevent" behält ein privates Manuelles Zurücksetzungs Ereignis bei, das von callworker festgelegt und durch die Methode " [**camthread:: Reply**](camthread-reply.md) " zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-111">The CAMEvent class keeps a private manual-reset event, which is set by CallWorker and reset by the [**CAMThread::Reply**](camthread-reply.md) method.</span></span>

<span data-ttu-id="6e3c7-112">Wenn Sie eine Funktion wie WaitForMultipleObjects aufrufen, verwenden Sie getrequesthandle, um das Ereignis Handle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="6e3c7-112">If you call a function such as WaitForMultipleObjects, use GetRequestHandle to retrieve the event handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e3c7-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6e3c7-113">Requirements</span></span>



| <span data-ttu-id="6e3c7-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6e3c7-114">Requirement</span></span> | <span data-ttu-id="6e3c7-115">Wert</span><span class="sxs-lookup"><span data-stu-id="6e3c7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e3c7-116">Header</span><span class="sxs-lookup"><span data-stu-id="6e3c7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6e3c7-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6e3c7-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="6e3c7-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6e3c7-118">Library</span></span><br/> | <dl> <span data-ttu-id="6e3c7-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6e3c7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e3c7-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e3c7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e3c7-121">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6e3c7-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




