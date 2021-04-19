---
description: Die onrenderend-Methode wird aufgerufen, nachdem ein Beispiel gerendert wurde.
ms.assetid: c9b3a3b2-a5c0-4a08-9e55-53c27a4d1032
title: Cbaserenderer. onrenderend-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderEnd
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5859cf81a5fd0306f3470ee0fc6d54476e99833d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370838"
---
# <a name="cbaserendereronrenderend-method"></a><span data-ttu-id="e11b6-103">Cbaserenderer. onrenderend-Methode</span><span class="sxs-lookup"><span data-stu-id="e11b6-103">CBaseRenderer.OnRenderEnd method</span></span>

<span data-ttu-id="e11b6-104">Die- `OnRenderEnd` Methode wird aufgerufen, nachdem ein Beispiel gerendert wurde.</span><span class="sxs-lookup"><span data-stu-id="e11b6-104">The `OnRenderEnd` method is called after a sample is rendered.</span></span>

## <a name="syntax"></a><span data-ttu-id="e11b6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e11b6-105">Syntax</span></span>


```C++
virtual void OnRenderEnd(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="e11b6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e11b6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e11b6-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="e11b6-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="e11b6-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="e11b6-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e11b6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e11b6-109">Return value</span></span>

<span data-ttu-id="e11b6-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="e11b6-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e11b6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e11b6-111">Remarks</span></span>

<span data-ttu-id="e11b6-112">Die [**cbaserdenderer:: Rendering**](cbaserenderer-render.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="e11b6-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="e11b6-113">Es wird keine Aktion in der Basisklasse durchführt, aber die abgeleitete Klasse kann Sie überschreiben. beispielsweise, um Qualitäts Steuerungsdaten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="e11b6-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="e11b6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e11b6-114">Requirements</span></span>



| <span data-ttu-id="e11b6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e11b6-115">Requirement</span></span> | <span data-ttu-id="e11b6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="e11b6-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e11b6-117">Header</span><span class="sxs-lookup"><span data-stu-id="e11b6-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e11b6-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e11b6-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e11b6-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="e11b6-119">Library</span></span><br/> | <dl> <span data-ttu-id="e11b6-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="e11b6-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e11b6-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e11b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e11b6-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="e11b6-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




