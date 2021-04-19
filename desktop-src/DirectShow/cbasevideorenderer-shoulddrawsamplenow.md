---
description: Die Methode "schulddrawsamplenow" bestimmt, ob das Video gezeichnet werden soll, ohne einen Zeit Geber-anweichung-Link mit der Uhr festzulegen
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Cbasevideorenderer. schulddrawsamplenow-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367578"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a><span data-ttu-id="d880b-103">Cbasevideorenderer. schulddrawsamplenow-Methode</span><span class="sxs-lookup"><span data-stu-id="d880b-103">CBaseVideoRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="d880b-104">Die- `ShouldDrawSampleNow` Methode bestimmt, ob das Video gezeichnet werden soll, ohne eine Zeit Geber Empfehlung mit der Uhr festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d880b-104">The `ShouldDrawSampleNow` method determines if the video should be drawn without setting a timer advise link with the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="d880b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d880b-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a><span data-ttu-id="d880b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d880b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d880b-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="d880b-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="d880b-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle für das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="d880b-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface for the sample.</span></span>

</dd> <dt>

<span data-ttu-id="d880b-109">*ptrstart*</span><span class="sxs-lookup"><span data-stu-id="d880b-109">*ptrStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d880b-110">Zeiger auf den Zeitpunkt, zu dem das Rendering begonnen wird.</span><span class="sxs-lookup"><span data-stu-id="d880b-110">Pointer to the time to begin rendering.</span></span>

</dd> <dt>

<span data-ttu-id="d880b-111">*ptrend*</span><span class="sxs-lookup"><span data-stu-id="d880b-111">*ptrEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="d880b-112">Zeiger auf die Zeit zum Abbrechen des Renderings.</span><span class="sxs-lookup"><span data-stu-id="d880b-112">Pointer to the time to stop rendering.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d880b-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d880b-113">Return value</span></span>

<span data-ttu-id="d880b-114">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="d880b-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d880b-115">Gibt den Wert "s OK" zurück, \_ um gleichzeitig zu zeichnen, ohne zu warten, "s false", um zum \_ Zeitpunkt " *ptrstart*" zu zeichnen, oder ein Fehler, der bedeutet, dass das Beispiel nicht gezeichnet wird</span><span class="sxs-lookup"><span data-stu-id="d880b-115">Returns S\_OK to mean draw at once without waiting, S\_FALSE to mean draw at time *ptrStart*, or an error to mean do not draw the sample; that is, skip it to save time.</span></span>

## <a name="remarks"></a><span data-ttu-id="d880b-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d880b-116">Remarks</span></span>

<span data-ttu-id="d880b-117">Diese Member-Funktion überschreibt [**cbaserenderer:: schulddrawsamplenow**](cbaserenderer-shoulddrawsamplenow.md).</span><span class="sxs-lookup"><span data-stu-id="d880b-117">This member function overrides [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="d880b-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d880b-118">Requirements</span></span>



| <span data-ttu-id="d880b-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d880b-119">Requirement</span></span> | <span data-ttu-id="d880b-120">Wert</span><span class="sxs-lookup"><span data-stu-id="d880b-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d880b-121">Header</span><span class="sxs-lookup"><span data-stu-id="d880b-121">Header</span></span><br/>  | <dl> <span data-ttu-id="d880b-122"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d880b-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d880b-123">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="d880b-123">Library</span></span><br/> | <dl> <span data-ttu-id="d880b-124">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="d880b-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d880b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d880b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d880b-126">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d880b-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




