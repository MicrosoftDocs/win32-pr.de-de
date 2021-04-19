---
description: Die getpin-Methode ruft eine PIN ab. Die cenumpins-Klasse ruft diese Methode auf, um Pins für den Filter aufzuzählen.
ms.assetid: e3ec3f11-1e7d-40b6-810e-3759f0511cb2
title: Cbasefilter. getpin-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bb8341bfd86b96a7358fb23036b71844f77d17a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354217"
---
# <a name="cbasefiltergetpin-method"></a><span data-ttu-id="f4e84-104">Cbasefilter. getpin-Methode</span><span class="sxs-lookup"><span data-stu-id="f4e84-104">CBaseFilter.GetPin method</span></span>

<span data-ttu-id="f4e84-105">Die **getpin** -Methode ruft eine PIN ab.</span><span class="sxs-lookup"><span data-stu-id="f4e84-105">The **GetPin** method retrieves a pin.</span></span> <span data-ttu-id="f4e84-106">Die [**cenumpins**](cenumpins.md) -Klasse ruft diese Methode auf, um Pins für den Filter aufzuzählen.</span><span class="sxs-lookup"><span data-stu-id="f4e84-106">The [**CEnumPins**](cenumpins.md) class calls this method to enumerate pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4e84-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f4e84-107">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="f4e84-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f4e84-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4e84-109">*n*</span><span class="sxs-lookup"><span data-stu-id="f4e84-109">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="f4e84-110">Der null basierte Index der PIN.</span><span class="sxs-lookup"><span data-stu-id="f4e84-110">The zero-based index of the pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4e84-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f4e84-111">Return value</span></span>

<span data-ttu-id="f4e84-112">Gibt einen Zeiger auf das [**cbasepin**](cbasepin.md) -Objekt zurück, das die PIN implementiert.</span><span class="sxs-lookup"><span data-stu-id="f4e84-112">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4e84-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4e84-113">Remarks</span></span>

<span data-ttu-id="f4e84-114">Sie müssen diese rein virtuelle Methode in der abgeleiteten Klasse implementieren.</span><span class="sxs-lookup"><span data-stu-id="f4e84-114">You must implement this pure virtual method in your derived class.</span></span> <span data-ttu-id="f4e84-115">Gibt einen Zeiger auf die *n*-te Pin dieses Filters zurück, indiziert von 0 (null).</span><span class="sxs-lookup"><span data-stu-id="f4e84-115">Return a pointer to the *n* th pin on this filter, indexed from zero.</span></span> <span data-ttu-id="f4e84-116">Sie können eine beliebige Indizierungs Reihenfolge auswählen, solange die Reihenfolge korrigiert ist.</span><span class="sxs-lookup"><span data-stu-id="f4e84-116">You can choose an arbitrary indexing order, as long as the ordering is fixed.</span></span> <span data-ttu-id="f4e84-117">Wenn der Filter Pins hinzufügt oder löscht oder die Bestellung aus einem anderen Grund zur Laufzeit geändert wird, wird die [**cbasefilter:: incrementpinversion**](cbasefilter-incrementpinversion.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f4e84-117">If the filter adds or deletes pins, or the ordering changes for some other reason at run time, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4e84-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4e84-118">Requirements</span></span>



| <span data-ttu-id="f4e84-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4e84-119">Requirement</span></span> | <span data-ttu-id="f4e84-120">Wert</span><span class="sxs-lookup"><span data-stu-id="f4e84-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f4e84-121">Header</span><span class="sxs-lookup"><span data-stu-id="f4e84-121">Header</span></span><br/>  | <dl> <span data-ttu-id="f4e84-122"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e84-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f4e84-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="f4e84-123">Library</span></span><br/> | <dl> <span data-ttu-id="f4e84-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="f4e84-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4e84-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4e84-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4e84-126">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="f4e84-126">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




