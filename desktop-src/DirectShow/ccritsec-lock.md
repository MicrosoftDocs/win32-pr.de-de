---
description: Die Lock-Methode sperrt das Critical Section-Objekt.
ms.assetid: b08be5ec-3f02-4ed8-8791-20e4d2a0c55f
title: Ccritsec. Lock-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Lock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 19599e9cd3c3b8fa913bd07d22fe743aaaa1382f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370943"
---
# <a name="ccritseclock-method"></a><span data-ttu-id="9f382-103">Ccritsec. Lock-Methode</span><span class="sxs-lookup"><span data-stu-id="9f382-103">CCritSec.Lock method</span></span>

<span data-ttu-id="9f382-104">Die **Lock** -Methode sperrt das Critical Section-Objekt.</span><span class="sxs-lookup"><span data-stu-id="9f382-104">The **Lock** method locks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f382-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f382-105">Syntax</span></span>


```C++
void Lock();
```



## <a name="parameters"></a><span data-ttu-id="9f382-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f382-106">Parameters</span></span>

<span data-ttu-id="9f382-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="9f382-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9f382-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f382-108">Return value</span></span>

<span data-ttu-id="9f382-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="9f382-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f382-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f382-110">Remarks</span></span>

<span data-ttu-id="9f382-111">Diese Methode ruft die [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="9f382-111">This method calls the [**EnterCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-entercriticalsection) function.</span></span>

<span data-ttu-id="9f382-112">Zum Entsperren des kritischen Abschnitts wird die [**ccritsec:: Unlock**](ccritsec-unlock.md) -Member-Funktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="9f382-112">Call the [**CCritSec::Unlock**](ccritsec-unlock.md) member function to unlock the critical section.</span></span> <span data-ttu-id="9f382-113">Sie können mehrere Aufrufe der **Lock** -Methode im gleichen Thread durchführen. Stellen Sie sicher, dass Sie die **Sperre** beliebig oft aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="9f382-113">You can make multiple calls to the **Lock** method on the same thread; be sure to call **Unlock** a corresponding number of times.</span></span>

<span data-ttu-id="9f382-114">Wenn das Objekt bereits von einem anderen Thread gesperrt ist, wird die **ccritsec:: Lock** -Methode blockiert, bis das Objekt freigegeben wird, oder bis eine mögliche deadlockausnahme auftritt.</span><span class="sxs-lookup"><span data-stu-id="9f382-114">If the object is already locked by another thread, the **CCritSec::Lock** method blocks until the object is released, or until a possible-deadlock exception occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f382-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f382-115">Requirements</span></span>



| <span data-ttu-id="9f382-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f382-116">Requirement</span></span> | <span data-ttu-id="9f382-117">Wert</span><span class="sxs-lookup"><span data-stu-id="9f382-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f382-118">Header</span><span class="sxs-lookup"><span data-stu-id="9f382-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9f382-119"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f382-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9f382-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="9f382-120">Library</span></span><br/> | <dl> <span data-ttu-id="9f382-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="9f382-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f382-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f382-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f382-123">**Ccritsec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="9f382-123">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

