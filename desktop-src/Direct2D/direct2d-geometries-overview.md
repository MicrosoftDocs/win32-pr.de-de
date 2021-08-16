---
title: Übersicht über Geometrien
description: Beschreibt die Grundlagen von Direct2D-Geometrien, Objekten, die Sie zum Darstellen, Bearbeiten und Analysieren von Formen verwenden können.
ms.assetid: f5870d4b-dd30-4034-884e-1c398a6865c6
keywords:
- Übersicht über Direct2D, Geometrien
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: d3f8cd7420325fd876897d538ea9e01a5c0adb64b2d0c55437514773904d6013
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825842"
---
# <a name="geometries-overview"></a>Übersicht über Geometrien

In dieser Übersicht wird beschrieben, wie [**Sie ID2D1Geometry-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) erstellen und verwenden, um 2D-Abbildungen zu definieren und zu bearbeiten. Der Abschnitt ist wie folgt gegliedert.

## <a name="what-is-a-direct2d-geometry"></a>Was ist eine Direct2D-Geometrie?

Eine Direct2D-Geometrie ist ein [**ID2D1Geometry-Objekt.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) Dieses Objekt kann eine einfache Geometrie ([**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry), [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)oder [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry)), eine Pfadgeometrie ([**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry)) oder eine zusammengesetzte Geometrie ([**ID2D1GeometryGroup**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) und [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)) sein.

Direct2D-Geometrien ermöglichen es Ihnen, zweidimensionale Abbildungen zu beschreiben und viele Verwendungsmöglichkeiten zu bieten, z. B. das Definieren von Treffertestbereichen, Clipbereichen und sogar Animationspfaden.

Direct2D-Geometrien sind unveränderliche und geräteunabhängige Ressourcen, die von [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)erstellt werden. Im Allgemeinen sollten Sie Geometrien einmal erstellen und für die Lebensdauer der Anwendung oder bis zu deren Änderung beibehalten. Weitere Informationen zu geräteunabhängigen und geräteabhängigen Ressourcen finden Sie in der [Ressourcenübersicht.](resources-and-resource-domains.md)

In den folgenden Abschnitten werden die verschiedenen Arten von Geometrien beschrieben.

## <a name="simple-geometries"></a>Einfache Geometrien

Einfache Geometrien umfassen DIE Objekte [**ID2D1RectangleGeometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry)und [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) und können zum Erstellen grundlegender geometrischer Abbildungen wie Rechtecke, abgerundete Rechtecke, Kreise und Ellipsen verwendet werden.

Verwenden Sie zum Erstellen einer einfachen Geometrie eine der [**Methoden ID2D1Factory::Create<*geometryType*>Geometry.**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) Diese Methoden erstellen ein Objekt des angegebenen Typs. Um beispielsweise ein Rechteck zu erstellen, rufen [**Sie ID2D1Factory::CreateRectangleGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createrectanglegeometry(constd2d1_rect_f_id2d1rectanglegeometry))auf, das ein [**ID2D1RectangleGeometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) zurückgibt. Um ein abgerundetes Rechteck zu erstellen, rufen [**Sie ID2D1Factory::CreateRoundedRectangleGeometry**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createroundedrectanglegeometry(constd2d1_rounded_rect__id2d1roundedrectanglegeometry))auf, das ein [**ID2D1RoundedRectangleGeometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) zurückgibt usw.

Das folgende Codebeispiel ruft die [**CreateEllipseGeometry-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createellipsegeometry(constd2d1_ellipse__id2d1ellipsegeometry)) auf und übergibt eine Ellipse-Struktur, wobei der *Mittelpunkt* auf (100, 100), *x-radius* auf 100 und *y-radius* auf 50 festgelegt ist. Anschließend ruft sie [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry)auf und übergibt die zurückgegebene Ellipsegeometrie, einen Zeiger auf einen schwarzen [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)und eine Strichbreite von 5. Die folgende Abbildung zeigt die Ausgabe des Codebeispiels.

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



Verwenden Sie die [**DrawGeometry-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) um die Kontur einer beliebigen Geometrie zu zeichnen. Verwenden Sie zum Zeichnen des Inneren die [**FillGeometry-Methode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)

## <a name="path-geometries"></a>Pfadgeometrien

