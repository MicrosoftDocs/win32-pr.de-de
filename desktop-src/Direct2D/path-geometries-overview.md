---
title: Übersicht über Pfadgeometrien
description: Beschreibt die Verwendung von Pfadgeometrien zum Definieren komplexer Formen.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/28/2021
ms.locfileid: "104551813"
---
# <a name="path-geometries-overview"></a>Übersicht über Pfadgeometrien

In diesem Thema wird beschrieben, wie Sie Direct2D Path Geometrien zum Erstellen komplexer Zeichnungen verwenden. Der Abschnitt ist wie folgt gegliedert.

-   [Voraussetzungen](#prerequisites)
-   [Pfadgeometrien in Direct2D](#path-geometries-in-direct2d)
-   [Verwenden eines ID2D1GeometrySink zum Auffüllen einer Pfad Geometrie](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [Beispiel: Erstellen einer komplexen Zeichnung](#example-create-a-complex-drawing)
    -   [Erstellen einer Pfad Geometrie für den linken Berg](#create-a-path-geometry-for-the-left-mountain)
    -   [Erstellen einer Pfad Geometrie für den rechten Berg](#create-a-path-geometry-for-the-right-mountain)
    -   [Erstellen einer Pfad Geometrie für die Sun](#create-a-path-geometry-for-the-sun)
    -   [Erstellen einer Pfad Geometrie für den Fluss](#create-a-path-geometry-for-the-river)
    -   [Rendering der Pfadgeometrien auf der Anzeige](#render-the-path-geometries-onto-the-display)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Diese Übersicht setzt voraus, dass Sie mit dem Erstellen von grundlegenden Direct2D-Anwendungen vertraut sind, wie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)beschrieben. Außerdem wird davon ausgegangen, dass Sie mit den grundlegenden Features von Direct2D Geometries vertraut sind, wie in [Übersicht über Geometrien](direct2d-geometries-overview.md)beschrieben.

## <a name="path-geometries-in-direct2d"></a>Pfadgeometrien in Direct2D

Pfadgeometrien werden durch die [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Schnittstelle dargestellt. Um eine Pfad Geometrie zu instanziieren, müssen Sie die [**ID2D1Factory:: kreatepathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) -Methode aufrufen. Diese Objekte können verwendet werden, um komplexe geometrische Abbildungen zu beschreiben, die aus Segmenten wie Arcs, Kurven und Linien bestehen. Um eine Pfad Geometrie mit Abbildungen und Segmenten aufzufüllen, rufen Sie die [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) -Methode auf, um ein [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) abzurufen, und verwenden Sie die Methoden der Geometry-Senke, um der Pfad Geometrie Abbildungen und Segmente hinzuzufügen.

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a>Verwenden eines ID2D1GeometrySink zum Auffüllen einer Pfad Geometrie

[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) beschreibt einen geometrischen Pfad, der Linien, Arcs, kubische Bezier-Kurven und quadratische Bezier-Kurven enthalten kann.

Eine Geometry-Senke besteht aus einer oder mehreren Abbildungen. Jede Abbildung besteht aus einem oder mehreren Linien-, Kurven-oder Bogen Segmenten. Rufen Sie zum Erstellen einer Abbildung die [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) -Methode auf, und übergeben Sie den Anfangspunkt der Abbildung. verwenden Sie dann die Add-Methoden (z. b. [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) und [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) ), um Segmente hinzuzufügen. Wenn Sie das Hinzufügen von Segmenten abgeschlossen haben, müssen Sie die [**endfigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) -Methode abrufen. Sie können diese Sequenz wiederholen, um zusätzliche Abbildungen zu erstellen. Wenn Sie mit dem Erstellen von Abbildungen fertig sind, müssen Sie die [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) -Methode abrufen.

## <a name="example-create-a-complex-drawing"></a>Beispiel: Erstellen einer komplexen Zeichnung

Die folgende Abbildung zeigt eine komplexe Zeichnung mit Linien-, Arcs-und Bezier-Kurven. Das folgende Codebeispiel zeigt, wie die Zeichnung mithilfe von vier Pfad Geometrie Objekten erstellt wird, eine für den linken Berg, eine für den rechten Berg, eine für den Fluss und eine für die Sonne mit Flares.

![Darstellung eines Flusses, Gebirges und der Sonne mithilfe von Pfadgeometrien](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a>Erstellen einer Pfad Geometrie für den linken Berg

Im Beispiel wird zuerst eine Pfad Geometrie für den linken Berg erstellt, wie in der folgenden Abbildung dargestellt.

![Zeigt eine komplexe Zeichnung eines Polygons, das einen Berg anzeigt.](images/path-geo-leftmnt.png)

Um den linken Berg zu erstellen, ruft das Beispiel die [**ID2D1Factory:: kreatepathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) -Methode auf, um eine [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)zu erstellen.


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



Im Beispiel wird dann die [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) -Methode verwendet, um eine Geometry-Senke von einem [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) abzurufen und in der *psink* -Variablen zu speichern.


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



Im Beispiel wird dann [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure)aufgerufen, wobei die [**D2D1 \_ Figure \_ Begin \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) Fill-Funktion übergeben wird, die angibt, dass diese Abbildung ausgefüllt ist. Anschließend werden [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines)aufgerufen und ein Array von [**D2D1 \_ Point \_ 2F**](d2d1-point-2f.md) -Punkten, (267, 177), (236, 192), (212, 160), (156, 255) und (346, 255) übergeben.

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



### <a name="create-a-path-geometry-for-the-right-mountain"></a>Erstellen einer Pfad Geometrie für den rechten Berg

Im Beispiel wird dann eine weitere Pfad Geometrie für den rechten Berg mit Punkten (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) und (575, 263) erstellt. Die folgende Abbildung zeigt, wie der Rechte Berg angezeigt wird.

![Abbildung eines Polygons, das einen Berg anzeigt](images/path-geo-rightmnt.png)

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



### <a name="create-a-path-geometry-for-the-sun"></a>Erstellen einer Pfad Geometrie für die Sun

Das Beispiel füllt dann eine andere Pfad Geometrie für die Sun, wie in der folgenden Abbildung dargestellt.

![Abbildung einer Bogen-und Bézier-Kurven, die die Sonne zeigen](images/path-geo-sun.png)

Zu diesem Zweck erstellt die Pfad Geometrie eine Senke und fügt eine Abbildung für den Bogen und eine Abbildung für jede Fackel der Senke hinzu. Durch Wiederholen der Sequenz von [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), der Add-Methode (z. b. [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) und [**endfigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure)werden der Senke mehrere Abbildungen hinzugefügt.

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



### <a name="create-a-path-geometry-for-the-river"></a>Erstellen einer Pfad Geometrie für den Fluss

Im Beispiel wird dann ein weiterer Geometry-Pfad für den Fluss erstellt, der Bezier-Kurven enthält. In der folgenden Abbildung wird gezeigt, wie der Fluss angezeigt wird.

![Abbildung der Bézier-Kurven, die einen Fluss anzeigen](images/path-geo-river.png)

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



### <a name="render-the-path-geometries-onto-the-display"></a>Rendering der Pfadgeometrien auf der Anzeige

Der folgende Code zeigt, wie die aufgefüllten Pfadgeometrien in der Anzeige dargestellt werden. Zuerst wird die Sun-Geometrie gezeichnet und gezeichnet, als nächstes die linke Mountain-Geometrie, dann die flussgeometrie und schließlich die Rechte Mountain-Geometrie.


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



Im Beispiel wird die folgende Abbildung ausgegeben.

![Darstellung eines Flusses, Gebirges und der Sonne mithilfe von Pfadgeometrien](images/path-geo-mnts.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)
</dt> <dt>

[Übersicht über Geometrien](direct2d-geometries-overview.md)
</dt> </dl>

 

 