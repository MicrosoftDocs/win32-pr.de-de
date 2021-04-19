---
description: Die Unlock-Methode entsperrt das Objekt des kritischen Abschnitts.
ms.assetid: 61811e0e-df77-48e9-96d5-b7dff8c8db9b
title: Ccritsec. Unlock-Methode (wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec.Unlock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca84ce452d71d0d3111039d7a95d8f5dd3155058
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370197"
---
# <a name="ccritsecunlock-method"></a><span data-ttu-id="1d8cc-103">Ccritsec. Unlock-Methode</span><span class="sxs-lookup"><span data-stu-id="1d8cc-103">CCritSec.Unlock method</span></span>

<span data-ttu-id="1d8cc-104">Die **Unlock** -Methode entsperrt das Objekt des kritischen Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-104">The **Unlock** method unlocks the critical section object.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d8cc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1d8cc-105">Syntax</span></span>


```C++
void Unlock();
```



## <a name="parameters"></a><span data-ttu-id="1d8cc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1d8cc-106">Parameters</span></span>

<span data-ttu-id="1d8cc-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d8cc-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1d8cc-108">Return value</span></span>

<span data-ttu-id="1d8cc-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d8cc-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1d8cc-110">Remarks</span></span>

<span data-ttu-id="1d8cc-111">Diese Methode ruft die [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) -Funktion auf.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-111">This method calls the [**LeaveCriticalSection**](/windows/desktop/api/synchapi/nf-synchapi-leavecriticalsection) function.</span></span> <span data-ttu-id="1d8cc-112">Diese Methode wird einmal für jeden aufzurufenden Befehl der [**ccritsec:: Lock**](ccritsec-lock.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="1d8cc-112">Call this method once for each call to the [**CCritSec::Lock**](ccritsec-lock.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d8cc-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1d8cc-113">Requirements</span></span>



| <span data-ttu-id="1d8cc-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1d8cc-114">Requirement</span></span> | <span data-ttu-id="1d8cc-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1d8cc-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d8cc-116">Header</span><span class="sxs-lookup"><span data-stu-id="1d8cc-116">Header</span></span><br/>  | <dl> <span data-ttu-id="1d8cc-117"><dt>Wxutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d8cc-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1d8cc-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1d8cc-118">Library</span></span><br/> | <dl> <span data-ttu-id="1d8cc-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1d8cc-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d8cc-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d8cc-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d8cc-121">**Ccritsec-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1d8cc-121">**CCritSec Class**</span></span>](ccritsec.md)
</dt> </dl>

 

