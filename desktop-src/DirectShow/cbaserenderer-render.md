---
description: Die Rendermethode rendert ein Beispiel.
ms.assetid: 82b47777-2900-4821-ab79-1856da432832
title: Cbaserderderer. Rendering-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Render
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9fefd44fe1b913fbba0e3ebfaa6f750b88d40813
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371555"
---
# <a name="cbaserendererrender-method"></a><span data-ttu-id="ca5f0-103">Cbaserderderer. Rendering-Methode</span><span class="sxs-lookup"><span data-stu-id="ca5f0-103">CBaseRenderer.Render method</span></span>

<span data-ttu-id="ca5f0-104">Die- `Render` Methode rendert ein Beispiel.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-104">The `Render` method renders a sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca5f0-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca5f0-105">Syntax</span></span>


```C++
virtual Render(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="ca5f0-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca5f0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca5f0-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="ca5f0-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="ca5f0-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca5f0-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca5f0-109">Return value</span></span>

<span data-ttu-id="ca5f0-110">Gibt einen **HRESULT** -Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-110">Returns an **HRESULT** value.</span></span> <span data-ttu-id="ca5f0-111">Mögliche Werte sind die in der folgenden Tabelle aufgeführten Werte.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-111">Possible values include those in the following table.</span></span>



| <span data-ttu-id="ca5f0-112">Rückgabecode</span><span class="sxs-lookup"><span data-stu-id="ca5f0-112">Return code</span></span>                                                                             | <span data-ttu-id="ca5f0-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ca5f0-113">Description</span></span>                                                      |
|-----------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca5f0-114"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="ca5f0-114"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="ca5f0-115">Der Filter wurde beendet, oder *pmediasample* ist **null**.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-115">The filter is stopped, or *pMediaSample* is **NULL**.</span></span><br/> |
| <dl> <span data-ttu-id="ca5f0-116"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="ca5f0-116"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="ca5f0-117">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-117">Success.</span></span><br/>                                              |



 

## <a name="remarks"></a><span data-ttu-id="ca5f0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca5f0-118">Remarks</span></span>

<span data-ttu-id="ca5f0-119">Diese Methode ruft die reine virtuelle Methode [**cbasererderderer::D orendersample**](cbaserenderer-dorendersample.md)auf, die die eigentliche Arbeit übernimmt.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-119">This method calls the pure virtual method [**CBaseRenderer::DoRenderSample**](cbaserenderer-dorendersample.md), which does the real work.</span></span> <span data-ttu-id="ca5f0-120">Die abgeleitete Klasse muss " **dorendersample**" implementieren.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-120">The derived class must implement **DoRenderSample**.</span></span>

<span data-ttu-id="ca5f0-121">Direkt vor dem Aufruf von " **dorendersample**" ruft diese Methode die [**cbaserdenderer:: onrenderstart**](cbaserenderer-onrenderstart.md) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-121">Immediately before calling **DoRenderSample**, this method calls the [**CBaseRenderer::OnRenderStart**](cbaserenderer-onrenderstart.md) method.</span></span> <span data-ttu-id="ca5f0-122">Unmittelbar danach wird die [**cbaserenderer:: onrenderend**](cbaserenderer-onrenderend.md) -Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-122">Immediately after, it calls the [**CBaseRenderer::OnRenderEnd**](cbaserenderer-onrenderend.md) method.</span></span> <span data-ttu-id="ca5f0-123">Die abgeleitete Klasse kann diese beiden Methoden nach Bedarf überschreiben.</span><span class="sxs-lookup"><span data-stu-id="ca5f0-123">The derived class can override those two methods as needed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca5f0-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca5f0-124">Requirements</span></span>



| <span data-ttu-id="ca5f0-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca5f0-125">Requirement</span></span> | <span data-ttu-id="ca5f0-126">Wert</span><span class="sxs-lookup"><span data-stu-id="ca5f0-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca5f0-127">Header</span><span class="sxs-lookup"><span data-stu-id="ca5f0-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ca5f0-128"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca5f0-128"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ca5f0-129">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="ca5f0-129">Library</span></span><br/> | <dl> <span data-ttu-id="ca5f0-130">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="ca5f0-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca5f0-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca5f0-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca5f0-132">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="ca5f0-132">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




