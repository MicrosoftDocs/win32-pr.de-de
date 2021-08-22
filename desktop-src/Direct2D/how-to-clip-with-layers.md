---
title: Ausschneiden einer geometrischen Maske
description: Zeigt, wie ein Bereich mit Ebenen beschnitten wird.
ms.assetid: eaeb6cfd-de62-46f1-972d-a11e0ccc11d9
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0c2258938020593014b5b6f5ea77516e7770f8589601cf4139971b3532b22fff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569345"
---
# <a name="how-to-clip-to-a-geometric-mask"></a>Ausschneiden einer geometrischen Maske

In diesem Thema wird beschrieben, wie eine geometrische Maske verwendet wird, um einen Bereich einer Ebene zu beschneiden.

**So beschneiden Sie einen Bereich mit einer geometrischen Maske**

1.  Erstellen Sie die [**ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) die zum Beschneiden des Bereichs verwendet wird.
2.  Rufen Sie [**ID2D1RenderTarget::CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) auf, um eine Ebene zu erstellen.
3.  Rufen Sie [**ID2D1RenderTarget::P ushLayer auf,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und übergeben Sie die geometrische Maske, die Sie in Schritt 1 definiert haben.
4.  Zeichnen Sie den zu beschneidende Inhalt.
5.  Rufen Sie [**ID2D1RenderTarget::P opLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) auf, um die Ebene aus dem Renderziel zu entfernen.

Im folgenden Beispiel wird eine geometrische Maske verwendet, um ein Bild und mehrere Rechtecke zu beschneiden. Die folgende Abbildung zeigt die ursprüngliche Bitmap auf der linken Seite und die Bitmap, die auf die geometrische Maske auf der rechten Seite abgeschnitten ist.

![Abbildung einer Goldfish-Bitmap vor und nach dem Abschneiden der Bitmap auf eine sternförmige Maske](images/cliparegion-layers.png)

Um die Zeichnung wie in der vorherigen Abbildung dargestellt zu beschneiden, erstellen Sie eine [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) und verwenden sie, um einen Stern zu definieren. Dies wird im folgenden Code veranschaulicht.


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



Rufen [**Sie CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) auf, um eine Ebene zu erstellen.

> [!Note]  
> Ab Windows 8 müssen Sie [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))nicht mehr aufrufen. In den meisten Situationen ist die Leistung besser, wenn Sie diese Methode nicht aufrufen und Direct2D die Ebenenressourcen verwaltet.

 

Rufen Sie [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) mit der Geometriemaske auf, um die Ebene zu pushen. Zeichnen Sie den Zuschneidende Inhalt, und rufen Sie dann [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) auf, um die Ebene zu befüllen. Dadurch wird die sternförmige Zeichnung erzeugt. Dies wird im folgenden Code veranschaulicht.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Ebenen](direct2d-layers-overview.md)
</dt> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 