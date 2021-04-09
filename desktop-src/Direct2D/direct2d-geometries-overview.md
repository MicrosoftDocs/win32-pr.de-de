---
title: Übersicht über Geometrien
description: Beschreibt die Grundlagen von Direct2D Geometries,-Objekten, die Sie zum darstellen, bearbeiten und Analysieren von Formen verwenden können.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Direct2D, Übersicht über Geometrien
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: cb97b0737bfad391fb9ba2501793a970fcbd9886
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "103734569"
---
# <a name="geometries-overview"></a>Übersicht über Geometrien

In dieser Übersicht wird beschrieben, wie [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekte zum Definieren und Bearbeiten von 2D-Abbildungen erstellt und verwendet werden. Der Abschnitt ist wie folgt gegliedert.

## <a name="what-is-a-direct2d-geometry"></a>Was ist eine Direct2D-Geometrie?

Eine Direct2D-Geometrie ist ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt. Bei diesem Objekt kann es sich um eine einfache Geometrie ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)oder [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), eine Pfad Geometrie ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) oder eine zusammengesetzte Geometrie ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) und [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)) handeln.

Mit Direct2D Geometrien können Sie zweidimensionale Abbildungen beschreiben und viele Verwendungsmöglichkeiten anbieten, wie z. b. das Definieren von Treffer-/Testbereichen, Clip Bereichen und sogar Animations Pfaden.

Direct2D-Geometrien sind unveränderliche und geräteunabhängige Ressourcen, die von [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)erstellt werden. Im Allgemeinen sollten Sie Geometrien einmal erstellen und Sie für die Lebensdauer der Anwendung aufbewahren, oder bis Sie geändert werden müssen. Weitere Informationen zu geräteunabhängigen und geräteabhängigen Ressourcen finden Sie in der Übersicht über [Ressourcen](resources-and-resource-domains.md).

In den folgenden Abschnitten werden die verschiedenen Arten von Geometrien beschrieben.

## <a name="simple-geometries"></a>Einfache Geometrien

Einfache Geometrien schließen [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)-, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)-und [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) -Objekte ein und können verwendet werden, um grundlegende geometrische Abbildungen, wie Rechtecke, abgerundete Rechtecke, Kreise und Ellipsen, zu erstellen.

Verwenden Sie zum Erstellen einer einfachen Geometrie eine der [**ID2D1Factory:: Create<*geometrytype* ->Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Methoden. Diese Methoden erstellen ein Objekt vom angegebenen Typ. Um z. b. ein Rechteck zu erstellen, rufen Sie [**ID2D1Factory:: froaterectanglegeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))auf, das ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) -Objekt zurückgibt. um ein abgerundetes Rechteck zu erstellen, rufen Sie [**ID2D1Factory:: froateroundrechglegeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry))auf, das ein [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) -Objekt zurückgibt, usw.

