---
description: 'Die endflush-Methode beendet einen Löschvorgang. Diese Methode überschreibt die ctransformfilter:: endflush-Methode.'
ms.assetid: e7dfc6f9-1630-426b-95b2-9814331b5e61
title: Cvideotransformfilter. endflush-Methode (vtrans. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CVideoTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ca160bd2e3e66df3bcf6f293abe6f828309172c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359662"
---
# <a name="cvideotransformfilterendflush-method"></a><span data-ttu-id="b354c-104">Cvideotransformfilter. endflush-Methode</span><span class="sxs-lookup"><span data-stu-id="b354c-104">CVideoTransformFilter.EndFlush method</span></span>

<span data-ttu-id="b354c-105">Die- `EndFlush` Methode beendet einen Löschvorgang.</span><span class="sxs-lookup"><span data-stu-id="b354c-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="b354c-106">Diese Methode überschreibt die [**ctransformfilter:: endflush**](ctransformfilter-endflush.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b354c-106">This method overrides the [**CTransformFilter::EndFlush**](ctransformfilter-endflush.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b354c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b354c-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="b354c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b354c-108">Parameters</span></span>

<span data-ttu-id="b354c-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="b354c-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b354c-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b354c-110">Return value</span></span>

<span data-ttu-id="b354c-111">Gibt \_ bei Erfolg S OK oder einen Fehlercode zurück.</span><span class="sxs-lookup"><span data-stu-id="b354c-111">Returns S\_OK if successful, or an error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b354c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b354c-112">Remarks</span></span>

<span data-ttu-id="b354c-113">Diese Methode setzt alle internen Leistungsmessungen des Filters zurück.</span><span class="sxs-lookup"><span data-stu-id="b354c-113">This method resets all of the filter's internal performance measurements.</span></span>

## <a name="requirements"></a><span data-ttu-id="b354c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b354c-114">Requirements</span></span>



| <span data-ttu-id="b354c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b354c-115">Requirement</span></span> | <span data-ttu-id="b354c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="b354c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b354c-117">Header</span><span class="sxs-lookup"><span data-stu-id="b354c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="b354c-118"><dt>Vtrans. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b354c-118"><dt>Vtrans.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b354c-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b354c-119">Library</span></span><br/> | <dl> <span data-ttu-id="b354c-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b354c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b354c-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b354c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b354c-122">**Cvideotransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b354c-122">**CVideoTransformFilter Class**</span></span>](cvideotransformfilter.md)
</dt> </dl>

 

 




