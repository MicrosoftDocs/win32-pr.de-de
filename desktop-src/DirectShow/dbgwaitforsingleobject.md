---
description: Wartet darauf, dass ein Objekt signalisiert wird.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Dbgwaitforsingleobject-Funktion (wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364478"
---
# <a name="dbgwaitforsingleobject-function"></a><span data-ttu-id="6c9b9-103">Dbgwaitforsingleobject-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c9b9-103">DbgWaitForSingleObject function</span></span>

<span data-ttu-id="6c9b9-104">Wartet darauf, dass ein Objekt signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-104">Waits for an object to become signaled.</span></span>

<span data-ttu-id="6c9b9-105">In einem Debugbuild löst diese Funktion eine Assert-Funktion aus, wenn das Timeout Intervall abläuft, bevor das Objekt signalisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-105">In a debug build, this function triggers an assert if the time-out interval expires before the object is signaled.</span></span> <span data-ttu-id="6c9b9-106">Um das Timeout Intervall festzulegen, müssen Sie die [**dbgsetwaittimeout**](dbgsetwaittimeout.md) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="6c9b9-107">In einem Einzelhandels Build entspricht diese Funktion der **WaitForSingleObject** -Funktion mit einem Timeout Intervall von unendlich.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-107">In a retail build, this function is equivalent to the **WaitForSingleObject** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c9b9-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c9b9-108">Syntax</span></span>


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a><span data-ttu-id="6c9b9-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c9b9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c9b9-110">*h*</span><span class="sxs-lookup"><span data-stu-id="6c9b9-110">*h*</span></span> 
</dt> <dd>

<span data-ttu-id="6c9b9-111">Handle für das-Objekt.</span><span class="sxs-lookup"><span data-stu-id="6c9b9-111">Handle to the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6c9b9-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c9b9-112">Requirements</span></span>



| <span data-ttu-id="6c9b9-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c9b9-113">Requirement</span></span> | <span data-ttu-id="6c9b9-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9b9-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9b9-115">Header</span><span class="sxs-lookup"><span data-stu-id="6c9b9-115">Header</span></span><br/>  | <dl> <span data-ttu-id="6c9b9-116"><dt>Wxdebug. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c9b9-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c9b9-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c9b9-117">Library</span></span><br/> | <dl> <span data-ttu-id="6c9b9-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6c9b9-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c9b9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c9b9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9b9-120">Wait-Debugging-Funktionen</span><span class="sxs-lookup"><span data-stu-id="6c9b9-120">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