Pfadgeometrien werden durch die [**ID2D1PathGeometry-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) dargestellt. Diese Objekte können verwendet werden, um komplexe geometrische Abbildungen zu beschreiben, die aus Segmenten wie Bogen, Kurven und Linien bestehen. Die folgende Abbildung zeigt eine Zeichnung, die mithilfe der Pfadgeometrie erstellt wurde.

![Abbildung eines Flusses, eines Flusses, eines Flusses und der Sonnenwelt](images/path-geo-mnts.png)

Weitere Informationen und Beispiele finden Sie unter [Übersicht über Pfadgeometrien.](path-geometries-overview.md)

## <a name="composite-geometries"></a>Zusammengesetzte Geometrien

Eine zusammengesetzte Geometrie ist eine Geometrie, die gruppiert oder mit einem anderen geometry-Objekt oder mit einer Transformation kombiniert wird. Zusammengesetzte Geometrien umfassen [**ID2D1TransformedGeometry-**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry) und [**ID2D1GeometryGroup-Objekte.**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup)

### <a name="geometry-groups"></a>Geometriegruppen

Geometriegruppen sind eine praktische Möglichkeit, mehrere Geometrien gleichzeitig zu gruppieren, sodass alle Abbildungen mehrerer unterschiedlicher Geometrien zu einer verkettet werden. Um ein [**ID2D1GeometryGroup-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrygroup) zu erstellen, rufen Sie die [**CreateGeometryGroup-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) für das [**ID2D1Factory-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) auf. Übergeben Sie dabei *fillMode* mit möglichen Werten von [**D2D1 \_ FILL MODE \_ \_ ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode) (alternate) und **D2D1 \_ FILL MODE \_ \_ WINDING,** einem Array von geometry-Objekten, die der Geometriegruppe hinzugefügt werden sollen, und der Anzahl der Elemente in diesem Array.

Im folgenden Codebeispiel wird zunächst ein Array von geometry-Objekten deklariert. Diese Objekte sind vier konzentrische Kreise mit den folgenden Radien: 25, 50, 75 und 100. Rufen Sie dann [**createGeometryGroup**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-creategeometrygroup) für das [**ID2D1Factory-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) auf, und übergeben Sie [**D2D1 \_ FILL MODE \_ \_ ALTERNATE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_fill_mode), ein Array von geometry-Objekten, die der geometry-Gruppe hinzugefügt werden sollen, und die Anzahl der Elemente in diesem Array.


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

Die folgende Abbildung zeigt die Ergebnisse des Renderns der beiden Gruppengeometrien aus dem Beispiel.

![Abbildung von zwei Gruppen von vier konzentrischen Kreisen, eines mit gefüllten abwechselnden Ringen und eines mit allen gefüllten Ringen](images/create-geometry-group.png)

### <a name="transformed-geometries"></a>Transformierte Geometrien

Es gibt mehrere Möglichkeiten, eine Geometrie zu transformieren. Sie können die [**SetTransform-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) eines Renderziels verwenden, um alles zu transformieren, was das Renderziel zeichnet, oder Sie können eine Transformation direkt einer Geometrie zuordnen, indem Sie die [**CreateTransformedGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f_id2d1transformedgeometry)) verwenden, um eine [**ID2D1TransformedGeometry**](/previous-versions/windows/desktop/legacy/dd371304(v=vs.85))zu erstellen.

Welche Methode Sie verwenden sollten, hängt von der gewünschten Auswirkung ab. Wenn Sie das Renderziel verwenden, um eine Geometrie zu transformieren und dann zu rendern, wirkt sich die Transformation auf alles über die Geometrie aus, einschließlich der Breite eines beliebigen Strichs, den Sie angewendet haben. Wenn Sie dagegen eine [**ID2D1TransformedGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1transformedgeometry)verwenden, wirkt sich die Transformation nur auf die Koordinaten aus, die die Form beschreiben. Die Transformation wirkt sich nicht auf die Strichstärke aus, wenn die Geometrie gezeichnet wird.

> [!Note]  
> Ab Windows 8 wirkt sich die Welttransformation nicht auf die Strichstärke von Strichen mit [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ FIXED**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)oder [**D2D1 \_ STROKE TRANSFORM TYPE \_ \_ \_ HAIRLINE**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_stroke_transform_type)aus. Sie sollten diese Transformationstypen verwenden, um transformationsunabhängige Striche zu erzielen.

 

