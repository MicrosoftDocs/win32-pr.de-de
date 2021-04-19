---
description: Die getmediatypeer Version-Methode ruft eine Versionsnummer für den Satz bevorzugter Medientypen ab.
ms.assetid: bd7b8070-eac5-458c-ada0-7fb0d789dd54
title: Cbasepin. getmediatypeer Version-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.GetMediaTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fe01d33d7a7c1cb65bc0e2391af63e3519d9cce3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371565"
---
# <a name="cbasepingetmediatypeversion-method"></a><span data-ttu-id="49a79-103">Cbasepin. getmediatypeer Version-Methode</span><span class="sxs-lookup"><span data-stu-id="49a79-103">CBasePin.GetMediaTypeVersion method</span></span>

<span data-ttu-id="49a79-104">Die- `GetMediaTypeVersion` Methode ruft eine Versionsnummer für den Satz bevorzugter Medientypen ab.</span><span class="sxs-lookup"><span data-stu-id="49a79-104">The `GetMediaTypeVersion` method retrieves a version number for the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="49a79-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49a79-105">Syntax</span></span>


```C++
virtual LONG GetMediaTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="49a79-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="49a79-106">Parameters</span></span>

<span data-ttu-id="49a79-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="49a79-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="49a79-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49a79-108">Return value</span></span>

<span data-ttu-id="49a79-109">Gibt die [**cbasepin:: m \_ typeversion**](cbasepin-m-typeversion.md) -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="49a79-109">Returns the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="49a79-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49a79-110">Remarks</span></span>

<span data-ttu-id="49a79-111">Der **cbasepin** -Konstruktor initialisiert die Versionsnummer auf 1.</span><span class="sxs-lookup"><span data-stu-id="49a79-111">The **CBasePin** constructor initializes the version number to 1.</span></span> <span data-ttu-id="49a79-112">In der Basisklasse ändert sich diese Zahl nie.</span><span class="sxs-lookup"><span data-stu-id="49a79-112">In the base class, this number never changes.</span></span> <span data-ttu-id="49a79-113">Wenn die PIN die Liste der bevorzugten Medientypen dynamisch ändert, sollte Sie die Versionsnummer erhöhen, wenn die Liste geändert wird.</span><span class="sxs-lookup"><span data-stu-id="49a79-113">If the pin dynamically changes its list of preferred media types, it should increment the version number whenever the list changes.</span></span> <span data-ttu-id="49a79-114">Um die Versionsnummer zu erhöhen, müssen Sie die [**cbasepin:: incrementtypeversion**](cbasepin-incrementtypeversion.md) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="49a79-114">To increment the version number, call the [**CBasePin::IncrementTypeVersion**](cbasepin-incrementtypeversion.md) method.</span></span>

<span data-ttu-id="49a79-115">Der Medientyp Enumerator, der von der [**cenummediatypes**](cenummediatypes.md) -Klasse implementiert wird, verwendet die Versionsnummer, um sich selbst mit der PIN zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="49a79-115">The media type enumerator, which is implemented by the [**CEnumMediaTypes**](cenummediatypes.md) class, uses the version number to keep itself synchronized with the pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="49a79-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49a79-116">Requirements</span></span>



| <span data-ttu-id="49a79-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49a79-117">Requirement</span></span> | <span data-ttu-id="49a79-118">Wert</span><span class="sxs-lookup"><span data-stu-id="49a79-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49a79-119">Header</span><span class="sxs-lookup"><span data-stu-id="49a79-119">Header</span></span><br/>  | <dl> <span data-ttu-id="49a79-120"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49a79-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="49a79-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="49a79-121">Library</span></span><br/> | <dl> <span data-ttu-id="49a79-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="49a79-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49a79-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49a79-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49a79-124">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="49a79-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




