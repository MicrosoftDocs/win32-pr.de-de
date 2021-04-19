---
description: Die drawvideoimagehere-Methode zeichnet ein Bild aus einem Medien Beispiel in einen angegebenen Gerätekontext.
ms.assetid: b11e1c6b-5a29-444f-a0a9-049cd9d49b13
title: Cdrawimage. drawvideoimagehere-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawVideoImageHere
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 599dd82e282f2d14ac7e974363a62695e209c080
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352950"
---
# <a name="cdrawimagedrawvideoimagehere-method"></a><span data-ttu-id="fb392-103">Cdrawimage. drawvideoimagehere-Methode</span><span class="sxs-lookup"><span data-stu-id="fb392-103">CDrawImage.DrawVideoImageHere method</span></span>

<span data-ttu-id="fb392-104">Die- `DrawVideoImageHere` Methode zeichnet ein Bild aus einem Medien Beispiel in einen angegebenen Gerätekontext.</span><span class="sxs-lookup"><span data-stu-id="fb392-104">The `DrawVideoImageHere` method draws an image from a media sample to a specified device context.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb392-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb392-105">Syntax</span></span>


```C++
BOOL DrawVideoImageHere(
   HDC          hdc,
   IMediaSample *pMediaSample,
   RECT         *lprcSrc,
   RECT         *lprcDst
);
```



## <a name="parameters"></a><span data-ttu-id="fb392-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb392-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb392-107">*HDC*</span><span class="sxs-lookup"><span data-stu-id="fb392-107">*hdc*</span></span> 
</dt> <dd>

<span data-ttu-id="fb392-108">Handle für einen Gerätekontext, in dem die Zeichnung stattfindet.</span><span class="sxs-lookup"><span data-stu-id="fb392-108">Handle to a device context, where the drawing will occur.</span></span>

</dd> <dt>

<span data-ttu-id="fb392-109">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="fb392-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="fb392-110">Ein Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels, das das Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="fb392-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> <dt>

<span data-ttu-id="fb392-111">*lprcsrc*</span><span class="sxs-lookup"><span data-stu-id="fb392-111">*lprcSrc*</span></span> 
</dt> <dd>

<span data-ttu-id="fb392-112">Zeiger auf ein Quell Rechteck, das zum Zeichnen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb392-112">Pointer to a source rectangle to use for drawing.</span></span> <span data-ttu-id="fb392-113">Wenn der Wert **null** ist, wird das Rechteck in [**cdrawimage:: m \_ SourceRect**](cdrawimage-m-sourcerect.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb392-113">If **NULL**, the rectangle in [**CDrawImage::m\_SourceRect**](cdrawimage-m-sourcerect.md) is used.</span></span>

</dd> <dt>

<span data-ttu-id="fb392-114">*lprcdst*</span><span class="sxs-lookup"><span data-stu-id="fb392-114">*lprcDst*</span></span> 
</dt> <dd>

<span data-ttu-id="fb392-115">Zeiger auf ein Ziel Rechteck, das zum Zeichnen verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="fb392-115">Pointer to a target rectangle to use for drawing.</span></span> <span data-ttu-id="fb392-116">Wenn der Wert **null** ist, wird das Rechteck in [**cdrawimage:: m \_ targetrect**](cdrawimage-m-targetrect.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="fb392-116">If **NULL**, the rectangle in [**CDrawImage::m\_TargetRect**](cdrawimage-m-targetrect.md) is used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb392-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fb392-117">Return value</span></span>

<span data-ttu-id="fb392-118">Gibt **true** zurück, wenn erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="fb392-118">Returns **TRUE** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb392-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fb392-119">Requirements</span></span>



| <span data-ttu-id="fb392-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fb392-120">Requirement</span></span> | <span data-ttu-id="fb392-121">Wert</span><span class="sxs-lookup"><span data-stu-id="fb392-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb392-122">Header</span><span class="sxs-lookup"><span data-stu-id="fb392-122">Header</span></span><br/>  | <dl> <span data-ttu-id="fb392-123"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fb392-123"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="fb392-124">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="fb392-124">Library</span></span><br/> | <dl> <span data-ttu-id="fb392-125">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="fb392-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fb392-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb392-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb392-127">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="fb392-127">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