Das folgende Beispiel erstellt eine [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry)und zeichnet sie dann, ohne sie zu transformieren. Sie erzeugt die ausgabe, die in der folgenden Abbildung dargestellt wird.

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



Im nächsten Beispiel wird das Renderziel verwendet, um die Geometrie um den Faktor 3 zu skalieren und dann zu zeichnen. Die folgende Abbildung zeigt das Ergebnis des Zeichnens des Rechtecks ohne die Transformation und mit der Transformation. Beachten Sie, dass der Strich nach der Transformation breiter ist, obwohl die Strichstärke 1 ist.

![Abbildung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit einem breiteren Strich](images/transformedgeometry2-step2.png)


```C++
// Transform the render target, then draw the rectangle geometry again.
m_pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Scale(
        D2D1::SizeF(3.f, 3.f),
        D2D1::Point2F(175.f, 175.f))
    );

m_pRenderTarget->DrawGeometry(m_pRectangleGeometry, m_pBlackBrush, 1);
```



Im nächsten Beispiel wird die [**CreateTransformedGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createtransformedgeometry(id2d1geometry_constd2d1_matrix_3x2_f__id2d1transformedgeometry)) verwendet, um die Geometrie um den Faktor 3 zu skalieren und dann zu zeichnen. Sie erzeugt die ausgabe, die in der folgenden Abbildung dargestellt wird. Beachten Sie, dass das Rechteck zwar größer ist, aber sein Strich nicht erhöht wurde.

![Abbildung eines kleineren Rechtecks innerhalb eines größeren Rechtecks mit der gleichen Strichstärke](images/transformedgeometry2-step3.png)


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

Sie können ein [**ID2D1Geometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) als geometrische Maske verwenden, wenn Sie die [**PushLayer-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) aufrufen. Die geometrische Maske gibt den Bereich der Ebene an, die in das Renderziel zusammengesetzt wird. Weitere Informationen finden Sie im Abschnitt Geometrische Masken der [Übersicht über Ebenen.](direct2d-layers-overview.md)

## <a name="geometric-operations"></a>Geometrische Vorgänge

Die [**ID2D1Geometry-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) stellt mehrere geometrische Vorgänge bereit, mit denen Sie geometrische Abbildungen bearbeiten und messen können. Sie können sie beispielsweise verwenden, um ihre Grenzen zu berechnen und zurückzugeben, zu vergleichen, um zu sehen, wie eine Geometrie räumlich mit einer anderen verbunden ist (nützlich für Treffertests), berechnen die Bereiche und Längen und vieles mehr. In der folgenden Tabelle werden die allgemeinen geometrischen Vorgänge beschrieben.



