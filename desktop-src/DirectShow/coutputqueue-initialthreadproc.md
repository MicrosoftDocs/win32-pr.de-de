---
description: 'Die initialthread proc-Methode ruft die coutputqueue:: Thread proc-Methode auf, wenn der Thread erstellt wird.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Initialthread proc-Methode (outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371271"
---
# <a name="coutputqueueinitialthreadproc-method"></a><span data-ttu-id="aa78f-103">COutputQueue.Initialthread proc-Methode</span><span class="sxs-lookup"><span data-stu-id="aa78f-103">COutputQueue.InitialThreadProc method</span></span>

<span data-ttu-id="aa78f-104">Die- `InitialThreadProc` Methode ruft die [**coutputqueue:: Thread proc**](coutputqueue-threadproc.md) -Methode auf, wenn der Thread erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="aa78f-104">The `InitialThreadProc` method calls the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method when the thread is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa78f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa78f-105">Syntax</span></span>


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="aa78f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aa78f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aa78f-107">*teuren*</span><span class="sxs-lookup"><span data-stu-id="aa78f-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="aa78f-108">`this` Zeichner.</span><span class="sxs-lookup"><span data-stu-id="aa78f-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aa78f-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aa78f-109">Return value</span></span>

<span data-ttu-id="aa78f-110">Gibt den Wert zurück, der von der [**coutputqueue:: ThreadProc**](coutputqueue-threadproc.md) -Methode zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aa78f-110">Returns the value returned by the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa78f-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aa78f-111">Remarks</span></span>

<span data-ttu-id="aa78f-112">Diese Methode ist die Thread Prozedur für den Arbeits Thread des Objekts.</span><span class="sxs-lookup"><span data-stu-id="aa78f-112">This method is the thread procedure for the object's worker thread.</span></span> <span data-ttu-id="aa78f-113">Der Zeiger des Objekts `this` ist der Thread Parameter.</span><span class="sxs-lookup"><span data-stu-id="aa78f-113">The object's `this` pointer is the thread parameter.</span></span> <span data-ttu-id="aa78f-114">Die-Methode dereferenziert dieses, um **ThreadProc** aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="aa78f-114">The method dereferences this to call **ThreadProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa78f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aa78f-115">Requirements</span></span>



| <span data-ttu-id="aa78f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aa78f-116">Requirement</span></span> | <span data-ttu-id="aa78f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="aa78f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa78f-118">Header</span><span class="sxs-lookup"><span data-stu-id="aa78f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="aa78f-119"><dt>Outputq. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aa78f-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aa78f-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="aa78f-120">Library</span></span><br/> | <dl> <span data-ttu-id="aa78f-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="aa78f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa78f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aa78f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa78f-123">**Coutputqueue-Klasse**</span><span class="sxs-lookup"><span data-stu-id="aa78f-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




