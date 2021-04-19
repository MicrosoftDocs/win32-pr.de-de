---
description: Die pstatus-Methode ruft einen Zeiger auf das kritische Abschnitts Objekt des Filters ab.
ms.assetid: 10a2e74b-a5aa-4d68-958e-d86f4b78037e
title: CSource. pstatuelock-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.pStateLock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c0705584a513d64dfd1cd17075d95617234f7f8b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367445"
---
# <a name="csourcepstatelock-method"></a><span data-ttu-id="d9141-103">CSource. pstatuelock-Methode</span><span class="sxs-lookup"><span data-stu-id="d9141-103">CSource.pStateLock method</span></span>

<span data-ttu-id="d9141-104">Die **pstatus** -Methode ruft einen Zeiger auf das kritische Abschnitts Objekt des Filters ab.</span><span class="sxs-lookup"><span data-stu-id="d9141-104">The **pStateLock** method retrieves a pointer to the filter's critical section object.</span></span>

> [!Note]  
> <span data-ttu-id="d9141-105">Obwohl der benannte Wert wie eine Member-Variable lautet, ist **pstatuelock** eine-Methode.</span><span class="sxs-lookup"><span data-stu-id="d9141-105">Although named like a member variable, **pStateLock** is a method.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d9141-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d9141-106">Syntax</span></span>


```C++
CCritSec* pStateLock();
```



## <a name="parameters"></a><span data-ttu-id="d9141-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="d9141-107">Parameters</span></span>

<span data-ttu-id="d9141-108">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d9141-108">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d9141-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d9141-109">Return value</span></span>

<span data-ttu-id="d9141-110">Gibt einen Zeiger auf die [**CSource:: m \_ cstatus**](csource-m-cstatelock.md) -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="d9141-110">Returns a pointer to the [**CSource::m\_cStateLock**](csource-m-cstatelock.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9141-111">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d9141-111">Requirements</span></span>



| <span data-ttu-id="d9141-112">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d9141-112">Requirement</span></span> | <span data-ttu-id="d9141-113">Wert</span><span class="sxs-lookup"><span data-stu-id="d9141-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9141-114">Header</span><span class="sxs-lookup"><span data-stu-id="d9141-114">Header</span></span><br/>  | <dl> <span data-ttu-id="d9141-115"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d9141-115"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="d9141-116">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d9141-116">Library</span></span><br/> | <dl> <span data-ttu-id="d9141-117">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d9141-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9141-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d9141-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9141-119">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d9141-119">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




