---
description: Gibt true zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Critcheckin-Funktion (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368390"
---
# <a name="critcheckin-function"></a><span data-ttu-id="83d3b-103">Critcheckin-Funktion</span><span class="sxs-lookup"><span data-stu-id="83d3b-103">CritCheckIn function</span></span>

<span data-ttu-id="83d3b-104">Gibt **true** zurück, wenn der aktuelle Thread der Besitzer des angegebenen kritischen Abschnitts ist.</span><span class="sxs-lookup"><span data-stu-id="83d3b-104">Returns **TRUE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="83d3b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="83d3b-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="83d3b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="83d3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83d3b-107">*pccrit*</span><span class="sxs-lookup"><span data-stu-id="83d3b-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="83d3b-108">Zeiger auf einen kritischen [**ccritsec**](ccritsec.md) -Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="83d3b-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83d3b-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="83d3b-109">Return value</span></span>

<span data-ttu-id="83d3b-110">In Debugbuilds gibt **true** zurück, wenn der aktuelle Thread der Besitzer dieses kritischen Abschnitts ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="83d3b-110">In debug builds, returns **TRUE** if the current thread is the owner of this critical section, or **FALSE** otherwise.</span></span> <span data-ttu-id="83d3b-111">In Einzelhandels Builds gibt immer **true** zurück.</span><span class="sxs-lookup"><span data-stu-id="83d3b-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="83d3b-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="83d3b-112">Remarks</span></span>

<span data-ttu-id="83d3b-113">Diese Funktion ist im [**Assert**](assert.md) -Makro besonders nützlich, um zu testen, ob ein Thread eine bestimmte Sperre besitzt.</span><span class="sxs-lookup"><span data-stu-id="83d3b-113">This function is especially useful within the [**ASSERT**](assert.md) macro, to test whether a thread owns a given lock.</span></span>

## <a name="examples"></a><span data-ttu-id="83d3b-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="83d3b-114">Examples</span></span>

<span data-ttu-id="83d3b-115">Das folgende Codebeispiel zeigt die Verwendung dieser Funktion:</span><span class="sxs-lookup"><span data-stu-id="83d3b-115">The following code example shows how to use this function:</span></span>


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a><span data-ttu-id="83d3b-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="83d3b-116">Requirements</span></span>



| <span data-ttu-id="83d3b-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="83d3b-117">Requirement</span></span> | <span data-ttu-id="83d3b-118">Wert</span><span class="sxs-lookup"><span data-stu-id="83d3b-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="83d3b-119">Header</span><span class="sxs-lookup"><span data-stu-id="83d3b-119">Header</span></span><br/>  | <dl> <span data-ttu-id="83d3b-120"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="83d3b-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="83d3b-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="83d3b-121">Library</span></span><br/> | <dl> <span data-ttu-id="83d3b-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="83d3b-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83d3b-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="83d3b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83d3b-124">Kritische Abschnitts Debuggingfunktionen</span><span class="sxs-lookup"><span data-stu-id="83d3b-124">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




