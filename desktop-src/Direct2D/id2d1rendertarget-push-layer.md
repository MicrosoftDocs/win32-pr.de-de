---
title: ID2D1RenderTarget pushlayer-Methoden (D2d1 \_ 1. h)
description: Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis poplayer aufgerufen wird.
ms.assetid: 9336662c-e94e-40ba-adbe-066d704958bc
keywords:
- Pushlayer-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 6a5609192162ae0b0c0e2af8f1b84429d8710509
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364487"
---
# <a name="id2d1rendertargetpushlayer-methods"></a><span data-ttu-id="b30fe-104">ID2D1RenderTarget::P ushlayer-Methoden</span><span class="sxs-lookup"><span data-stu-id="b30fe-104">ID2D1RenderTarget::PushLayer methods</span></span>

<span data-ttu-id="b30fe-105">Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b30fe-105">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span>

### <a name="overload-list"></a><span data-ttu-id="b30fe-106">Überladeliste</span><span class="sxs-lookup"><span data-stu-id="b30fe-106">Overload list</span></span>



| <span data-ttu-id="b30fe-107">Methode</span><span class="sxs-lookup"><span data-stu-id="b30fe-107">Method</span></span>                                                                                                                            | <span data-ttu-id="b30fe-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b30fe-108">Description</span></span>                                                                                                                                                                     |
|:----------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b30fe-109">[**Pushlayer (D2D1 \_ Layer \_ Parameters&, ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="b30fe-109">[**PushLayer(D2D1\_LAYER\_PARAMETERS&,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))</span></span>  | <span data-ttu-id="b30fe-110">Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b30fe-110">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |
| <span data-ttu-id="b30fe-111">[**Pushlayer (D2D1 \_ Layer \_ Parameters \* , ID2D1Layer \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span><span class="sxs-lookup"><span data-stu-id="b30fe-111">[**PushLayer(D2D1\_LAYER\_PARAMETERS\*,ID2D1Layer\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters_id2d1layer))</span></span> | <span data-ttu-id="b30fe-112">Fügt dem Renderziel die angegebene Ebene hinzu, sodass alle nachfolgenden Zeichnungsvorgänge empfangen werden, bis [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b30fe-112">Adds the specified layer to the render target so that it receives all subsequent drawing operations until [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) is called.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="b30fe-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b30fe-113">Remarks</span></span>

<span data-ttu-id="b30fe-114">Mithilfe der [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -Methode kann ein Aufrufer mit dem Umleiten des Rendering zu einer Ebene beginnen.</span><span class="sxs-lookup"><span data-stu-id="b30fe-114">The [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method enables a caller to begin redirecting rendering to a layer.</span></span> <span data-ttu-id="b30fe-115">Alle Renderingvorgänge sind in einer Ebene gültig.</span><span class="sxs-lookup"><span data-stu-id="b30fe-115">All rendering operations are valid in a layer.</span></span> <span data-ttu-id="b30fe-116">Der Speicherort der Ebene wird von der Welt Transformation beeinflusst, die auf dem Renderziel festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b30fe-116">The location of the layer is affected by the world transform set on the render target.</span></span>

<span data-ttu-id="b30fe-117">Jede **pushschicht** muss über einen passenden [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) -Befehl verfügen.</span><span class="sxs-lookup"><span data-stu-id="b30fe-117">Each **PushLayer** must have a matching [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) call.</span></span> <span data-ttu-id="b30fe-118">Wenn mehr **poplayer** -Aufrufe als **pushlayer** -Aufrufe vorhanden sind, wird das Renderziel in einen Fehlerzustand versetzt.</span><span class="sxs-lookup"><span data-stu-id="b30fe-118">If there are more **PopLayer** calls than **PushLayer** calls, the render target is placed into an error state.</span></span> <span data-ttu-id="b30fe-119">Wenn [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) vor allen ausstehenden Ebenen aufgerufen wird, wird das Renderziel in einen Fehlerzustand versetzt, und es wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b30fe-119">If [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) is called before all outstanding layers are popped, the render target is placed into an error state, and an error is returned.</span></span> <span data-ttu-id="b30fe-120">Der Fehlerzustand kann durch einen Aufrufen von [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b30fe-120">The error state can be cleared by a call to [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).</span></span>

<span data-ttu-id="b30fe-121">Eine bestimmte [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Ressource kann nur zu einem bestimmten Zeitpunkt aktiv sein.</span><span class="sxs-lookup"><span data-stu-id="b30fe-121">A particular [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) resource can be active only at one time.</span></span> <span data-ttu-id="b30fe-122">Anders ausgedrückt: Sie können keine [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -Methode aufzurufen und dann sofort mit einer anderen **pushlayer** -Methode mit derselben ebenenressource folgen.</span><span class="sxs-lookup"><span data-stu-id="b30fe-122">In other words, you cannot call a [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) method, and then immediately follow with another **PushLayer** method with the same layer resource.</span></span> <span data-ttu-id="b30fe-123">Stattdessen müssen Sie die zweite **pushlayer** -Methode mit unterschiedlichen ebenenressourcen abrufen.</span><span class="sxs-lookup"><span data-stu-id="b30fe-123">Instead, you must call the second **PushLayer** method with different layer resources.</span></span>

<span data-ttu-id="b30fe-124">Ein Beispiel finden Sie unter Gewusst [wie: Abschneiden eines Bereichs mit Ebenen](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="b30fe-124">For an example, see [How to Clip a Region with Layers](how-to-clip-with-layers.md).</span></span>

<span data-ttu-id="b30fe-125">Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt.</span><span class="sxs-lookup"><span data-stu-id="b30fe-125">This method doesn't return an error code if it fails.</span></span> <span data-ttu-id="b30fe-126">Um zu ermitteln, ob ein Zeichnungs Vorgang (z. b. **pushlayer**) fehlgeschlagen ist, überprüfen Sie das von den Methoden [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis.</span><span class="sxs-lookup"><span data-stu-id="b30fe-126">To determine whether a drawing operation (such as **PushLayer**) failed, check the result returned by the [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) or [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) methods.</span></span>

## <a name="examples"></a><span data-ttu-id="b30fe-127">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b30fe-127">Examples</span></span>

<span data-ttu-id="b30fe-128">Im folgenden Beispiel wird eine-Ebene verwendet, um eine Bitmap an eine geometrische Maske auszuschneiden.</span><span class="sxs-lookup"><span data-stu-id="b30fe-128">The following example uses a layer to clip a bitmap to a geometric mask.</span></span> <span data-ttu-id="b30fe-129">Das komplette Beispiel finden Sie unter Gewusst [wie: Abschneiden einer geometrischen Maske](how-to-clip-with-layers.md).</span><span class="sxs-lookup"><span data-stu-id="b30fe-129">For the complete example, see [How to Clip to a Geometric Mask](how-to-clip-with-layers.md).</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &amp;pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(350, 50));

        // Push the layer with the geometric mask.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );
            
  
        pRT->DrawBitmap(m_pOrigBitmap, D2D1::RectF(0, 0, 200, 133));
        pRT->FillRectangle(D2D1::RectF(0.f, 0.f, 25.f, 25.f), m_pSolidColorBrush);  
        pRT->FillRectangle(D2D1::RectF(25.f, 25.f, 50.f, 50.f), m_pSolidColorBrush);
        pRT->FillRectangle(D2D1::RectF(50.f, 50.f, 75.f, 75.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(75.f, 75.f, 100.f, 100.f), m_pSolidColorBrush);    
        pRT->FillRectangle(D2D1::RectF(100.f, 100.f, 125.f, 125.f), m_pSolidColorBrush); 
        pRT->FillRectangle(D2D1::RectF(125.f, 125.f, 150.f, 150.f), m_pSolidColorBrush);    
        

        pRT->PopLayer();
    }

    SafeRelease(&amp;pLayer);

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="b30fe-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b30fe-130">Requirements</span></span>



| <span data-ttu-id="b30fe-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b30fe-131">Requirement</span></span> | <span data-ttu-id="b30fe-132">Wert</span><span class="sxs-lookup"><span data-stu-id="b30fe-132">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b30fe-133">Header</span><span class="sxs-lookup"><span data-stu-id="b30fe-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b30fe-134"><dt>D2d1 \_ 1. h (Include D2d1. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b30fe-134"><dt>D2d1\_1.h (include D2d1.h)</dt></span></span> </dl> |
| <span data-ttu-id="b30fe-135">Bibliothek</span><span class="sxs-lookup"><span data-stu-id="b30fe-135">Library</span></span><br/> | <dl> <span data-ttu-id="b30fe-136"><dt>D2d1. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b30fe-136"><dt>D2d1.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="b30fe-137">DLL</span><span class="sxs-lookup"><span data-stu-id="b30fe-137">DLL</span></span><br/>     | <dl> <span data-ttu-id="b30fe-138"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b30fe-138"><dt>D2d1.dll</dt></span></span> </dl>                   |



## <a name="see-also"></a><span data-ttu-id="b30fe-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b30fe-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30fe-140">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="b30fe-140">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[<span data-ttu-id="b30fe-141">Übersicht über Schichten</span><span class="sxs-lookup"><span data-stu-id="b30fe-141">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

<span data-ttu-id="b30fe-142">�</span><span class="sxs-lookup"><span data-stu-id="b30fe-142">�</span></span>

<span data-ttu-id="b30fe-143">�</span><span class="sxs-lookup"><span data-stu-id="b30fe-143">�</span></span>