Im folgenden Codebeispiel wird die [**Methode "**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) -Methode" (Methode) aufgerufen, wobei eine Ellipse-Struktur mit dem *Mittelpunkt* (100, 100), *x-Radius* und 100 und *y-Radius* an 50 übergeben wird. Anschließend ruft Sie [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)auf und übergibt die zurückgegebene Ellipse-Geometrie, einen Zeiger auf ein schwarzes [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)und eine Strichbreite von 5. Die folgende Abbildung zeigt die Ausgabe des Code Beispiels.

![Abbildung einer Ellipse](images/geometry-ovw-drawstep6.png)


```C++
ID2D1EllipseGeometry *m_pEllipseGeometry;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateEllipseGeometry(
        D2D1::Ellipse(D2D1::Point2F(100.f, 60.f), 100.f, 50.f),
        &m_pEllipseGeometry
        );
}
```




```C++
m_pRenderTarget->DrawGeometry(m_pEllipseGeometry, m_pBlackBrush, 5);
```



Verwenden Sie die [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Methode, um die Kontur der Geometrie zu zeichnen. Um das Innere zu zeichnen, verwenden Sie die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode.

## <a name="path-geometries"></a>Pfadgeometrien

Pfadgeometrien werden durch die [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Schnittstelle dargestellt. Diese Objekte können verwendet werden, um komplexe geometrische Abbildungen zu beschreiben, die aus Segmenten wie Arcs, Kurven und Linien bestehen. In der folgenden Abbildung wird eine Zeichnung gezeigt, die mit der Pfad Geometrie erstellt wurde.

![Darstellung eines Flusses, eines Gebirges und der Sonne](images/path-geo-mnts.png)

Weitere Informationen und Beispiele finden Sie in der [Übersicht über Pfadgeometrien](path-geometries-overview.md).

## <a name="composite-geometries"></a>Zusammengesetzte Geometrien

Eine zusammengesetzte Geometrie ist eine mit einem anderen Geometry-Objekt oder mit einer Transformation gruppierte Geometrie. Zusammengesetzte Geometrien schließen [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) -und [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) -Objekte ein.

### <a name="geometry-groups"></a>Geometrie Gruppen

Geometry-Gruppen stellen eine bequeme Möglichkeit dar, mehrere Geometrien gleichzeitig zu gruppieren, sodass alle Abbildungen verschiedener geometrischer Geometrien in eins verkettet werden. Um ein [**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) -Objekt zu erstellen, rufen Sie [**die Methode "**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) -Methode" für das [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Objekt auf, und übergeben Sie den *FillMode* -Wert mit möglichen Werten der alternativen (Alternativen) [**D2D1 \_ Fill \_ Mode \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) -Methode (Alternative) und **D2D1 Fill- \_ \_ Modus \_**, einem Array von Geometrie Objekten, das der Geometrie Gruppe hinzugefügt werden soll, und der Anzahl der Elemente in diesem Array.

Im folgenden Codebeispiel wird zunächst ein Array von Geometry-Objekten deklariert. Bei diesen Objekten handelt es sich um vier konzentrische Kreise mit den folgenden Radii-Objekten: 25, 50, 75 und 100. Aufrufen Sie anschließend [**die Datei**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) "" für das Objekt " [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ", und übergeben Sie den [**D2D1 Fill- \_ \_ Modus \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), ein Array von Geometry-Objekten, die der Geometrie Gruppe hinzugefügt werden sollen, und die Anzahl der Elemente in diesem Array.


```C++
ID2D1Geometry *ppGeometries[] =
{
    m_pEllipseGeometry1,
    m_pEllipseGeometry2,
    m_pEllipseGeometry3,
    m_pEllipseGeometry4
};

hr = m_pD2DFactory->CreateGeometryGroup(
    D2D1_FILL_MODE_ALTERNATE,
    ppGeometries,
    ARRAYSIZE(ppGeometries),
    &m_pGeoGroup_AlternateFill
    );

if (SUCCEEDED(hr))
{
    hr = m_pD2DFactory->CreateGeometryGroup(
        D2D1_FILL_MODE_WINDING,
        ppGeometries,
        ARRAYSIZE(ppGeometries),
        &m_pGeoGroup_WindingFill
        );
}
```

In der folgenden Abbildung werden die Ergebnisse des Renderings der beiden Gruppen Geometrien aus dem Beispiel gezeigt.

![Abbildung von zwei Sätzen von vier konzentrischen Kreisen, eine mit abwechselnden Ringen und eine mit allen Ringen gefüllt](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>Transformierte Geometrien

Es gibt mehrere Möglichkeiten, eine Geometrie zu transformieren. Mit der [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) -Methode eines Renderziels können Sie alle Elemente transformieren, die das Renderziel zeichnet, oder Sie können eine Transformation direkt einer Geometrie zuordnen, indem Sie mithilfe der Methode "| [**atetransformedgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) " eine [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))erstellen.

Die Methode, die Sie verwenden sollten, hängt von den gewünschten Auswirkungen ab. Wenn Sie das Renderziel zum Transformieren und anschließenden Rendern einer Geometrie verwenden, wirkt sich die Transformation auf alles über die Geometrie aus, einschließlich der Breite eines beliebigen Strichs, den Sie angewendet haben. Wenn Sie hingegen ein [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)verwenden, wirkt sich die Transformation nur auf die Koordinaten aus, die die Form beschreiben. Die Transformation wirkt sich nicht auf die Strichstärke aus, wenn die Geometrie gezeichnet wird.

> [!Note]  
> Ab Windows 8 wirkt sich die Welt Transformation nicht auf die Strichstärke von Strichen mit dem Typ [**\_ \_ \_ \_ Fixed**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)oder [**D2D1 \_ Stroke \_ Transform \_ Type \_ Hairline**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)aus. Sie sollten diese Transformations Typen verwenden, um transformier unabhängige Striche zu erzielen.

 

Im folgenden Beispiel wird ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)erstellt und dann gezeichnet, ohne es zu transformieren. Sie erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines Rechtecks](images/transformedgeometry2-step1.png)


```C++
hr = m_pD2DFactory->CreateRectangleGeometry(
    D2D1::RectF(150.f, 150.f, 200.f, 200.f),
    &m_pRectangleGeometry
    );
```




```C++
// Draw the untransformed rectangle geometry.
m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



Im nächsten Beispiel wird das Renderziel verwendet, um die Geometrie um den Faktor 3 zu skalieren, und dann gezeichnet. Die folgende Abbildung zeigt das Ergebnis des Zeichnens des Rechtecks ohne die Transformation und mit der Transformation. Beachten Sie, dass der Strich nach der Transformation dicker ist, auch wenn die Strichstärke 1 ist.

![Darstellung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit einem dickeren Strich](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



Im nächsten Beispiel wird die Methode " [**kreatetransformedgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) " verwendet, um die Geometrie mit dem Faktor 3 zu skalieren, und dann gezeichnet. Sie erzeugt die in der folgenden Abbildung gezeigte Ausgabe. Beachten Sie, dass, obwohl das Rechteck größer ist, der Strich nicht vergrößert wurde.

![Abbildung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit derselben Strichstärke](images/transformedgeometry2-step3.png)


```C++
 // Create a geometry that is a scaled version
 // of m_pRectangleGeometry.
 // The new geometry is scaled by a factory of 3
 // from the center of the geometry, (35, 35).

 hr = m_pD2DFactory->CreateTransformedGeometry(
     m_pRectangleGeometry,
     D2D1::Matrix3x2F::Scale(
         D2D1::SizeF(3.f, 3.f),
         D2D1::Point2F(175.f, 175.f)),
     &m_pTransformedGeometry
     );
```




```C++
// Replace the previous render target transform.
m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

// Draw the transformed geometry.
m_pRenderTarget->DrawGeometry(m_pTransformedGeometry, m_pBlackBrush, 1);
```



## <a name="geometries-as-masks"></a>Geometrien als Masken

Sie können ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt als geometrische Maske verwenden, wenn Sie die [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -Methode aufzurufen. Die geometrische Maske gibt den Bereich der Ebene an, der in das Renderziel zusammengesetzt wird. Weitere Informationen finden Sie im Abschnitt geometrische Masken der Übersicht über [Ebenen](direct2d-layers-overview.md).

## <a name="geometric-operations"></a>Geometrische Vorgänge

Die [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Schnittstelle stellt verschiedene geometrische Vorgänge bereit, mit denen Sie geometrische Abbildungen bearbeiten und messen können. Beispielsweise können Sie Sie zum Berechnen und zurückgeben ihrer Begrenzungen verwenden, vergleichen, um zu sehen, wie sich eine Geometrie räumlich mit einem anderen (nützlich für Treffer Tests), Berechnen der Bereiche und Längen und mehr eignet. In der folgenden Tabelle werden die gängigen geometrischen Vorgänge beschrieben.



| Vorgang                                                   | Methode                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kombinieren                                                     | [**Combinewithgeometry**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| Begrenzungen/erweiterte Begrenzungen/Abruf Begrenzungen, geänderte Regions Aktualisierung | [**Erweitert**](id2d1geometry-widen.md), [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds), [**getwidenedbounds**](id2d1geometry-getwidenedbounds.md)                             |
| Treffertests                                                 | [**Fillcontainspoint**](id2d1geometry-fillcontainspoint.md), [ **strokecontainspoint**](id2d1geometry-strokecontainspoint.md)                                             |
| Stroke                                                      | [**Strokecontainspoint**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| Vergleich                                                  | [**Comparewithgeometry**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| Vereinfachung (entfernt Bögen und quadratische Bezier-Kurven)   | [**Vereinfachen**](id2d1geometry-simplify.md)                                                                                                                                 |
| Mosaik                                                | [**& Nbsp;**](id2d1geometry-tessellate.md)                                                                                                                             |
| Gliederung (Schnittmenge entfernen)                               | [**Outline**](id2d1geometry-outline.md)                                                                                                                                   |
| Berechnen des Bereichs oder der Länge einer Geometrie                  | [**Computearea**](id2d1geometry-computearea.md), [**computelength**](id2d1geometry-computelength.md), [**computepointatlength**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> Ab Windows 8 können Sie die [**computepointandsegmentatlength**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) -Methode für den [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) verwenden, um den Bereich oder die Länge einer Geometrie zu berechnen.

 

### <a name="combining-geometries"></a>Kombinieren von Geometrien

Um eine Geometrie mit einer anderen zu kombinieren, nennen Sie die [**ID2D1Geometry:: combinewithgeometry**](id2d1geometry-combinewithgeometry.md) -Methode. Wenn Sie die Geometrien kombinieren, geben Sie eine der vier Möglichkeiten zum Durchführen des kombinierungsvorgangs an: [**D2D1 \_ Combine \_ Mode \_ Union**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Union), [**D2D1 \_ Combine \_ Mode \_ Intersect**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Intersect), [**D2D1 \_ Combine \_ Mode \_ Xor**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (XOR) und [**D2D1 \_ Combine \_ Mode \_ Exclude**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (Exclude). Im folgenden Codebeispiel werden zwei Kreise veranschaulicht, die mithilfe des Union-kombinierungsmodus kombiniert werden, wobei der erste Kreis den Mittelpunkt von (75, 75) und den RADIUS 50 hat und der zweite Kreis den Mittelpunkt von (125, 75) und den Radius von 50 hat.


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}


if (SUCCEEDED(hr))
{
    //
    // Use D2D1_COMBINE_MODE_UNION to combine the geometries.
    //
    hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometryUnion);

    if (SUCCEEDED(hr))
    {
        hr = m_pPathGeometryUnion->Open(&pGeometrySink);

        if (SUCCEEDED(hr))
        {
            hr = m_pCircleGeometry1->CombineWithGeometry(
                m_pCircleGeometry2,
                D2D1_COMBINE_MODE_UNION,
                NULL,
                NULL,
                pGeometrySink
                );
        }

        if (SUCCEEDED(hr))
        {
            hr = pGeometrySink->Close();
        }

        SafeRelease(&pGeometrySink);
    }
}
```



In der folgenden Abbildung werden zwei Kreise in Kombination mit einem kombinierungsmodus von Union gezeigt.

![Abbildung von zwei überlappenden Kreisen, kombiniert zu einer Union](images/combine-mode-union.png)

Abbildungen aller kombinierungsmodi finden Sie unter [**D2D1 \_ Combine \_ Mode Enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).

### <a name="widen"></a>Ausbreiten

Die [**Methode "**](id2d1geometry-widen.md) -Methode" generiert eine neue Geometrie, deren Füllung dem Überschreiben der vorhandenen Geometrie entspricht, und schreibt dann das Ergebnis in das angegebene [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) -Objekt. Im folgenden Codebeispiel wird [**geöffnet**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) für das [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Objekt aufgerufen. Wenn das **Öffnen** erfolgreich ist, wird die **Erweiterung** für das Geometry-Objekt aufgerufen.


```C++
ID2D1GeometrySink *pGeometrySink = NULL;
hr = pPathGeometry->Open(&pGeometrySink);
if (SUCCEEDED(hr))
{
    hr = pGeometry->Widen(
            strokeWidth,
            pIStrokeStyle,
            pWorldTransform,
            pGeometrySink
            );
```



### <a name="tessellate"></a>& Nbsp;

Die [**Mosaik Methode erstellt**](id2d1geometry-tessellate.md) eine Reihe von Dreiecken im Uhrzeigersinn, die die Geometrie abdecken, nachdem Sie mithilfe der angegebenen Matrix transformiert und mithilfe der angegebenen Toleranz vereinfacht wurde. Im folgenden Codebeispiel wird **Mosaik verwendet,** um eine Liste von Dreiecken zu erstellen, die *ppathgeometry* darstellen. Die Dreiecke werden in [**ID2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pmesh*, gespeichert und dann für die spätere Verwendung beim Rendern an den Klassenmember *m \_ pstrokemesh* übertragen.


```C++
ID2D1Mesh *pMesh = NULL;
hr = m_pRT->CreateMesh(&pMesh);
if (SUCCEEDED(hr))
{
    ID2D1TessellationSink *pSink = NULL;
    hr = pMesh->Open(&pSink);
    if (SUCCEEDED(hr))
    {
        hr = pPathGeometry->Tessellate(
                NULL, // world transform (already handled in Widen)
                pSink
                );
        if (SUCCEEDED(hr))
        {
            hr = pSink->Close();
            if (SUCCEEDED(hr))
            {
                SafeReplace(&m_pStrokeMesh, pMesh);
            }
        }
        pSink->Release();
    }
    pMesh->Release();
}
```



### <a name="fillcontainspoint-and-strokecontainspoint"></a>Fillcontainspoint und strokecontainspoint

Die [**fillcontainspoint**](id2d1geometry-fillcontainspoint.md) -Methode gibt an, ob der von der Geometrie gefüllte Bereich den angegebenen Punkt enthält. Mit dieser Methode können Sie Treffer Tests durchführen. Das folgende Codebeispiel ruft **fillcontainspoint** für ein [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) -Objekt auf und übergibt einen Punkt an (0,0) und eine [**Identitäts**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity) Matrix.


```C++
BOOL containsPoint1;
hr = m_pCircleGeometry1->FillContainsPoint(
    D2D1::Point2F(0,0),
    D2D1::Matrix3x2F::Identity(),
    &containsPoint1
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



Die [**strokecontainspoint**](id2d1geometry-strokecontainspoint.md) -Methode bestimmt, ob der Strich der Geometrie den angegebenen Punkt enthält. Mit dieser Methode können Sie Treffer Tests durchführen. Im folgenden Codebeispiel wird **strokecontainspoint** verwendet.


```C++
BOOL containsPoint;

hr = m_pCircleGeometry1->StrokeContainsPoint(
    D2D1::Point2F(0,0),
    10,     // stroke width
    NULL,   // stroke style
    NULL,   // world transform
    &containsPoint
    );

if (SUCCEEDED(hr))
{
    // Process containsPoint.
}
```



### <a name="simplify"></a>Vereinfachen von 

Die Methode " [**vereinfachen**](id2d1geometry-simplify.md) " entfernt Bögen und quadratische Bezier-Kurven aus einer angegebenen Geometrie. Daher enthält die resultierende Geometrie nur Zeilen und optional kubische Bezier-Kurven. Im folgenden Codebeispiel wird die Verwendung von **vereinfachen** , um eine Geometrie mit Bezier-Kurven in eine Geometrie umzuwandeln, die nur Liniensegmente enthält.


```C++
HRESULT D2DFlatten(
    ID2D1Geometry *pGeometry,
    float flatteningTolerance,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Simplify(
                    D2D1_GEOMETRY_SIMPLIFICATION_OPTION_LINES,
                    NULL, // world transform
                    flatteningTolerance,
                    pSink
                    );

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="computelength-and-computearea"></a>Computelength und computearea

Die [**computelength**](id2d1geometry-computelength.md) -Methode berechnet die Länge der angegebenen Geometrie, wenn für jedes Segment ein Rollback in eine Zeile durchgeführt wurde. Dies schließt das implizite schließende Segment ein, wenn die Geometrie geschlossen ist. Im folgenden Codebeispiel wird **computelength** verwendet, um die Länge eines angegebenen Kreises (**m \_ pCircleGeometry1**) zu berechnen.


```C++
float length;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeLength(
    D2D1::IdentityMatrix(),
    &length
    );

if (SUCCEEDED(hr))
{
    // Process the length of the geometry.
}
```



Die [**computearea**](id2d1geometry-computearea.md) -Methode berechnet den Bereich der angegebenen Geometrie. Im folgenden Codebeispiel wird **computearea** verwendet, um den Bereich eines angegebenen Kreises (**m \_ pCircleGeometry1**) zu berechnen.


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>Comparewithgeometry

Die [**comparewithgeometry**](id2d1geometry-comparewithgeometry.md) -Methode beschreibt die Schnittmenge zwischen der Geometrie, die diese Methode aufruft, und der angegebenen Geometrie. Die möglichen Werte für die Schnittmenge umfassen [**D2D1 \_ Geometry- \_ Beziehung \_ Disjoint**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) (Disjoint), **D2D1 \_ Geometry \_ Relation \_ ist \_** enthalten (ist enthalten), **D2D1 \_ Geometry- \_ Beziehung \_ enthält** (enthält) und **D2D1 Geometry- \_ \_ Beziehungs \_ Überschneidung** (überlappend). "Disjoint" bedeutet, dass sich zwei Geometrie Füllungen überhaupt nicht überschneiden. "ist enthalten" bedeutet, dass die Geometrie vollständig in der angegebenen Geometrie enthalten ist. "enthält" bedeutet, dass die Geometrie die angegebene Geometrie vollständig enthält und "Überlappend" bedeutet, dass sich die beiden Geometrien überlappen, aber keines der anderen enthält.

Im folgenden Codebeispiel wird gezeigt, wie zwei Kreise verglichen werden, die den gleichen RADIUS von 50 aufweisen, aber um 50 versetzt werden.


```C++
HRESULT hr = S_OK;
ID2D1GeometrySink *pGeometrySink = NULL;

// Create the first ellipse geometry to merge.
const D2D1_ELLIPSE circle1 = D2D1::Ellipse(
    D2D1::Point2F(75.0f, 75.0f),
    50.0f,
    50.0f
    );

hr = m_pD2DFactory->CreateEllipseGeometry(
    circle1,
    &m_pCircleGeometry1
    );

if (SUCCEEDED(hr))
{
    // Create the second ellipse geometry to merge.
    const D2D1_ELLIPSE circle2 = D2D1::Ellipse(
        D2D1::Point2F(125.0f, 75.0f),
        50.0f,
        50.0f
        );

    hr = m_pD2DFactory->CreateEllipseGeometry(circle2, &m_pCircleGeometry2);
}

```




```C++
D2D1_GEOMETRY_RELATION result = D2D1_GEOMETRY_RELATION_UNKNOWN;

// Compare circle1 with circle2
hr = m_pCircleGeometry1->CompareWithGeometry(
    m_pCircleGeometry2,
    D2D1::IdentityMatrix(),
    0.1f,
    &result
    );

if (SUCCEEDED(hr))
{
    static const WCHAR szGeometryRelation[] = L"Two circles overlap.";
    m_pRenderTarget->SetTransform(D2D1::IdentityMatrix());
    if (result == D2D1_GEOMETRY_RELATION_OVERLAP)
    {
        m_pRenderTarget->DrawText(
            szGeometryRelation,
            ARRAYSIZE(szGeometryRelation) - 1,
            m_pTextFormat,
            D2D1::RectF(25.0f, 160.0f, 200.0f, 300.0f),
            m_pTextBrush
            );
    }
}
```



### <a name="outline"></a>Outline

Die Gliederungs [**Methode berechnet die**](id2d1geometry-outline.md) Gliederung der Geometrie (eine Version der Geometrie, in der keine Abbildung sich selbst oder eine andere Abbildung überschneidet) und schreibt das Ergebnis in ein [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). Im folgenden Codebeispiel wird **Gliederung verwendet,** um eine äquivalente Geometrie ohne selbst Austausch Vorgänge zu erstellen. Sie verwendet die standardmäßige Vereinfachungs Toleranz.


```C++
HRESULT D2DOutline(
    ID2D1Geometry *pGeometry,
    ID2D1Geometry **ppGeometry
    )
{
    HRESULT hr;
    ID2D1Factory *pFactory = NULL;
    pGeometry->GetFactory(&pFactory);

    ID2D1PathGeometry *pPathGeometry = NULL;
    hr = pFactory->CreatePathGeometry(&pPathGeometry);

    if (SUCCEEDED(hr))
    {
        ID2D1GeometrySink *pSink = NULL;
        hr = pPathGeometry->Open(&pSink);

        if (SUCCEEDED(hr))
        {
            hr = pGeometry->Outline(NULL, pSink);

            if (SUCCEEDED(hr))
            {
                hr = pSink->Close();

                if (SUCCEEDED(hr))
                {
                    *ppGeometry = pPathGeometry;
                    (*ppGeometry)->AddRef();
                }
            }
            pSink->Release();
        }
        pPathGeometry->Release();
    }

    pFactory->Release();

    return hr;
}
```



### <a name="getbounds-and-getwidenedbounds"></a>GetBounds und getwidenedbounds

Die [**GetBounds**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) -Methode ruft die Begrenzungen der Geometrie ab. Im folgenden Codebeispiel wird **GetBounds** verwendet, um die Begrenzungen eines angegebenen Kreises (**m \_ pCircleGeometry1**) abzurufen.


```C++
D2D1_RECT_F bounds;

hr = m_pCircleGeometry1->GetBounds(
      D2D1::IdentityMatrix(),
      &bounds
     );

if (SUCCEEDED(hr))
{
    // Retrieve the bounds.
}
```



Die [**getwidenedbounds**](id2d1geometry-getwidenedbounds.md) -Methode ruft die Grenzen der Geometrie ab, nachdem Sie durch die angegebene Strichbreite und den angegebenen Stil erweitert und durch die angegebene Matrix transformiert wurde. Im folgenden Codebeispiel wird **getwidenedbounds** verwendet, um die Begrenzungen eines angegebenen Kreises (**m \_ pCircleGeometry1**) abzurufen, nachdem er um die angegebene Strichbreite erweitert wurde.


```C++
float dashes[] = {1.f, 1.f, 2.f, 3.f, 5.f};

m_pD2DFactory->CreateStrokeStyle(
    D2D1::StrokeStyleProperties(
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_FLAT,
        D2D1_CAP_STYLE_ROUND,
        D2D1_LINE_JOIN_ROUND,   // lineJoin
        10.f,   //miterLimit
        D2D1_DASH_STYLE_CUSTOM,
        0.f     //dashOffset
        ),
     dashes,
     ARRAYSIZE(dashes)-1,
     &m_pStrokeStyle
     );
```




```C++
D2D1_RECT_F bounds1;
hr = m_pCircleGeometry1->GetWidenedBounds(
      5.0,
      m_pStrokeStyle,
      D2D1::IdentityMatrix(),
      &bounds1
     );
if (SUCCEEDED(hr))
{
    // Retrieve the widened bounds.
}
```



### <a name="computepointatlength"></a>Computepointatlength

Die [**computepointatlength**](id2d1geometry-computepointatlength.md) -Methode berechnet den Punkt und den Tangenten Vektor in der angegebenen Entfernung entlang der Geometrie. Im folgenden Codebeispiel wird **computepointatlength** verwendet.


```C++
D2D1_POINT_2F point;
D2D1_POINT_2F tangent;

hr = m_pCircleGeometry1->ComputePointAtLength(
    10, 
    NULL, 
    &point, 
    &tangent); 
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Pfadgeometrien](path-geometries-overview.md)
</dt> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 