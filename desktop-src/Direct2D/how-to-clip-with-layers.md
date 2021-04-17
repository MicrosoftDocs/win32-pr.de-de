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
# <a name="how-to-clip-to-a-geometric-mask"></a>Vorgehensweise beim Abschneiden einer geometrischen Maske

In diesem Thema wird beschrieben, wie Sie mit einer geometrischen Maske einen Bereich einer Ebene ausschneiden.

**So schneiden Sie einen Bereich mit einer geometrischen Maske ab**

1.  Erstellen Sie die [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) , die zum Abschneiden des Bereichs verwendet wird.
2.  Rufen Sie [**ID2D1RenderTarget:: kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) auf, um eine Ebene zu erstellen.
3.  Nennen Sie [**ID2D1RenderTarget::P ushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) , und übergeben Sie die geometrische Maske, die Sie in Schritt 1 definiert haben.
4.  Zeichnen Sie den Inhalt zu Clip.
5.  [**ID2D1RenderTarget::P oplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen, um die Ebene aus dem Renderziel zu entfernen.

Im folgenden Beispiel wird eine geometrische Maske zum Ausschneiden eines Bilds und mehrerer Rechtecke verwendet. Die folgende Abbildung zeigt die ursprüngliche Bitmap auf der linken Seite und die Bitmap, die auf der rechten Seite der geometrischen Maske abgeschnitten wird.

![Abbildung einer Goldfisch-Bitmap vor und nach dem Abschneiden der Bitmap auf eine sternförmige Maske](images/cliparegion-layers.png)

Um die Zeichnung wie in der obigen Abbildung gezeigt zu schneiden, erstellen Sie eine [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) , und verwenden Sie Sie, um einen Stern zu definieren. Dies wird im folgenden Code veranschaulicht.


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



Rufen Sie zum Erstellen einer Ebene " [**kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) " auf.

> [!Note]  
> Ab Windows 8 müssen Sie nicht " [**kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))" aufrufen. In den meisten Fällen ist die Leistung besser, wenn Sie diese Methode nicht aufzurufen und Direct2D die ebenenressourcen verwaltet.

 

Ruft die [**pushschicht**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) mit der Geometrie Maske auf, um die Ebene zu pushen. Zeichnen Sie den Inhalt, und klicken Sie dann auf [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) , um die Ebene zu poptieren. Dadurch wird die sternförmige Zeichnung erzeugt. Dies wird im folgenden Code veranschaulicht.


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

[Übersicht über Schichten](direct2d-layers-overview.md)
</dt> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 