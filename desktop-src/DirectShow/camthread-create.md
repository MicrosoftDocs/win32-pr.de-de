---
description: Die Create-Methode erstellt den Thread.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: Camthread. Create-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0316cf053326d23d45c0d82f3c410d68d68a92dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371435"
---
# <a name="camthreadcreate-method"></a><span data-ttu-id="c526f-103">Camthread. Create-Methode</span><span class="sxs-lookup"><span data-stu-id="c526f-103">CAMThread.Create method</span></span>

<span data-ttu-id="c526f-104">Die- `Create` Methode erstellt den Thread.</span><span class="sxs-lookup"><span data-stu-id="c526f-104">The `Create` method creates the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="c526f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c526f-105">Syntax</span></span>


```C++
BOOL Create();
```



## <a name="parameters"></a><span data-ttu-id="c526f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c526f-106">Parameters</span></span>

<span data-ttu-id="c526f-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c526f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c526f-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c526f-108">Return value</span></span>

<span data-ttu-id="c526f-109">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="c526f-109">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="c526f-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c526f-110">Remarks</span></span>

<span data-ttu-id="c526f-111">Diese Methode erstellt den Thread mithilfe der [**camthread:: initialthread proc**](camthread-initialthreadproc.md) -Methode für die Thread Prozedur und `this` für das Thread Argument.</span><span class="sxs-lookup"><span data-stu-id="c526f-111">This method creates the thread, using the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method for the thread procedure and `this` for the thread argument.</span></span>

<span data-ttu-id="c526f-112">Die Methode schlägt fehl, wenn der Thread bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c526f-112">The method fails if the thread already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="c526f-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c526f-113">Requirements</span></span>



| <span data-ttu-id="c526f-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c526f-114">Requirement</span></span> | <span data-ttu-id="c526f-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c526f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c526f-116">Header</span><span class="sxs-lookup"><span data-stu-id="c526f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="c526f-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c526f-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="c526f-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c526f-118">Library</span></span><br/> | <dl> <span data-ttu-id="c526f-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c526f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c526f-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c526f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c526f-121">**Camthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c526f-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




