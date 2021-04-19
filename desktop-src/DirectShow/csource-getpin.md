---
description: 'Die getpin-Methode ruft eine PIN ab. Diese Methode implementiert die rein virtuelle cbasefilter:: getpin-Methode.'
ms.assetid: 7f30a1ba-8e7b-4bde-9f4d-a85b3a2122e9
title: CSource. getpin-Methode (Quelle. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f11ff79c9d2d535a3370183b7f36bae25c5e1383
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370041"
---
# <a name="csourcegetpin-method"></a><span data-ttu-id="b73c4-104">CSource. getpin-Methode</span><span class="sxs-lookup"><span data-stu-id="b73c4-104">CSource.GetPin method</span></span>

<span data-ttu-id="b73c4-105">Die- `GetPin` Methode ruft eine PIN ab.</span><span class="sxs-lookup"><span data-stu-id="b73c4-105">The `GetPin` method retrieves a pin.</span></span> <span data-ttu-id="b73c4-106">Diese Methode implementiert die rein virtuelle [**cbasefilter:: getpin**](cbasefilter-getpin.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b73c4-106">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="b73c4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="b73c4-107">Syntax</span></span>


```C++
CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="b73c4-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="b73c4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b73c4-109">*n*</span><span class="sxs-lookup"><span data-stu-id="b73c4-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="b73c4-110">Die Nummer der angegebenen PIN.</span><span class="sxs-lookup"><span data-stu-id="b73c4-110">Number of the specified pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b73c4-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b73c4-111">Return value</span></span>

<span data-ttu-id="b73c4-112">Gibt den Zeiger auf das [**cbasepin**](cbasepin.md) -Objekt zurück, das die PIN implementiert, oder **null** , wenn der Index außerhalb des gültigen Bereichs liegt.</span><span class="sxs-lookup"><span data-stu-id="b73c4-112">Returns the pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the index is out of range.</span></span>

## <a name="requirements"></a><span data-ttu-id="b73c4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b73c4-113">Requirements</span></span>



| <span data-ttu-id="b73c4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b73c4-114">Requirement</span></span> | <span data-ttu-id="b73c4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b73c4-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b73c4-116">Header</span><span class="sxs-lookup"><span data-stu-id="b73c4-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b73c4-117"><dt>Source. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b73c4-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b73c4-118">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b73c4-118">Library</span></span><br/> | <dl> <span data-ttu-id="b73c4-119">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="b73c4-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b73c4-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b73c4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b73c4-121">**CSource-Klasse**</span><span class="sxs-lookup"><span data-stu-id="b73c4-121">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




