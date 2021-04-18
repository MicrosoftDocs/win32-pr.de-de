---
description: Die Receive-Methode empfängt das nächste Medien Beispiel im Stream.
ms.assetid: b340f76c-2305-444f-bc00-1ef5acdea329
title: Cbaserderderer. Receive-Methode (renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.Receive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 96abb2ee3d44604c23e9943e086a52312a011e92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372517"
---
# <a name="cbaserendererreceive-method"></a><span data-ttu-id="6c2d6-103">Cbaserderderer. Receive-Methode</span><span class="sxs-lookup"><span data-stu-id="6c2d6-103">CBaseRenderer.Receive method</span></span>

<span data-ttu-id="6c2d6-104">Die- `Receive` Methode empfängt das nächste Medien Beispiel im Stream.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-104">The `Receive` method receives the next media sample in the stream.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c2d6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="6c2d6-105">Syntax</span></span>


```C++
virtual Receive(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="6c2d6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6c2d6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c2d6-107">*pmediasample*</span><span class="sxs-lookup"><span data-stu-id="6c2d6-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="6c2d6-108">Zeiger auf die [**imediasample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) -Schnittstelle des Beispiels.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c2d6-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6c2d6-109">Return value</span></span>

<span data-ttu-id="6c2d6-110">Gibt \_ bei Erfolg S OK oder einen **HRESULT** -Wert zurück, der die Ursache des Fehlers angibt.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c2d6-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c2d6-111">Remarks</span></span>

<span data-ttu-id="6c2d6-112">Die Eingabe-PIN ruft diese Methode auf, wenn Sie ein Beispiel aus dem upstreamfilter empfängt.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-112">The input pin calls this method when it receives a sample from the upstream filter.</span></span>

<span data-ttu-id="6c2d6-113">Wenn der Filter ausgeführt wird, führt diese Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="6c2d6-113">If the filter is running, this method performs the following steps:</span></span>

1.  <span data-ttu-id="6c2d6-114">Plant das Beispiel für das Rendering ([**cbaserenderer::P**](cbaserenderer-preparereceive.md)Analyse).</span><span class="sxs-lookup"><span data-stu-id="6c2d6-114">Schedules the sample for rendering ([**CBaseRenderer::PrepareReceive**](cbaserenderer-preparereceive.md)).</span></span>
2.  <span data-ttu-id="6c2d6-115">Wartet auf die geplante Zeit ([**cbaserenderer:: waitforrendertime**](cbaserenderer-waitforrendertime.md)).</span><span class="sxs-lookup"><span data-stu-id="6c2d6-115">Waits for the scheduled time ([**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)).</span></span>
3.  <span data-ttu-id="6c2d6-116">Rendert das Beispiel ([**cbaserenderer:: Rendering**](cbaserenderer-render.md)).</span><span class="sxs-lookup"><span data-stu-id="6c2d6-116">Renders the sample ([**CBaseRenderer::Render**](cbaserenderer-render.md)).</span></span>
4.  <span data-ttu-id="6c2d6-117">Gibt das Beispiel ([**cbaserderderer:: clearpdingsample**](cbaserenderer-clearpendingsample.md)) frei.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-117">Releases the sample ([**CBaseRenderer::ClearPendingSample**](cbaserenderer-clearpendingsample.md)).</span></span>

<span data-ttu-id="6c2d6-118">Wenn der Filter angehalten ist, führt die-Methode die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="6c2d6-118">If the filter is paused, the method performs the following steps:</span></span>

1.  <span data-ttu-id="6c2d6-119">Benachrichtigt die abgeleitete-Klasse, dass eine Stichprobe verfügbar ist ([**cbasererderderer:: onreceivefirstsample**](cbaserenderer-onreceivefirstsample.md)).</span><span class="sxs-lookup"><span data-stu-id="6c2d6-119">Notifies the derived class that a sample is available ([**CBaseRenderer::OnReceiveFirstSample**](cbaserenderer-onreceivefirstsample.md)).</span></span>
2.  <span data-ttu-id="6c2d6-120">Wartet auf die geplante Zeit.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-120">Waits for the scheduled time.</span></span>
3.  <span data-ttu-id="6c2d6-121">Rendert das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-121">Renders the sample.</span></span>
4.  <span data-ttu-id="6c2d6-122">Gibt das Beispiel frei.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-122">Releases the sample.</span></span>

<span data-ttu-id="6c2d6-123">Obwohl die-Methode angehalten wurde, wartet Sie in Schritt 2, bis der Filter in den Status wird ausgeführt wechselt.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-123">While paused, the method waits in step 2 until the filter switches to a running state.</span></span> <span data-ttu-id="6c2d6-124">An diesem Punkt plant der Filter das Beispiel.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-124">At that point, the filter schedules the sample.</span></span>

<span data-ttu-id="6c2d6-125">In der Basisklasse führt die **onreceivefirstsample** -Methode keine Aktion aus.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-125">In the base class, the **OnReceiveFirstSample** method does nothing.</span></span> <span data-ttu-id="6c2d6-126">Diese kann von der abgeleiteten Klasse überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-126">The derived class can override it.</span></span> <span data-ttu-id="6c2d6-127">Wenn ein Videorenderer z. b. angehalten wird, wird das erste Beispiel als Bild angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6c2d6-127">For example, when a video renderer is paused, it displays the first sample as a still image.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c2d6-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c2d6-128">Requirements</span></span>



| <span data-ttu-id="6c2d6-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c2d6-129">Requirement</span></span> | <span data-ttu-id="6c2d6-130">Wert</span><span class="sxs-lookup"><span data-stu-id="6c2d6-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c2d6-131">Header</span><span class="sxs-lookup"><span data-stu-id="6c2d6-131">Header</span></span><br/>  | <dl> <span data-ttu-id="6c2d6-132"><dt>Renbase. h (Include Streams. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6c2d6-132"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6c2d6-133">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="6c2d6-133">Library</span></span><br/> | <dl> <span data-ttu-id="6c2d6-134">" <dt>Straumbase. lib" (Einzelhandels Builds);</dt> " <dt>Straumbasd. lib" (Debugbuilds)</dt></span><span class="sxs-lookup"><span data-stu-id="6c2d6-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c2d6-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c2d6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c2d6-136">**Cbaserderderer-Klasse**</span><span class="sxs-lookup"><span data-stu-id="6c2d6-136">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




