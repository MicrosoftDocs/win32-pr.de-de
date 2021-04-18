---
description: Die ThreadProc-Methode ist die Thread Prozedur.
ms.assetid: 2d991f15-afea-4843-bc68-aeb5ca69d28b
title: Camthread. ThreadProc-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.ThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7081a7f7e1cd84a6bf8d482aa7dddf7a48b39f0a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352035"
---
# <a name="camthreadthreadproc-method"></a><span data-ttu-id="f4877-103">Camthread. ThreadProc-Methode</span><span class="sxs-lookup"><span data-stu-id="f4877-103">CAMThread.ThreadProc method</span></span>

<span data-ttu-id="f4877-104">Die- `ThreadProc` Methode ist die Thread Prozedur.</span><span class="sxs-lookup"><span data-stu-id="f4877-104">The `ThreadProc` method is the thread procedure.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4877-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4877-105">Syntax</span></span>


```C++
virtual DWORD ThreadProc() = 0;
```



## <a name="parameters"></a><span data-ttu-id="f4877-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4877-106">Parameters</span></span>

<span data-ttu-id="f4877-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="f4877-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="f4877-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4877-108">Return value</span></span>

<span data-ttu-id="f4877-109">Gibt einen **DWORD** -Wert zurück, dessen Bedeutung durch die abgeleitete Klasse definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f4877-109">Returns a **DWORD** value whose meaning is defined by the derived class.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4877-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4877-110">Remarks</span></span>

<span data-ttu-id="f4877-111">Dies ist eine reine virtuelle Methode.</span><span class="sxs-lookup"><span data-stu-id="f4877-111">This is a pure virtual method.</span></span> <span data-ttu-id="f4877-112">Implementieren Sie diese Methode in der abgeleiteten Klasse, um eine Thread Prozedur bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f4877-112">Implement this method in your derived class to supply a thread procedure.</span></span> <span data-ttu-id="f4877-113">Wenn die Methode " [**camthread:: Create**](camthread-create.md) " einen Thread erstellt, erhält Sie die Adresse der " [**camthread:: initialthleproc**](camthread-initialthreadproc.md) "-Methode, die wiederum ihre ThreadProc-Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="f4877-113">When the [**CAMThread::Create**](camthread-create.md) method creates a thread, it gives the address of the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method, which in turn calls your ThreadProc method.</span></span>

<span data-ttu-id="f4877-114">In der Regel wird von der ThreadProc-Methode eine Schleife eingegeben, die Anforderungen abruft (durch Aufrufen der Methoden [**camthread:: GetRequest**](camthread-getrequest.md) oder [**camthread:: CheckRequest**](camthread-checkrequest.md) ) und die Daten verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f4877-114">Typically, your ThreadProc method will enter a loop that retrieves requests (by calling the [**CAMThread::GetRequest**](camthread-getrequest.md) or [**CAMThread::CheckRequest**](camthread-checkrequest.md) methods) and processes data.</span></span>

<span data-ttu-id="f4877-115">Wenn diese Methode zurückgegeben wird, wird der Thread beendet.</span><span class="sxs-lookup"><span data-stu-id="f4877-115">When this method returns, the thread exits.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4877-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4877-116">Requirements</span></span>



| <span data-ttu-id="f4877-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4877-117">Requirement</span></span> | <span data-ttu-id="f4877-118">Wert</span><span class="sxs-lookup"><span data-stu-id="f4877-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4877-119">Header</span><span class="sxs-lookup"><span data-stu-id="f4877-119">Header</span></span><br/>  | <dl> <span data-ttu-id="f4877-120"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4877-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="f4877-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f4877-121">Library</span></span><br/> | <dl> <span data-ttu-id="f4877-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f4877-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4877-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4877-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4877-124">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f4877-124">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




