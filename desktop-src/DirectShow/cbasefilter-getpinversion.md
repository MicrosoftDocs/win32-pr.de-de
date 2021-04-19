---
description: Die getpinversion-Methode ruft eine Versionsnummer für den Satz von Pins für diesen Filter ab.
ms.assetid: 6cc186b2-4d9f-4d1c-a8b3-975e9c248df7
title: Cbasefilter. getpinversion-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2d8cb2e67f88ef7a02958cc851dd9b8c0c751096
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361419"
---
# <a name="cbasefiltergetpinversion-method"></a><span data-ttu-id="3aa03-103">Cbasefilter. getpinversion-Methode</span><span class="sxs-lookup"><span data-stu-id="3aa03-103">CBaseFilter.GetPinVersion method</span></span>

<span data-ttu-id="3aa03-104">Die- `GetPinVersion` Methode ruft eine Versionsnummer für den Satz von Pins für diesen Filter ab.</span><span class="sxs-lookup"><span data-stu-id="3aa03-104">The `GetPinVersion` method retrieves a version number for the set of pins on this filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa03-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3aa03-105">Syntax</span></span>


```C++
virtual long GetPinVersion();
```



## <a name="parameters"></a><span data-ttu-id="3aa03-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3aa03-106">Parameters</span></span>

<span data-ttu-id="3aa03-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3aa03-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3aa03-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3aa03-108">Return value</span></span>

<span data-ttu-id="3aa03-109">Gibt die [**cbasefilter:: m \_ pinversion**](cbasefilter-m-pinversion.md) -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="3aa03-109">Returns the [**CBaseFilter::m\_PinVersion**](cbasefilter-m-pinversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="3aa03-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3aa03-110">Remarks</span></span>

<span data-ttu-id="3aa03-111">Der **cbasefilter** -Konstruktor initialisiert die PIN-Version auf 1.</span><span class="sxs-lookup"><span data-stu-id="3aa03-111">The **CBaseFilter** constructor initializes the pin version to 1.</span></span> <span data-ttu-id="3aa03-112">In der Basisklasse ändert sich diese Zahl nie.</span><span class="sxs-lookup"><span data-stu-id="3aa03-112">In the base class, this number never changes.</span></span> <span data-ttu-id="3aa03-113">Wenn der Filter Pins dynamisch erstellt oder zerstört, sollte er die PIN-Version erhöhen, wenn die Pins geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3aa03-113">If the filter dynamically creates or destroys pins, it should increment the pin version whenever the pins change.</span></span> <span data-ttu-id="3aa03-114">Um die Versionsnummer zu erhöhen, müssen Sie die [**cbasefilter:: incrementpinversion**](cbasefilter-incrementpinversion.md) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3aa03-114">To increment the version number, call the [**CBaseFilter::IncrementPinVersion**](cbasefilter-incrementpinversion.md) method.</span></span>

<span data-ttu-id="3aa03-115">Das Pin-Enumeratorobjekt, das von der [**cenumpins**](cenumpins.md) -Klasse implementiert wird, verwendet die PIN-Version, um sich selbst mit dem Filter zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3aa03-115">The pin enumerator object, which is implemented by the [**CEnumPins**](cenumpins.md) class, uses the pin version to keep itself synchronized with the filter.</span></span>

## <a name="requirements"></a><span data-ttu-id="3aa03-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3aa03-116">Requirements</span></span>



| <span data-ttu-id="3aa03-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3aa03-117">Requirement</span></span> | <span data-ttu-id="3aa03-118">Wert</span><span class="sxs-lookup"><span data-stu-id="3aa03-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3aa03-119">Header</span><span class="sxs-lookup"><span data-stu-id="3aa03-119">Header</span></span><br/>  | <dl> <span data-ttu-id="3aa03-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3aa03-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3aa03-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="3aa03-121">Library</span></span><br/> | <dl> <span data-ttu-id="3aa03-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="3aa03-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3aa03-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3aa03-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa03-124">**Cbasefilter-Klasse**</span><span class="sxs-lookup"><span data-stu-id="3aa03-124">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




