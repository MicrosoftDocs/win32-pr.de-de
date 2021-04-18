---
description: Die incrementtypeversion-Methode erhöht die Versionsnummer für den Satz bevorzugter Medientypen.
ms.assetid: 30cad0ae-58e7-47f6-94ee-75e24ce0a7e9
title: Cbasepin. incrementtypeversion-Methode (amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.IncrementTypeVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6db3c08972bebbaf1172c44412ae9c8652100da8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371534"
---
# <a name="cbasepinincrementtypeversion-method"></a><span data-ttu-id="1a8b6-103">Cbasepin. incrementtypeversion-Methode</span><span class="sxs-lookup"><span data-stu-id="1a8b6-103">CBasePin.IncrementTypeVersion method</span></span>

<span data-ttu-id="1a8b6-104">Die- `IncrementTypeVersion` Methode erhöht die Versionsnummer für den Satz bevorzugter Medientypen.</span><span class="sxs-lookup"><span data-stu-id="1a8b6-104">The `IncrementTypeVersion` method increments the version number on the set of preferred media types.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a8b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a8b6-105">Syntax</span></span>


```C++
void IncrementTypeVersion();
```



## <a name="parameters"></a><span data-ttu-id="1a8b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a8b6-106">Parameters</span></span>

<span data-ttu-id="1a8b6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1a8b6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1a8b6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a8b6-108">Return value</span></span>

<span data-ttu-id="1a8b6-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="1a8b6-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a8b6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1a8b6-110">Remarks</span></span>

<span data-ttu-id="1a8b6-111">Diese Methode erhöht die Member-Variable [**cbasepin:: m \_ typeversion**](cbasepin-m-typeversion.md) .</span><span class="sxs-lookup"><span data-stu-id="1a8b6-111">This method increments the [**CBasePin::m\_TypeVersion**](cbasepin-m-typeversion.md) member variable.</span></span> <span data-ttu-id="1a8b6-112">Wenn die PIN die Liste der bevorzugten Medientypen dynamisch ändert, wird diese Methode immer dann aufgerufen, wenn die Liste geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1a8b6-112">If the pin dynamically changes the list of preferred media types, call this method whenever the list changes.</span></span> <span data-ttu-id="1a8b6-113">Weitere Informationen finden Sie unter [**cbasepin:: getmediatypeer Version**](cbasepin-getmediatypeversion.md).</span><span class="sxs-lookup"><span data-stu-id="1a8b6-113">For more information, see [**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1a8b6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1a8b6-114">Requirements</span></span>



| <span data-ttu-id="1a8b6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1a8b6-115">Requirement</span></span> | <span data-ttu-id="1a8b6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="1a8b6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1a8b6-117">Header</span><span class="sxs-lookup"><span data-stu-id="1a8b6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="1a8b6-118"><dt>Amfilter. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8b6-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1a8b6-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="1a8b6-119">Library</span></span><br/> | <dl> <span data-ttu-id="1a8b6-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="1a8b6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1a8b6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a8b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a8b6-122">**Cbasepin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="1a8b6-122">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




