---
title: Vorgehensweise beim Abschneiden einer geometrischen Maske
description: Zeigt, wie Sie einen Bereich mit Ebenen Ausschneiden.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 979281fb7fa6e034894bffaecbd6246fe8a9aa94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473725"
---
# <a name="how-to-clip-to-a-geometric-mask"></a><span data-ttu-id="d8e57-103">Vorgehensweise beim Abschneiden einer geometrischen Maske</span><span class="sxs-lookup"><span data-stu-id="d8e57-103">How to Clip to a Geometric Mask</span></span>

<span data-ttu-id="d8e57-104">In diesem Thema wird beschrieben, wie Sie mit einer geometrischen Maske einen Bereich einer Ebene ausschneiden.</span><span class="sxs-lookup"><span data-stu-id="d8e57-104">This topic describes how to use a geometric mask to clip a region of a layer.</span></span>

<span data-ttu-id="d8e57-105">**So schneiden Sie einen Bereich mit einer geometrischen Maske ab**</span><span class="sxs-lookup"><span data-stu-id="d8e57-105">**To clip a region with a geometric mask**</span></span>

1.  <span data-ttu-id="d8e57-106">Erstellen Sie die [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , die zum Abschneiden des Bereichs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d8e57-106">Create the [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) that will be used to clip the region.</span></span>
2.  <span data-ttu-id="d8e57-107">Rufen Sie [**ID2D1RenderTarget:: kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) auf, um eine Ebene zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d8e57-107">Call [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>
3.  <span data-ttu-id="d8e57-108">Nennen Sie [**ID2D1RenderTarget::P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) , und übergeben Sie die geometrische Maske, die Sie in Schritt 1 definiert haben.</span><span class="sxs-lookup"><span data-stu-id="d8e57-108">Call [**ID2D1RenderTarget::PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) and pass the geometric mask you defined in step 1.</span></span>
4.  <span data-ttu-id="d8e57-109">Zeichnen Sie den Inhalt zu Clip.</span><span class="sxs-lookup"><span data-stu-id="d8e57-109">Draw the content to clip.</span></span>
5.  <span data-ttu-id="d8e57-110">[**ID2D1RenderTarget::P oplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen, um die Ebene aus dem Renderziel zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="d8e57-110">Call [**ID2D1RenderTarget::PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to remove the layer from the render target.</span></span>

<span data-ttu-id="d8e57-111">Im folgenden Beispiel wird eine geometrische Maske zum Ausschneiden eines Bilds und mehrerer Rechtecke verwendet.</span><span class="sxs-lookup"><span data-stu-id="d8e57-111">The example that follows uses a geometric mask to clip an image and several rectangles.</span></span> <span data-ttu-id="d8e57-112">Die folgende Abbildung zeigt die ursprüngliche Bitmap auf der linken Seite und die Bitmap, die auf der rechten Seite der geometrischen Maske abgeschnitten wird.</span><span class="sxs-lookup"><span data-stu-id="d8e57-112">The following illustration shows the original bitmap on the left, and the bitmap clipped to the geometric mask on the right.</span></span>

![Abbildung einer Goldfisch-Bitmap vor und nach dem Abschneiden der Bitmap auf eine sternförmige Maske](images/cliparegion-layers.png)

<span data-ttu-id="d8e57-114">Um die Zeichnung wie in der obigen Abbildung gezeigt zu schneiden, erstellen Sie eine [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , und verwenden Sie Sie, um einen Stern zu definieren.</span><span class="sxs-lookup"><span data-stu-id="d8e57-114">To clip the drawing as shown in the preceding illustration, you create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and use it to define a star.</span></span> <span data-ttu-id="d8e57-115">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d8e57-115">The following code shows how to do this.</span></span>


```C++
// Create the path geometry.
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
}

// Write to the path geometry using the geometry sink to create a star.
if (SUCCEEDED(hr))
{
    hr = m_pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
    pSink->BeginFigure(D2D1::Point2F(20, 50), D2D1_FIGURE_BEGIN_FILLED);
    pSink->AddLine(D2D1::Point2F(130, 50));
    pSink->AddLine(D2D1::Point2F(20, 130));
    pSink->AddLine(D2D1::Point2F(80, 0));
    pSink->AddLine(D2D1::Point2F(130, 130));
    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}

SafeRelease(&pSink);
```



<span data-ttu-id="d8e57-116">Rufen Sie zum Erstellen einer Ebene " [**kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) " auf.</span><span class="sxs-lookup"><span data-stu-id="d8e57-116">Call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) to create a layer.</span></span>

> [!Note]  
> <span data-ttu-id="d8e57-117">Ab Windows 8 müssen Sie nicht " [**kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))" aufrufen.</span><span class="sxs-lookup"><span data-stu-id="d8e57-117">Starting with Windows 8, you don't need to call [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)).</span></span> <span data-ttu-id="d8e57-118">In den meisten Fällen ist die Leistung besser, wenn Sie diese Methode nicht aufzurufen und Direct2D die ebenenressourcen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="d8e57-118">In most situations performance is better if you don't call this method and Direct2D manages the layer resources.</span></span>

 

<span data-ttu-id="d8e57-119">Ruft die [**pushschicht**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) mit der Geometrie Maske auf, um die Ebene zu pushen.</span><span class="sxs-lookup"><span data-stu-id="d8e57-119">Call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) with the geometry mask to push the layer.</span></span> <span data-ttu-id="d8e57-120">Zeichnen Sie den Inhalt, und klicken Sie dann auf [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , um die Ebene zu poptieren.</span><span class="sxs-lookup"><span data-stu-id="d8e57-120">Draw the content to clip, then call [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) to pop the layer.</span></span> <span data-ttu-id="d8e57-121">Dadurch wird die sternförmige Zeichnung erzeugt.</span><span class="sxs-lookup"><span data-stu-id="d8e57-121">This produces the star-shaped drawing.</span></span> <span data-ttu-id="d8e57-122">Dies wird im folgenden Code veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="d8e57-122">The following code shows how to do this.</span></span>


```C++
HRESULT DemoApp::RenderWithLayer(ID2D1RenderTarget *pRT)
{
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

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

    SafeRelease(&pLayer);

    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="d8e57-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d8e57-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d8e57-124">Übersicht über Schichten</span><span class="sxs-lookup"><span data-stu-id="d8e57-124">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> <dt>

[<span data-ttu-id="d8e57-125">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="d8e57-125">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 