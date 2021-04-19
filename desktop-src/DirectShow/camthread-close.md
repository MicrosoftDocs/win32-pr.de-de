---
description: Die Close-Methode wartet darauf, dass der Thread beendet wird, und gibt dann seine Ressourcen frei.
ms.assetid: 57e27ff7-3665-416e-8a6e-660483c5aed2
title: Camthread. Close-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Close
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9cac5ee4a1e1a9cc3fecc8d09096d031e9fc9a63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362051"
---
# <a name="camthreadclose-method"></a><span data-ttu-id="7aecd-103">Camthread. Close-Methode</span><span class="sxs-lookup"><span data-stu-id="7aecd-103">CAMThread.Close method</span></span>

<span data-ttu-id="7aecd-104">Die- `Close` Methode wartet, bis der Thread beendet wird, und gibt dann die zugehörigen Ressourcen frei.</span><span class="sxs-lookup"><span data-stu-id="7aecd-104">The `Close` method waits for the thread to exit, then releases its resources.</span></span>

## <a name="syntax"></a><span data-ttu-id="7aecd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7aecd-105">Syntax</span></span>


```C++
void Close();
```



## <a name="parameters"></a><span data-ttu-id="7aecd-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7aecd-106">Parameters</span></span>

<span data-ttu-id="7aecd-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="7aecd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7aecd-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7aecd-108">Return value</span></span>

<span data-ttu-id="7aecd-109">Kein Rückgabewert.</span><span class="sxs-lookup"><span data-stu-id="7aecd-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7aecd-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7aecd-110">Remarks</span></span>

<span data-ttu-id="7aecd-111">Vor dem Aufrufen dieser Methode müssen Sie eine Möglichkeit zum Beenden des Threads bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7aecd-111">Before calling this method, you must provide a way for the thread to exit.</span></span> <span data-ttu-id="7aecd-112">Definieren Sie beispielsweise in der Methode " [**camthread:: ThreadProc**](camthread-threadproc.md) " eine Anforderung, mit der der Thread beendet wird.</span><span class="sxs-lookup"><span data-stu-id="7aecd-112">For example, in your [**CAMThread::ThreadProc**](camthread-threadproc.md) method, define a request that signals the thread to exit.</span></span> <span data-ttu-id="7aecd-113">Rufen Sie dann die Methode " [**camthread:: callworker**](camthread-callworker.md) " mit diesem Wert auf.</span><span class="sxs-lookup"><span data-stu-id="7aecd-113">Then call the [**CAMThread::CallWorker**](camthread-callworker.md) method with that value.</span></span>

<span data-ttu-id="7aecd-114">Die [**~ camthread**](camthread--camthread.md) -deeinigermethode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="7aecd-114">The [**~ CAMThread**](camthread--camthread.md) destructor method calls this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7aecd-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7aecd-115">Requirements</span></span>



| <span data-ttu-id="7aecd-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7aecd-116">Requirement</span></span> | <span data-ttu-id="7aecd-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7aecd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7aecd-118">Header</span><span class="sxs-lookup"><span data-stu-id="7aecd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="7aecd-119"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7aecd-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7aecd-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7aecd-120">Library</span></span><br/> | <dl> <span data-ttu-id="7aecd-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7aecd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7aecd-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7aecd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7aecd-123">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7aecd-123">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




