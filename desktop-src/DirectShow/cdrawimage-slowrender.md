---
description: Mit der slowrendering-Methode wird das Video Bild mithilfe der Funktionen SetDIBitsToDevice oder StretchDIBits gezeichnet.
ms.assetid: e1d8b189-b588-48eb-988a-3e5dedb38dbd
title: Cdrawimage. slowrendering-Methode (winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SlowRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b736bf6c44d4ada6e0a28408c449c9f8b2f1e1cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358363"
---
# <a name="cdrawimageslowrender-method"></a><span data-ttu-id="12e96-103">Cdrawimage. slowrendering-Methode</span><span class="sxs-lookup"><span data-stu-id="12e96-103">CDrawImage.SlowRender method</span></span>

<span data-ttu-id="12e96-104">Mit der- `SlowRender` Methode wird das Video Bild mithilfe der Funktionen **SetDIBitsToDevice** oder **StretchDIBits** gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="12e96-104">The `SlowRender` method draws the video image using the **SetDIBitsToDevice** or **StretchDIBits** functions.</span></span>

## <a name="syntax"></a><span data-ttu-id="12e96-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="12e96-105">Syntax</span></span>


```C++
void SlowRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="12e96-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="12e96-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="12e96-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="12e96-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="12e96-108">Ein Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels, das das Bild enthält.</span><span class="sxs-lookup"><span data-stu-id="12e96-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the sample that contains the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="12e96-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="12e96-109">Return value</span></span>

<span data-ttu-id="12e96-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="12e96-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="12e96-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="12e96-111">Remarks</span></span>

<span data-ttu-id="12e96-112">Wenn [**cdrawimage:: usingimagezuordcator**](cdrawimage-usingimageallocator.md) **false** zurückgibt, verwendet die [**cdrawimage::D rawImage**](cdrawimage-drawimage.md) -Methode `SlowRender` zum Zeichnen des Video Bilds.</span><span class="sxs-lookup"><span data-stu-id="12e96-112">If [**CDrawImage::UsingImageAllocator**](cdrawimage-usingimageallocator.md) returns **FALSE**, the [**CDrawImage::DrawImage**](cdrawimage-drawimage.md) method uses `SlowRender` to draw the video image.</span></span> <span data-ttu-id="12e96-113">Andernfalls verwendet DrawImage die **fastrinender** -Methode.</span><span class="sxs-lookup"><span data-stu-id="12e96-113">Otherwise, DrawImage uses the **FastRender** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="12e96-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="12e96-114">Requirements</span></span>



| <span data-ttu-id="12e96-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="12e96-115">Requirement</span></span> | <span data-ttu-id="12e96-116">Wert</span><span class="sxs-lookup"><span data-stu-id="12e96-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12e96-117">Header</span><span class="sxs-lookup"><span data-stu-id="12e96-117">Header</span></span><br/>  | <dl> <span data-ttu-id="12e96-118"><dt>Winutil. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="12e96-118"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="12e96-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="12e96-119">Library</span></span><br/> | <dl> <span data-ttu-id="12e96-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="12e96-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12e96-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="12e96-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12e96-122">**Cdrawimage-Klasse**</span><span class="sxs-lookup"><span data-stu-id="12e96-122">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> <dt>

[<span data-ttu-id="12e96-123">**Cdrawimage:: fastrauender**</span><span class="sxs-lookup"><span data-stu-id="12e96-123">**CDrawImage::FastRender**</span></span>](cdrawimage-fastrender.md)
</dt> </dl>

 

 




