---
description: 'Die Receive-Methode empfängt das nächste Medien Beispiel im Stream. Diese Methode überschreibt die cbasinput PIN:: Receive-Methode.'
ms.assetid: b09140f0-2e3a-47b1-ace7-954043dd62eb
title: Crendererinputpin. Receive-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d3ddac3f456e1ab24574a4743983d20a828896e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354816"
---
# <a name="crendererinputpinreceive-method"></a><span data-ttu-id="78477-104">Crendererinputpin. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="78477-104">CRendererInputPin.Receive method</span></span>

<span data-ttu-id="78477-105">Die- `Receive` Methode empfängt das nächste Medien Beispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="78477-105">The `Receive` method receives the next media sample in the stream.</span></span> <span data-ttu-id="78477-106">Diese Methode überschreibt die [**cbasinput PIN:: Receive**](cbaseinputpin-receive.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="78477-106">This method overrides the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="78477-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="78477-107">Syntax</span></span>


```C++
HRESULT Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="78477-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="78477-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78477-109">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="78477-109">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="78477-110">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="78477-110">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78477-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78477-111">Return value</span></span>

<span data-ttu-id="78477-112">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="78477-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="78477-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78477-113">Remarks</span></span>

<span data-ttu-id="78477-114">Diese Methode ruft die [**cbaserenderer:: Receive**](cbaserenderer-receive.md) -Methode des Filters auf, die das Rendering behandelt.</span><span class="sxs-lookup"><span data-stu-id="78477-114">This method calls the filter's [**CBaseRenderer::Receive**](cbaserenderer-receive.md) method, which handles the rendering.</span></span> <span data-ttu-id="78477-115">Wenn diese Methode fehlschlägt, sendet die PIN ein EC \_ errorabort-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="78477-115">If that method fails, the pin sends an EC\_ERRORABORT event.</span></span>

## <a name="requirements"></a><span data-ttu-id="78477-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="78477-116">Requirements</span></span>



| <span data-ttu-id="78477-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="78477-117">Requirement</span></span> | <span data-ttu-id="78477-118">Wert</span><span class="sxs-lookup"><span data-stu-id="78477-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78477-119">Header</span><span class="sxs-lookup"><span data-stu-id="78477-119">Header</span></span><br/>  | <dl> <span data-ttu-id="78477-120"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="78477-120"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="78477-121">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="78477-121">Library</span></span><br/> | <dl> <span data-ttu-id="78477-122">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="78477-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="78477-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78477-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78477-124">**Crendererinputpin-Klasse**</span><span class="sxs-lookup"><span data-stu-id="78477-124">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




