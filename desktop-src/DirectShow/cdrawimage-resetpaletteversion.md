---
description: Die resetpaletteversion-Methode setzt die palettenversion zurück. Ruft diese Methode auf, wenn die PIN des besitzenden Filters erneut eine Verbindung herstellt.
ms.assetid: c9e5588c-5501-4356-bdec-a339d33f9eb5
title: Cdrawimage. resetpaletteversion-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.ResetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a94cd04de428a29308ead8fa33ccfe1792e021a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358028"
---
# <a name="cdrawimageresetpaletteversion-method"></a><span data-ttu-id="ce3fa-104">Cdrawimage. resetpaletteversion-Methode</span><span class="sxs-lookup"><span data-stu-id="ce3fa-104">CDrawImage.ResetPaletteVersion method</span></span>

<span data-ttu-id="ce3fa-105">Die- `ResetPaletteVersion` Methode setzt die palettenversion zurück.</span><span class="sxs-lookup"><span data-stu-id="ce3fa-105">The `ResetPaletteVersion` method resets the palette version.</span></span> <span data-ttu-id="ce3fa-106">Ruft diese Methode auf, wenn die PIN des besitzenden Filters erneut eine Verbindung herstellt.</span><span class="sxs-lookup"><span data-stu-id="ce3fa-106">Call this method if the owning filter's pin reconnects.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3fa-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce3fa-107">Syntax</span></span>


```C++
void ResetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="ce3fa-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce3fa-108">Parameters</span></span>

<span data-ttu-id="ce3fa-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ce3fa-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ce3fa-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ce3fa-110">Return value</span></span>

<span data-ttu-id="ce3fa-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ce3fa-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ce3fa-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce3fa-112">Remarks</span></span>

<span data-ttu-id="ce3fa-113">Diese Methode legt den Wert von **m \_ paletteversion** auf eine vordefinierte Konstante **, \_ palettenversion**, fest.</span><span class="sxs-lookup"><span data-stu-id="ce3fa-113">This method sets the value of **m\_PaletteVersion** to a predefined constant, **PALETTE\_VERSION**.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3fa-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ce3fa-114">Requirements</span></span>



| <span data-ttu-id="ce3fa-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ce3fa-115">Requirement</span></span> | <span data-ttu-id="ce3fa-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ce3fa-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3fa-117">Header</span><span class="sxs-lookup"><span data-stu-id="ce3fa-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ce3fa-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce3fa-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ce3fa-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ce3fa-119">Library</span></span><br/> | <dl> <span data-ttu-id="ce3fa-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ce3fa-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce3fa-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce3fa-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce3fa-122">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ce3fa-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="ce3fa-123">**Cdrawimage:: getpaletteversion**</span><span class="sxs-lookup"><span data-stu-id="ce3fa-123">**CDrawImage::GetPaletteVersion**</span></span>](cdrawimage-getpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="ce3fa-124">**Cdrawimage:: incrementpaletteversion**</span><span class="sxs-lookup"><span data-stu-id="ce3fa-124">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> </dl>

 

 




