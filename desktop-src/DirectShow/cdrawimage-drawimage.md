---
description: Mit der DrawImage-Methode wird ein Videorahmen im Videofenster gezeichnet.
ms.assetid: 22e7f59c-90f7-4e0c-8993-eea1eaf58fba
title: Cdrawimage. DrawImage-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.DrawImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d219eb82ab2cf1929605eee4045c2f278022ad98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357645"
---
# <a name="cdrawimagedrawimage-method"></a><span data-ttu-id="8eb77-103">Cdrawimage. DrawImage-Methode</span><span class="sxs-lookup"><span data-stu-id="8eb77-103">CDrawImage.DrawImage method</span></span>

<span data-ttu-id="8eb77-104">Die- `DrawImage` Methode zeichnet einen Videoframe im Videofenster.</span><span class="sxs-lookup"><span data-stu-id="8eb77-104">The `DrawImage` method draws a video frame on the video window.</span></span>

## <a name="syntax"></a><span data-ttu-id="8eb77-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eb77-105">Syntax</span></span>


```C++
BOOL DrawImage(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="8eb77-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8eb77-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8eb77-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="8eb77-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8eb77-108">Ein Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels, das das Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="8eb77-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8eb77-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8eb77-109">Return value</span></span>

<span data-ttu-id="8eb77-110">Gibt **true** zurück, wenn erfolgreich, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="8eb77-110">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8eb77-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8eb77-111">Remarks</span></span>

<span data-ttu-id="8eb77-112">Diese Methode delegiert an [**cdrawimage:: fastrinender**](cdrawimage-fastrender.md) oder [**cdrawimage:: slowrendering**](cdrawimage-slowrender.md), je nachdem, ob der Filter die Zuweisung besitzt, die das Beispiel bereitgestellt hat.</span><span class="sxs-lookup"><span data-stu-id="8eb77-112">This method delegates to [**CDrawImage::FastRender**](cdrawimage-fastrender.md) or [**CDrawImage::SlowRender**](cdrawimage-slowrender.md), depending on whether the filter owns the allocator that provided the sample.</span></span> <span data-ttu-id="8eb77-113">Wenn der Filter die Zuweisung besitzt, ist das Beispiel garantiert ein [**cimagesample**](cimagesample.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="8eb77-113">If the filter does own the allocator, the sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="8eb77-114">In diesem Fall verwendet das Beispiel den gemeinsam genutzten Speicher, der von GDI zugeordnet wird, und das Image kann entweder mithilfe von **BitBLT** oder **StretchBlt** gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8eb77-114">In that case, the sample uses shared memory allocated by GDI, and the image can be drawn using either **BitBlt** or **StretchBlt**.</span></span> <span data-ttu-id="8eb77-115">Andernfalls müssen die Bilder mithilfe der langsameren Funktionen **SetDIBitsToDevice** oder **StretchDIBits** gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="8eb77-115">Otherwise, the images must be drawn using the slower **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

<span data-ttu-id="8eb77-116">In Debugbuilds ruft diese Methode **displaysampletimes** auf, um die Zeitstempel des Beispiels über das Video Bild zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="8eb77-116">In debug builds, this method calls **DisplaySampleTimes** to draw the sample's time stamps over the video image.</span></span>

## <a name="requirements"></a><span data-ttu-id="8eb77-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8eb77-117">Requirements</span></span>



| <span data-ttu-id="8eb77-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8eb77-118">Requirement</span></span> | <span data-ttu-id="8eb77-119">Wert</span><span class="sxs-lookup"><span data-stu-id="8eb77-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8eb77-120">Header</span><span class="sxs-lookup"><span data-stu-id="8eb77-120">Header</span></span><br/>  | <dl> <span data-ttu-id="8eb77-121"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8eb77-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8eb77-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8eb77-122">Library</span></span><br/> | <dl> <span data-ttu-id="8eb77-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8eb77-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8eb77-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8eb77-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8eb77-125">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8eb77-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="8eb77-126">**Cdrawimage:: usingimagezuordcator**</span><span class="sxs-lookup"><span data-stu-id="8eb77-126">**CDrawImage::UsingImageAllocator**</span></span>](cdrawimage-usingimageallocator.md)
</dt> </dl>

 

 




