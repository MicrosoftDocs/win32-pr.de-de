---
title: Übersicht über Pfadgeometrien
description: Beschreibt die Verwendung von Pfadgeometrien zum Definieren komplexer Formen.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5fb177cbbd82ef56a03ef2c8a6faa7ef6c11f7889423ce79102d11eb42090231
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119636158"
---
# <a name="path-geometries-overview"></a>Übersicht über Pfadgeometrien

In diesem Thema wird beschrieben, wie Sie Direct2D-Pfadgeometrien verwenden, um komplexe Zeichnungen zu erstellen. Der Abschnitt ist wie folgt gegliedert.

-   [Voraussetzungen](#prerequisites)
-   [Pfadgeometrien in Direct2D](#path-geometries-in-direct2d)
-   [Verwenden von ID2D1GeometrySink zum Auffüllen einer Pfadgeometrie](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [Beispiel: Erstellen einer komplexen Zeichnung](#example-create-a-complex-drawing)
    -   [Erstellen einer Pfadgeometrie für den linken Mountain](#create-a-path-geometry-for-the-left-mountain)
    -   [Erstellen einer Pfadgeometrie für den rechten Mountain](#create-a-path-geometry-for-the-right-mountain)
    -   [Erstellen einer Pfadgeometrie für die Sun](#create-a-path-geometry-for-the-sun)
    -   [Erstellen einer Pfadgeometrie für den Fluss](#create-a-path-geometry-for-the-river)
    -   [Rendern der Pfadgeometrien auf der Anzeige](#render-the-path-geometries-onto-the-display)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In dieser Übersicht wird davon ausgegangen, dass Sie mit dem Erstellen grundlegender Direct2D-Anwendungen vertraut sind, wie unter Erstellen einer einfachen [Direct2D-Anwendung beschrieben.](direct2d-quickstart.md) Außerdem wird davon ausgegangen, dass Sie mit den grundlegenden Features von Direct2D-Geometrien vertraut sind, wie in [der Übersicht über Geometrien beschrieben.](direct2d-geometries-overview.md)

## <a name="path-geometries-in-direct2d"></a>Pfadgeometrien in Direct2D

Pfadgeometrien werden durch die [**ID2D1PathGeometry-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) dargestellt. Rufen Sie zum Instanziieren einer Pfadgeometrie die [**ID2D1Factory::CreatePathGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) auf. Diese Objekte können verwendet werden, um komplexe geometrische Abbildungen zu beschreiben, die aus Segmenten wie Bogen, Kurven und Linien bestehen. Um eine Pfadgeometrie mit Abbildungen und Segmenten zu füllen, rufen Sie die [**Open-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) auf, um eine [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) abzurufen, und verwenden Sie die Methoden der Geometry-Senke, um der Pfadgeometrie Abbildungen und Segmente hinzuzufügen.

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>Verwenden von ID2D1GeometrySink zum Auffüllen einer Pfadgeometrie

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) beschreibt einen geometrischen Pfad, der Linien, Bogen, kubische Bézierkurven und quadratische Bézierkurven enthalten kann.

Eine Geometriesenke besteht aus einer oder mehreren Abbildungen. Jede Abbildung besteht aus einem oder mehr Linien-, Kurven- oder Bogensegmenten. Rufen Sie zum Erstellen einer Abbildung die [**BeginFigure-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) auf, übergeben Sie den Ausgangspunkt der Abbildung, und verwenden Sie dann die Add-Methoden (z. B. [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) und [**AddBezier),**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) um Segmente hinzuzufügen. Wenn Sie mit dem Hinzufügen von Segmenten fertig sind, rufen Sie die [**EndFigure-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) auf. Sie können diese Sequenz wiederholen, um zusätzliche Abbildungen zu erstellen. Wenn Sie mit dem Erstellen von Abbildungen fertig sind, rufen Sie die [**Close-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) auf.

## <a name="example-create-a-complex-drawing"></a>Beispiel: Erstellen einer komplexen Zeichnung

Die folgende Abbildung zeigt eine komplexe Zeichnung mit Linien, Bogen und Bézierkurven. Das folgende Codebeispiel zeigt, wie die Zeichnung mithilfe von vier Pfadgeometrieobjekten erstellt wird: eines für den linken, eines für den rechten, eines für den Fluss und eines für die Sun mit Flares.

![Abbildung eines Flusses, einer Flüsse und der Sun mithilfe von Pfadgeometrien](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>Erstellen einer Pfadgeometrie für den linken Mountain

Im Beispiel wird zunächst eine Pfadgeometrie für den linken Mountain erstellt, wie in der folgenden Abbildung dargestellt.

![Zeigt eine komplexe Zeichnung eines Polygons, das einen Mountain zeigt.](images/path-geo-leftmnt.png)

Um den linken Mountain zu erstellen, ruft das Beispiel die [**ID2D1Factory::CreatePathGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) auf, um eine [**ID2D1PathGeometry zu erstellen.**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



Im Beispiel wird dann die [**Open-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) verwendet, um eine geometry-Senke aus einer [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) zu erhalten und in der *pSink-Variablen zu* speichern.


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



Das Beispiel ruft dann [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure)auf, übergibt [**D2D1 \_ FIGURE BEGIN \_ \_ FILLED,**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) das angibt, dass diese Abbildung ausgefüllt ist, und ruft dann [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines)auf und übergibt ein Array von [**D2D1 \_ POINT \_ 2F-Punkten,**](d2d1-point-2f.md) (267, 177), (236, 192), (212, 160), (156, 255) und (346, 255).

Dies wird im folgenden Code veranschaulicht.


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a>Erstellen einer Pfadgeometrie für den rechten Mountain

Im Beispiel wird dann eine weitere Pfadgeometrie für den rechten Mountain mit Punkten (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) und (575, 263) erstellt. Die folgende Abbildung zeigt, wie der rechte Mountain angezeigt wird.

![Abbildung eines Polygons, das einen Mountain zeigt](images/path-geo-rightmnt.png)

Dies wird im folgenden Code veranschaulicht.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a>Erstellen einer Pfadgeometrie für die Sun

Im Beispiel wird dann eine andere Pfadgeometrie für die Sun aufgefüllt, wie in der folgenden Abbildung dargestellt.

![Abbildung eines Bogens und einer Bézierkurve, die die Sun zeigt](images/path-geo-sun.png)

Zu diesem Grund erstellt die Pfadgeometrie eine Senke und fügt der Senke eine Abbildung für den Bogen und eine Abbildung für jedes Flare hinzu. Durch Wiederholen der Sequenz von [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), den Add-Methoden (z. B. [**AddBezier)**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))und [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure)werden der Senke mehrere Abbildungen hinzugefügt.

Dies wird im folgenden Code veranschaulicht.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a>Erstellen einer Pfadgeometrie für den Fluss

Im Beispiel wird dann ein weiterer Geometriepfad für den Fluss erstellt, der Bézierkurven enthält. Die folgende Abbildung zeigt, wie der Fluss angezeigt wird.

![Abbildung von Bézierkurven, die einen Fluss zeigen](images/path-geo-river.png)

Dies wird im folgenden Code veranschaulicht.


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a>Rendern der Pfadgeometrien auf der Anzeige

Der folgende Code zeigt, wie die aufgefüllten Pfadgeometrien auf der Anzeige gerendert werden. Es zeichnet zuerst die Sonnengeometrie, die linke Mountaingeometrie, dann die Flussgeometrie und schließlich die rechte Mountaingeometrie.


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



Im vollständigen Beispiel wird die folgende Abbildung ausgegeben.

![Abbildung eines Flusses, einer Flüsse und der Sun mithilfe von Pfadgeometrien](images/path-geo-mnts.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)
</dt> <dt>

[Übersicht über Geometrien](direct2d-geometries-overview.md)
</dt> </dl>

 

 