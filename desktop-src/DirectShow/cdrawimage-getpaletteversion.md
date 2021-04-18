---
description: Die getpaletteversion-Methode ruft die aktuelle palettenversion ab.
ms.assetid: 9f97a810-04a4-4ea3-8918-416e9cd8e5e4
title: Cdrawimage. getpaletteversion-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.GetPaletteVersion
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c86f1a0dad8d33913a52962dfe2ec09b7b8244db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371527"
---
# <a name="cdrawimagegetpaletteversion-method"></a><span data-ttu-id="47a72-103">Cdrawimage. getpaletteversion-Methode</span><span class="sxs-lookup"><span data-stu-id="47a72-103">CDrawImage.GetPaletteVersion method</span></span>

<span data-ttu-id="47a72-104">Die- `GetPaletteVersion` Methode ruft die aktuelle palettenversion ab.</span><span class="sxs-lookup"><span data-stu-id="47a72-104">The `GetPaletteVersion` method retrieves the current palette version.</span></span>

## <a name="syntax"></a><span data-ttu-id="47a72-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="47a72-105">Syntax</span></span>


```C++
LONG GetPaletteVersion();
```



## <a name="parameters"></a><span data-ttu-id="47a72-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="47a72-106">Parameters</span></span>

<span data-ttu-id="47a72-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="47a72-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="47a72-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="47a72-108">Return value</span></span>

<span data-ttu-id="47a72-109">Gibt den Wert der **m \_ paletteversion** -Member-Variable zurück.</span><span class="sxs-lookup"><span data-stu-id="47a72-109">Returns the value of the **m\_PaletteVersion** member variable.</span></span>

## <a name="remarks"></a><span data-ttu-id="47a72-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="47a72-110">Remarks</span></span>

<span data-ttu-id="47a72-111">Der von dieser Methode zurückgegebene Wert gilt nur, wenn die Zuweisung ein [**cimagezuordcator**](cimageallocator.md) -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="47a72-111">The value returned by this method applies only when the allocator is a [**CImageAllocator**](cimageallocator.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a72-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="47a72-112">Requirements</span></span>



| <span data-ttu-id="47a72-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="47a72-113">Requirement</span></span> | <span data-ttu-id="47a72-114">Wert</span><span class="sxs-lookup"><span data-stu-id="47a72-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47a72-115">Header</span><span class="sxs-lookup"><span data-stu-id="47a72-115">Header</span></span><br/>  | <dl> <span data-ttu-id="47a72-116"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="47a72-116"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="47a72-117">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="47a72-117">Library</span></span><br/> | <dl> <span data-ttu-id="47a72-118">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="47a72-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a72-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="47a72-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a72-120">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="47a72-120">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="47a72-121">**Cdrawimage:: incrementpaletteversion**</span><span class="sxs-lookup"><span data-stu-id="47a72-121">**CDrawImage::IncrementPaletteVersion**</span></span>](cdrawimage-incrementpaletteversion.md)
</dt> <dt>

[<span data-ttu-id="47a72-122">**Cdrawimage:: resetpaletteversion**</span><span class="sxs-lookup"><span data-stu-id="47a72-122">**CDrawImage::ResetPaletteVersion**</span></span>](cdrawimage-resetpaletteversion.md)
</dt> </dl>

 

 




