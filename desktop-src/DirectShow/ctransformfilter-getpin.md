---
description: Die getpin-Methode ruft eine PIN ab.
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Ctransformfilter. getpin-Methode (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 30567db84eefd5471dbbe1fbd2d2e5ed64514ba2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373915"
---
# <a name="ctransformfiltergetpin-method"></a><span data-ttu-id="ce3b4-103">Ctransformfilter. getpin-Methode</span><span class="sxs-lookup"><span data-stu-id="ce3b4-103">CTransformFilter.GetPin method</span></span>

<span data-ttu-id="ce3b4-104">Die- `GetPin` Methode ruft eine PIN ab.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3b4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce3b4-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="ce3b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce3b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce3b4-107">*n*</span><span class="sxs-lookup"><span data-stu-id="ce3b4-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="ce3b4-108">Nummer der angegebenen PIN, indiziert von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="ce3b4-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="ce3b4-109">Bei diesem Filter ist Pin 0 die Eingabe-PIN, und Pin 1 ist die Ausgabe-PIN.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce3b4-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce3b4-110">Return value</span></span>

<span data-ttu-id="ce3b4-111">Gibt einen Zeiger auf das [**cbasepin**](cbasepin.md) -Objekt zurück, das die PIN implementiert, oder **null** , wenn die Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce3b4-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce3b4-112">Remarks</span></span>

<span data-ttu-id="ce3b4-113">Diese Methode implementiert die rein virtuelle [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-113">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span> <span data-ttu-id="ce3b4-114">Wenn die-Methode zum ersten Mal aufgerufen wird, werden beide Pins erstellt.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="ce3b4-115">Diese Methode erhöht nicht den Verweis Zähler für die zurückgegebene PIN, sodass die zurückgegebene Pin keinen ausstehenden Verweis Zähler enthält.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="ce3b4-116">Wenn der Aufrufer einen Verweis auf die PIN aufbewahren muss, sollte die **IUnknown:: adressf** -Methode für die PIN aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="ce3b4-117">Wenn der Filter die standardmäßigen [**ctransforminputpin**](ctransforminputpin.md) -und [**ctransformoutputpin**](ctransformoutputpin.md) -Pins verwendet, müssen Sie diese Methode wahrscheinlich nicht außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-117">If the filter uses the default [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="ce3b4-118">Wenn der Filter Pins verwendet, mit denen diese Klassen erweitert werden, müssen Sie diese Methode jedoch außer Kraft setzen, um Pins dieses Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="ce3b4-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3b4-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce3b4-119">Requirements</span></span>



| <span data-ttu-id="ce3b4-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce3b4-120">Requirement</span></span> | <span data-ttu-id="ce3b4-121">Wert</span><span class="sxs-lookup"><span data-stu-id="ce3b4-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3b4-122">Header</span><span class="sxs-lookup"><span data-stu-id="ce3b4-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ce3b4-123"><dt>Transfrm. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce3b4-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ce3b4-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce3b4-124">Library</span></span><br/> | <dl> <span data-ttu-id="ce3b4-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ce3b4-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce3b4-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce3b4-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3b4-127">**Ctransformfilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ce3b4-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




