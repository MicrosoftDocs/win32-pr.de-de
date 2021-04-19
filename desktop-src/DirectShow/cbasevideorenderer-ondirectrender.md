---
description: Die ondirectrender-Methode sammelt Zeit Steuerungsinformationen, die die Synchronisierung und die Qualitätskontrolle steuern.
ms.assetid: ed617fac-b2c6-4a3a-ac91-77e2d7cce981
title: Cbasevideorenderer. ondirectrender-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnDirectRender
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7c117366590c96b63ff4595d4563e92aec542cfb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359298"
---
# <a name="cbasevideorendererondirectrender-method"></a><span data-ttu-id="8573d-103">Cbasevideorenderer. ondirectrender-Methode</span><span class="sxs-lookup"><span data-stu-id="8573d-103">CBaseVideoRenderer.OnDirectRender method</span></span>

<span data-ttu-id="8573d-104">Die **ondirectrender** -Methode sammelt Zeit Steuerungsinformationen, die die Synchronisierung und die Qualitätskontrolle steuern.</span><span class="sxs-lookup"><span data-stu-id="8573d-104">The **OnDirectRender** method collects timing information that controls synchronization and quality control.</span></span>

## <a name="syntax"></a><span data-ttu-id="8573d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="8573d-105">Syntax</span></span>


```C++
virtual HRESULT OnDirectRender(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="8573d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8573d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8573d-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="8573d-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="8573d-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Mediums Sample.</span><span class="sxs-lookup"><span data-stu-id="8573d-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8573d-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8573d-109">Return value</span></span>

<span data-ttu-id="8573d-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="8573d-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8573d-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8573d-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8573d-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8573d-112">Remarks</span></span>

<span data-ttu-id="8573d-113">Diese Methode anstelle von " [**onrenderstart**](cbasevideorenderer-onrenderstart.md) " und " [**onrenderend**](cbasevideorenderer-onrenderend.md)" aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="8573d-113">Call this method instead of [**OnRenderStart**](cbasevideorenderer-onrenderstart.md) and [**OnRenderEnd**](cbasevideorenderer-onrenderend.md).</span></span> <span data-ttu-id="8573d-114">Diese Methode wird vom DirectDraw-Videorenderer verwendet.</span><span class="sxs-lookup"><span data-stu-id="8573d-114">This method is used by the DirectDraw video renderer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8573d-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8573d-115">Requirements</span></span>



| <span data-ttu-id="8573d-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8573d-116">Requirement</span></span> | <span data-ttu-id="8573d-117">Wert</span><span class="sxs-lookup"><span data-stu-id="8573d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8573d-118">Header</span><span class="sxs-lookup"><span data-stu-id="8573d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8573d-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8573d-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="8573d-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="8573d-120">Library</span></span><br/> | <dl> <span data-ttu-id="8573d-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="8573d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8573d-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8573d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8573d-123">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="8573d-123">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




