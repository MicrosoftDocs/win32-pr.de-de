---
description: Die fastrauender-Methode zeichnet das Video Bild mithilfe der Funktionen BitBLT oder StretchBlt.
ms.assetid: 8bbc96ce-393f-46fb-bf90-61d3ce0ef0d6
title: Cdrawimage. fastrauender-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.FastRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 823583beed6696d40803ccc098410dac053b8948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106373730"
---
# <a name="cdrawimagefastrender-method"></a><span data-ttu-id="e2fad-103">Cdrawimage. fastrauender-Methode</span><span class="sxs-lookup"><span data-stu-id="e2fad-103">CDrawImage.FastRender method</span></span>

<span data-ttu-id="e2fad-104">Die- `FastRender` Methode zeichnet das Video Bild mithilfe der Funktionen **BitBLT** oder **StretchBlt** .</span><span class="sxs-lookup"><span data-stu-id="e2fad-104">The `FastRender` method draws the video image using the **BitBlt** or **StretchBlt** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fad-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2fad-105">Syntax</span></span>


```C++
void FastRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="e2fad-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e2fad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fad-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="e2fad-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fad-108">Ein Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels, das das Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="e2fad-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fad-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e2fad-109">Return value</span></span>

<span data-ttu-id="e2fad-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e2fad-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2fad-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2fad-111">Remarks</span></span>

<span data-ttu-id="e2fad-112">Die [**cdrawimage::D rawImage**](cdrawimage-drawimage.md) -Methode ruft diese Methode auf, aber nur, wenn die Zuweisung für die Verbindung ein [**cimagezuordcator**](cimageallocator.md) -Objekt ist.</span><span class="sxs-lookup"><span data-stu-id="e2fad-112">The [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method calls this method, but only if the allocator for the connection is a [**CImageAllocator**](cimageallocator.md) object.</span></span> <span data-ttu-id="e2fad-113">In diesem Fall ist das Medien Beispiel garantiert ein [**cimagesample**](cimagesample.md) -Objekt.</span><span class="sxs-lookup"><span data-stu-id="e2fad-113">In that case, the media sample is guaranteed to be a [**CImageSample**](cimagesample.md) object.</span></span> <span data-ttu-id="e2fad-114">Das **cimagesample** -Objekt verwendet die Funktion " **kreatedibsection** ", um den gemeinsamen Speicher für die Bitmap zuzuordnen, sodass das Bild entweder mithilfe von **BitBLT** oder **StretchBlt** gezeichnet werden kann.</span><span class="sxs-lookup"><span data-stu-id="e2fad-114">The **CImageSample** object uses the **CreateDIBSection** function to allocate shared memory for the bitmap, which makes it possible to draw the image using either **BitBlt** or **StretchBlt**.</span></span>

<span data-ttu-id="e2fad-115">Diese Methode ruft **BitBLT** auf, wenn die Quell-und ungültige Ziel-Rechtecke genau übereinstimmen oder andernfalls **StretchBlt** .</span><span class="sxs-lookup"><span data-stu-id="e2fad-115">This method calls **BitBlt** if the source and targer rectangles exactly match, or **StretchBlt** otherwise.</span></span>

<span data-ttu-id="e2fad-116">Wenn der Filter nicht Besitzer der Zuweisung ist, verwendet die **DrawImage** -Methode [**cdrawimage:: slowrendering**](cdrawimage-slowrender.md) zum Zeichnen des Bilds.</span><span class="sxs-lookup"><span data-stu-id="e2fad-116">If the filter does not own the allocator, the **DrawImage** method uses [**CDrawImage::SlowRender**](cdrawimage-slowrender.md) to draw the image.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fad-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e2fad-117">Requirements</span></span>



| <span data-ttu-id="e2fad-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e2fad-118">Requirement</span></span> | <span data-ttu-id="e2fad-119">Wert</span><span class="sxs-lookup"><span data-stu-id="e2fad-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fad-120">Header</span><span class="sxs-lookup"><span data-stu-id="e2fad-120">Header</span></span><br/>  | <dl> <span data-ttu-id="e2fad-121"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2fad-121"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e2fad-122">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e2fad-122">Library</span></span><br/> | <dl> <span data-ttu-id="e2fad-123">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e2fad-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2fad-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2fad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fad-125">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e2fad-125">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




