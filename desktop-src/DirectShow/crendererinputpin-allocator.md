---
description: Die zuordnermethode Ruft einen Zeiger auf die Speicherzuweisung ab.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Crendererinputpin. zuordcator-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372092"
---
# <a name="crendererinputpinallocator-method"></a><span data-ttu-id="e3a24-103">Crendererinputpin. zuordcator-Methode</span><span class="sxs-lookup"><span data-stu-id="e3a24-103">CRendererInputPin.Allocator method</span></span>

<span data-ttu-id="e3a24-104">Die- `Allocator` Methode ruft einen Zeiger auf die Speicherzuweisung ab.</span><span class="sxs-lookup"><span data-stu-id="e3a24-104">The `Allocator` method retrieves a pointer to the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3a24-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3a24-105">Syntax</span></span>


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a><span data-ttu-id="e3a24-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e3a24-106">Parameters</span></span>

<span data-ttu-id="e3a24-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="e3a24-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e3a24-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e3a24-108">Return value</span></span>

<span data-ttu-id="e3a24-109">Gibt einen Zeiger auf die [**imemfercator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) -Schnittstelle des Zuordners oder **null** zurück.</span><span class="sxs-lookup"><span data-stu-id="e3a24-109">Returns a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3a24-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e3a24-110">Remarks</span></span>

<span data-ttu-id="e3a24-111">Diese Methode gibt die [**cbaseingeputpin:: m \_ pallocator**](cbaseinputpin-m-pallocator.md) -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="e3a24-111">This method returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span> <span data-ttu-id="e3a24-112">Die-Methode erhöht nicht den Verweis Zähler für die-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e3a24-112">The method does not increment the reference count on the interface.</span></span> <span data-ttu-id="e3a24-113">Bei dieser Methode handelt es sich um eine-Accessor-Methode.</span><span class="sxs-lookup"><span data-stu-id="e3a24-113">This method is strictly an accessor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3a24-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e3a24-114">Requirements</span></span>



| <span data-ttu-id="e3a24-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e3a24-115">Requirement</span></span> | <span data-ttu-id="e3a24-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e3a24-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3a24-117">Header</span><span class="sxs-lookup"><span data-stu-id="e3a24-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e3a24-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a24-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e3a24-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e3a24-119">Library</span></span><br/> | <dl> <span data-ttu-id="e3a24-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e3a24-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3a24-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3a24-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3a24-122">**Crendererinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e3a24-122">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




