---
description: Die getpincount-Methode ruft die Anzahl der Pins für den Filter ab.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Ctransformfilter. getpincount-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371680"
---
# <a name="ctransformfiltergetpincount-method"></a><span data-ttu-id="befc8-103">Ctransformfilter. getpincount-Methode</span><span class="sxs-lookup"><span data-stu-id="befc8-103">CTransformFilter.GetPinCount method</span></span>

<span data-ttu-id="befc8-104">Die- `GetPinCount` Methode ruft die Anzahl der Pins für den Filter ab.</span><span class="sxs-lookup"><span data-stu-id="befc8-104">The `GetPinCount` method retrieves the number of pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="befc8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="befc8-105">Syntax</span></span>


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a><span data-ttu-id="befc8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="befc8-106">Parameters</span></span>

<span data-ttu-id="befc8-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="befc8-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="befc8-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="befc8-108">Return value</span></span>

<span data-ttu-id="befc8-109">Gibt 2 zurück.</span><span class="sxs-lookup"><span data-stu-id="befc8-109">Returns 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="befc8-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="befc8-110">Remarks</span></span>

<span data-ttu-id="befc8-111">Diese Methode überschreibt die [**cbasefilter:: getpincount**](cbasefilter-getpincount.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="befc8-111">This method overrides the [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md) method.</span></span> <span data-ttu-id="befc8-112">Die **ctransformfilter** -Klasse unterstützt genau eine Eingabe-PIN und eine Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="befc8-112">The **CTransformFilter** class supports exactly one input pin and one output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="befc8-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="befc8-113">Requirements</span></span>



| <span data-ttu-id="befc8-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="befc8-114">Requirement</span></span> | <span data-ttu-id="befc8-115">Wert</span><span class="sxs-lookup"><span data-stu-id="befc8-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="befc8-116">Header</span><span class="sxs-lookup"><span data-stu-id="befc8-116">Header</span></span><br/>  | <dl> <span data-ttu-id="befc8-117"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="befc8-117"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="befc8-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="befc8-118">Library</span></span><br/> | <dl> <span data-ttu-id="befc8-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="befc8-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="befc8-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="befc8-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="befc8-121">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="befc8-121">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




