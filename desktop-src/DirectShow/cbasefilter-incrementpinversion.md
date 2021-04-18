---
description: Die incremementpinversion-Methode erhöht die Versionsnummer für den Satz von Pins.
ms.assetid: e1b3ec33-104d-4a12-9b11-f8bea09690a7
title: Cbasefilter. incrementpinversion-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.IncrementPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 53e66ccd5bdd34c4767001403439f4372ff2938a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372672"
---
# <a name="cbasefilterincrementpinversion-method"></a><span data-ttu-id="de95c-103">Cbasefilter. incrementpinversion-Methode</span><span class="sxs-lookup"><span data-stu-id="de95c-103">CBaseFilter.IncrementPinVersion method</span></span>

<span data-ttu-id="de95c-104">Die- `IncremementPinVersion` Methode erhöht die Versionsnummer für den Satz von Pins.</span><span class="sxs-lookup"><span data-stu-id="de95c-104">The `IncremementPinVersion` method increments the version number on the set of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="de95c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de95c-105">Syntax</span></span>


```C++
void IncrementPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="de95c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="de95c-106">Parameters</span></span>

<span data-ttu-id="de95c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="de95c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="de95c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="de95c-108">Return value</span></span>

<span data-ttu-id="de95c-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="de95c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="de95c-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de95c-110">Remarks</span></span>

<span data-ttu-id="de95c-111">Diese Methode erhöht die Member-Variable [**cbasefilter:: m \_ pinversion**](cbasefilter-m-pinversion.md) .</span><span class="sxs-lookup"><span data-stu-id="de95c-111">This method increments the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span> <span data-ttu-id="de95c-112">Wenn der Filter Pins dynamisch erstellt oder zerstört, wird diese Methode immer dann aufgerufen, wenn die Pins geändert werden.</span><span class="sxs-lookup"><span data-stu-id="de95c-112">If the filter dynamically creates or destroys pins, call this method whenever the pins change.</span></span>

## <a name="requirements"></a><span data-ttu-id="de95c-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="de95c-113">Requirements</span></span>



| <span data-ttu-id="de95c-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="de95c-114">Requirement</span></span> | <span data-ttu-id="de95c-115">Wert</span><span class="sxs-lookup"><span data-stu-id="de95c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de95c-116">Header</span><span class="sxs-lookup"><span data-stu-id="de95c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="de95c-117"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="de95c-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="de95c-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="de95c-118">Library</span></span><br/> | <dl> <span data-ttu-id="de95c-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="de95c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="de95c-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de95c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="de95c-121">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="de95c-121">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="de95c-122">**Cbasefilter:: getpinversion**</span><span class="sxs-lookup"><span data-stu-id="de95c-122">**CBaseFilter::GetPinVersion**</span></span>](cbasefilter-getpinversion.md)
</dt> </dl>

 

 




