---
description: Wartet darauf, dass alle (oder alle) der angegebenen Objekte signalisiert werden.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Dbgwaitformultipleobjects-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364539"
---
# <a name="dbgwaitformultipleobjects-function"></a><span data-ttu-id="4b122-103">Dbgwaitformultipleobjects-Funktion</span><span class="sxs-lookup"><span data-stu-id="4b122-103">DbgWaitForMultipleObjects function</span></span>

<span data-ttu-id="4b122-104">Wartet darauf, dass alle (oder alle) der angegebenen Objekte signalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b122-104">Waits for any (or all) of the specified objects to be signaled.</span></span>

<span data-ttu-id="4b122-105">In einem Debugbuild löst diese Funktion eine Assert-Funktion aus, wenn das Timeout Intervall abläuft, bevor die Objekte signalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b122-105">In a debug build, this function triggers an assert if the time-out interval expires before the objects are signaled.</span></span> <span data-ttu-id="4b122-106">Um das Timeout Intervall festzulegen, müssen Sie die [**dbgsetwaittimeout**](dbgsetwaittimeout.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4b122-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="4b122-107">In einem Einzelhandels Build entspricht diese Funktion der **WaitForMultipleObjects** -Funktion mit einem Timeout Intervall von unendlich.</span><span class="sxs-lookup"><span data-stu-id="4b122-107">In a retail build, this function is equivalent to the **WaitForMultipleObjects** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="4b122-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="4b122-108">Syntax</span></span>


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a><span data-ttu-id="4b122-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="4b122-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b122-110">*nCount*</span><span class="sxs-lookup"><span data-stu-id="4b122-110">*nCount*</span></span> 
</dt> <dd>

<span data-ttu-id="4b122-111">Anzahl von Objekten.</span><span class="sxs-lookup"><span data-stu-id="4b122-111">Number of objects.</span></span>

</dd> <dt>

<span data-ttu-id="4b122-112">*lphandles*</span><span class="sxs-lookup"><span data-stu-id="4b122-112">*lpHandles*</span></span> 
</dt> <dd>

<span data-ttu-id="4b122-113">Array von Handles zu Objekten, Größe *nCount*.</span><span class="sxs-lookup"><span data-stu-id="4b122-113">Array of handles to objects, of size *nCount*.</span></span>

</dd> <dt>

<span data-ttu-id="4b122-114">*bwaitall*</span><span class="sxs-lookup"><span data-stu-id="4b122-114">*bWaitAll*</span></span> 
</dt> <dd>

<span data-ttu-id="4b122-115">Boolescher Wert, der angibt, ob auf alle-Objekte gewartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="4b122-115">Boolean value that specifies whether to wait for all of the objects.</span></span> <span data-ttu-id="4b122-116">**True** gibt an, dass die Funktion darauf wartet, dass alle Objekte signalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="4b122-116">If **TRUE**, the function waits for all of the objects to be signaled.</span></span> <span data-ttu-id="4b122-117">Andernfalls wartet es darauf, dass mindestens ein Objekt signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="4b122-117">Otherwise, it waits for at least one object to be signaled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4b122-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b122-118">Requirements</span></span>



| <span data-ttu-id="4b122-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b122-119">Requirement</span></span> | <span data-ttu-id="4b122-120">Wert</span><span class="sxs-lookup"><span data-stu-id="4b122-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b122-121">Header</span><span class="sxs-lookup"><span data-stu-id="4b122-121">Header</span></span><br/>  | <dl> <span data-ttu-id="4b122-122"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4b122-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4b122-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="4b122-123">Library</span></span><br/> | <dl> <span data-ttu-id="4b122-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="4b122-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b122-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b122-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b122-126">Wait-Debugging-Funktionen</span><span class="sxs-lookup"><span data-stu-id="4b122-126">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




