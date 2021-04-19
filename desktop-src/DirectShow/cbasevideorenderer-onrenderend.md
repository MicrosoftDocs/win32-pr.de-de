---
description: Die onrenderend-Methode führt Glättung für Fälle aus, bei denen die Renderingzeit aufgrund von Unterbrechungen variiert.
ms.assetid: 561b3306-0c41-4f04-b73a-78e7b4038e86
title: Cbasevideorenderer. onrenderend-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f37b4d03f77090f4cac40a218fd3ac27c0c349d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365392"
---
# <a name="cbasevideorendereronrenderend-method"></a><span data-ttu-id="c0517-103">Cbasevideorenderer. onrenderend-Methode</span><span class="sxs-lookup"><span data-stu-id="c0517-103">CBaseVideoRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="c0517-104">Die- `OnRenderEnd` Methode führt Glättung in Fällen aus, in denen die Renderingzeit aufgrund von Unterbrechungen variiert</span><span class="sxs-lookup"><span data-stu-id="c0517-104">The `OnRenderEnd` method performs smoothing for cases where the rendering time varies due to interruptions.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0517-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c0517-105">Syntax</span></span>


```C++
void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="c0517-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c0517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c0517-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="c0517-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c0517-108">Zeiger auf das Medien Beispiel.</span><span class="sxs-lookup"><span data-stu-id="c0517-108">Pointer to the media sample.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c0517-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c0517-109">Return value</span></span>

<span data-ttu-id="c0517-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c0517-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0517-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0517-111">Remarks</span></span>

<span data-ttu-id="c0517-112">Diese Member-Funktion sollte direkt nach dem Zeichnen eines Bilds aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="c0517-112">This member function should be called just after drawing an image.</span></span>

<span data-ttu-id="c0517-113">Diese Member-Funktion überschreibt [**cbaserenderer:: onrenderend**](cbaserenderer-onrenderend.md).</span><span class="sxs-lookup"><span data-stu-id="c0517-113">This member function overrides [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0517-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c0517-114">Requirements</span></span>



| <span data-ttu-id="c0517-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c0517-115">Requirement</span></span> | <span data-ttu-id="c0517-116">Wert</span><span class="sxs-lookup"><span data-stu-id="c0517-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0517-117">Header</span><span class="sxs-lookup"><span data-stu-id="c0517-117">Header</span></span><br/>  | <dl> <span data-ttu-id="c0517-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c0517-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c0517-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="c0517-119">Library</span></span><br/> | <dl> <span data-ttu-id="c0517-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="c0517-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0517-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0517-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0517-122">**Cbasevideorenderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="c0517-122">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




