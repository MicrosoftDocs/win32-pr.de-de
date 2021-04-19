---
description: Ruft das Handle für den Thread im cmsgthread-Objekt ab.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Cmsgthread. getthreadhandle-Methode (msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354209"
---
# <a name="cmsgthreadgetthreadhandle-method"></a><span data-ttu-id="87fb5-103">Cmsgthread. getthreadhandle-Methode</span><span class="sxs-lookup"><span data-stu-id="87fb5-103">CMsgThread.GetThreadHandle method</span></span>

<span data-ttu-id="87fb5-104">Ruft das Handle für den Thread im [**cmsgthread**](cmsgthread.md) -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="87fb5-104">Retrieves the handle to the thread in the [**CMsgThread**](cmsgthread.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="87fb5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="87fb5-105">Syntax</span></span>


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a><span data-ttu-id="87fb5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="87fb5-106">Parameters</span></span>

<span data-ttu-id="87fb5-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="87fb5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="87fb5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="87fb5-108">Return value</span></span>

<span data-ttu-id="87fb5-109">Gibt das Thread Handle zurück.</span><span class="sxs-lookup"><span data-stu-id="87fb5-109">Returns the thread handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="87fb5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87fb5-110">Remarks</span></span>

<span data-ttu-id="87fb5-111">Das Thread Handle kann an Wait-Funktionen wie [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects)übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="87fb5-111">The thread handle can be passed to wait functions, such as [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span></span> <span data-ttu-id="87fb5-112">Das Thread Handle wird signalisiert, wenn der Thread beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="87fb5-112">The thread handle is signaled when the thread has exited.</span></span>

## <a name="requirements"></a><span data-ttu-id="87fb5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="87fb5-113">Requirements</span></span>



| <span data-ttu-id="87fb5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="87fb5-114">Requirement</span></span> | <span data-ttu-id="87fb5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="87fb5-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="87fb5-116">Header</span><span class="sxs-lookup"><span data-stu-id="87fb5-116">Header</span></span><br/>  | <dl> <span data-ttu-id="87fb5-117"><dt>Msgthrd. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="87fb5-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="87fb5-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="87fb5-118">Library</span></span><br/> | <dl> <span data-ttu-id="87fb5-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="87fb5-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87fb5-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87fb5-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87fb5-121">**Cmsgthread-Klasse**</span><span class="sxs-lookup"><span data-stu-id="87fb5-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

