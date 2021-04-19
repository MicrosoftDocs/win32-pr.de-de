---
description: Die dorendersample-Methode rendert ein Beispiel.
ms.assetid: cf06192c-44c0-4d88-a20e-6501ea48cbfd
title: Cbaserderderer. dorendersample-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.DoRenderSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 935fd7b92cef5d51056b2eb2daa9d2fb775647b6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360884"
---
# <a name="cbaserendererdorendersample-method"></a><span data-ttu-id="e53e3-103">Cbaserderderer. dorendersample-Methode</span><span class="sxs-lookup"><span data-stu-id="e53e3-103">CBaseRenderer.DoRenderSample method</span></span>

<span data-ttu-id="e53e3-104">Die- `DoRenderSample` Methode rendert ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="e53e3-104">The `DoRenderSample` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="e53e3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e53e3-105">Syntax</span></span>


```C++
virtual HRESULT DoRenderSample(
   IMediaSample *pMediaSample
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="e53e3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e53e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e53e3-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="e53e3-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e53e3-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="e53e3-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e53e3-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e53e3-109">Return value</span></span>

<span data-ttu-id="e53e3-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e53e3-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e53e3-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e53e3-111">Remarks</span></span>

<span data-ttu-id="e53e3-112">Diese Methode muss von der abgeleiteten Klasse implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="e53e3-112">The derived class must implement this method.</span></span> <span data-ttu-id="e53e3-113">Das Verhalten hängt vollständig von dem implementierten Filtertyp ab.</span><span class="sxs-lookup"><span data-stu-id="e53e3-113">The behavior depends entirely on the type of filter being implemented.</span></span> <span data-ttu-id="e53e3-114">Ein Videorenderer beispielsweise würde das Video Bild zeichnen, das im Beispiel enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="e53e3-114">A video renderer, for example, would draw the video image contained in the sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="e53e3-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e53e3-115">Requirements</span></span>



| <span data-ttu-id="e53e3-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e53e3-116">Requirement</span></span> | <span data-ttu-id="e53e3-117">Wert</span><span class="sxs-lookup"><span data-stu-id="e53e3-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e53e3-118">Header</span><span class="sxs-lookup"><span data-stu-id="e53e3-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e53e3-119"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e53e3-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e53e3-120">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e53e3-120">Library</span></span><br/> | <dl> <span data-ttu-id="e53e3-121">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e53e3-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e53e3-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e53e3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e53e3-123">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e53e3-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




