---
description: 'Die Thread proc-Methode ist die Thread Prozedur für den Arbeits Thread. Diese Methode implementiert die pure Virtual camthread:: ThreadProc-Methode.'
ms.assetid: 8e66b609-d795-45a8-8fe5-774c659ee350
title: Csourcestream. ThreadProc-Methode (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6dc7d08643cc0ca76d3d05f0b9090f30200eb181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365962"
---
# <a name="csourcestreamthreadproc-method"></a><span data-ttu-id="06b77-104">Csourcestream. ThreadProc-Methode</span><span class="sxs-lookup"><span data-stu-id="06b77-104">CSourceStream.ThreadProc method</span></span>

<span data-ttu-id="06b77-105">Die- `ThreadProc` Methode ist die Thread Prozedur für den Arbeits Thread.</span><span class="sxs-lookup"><span data-stu-id="06b77-105">The `ThreadProc` method is the thread procedure for the worker thread.</span></span> <span data-ttu-id="06b77-106">Diese Methode implementiert die pure Virtual [**camthread:: ThreadProc**](camthread-threadproc.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="06b77-106">This method implements the pure virtual [**CAMThread::ThreadProc**](camthread-threadproc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="06b77-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="06b77-107">Syntax</span></span>


```C++
virtual DWORD ThreadProc();
```



## <a name="parameters"></a><span data-ttu-id="06b77-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="06b77-108">Parameters</span></span>

<span data-ttu-id="06b77-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="06b77-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="06b77-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="06b77-110">Return value</span></span>

<span data-ttu-id="06b77-111">Gibt 0 zurück, wenn der Thread erfolgreich abgeschlossen wurde, oder andernfalls 1.</span><span class="sxs-lookup"><span data-stu-id="06b77-111">Returns 0 if the thread completed successfully or 1 otherwise.</span></span> <span data-ttu-id="06b77-112">Wenn der Rückgabewert 1 ist, werden die Ressourcen des Threads möglicherweise trotzdem zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="06b77-112">If the return value is 1, the thread's resources might still be allocated.</span></span>

## <a name="remarks"></a><span data-ttu-id="06b77-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="06b77-113">Remarks</span></span>

<span data-ttu-id="06b77-114">Diese Methode wartet unbegrenzt auf Thread Anforderungen, indem die Methode " [**camthread:: GetRequest**](camthread-getrequest.md) " aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="06b77-114">This method waits indefinitely for thread requests, by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) method.</span></span> <span data-ttu-id="06b77-115">Wenn eine [**csourcestream:: Run**](csourcestream-run.md) -oder [**csourcestream::P ause**](csourcestream-pause.md) -Anforderung empfangen wird, wird die [**csourcestream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="06b77-115">If it receives a [**CSourceStream::Run**](csourcestream-run.md) or [**CSourceStream::Pause**](csourcestream-pause.md) request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="06b77-116">Die Methode **dobufferprocessingloop** überträgt Daten, bis Sie eine [**csourcestream:: Stoppanforderung**](csourcestream-stop.md) empfängt.</span><span class="sxs-lookup"><span data-stu-id="06b77-116">The **DoBufferProcessingLoop** method pushes data until it receives a [**CSourceStream::Stop**](csourcestream-stop.md) request.</span></span> <span data-ttu-id="06b77-117">Die Thread Prozedur wird beendet, wenn Sie eine [**csourcestream:: Exit**](csourcestream-exit.md) -Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="06b77-117">The thread procedure exits when it receives a [**CSourceStream::Exit**](csourcestream-exit.md) request.</span></span>

## <a name="requirements"></a><span data-ttu-id="06b77-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="06b77-118">Requirements</span></span>



| <span data-ttu-id="06b77-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="06b77-119">Requirement</span></span> | <span data-ttu-id="06b77-120">Wert</span><span class="sxs-lookup"><span data-stu-id="06b77-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b77-121">Header</span><span class="sxs-lookup"><span data-stu-id="06b77-121">Header</span></span><br/>  | <dl> <span data-ttu-id="06b77-122"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="06b77-122"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="06b77-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="06b77-123">Library</span></span><br/> | <dl> <span data-ttu-id="06b77-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="06b77-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06b77-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="06b77-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06b77-126">**Csourcestream-Klasse**</span><span class="sxs-lookup"><span data-stu-id="06b77-126">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




