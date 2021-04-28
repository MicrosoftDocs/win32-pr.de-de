---
description: 'CTransInPlaceFilter.GetPin-Methode: Die GetPin-Methode ruft einen Pin ab.'
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: CTransInPlaceFilter.GetPin-Methode (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084768"
---
# <a name="ctransinplacefiltergetpin-method"></a><span data-ttu-id="13e31-103">CTransInPlaceFilter.GetPin-Methode</span><span class="sxs-lookup"><span data-stu-id="13e31-103">CTransInPlaceFilter.GetPin method</span></span>

<span data-ttu-id="13e31-104">Die `GetPin` -Methode ruft einen Pin ab.</span><span class="sxs-lookup"><span data-stu-id="13e31-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="13e31-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="13e31-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="13e31-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="13e31-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13e31-107">*n*</span><span class="sxs-lookup"><span data-stu-id="13e31-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="13e31-108">Die Nummer des angegebenen Pins, indiziert von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="13e31-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="13e31-109">Bei diesem Filter ist Pin 0 der Eingabepin und Pin 1 der Ausgabepin.</span><span class="sxs-lookup"><span data-stu-id="13e31-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13e31-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13e31-110">Return value</span></span>

<span data-ttu-id="13e31-111">Gibt einen Zeiger auf das [**CBasePin-Objekt**](cbasepin.md) zurück, das den Pin implementiert, oder **NULL,** wenn die Methode fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="13e31-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="13e31-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="13e31-112">Remarks</span></span>

<span data-ttu-id="13e31-113">Diese Methode überschreibt die [**CTransformFilter::GetPin-Methode.**](ctransformfilter-getpin.md)</span><span class="sxs-lookup"><span data-stu-id="13e31-113">This method overrides the [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="13e31-114">Wenn die -Methode zum ersten Mal aufgerufen wird, werden beide Pins erstellt.</span><span class="sxs-lookup"><span data-stu-id="13e31-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="13e31-115">Diese Methode erhöht den Verweiszähler für den zurückgegebenen Pin nicht, sodass der zurückgegebene Pin keinen ausstehenden Verweiszähler hat.</span><span class="sxs-lookup"><span data-stu-id="13e31-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="13e31-116">Wenn der Aufrufer einen Verweis auf der Stecknadel behalten muss, sollte er die **IUnknown::AddRef-Methode** auf dem Pin aufrufen.</span><span class="sxs-lookup"><span data-stu-id="13e31-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="13e31-117">Wenn der Filter die Standardpins [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) und [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) verwendet, müssen Sie diese Methode wahrscheinlich nicht überschreiben.</span><span class="sxs-lookup"><span data-stu-id="13e31-117">If the filter uses the default [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) and [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="13e31-118">Wenn der Filter jedoch Pins verwendet, die diese Klassen erweitern, müssen Sie diese Methode überschreiben, um Pins dieses Typs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="13e31-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="13e31-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13e31-119">Requirements</span></span>



| <span data-ttu-id="13e31-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13e31-120">Requirement</span></span> | <span data-ttu-id="13e31-121">Wert</span><span class="sxs-lookup"><span data-stu-id="13e31-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13e31-122">Header</span><span class="sxs-lookup"><span data-stu-id="13e31-122">Header</span></span><br/>  | <dl> <span data-ttu-id="13e31-123"><dt>Transip.h (einschließlich Streams.h)</dt></span><span class="sxs-lookup"><span data-stu-id="13e31-123"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="13e31-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="13e31-124">Library</span></span><br/> | <dl> <span data-ttu-id="13e31-125"><dt>Strmbase.lib (Einzelhandels-Builds); </dt> <dt>Strmbasd.lib (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="13e31-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13e31-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="13e31-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13e31-127">**CTransInPlaceFilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="13e31-127">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




