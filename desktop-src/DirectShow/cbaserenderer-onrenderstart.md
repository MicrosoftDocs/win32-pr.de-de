---
description: Die onrenderstart-Methode wird aufgerufen, wenn das Rendering gerade gestartet wird.
ms.assetid: 46af24cf-9075-4ebc-a49b-85f8f0c3da6f
title: Cbaserderderer. onrenderstart-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnRenderStart
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a7838b0ba43c1e570b745541882a2f2f815dd948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367015"
---
# <a name="cbaserendereronrenderstart-method"></a><span data-ttu-id="7370e-103">Cbaserderderer. onrenderstart-Methode</span><span class="sxs-lookup"><span data-stu-id="7370e-103">CBaseRenderer.OnRenderStart method</span></span>

<span data-ttu-id="7370e-104">Die- `OnRenderStart` Methode wird aufgerufen, wenn das Rendering gerade gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7370e-104">The `OnRenderStart` method is called when rendering is about to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="7370e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7370e-105">Syntax</span></span>


```C++
virtual void OnRenderStart(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="7370e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7370e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7370e-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="7370e-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="7370e-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="7370e-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7370e-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7370e-109">Return value</span></span>

<span data-ttu-id="7370e-110">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7370e-110">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7370e-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7370e-111">Remarks</span></span>

<span data-ttu-id="7370e-112">Die [**cbaserdenderer:: Rendering**](cbaserenderer-render.md) -Methode ruft diese Methode auf.</span><span class="sxs-lookup"><span data-stu-id="7370e-112">The [**CBaseRenderer::Render**](cbaserenderer-render.md) method calls this method.</span></span> <span data-ttu-id="7370e-113">Es wird keine Aktion in der Basisklasse durchführt, aber die abgeleitete Klasse kann Sie überschreiben. beispielsweise, um Qualitäts Steuerungsdaten zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="7370e-113">It does nothing in the base class, but the derived class can override it; for example, to collect quality-control data.</span></span>

## <a name="requirements"></a><span data-ttu-id="7370e-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7370e-114">Requirements</span></span>



| <span data-ttu-id="7370e-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7370e-115">Requirement</span></span> | <span data-ttu-id="7370e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="7370e-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7370e-117">Header</span><span class="sxs-lookup"><span data-stu-id="7370e-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7370e-118"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7370e-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7370e-119">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="7370e-119">Library</span></span><br/> | <dl> <span data-ttu-id="7370e-120">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="7370e-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7370e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7370e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7370e-122">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="7370e-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