| Vorgang                                                   | Methode                                                                                                                                                                     |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Kombinieren                                                     | [**CombineWithGeometry**](id2d1geometry-combinewithgeometry.md)                                                                                                           |
| Bounds/Widened Bounds/Retrieve Bounds, Dirty Region update | [**Widen,**](id2d1geometry-widen.md) [**GetBounds,**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) [**GetWidenedBounds**](id2d1geometry-getwidenedbounds.md)                             |
| Treffertests                                                 | [**FillContainsPoint,**](id2d1geometry-fillcontainspoint.md) [ **StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                             |
| Stroke                                                      | [**StrokeContainsPoint**](id2d1geometry-strokecontainspoint.md)                                                                                                           |
| Vergleich                                                  | [**CompareWithGeometry**](id2d1geometry-comparewithgeometry.md)                                                                                                           |
| Vereinfachung (entfernt Bogen und quadratische Bézierkurven)   | [**Vereinfachen**](id2d1geometry-simplify.md)                                                                                                                                 |
| Mosaik                                                | [**Mosaik**](id2d1geometry-tessellate.md)                                                                                                                             |
| Kontur (Schnittmenge entfernen)                               | [**Kontur**](id2d1geometry-outline.md)                                                                                                                                   |
| Berechnen des Bereichs oder der Länge einer Geometrie                  | [**ComputeArea,**](id2d1geometry-computearea.md) [**ComputeLength,**](id2d1geometry-computelength.md) [**ComputePointAtLength**](id2d1geometry-computepointatlength.md) |



 

> [!Note]  
> Ab Windows 8 können Sie die [**ComputePointAndSegmentAtLength-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1pathgeometry1-computepointandsegmentatlength(float_uint32_constd2d1_matrix_3x2_f_float_d2d1_point_description)) für [**ID2D1PathGeometry1**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1pathgeometry1) verwenden, um den Bereich oder die Länge einer Geometrie zu berechnen.

 

### <a name="combining-geometries"></a>Kombinieren von Geometrien

Um eine Geometrie mit einer anderen zu kombinieren, rufen Sie die [**ID2D1Geometry::CombineWithGeometry-Methode**](id2d1geometry-combinewithgeometry.md) auf. Wenn Sie die Geometrien kombinieren, geben Sie eine der vier Methoden zum Ausführen des Kombinationsvorgangs an: [**D2D1 \_ COMBINE \_ MODE \_ UNION**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (union), [**D2D1 \_ COMBINE MODE \_ \_ INTERSECT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (überschneiden), [**D2D1 \_ COMBINE MODE XOR \_ \_ (xor)**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) und [**D2D1 \_ COMBINE MODE \_ \_ EXCLUDE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode) (exclude). Das folgende Codebeispiel zeigt zwei Kreise, die mithilfe des Vereinigungs-Kombinationsmodus kombiniert werden, wobei der erste Kreis den Mittelpunkt von (75, 75) und den Radius von 50 und der zweite Kreis den Mittelpunkt von (125, 75) und den Radius von 50 hat.


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



Die folgende Abbildung zeigt zwei Kreise in Kombination mit einem Kombinationsmodus der Union.

![Abbildung von zwei überlappenden Kreisen, die zu einer Union kombiniert werden](images/combine-mode-union.png)

Abbildungen aller Kombinationsmodi finden Sie unter der [**D2D1 \_ COMBINE \_ MODE-Enumeration**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_combine_mode).

### <a name="widen"></a>Erweitern

Die [**Widen-Methode**](id2d1geometry-widen.md) generiert eine neue Geometrie, deren Füllung dem Füllen der vorhandenen Geometrie entspricht, und schreibt das Ergebnis dann in das angegebene [**ID2D1SimplifiedGeometrySink-Objekt.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) Im folgenden Codebeispiel wird [**Open für**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) das [**ID2D1PathGeometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) aufruft. Wenn **Open** erfolgreich ist, ruft es **Widen für das** geometry-Objekt auf.


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



### <a name="tessellate"></a>Mosaik

Die [**Tessellate-Methode**](id2d1geometry-tessellate.md) erstellt einen Satz von dreieckigen Dreiecken im Uhrzeigersinn, die die Geometrie abdecken, nachdem sie mithilfe der angegebenen Matrix transformiert und mithilfe der angegebenen Toleranz abgeflachen wurde. Im folgenden Codebeispiel wird **Tessellate** verwendet, um eine Liste von Dreiecken zu erstellen, die *pPathGeometry darstellen.* Die Dreiecke werden in [**id2D1Mesh**](/windows/win32/api/d2d1/nn-d2d1-id2d1mesh), *pMesh* gespeichert und dann zur späteren Verwendung beim Rendering an den Klassen member *m \_ pStrokeMesh* übertragen.


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



### <a name="fillcontainspoint-and-strokecontainspoint"></a>FillContainsPoint und StrokeContainsPoint

Die [**FillContainsPoint-Methode**](id2d1geometry-fillcontainspoint.md) gibt an, ob der von der Geometrie ausgefüllte Bereich den angegebenen Punkt enthält. Sie können diese Methode für Treffertests verwenden. Das folgende Codebeispiel ruft **FillContainsPoint für** ein [**ID2D1EllipseGeometry-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) auf und überträgt einen Punkt bei (0,0) und eine [**Identitätsmatrix.**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-isidentity)


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



Die [**StrokeContainsPoint-Methode**](id2d1geometry-strokecontainspoint.md) bestimmt, ob der Strich der Geometrie den angegebenen Punkt enthält. Sie können diese Methode für Treffertests verwenden. Im folgenden Codebeispiel wird **StrokeContainsPoint verwendet.**


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

Die [**Simplify-Methode**](id2d1geometry-simplify.md) entfernt Bogen und quadratische Bézierkurven aus einer angegebenen Geometrie. Die resultierende Geometrie enthält also nur Linien und optional kubische Bézierkurven. Im folgenden Codebeispiel wird **Simplify** verwendet, um eine Geometrie mit Bézierkurven in eine Geometrie zu transformieren, die nur Liniensegmente enthält.


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



### <a name="computelength-and-computearea"></a>ComputeLength und ComputeArea

Die [**ComputeLength-Methode**](id2d1geometry-computelength.md) berechnet die Länge der angegebenen Geometrie, wenn jedes Segment in eine Linie entrollt wurde. Dies schließt das implizite schließende Segment ein, wenn die Geometrie geschlossen ist. Im folgenden Codebeispiel wird **ComputeLength** verwendet, um die Länge eines angegebenen Kreises (**m \_ pCircleGeometry1 ) zu berechnen.**


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



Die [**ComputeArea-Methode**](id2d1geometry-computearea.md) berechnet den Bereich der angegebenen Geometrie. Im folgenden Codebeispiel wird **ComputeArea** verwendet, um den Bereich eines angegebenen Kreises (**m \_ pCircleGeometry1 ) zu berechnen.**


```C++
float area;

// Compute the area of circle1
hr = m_pCircleGeometry1->ComputeArea(
    D2D1::IdentityMatrix(),
    &area
    );
```



### <a name="comparewithgeometry"></a>CompareWithGeometry

Die [**CompareWithGeometry-Methode**](id2d1geometry-comparewithgeometry.md) beschreibt die Schnittmenge zwischen der Geometrie, die diese Methode aufruft, und der angegebenen Geometrie. Zu den möglichen Werten für die Schnittmenge zählen [**D2D1 \_ GEOMETRY \_ RELATION \_ DISJOINT (disjoint),**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_geometry_relation) **D2D1 \_ GEOMETRY \_ RELATION IS \_ \_ CONTAINED** (enthalten), **D2D1 \_ GEOMETRY RELATION \_ \_ CONTAINS** (contains) und **D2D1 \_ GEOMETRY RELATION \_ \_ OVERLAP** (overlap). "disjoint" bedeutet, dass sich zwei Geometriefüllungen überhaupt nicht überschneiden. "is contained" bedeutet, dass die Geometrie vollständig in der angegebenen Geometrie enthalten ist. "contains" bedeutet, dass die Geometrie die angegebene Geometrie vollständig enthält, und "overlap" bedeutet, dass sich die beiden Geometrien überlappen, aber keines von beiden vollständig die andere enthält.

Das folgende Codebeispiel zeigt, wie zwei Kreise verglichen werden, die den gleichen Radius von 50 haben, aber um 50 versetzt sind.


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



### <a name="outline"></a>Kontur

Die [**Outline-Methode**](id2d1geometry-outline.md) berechnet die Kontur der Geometrie (eine Version der Geometrie, in der keine Abbildung sich selbst oder eine andere Abbildung überkreuzt) und schreibt das Ergebnis in eine [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink). Im folgenden Codebeispiel wird **Outline verwendet,** um eine entsprechende Geometrie ohne Selbstschnitte zu erstellen. Es wird die standardmäßige Flatteningtoleranz verwendet.


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



### <a name="getbounds-and-getwidenedbounds"></a>GetBounds und GetWidenedBounds

Die [**GetBounds-Methode**](/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1gdimetafile-getbounds) ruft die Begrenzungen der Geometrie ab. Im folgenden Codebeispiel wird **GetBounds verwendet,** um die Grenzen eines angegebenen Kreises abzurufen (**m \_ pCircleGeometry1**).


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



Die [**GetWidenedBounds-Methode**](id2d1geometry-getwidenedbounds.md) ruft die Begrenzungen der Geometrie ab, nachdem sie um die angegebene Strichbreite und den angegebenen Stil geweitet und von der angegebenen Matrix transformiert wurde. Im folgenden Codebeispiel wird **GetWidenedBounds** verwendet, um die Grenzen eines angegebenen Kreises (**m \_ pCircleGeometry1**) abzurufen, nachdem er um die angegebene Strichbreite geweitet wurde.


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



### <a name="computepointatlength"></a>ComputePointAtLength

Die [**ComputePointAtLength-Methode**](id2d1geometry-computepointatlength.md) berechnet den Punkt- und Tangensvektor im angegebenen Abstand entlang der Geometrie. Im folgenden Codebeispiel wird **ComputePointAtLength verwendet.**


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

 

 