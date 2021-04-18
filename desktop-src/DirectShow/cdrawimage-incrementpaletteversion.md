---
description: Die incrementpaletteversion-Methode erhöht die palettenversion. Ruft diese Methode auf, wenn der Medientyp in ein neues Format geändert wird.
ms.assetid: 1ce77f97-d225-45f5-a259-1dcca1272d15
title: Cdrawimage. incrementpaletteversion-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.IncrementPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21b4220ec98c5b083913e92f5749866f629a4854
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372234"
---
# <a name="cdrawimageincrementpaletteversion-method"></a><span data-ttu-id="acf04-104">Cdrawimage. incrementpaletteversion-Methode</span><span class="sxs-lookup"><span data-stu-id="acf04-104">CDrawImage.IncrementPaletteVersion method</span></span>

<span data-ttu-id="acf04-105">Die- `IncrementPaletteVersion` Methode erhöht die palettenversion.</span><span class="sxs-lookup"><span data-stu-id="acf04-105">The `IncrementPaletteVersion` method increments the palette version.</span></span> <span data-ttu-id="acf04-106">Ruft diese Methode auf, wenn der Medientyp in ein neues Format geändert wird.</span><span class="sxs-lookup"><span data-stu-id="acf04-106">Call this method if the media type changes to a new palettized format.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf04-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="acf04-107">Syntax</span></span>


```C++
void IncrementPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="acf04-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="acf04-108">Parameters</span></span>

<span data-ttu-id="acf04-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="acf04-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="acf04-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="acf04-110">Return value</span></span>

<span data-ttu-id="acf04-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="acf04-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf04-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="acf04-112">Remarks</span></span>

<span data-ttu-id="acf04-113">Diese Methode erhöht den Wert der **m \_ paletteversion** -Member-Variablen.</span><span class="sxs-lookup"><span data-stu-id="acf04-113">This method increments the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="acf04-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="acf04-114">Requirements</span></span>



| <span data-ttu-id="acf04-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="acf04-115">Requirement</span></span> | <span data-ttu-id="acf04-116">Wert</span><span class="sxs-lookup"><span data-stu-id="acf04-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acf04-117">Header</span><span class="sxs-lookup"><span data-stu-id="acf04-117">Header</span></span><br/>  | <dl> <span data-ttu-id="acf04-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acf04-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="acf04-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="acf04-119">Library</span></span><br/> | <dl> <span data-ttu-id="acf04-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="acf04-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acf04-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acf04-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acf04-122">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="acf04-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="acf04-123">**Cdrawimage:: getpaletteversion**</span><span class="sxs-lookup"><span data-stu-id="acf04-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="acf04-124">**Cdrawimage:: resetpaletteversion**</span><span class="sxs-lookup"><span data-stu-id="acf04-124">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




