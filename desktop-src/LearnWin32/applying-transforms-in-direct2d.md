---
title: Anwenden von Transformationen in Direct2D
description: Anwenden von Transformationen in Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8edddbb3150f16428c56bd4c6da828c9b2ce594e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103727337"
---
# <a name="applying-transforms-in-direct2d"></a>Anwenden von Transformationen in Direct2D

Beim [Zeichnen mit Direct2D](drawing-with-direct2d.md)haben wir gesehen, dass die [**ID2D1RenderTarget:: FillEllipse**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) -Methode eine Ellipse zeichnet, die an der x-und y-Achse ausgerichtet ist. Angenommen, Sie möchten eine Ellipse, die an einem Winkel gekippt ist, zeichnen?

![ein Bild, das eine gekippte Ellipse anzeigt.](images/graphics16.png)

Mithilfe von Transformationen können Sie eine Form wie folgt ändern.

-   Drehung um einen Punkt.
-   Skalieren.
-   Übersetzung (Verschiebung in der X-oder Y-Richtung).
-   Schiefe (auch als *Schere* bezeichnet).

Eine Transformation ist eine mathematische Operation, bei der eine Gruppe von Punkten einem neuen Satz von Punkten zugeordnet wird. Das folgende Diagramm zeigt z. b. ein Dreieck, das um den Punkt P3 gedreht wurde. Nachdem die Drehung angewendet wurde, wird der Punkt P1 "P1" zugeordnet, der Punkt P2 wird P2 zugeordnet, und der Punkt P3 wird sich selbst zugeordnet.

![ein Diagramm, das die Drehung um einen Punkt zeigt.](images/graphics17.png)

Transformationen werden mithilfe von Matrizen implementiert. Allerdings müssen Sie die Mathematik von Matrizen nicht verstehen, um Sie zu verwenden. Weitere Informationen über die mathematische Informationen finden Sie unter [Anhang: Matrix Transformationen](appendix--matrix-transforms.md).

Um eine Transformation in Direct2D anzuwenden, müssen Sie die [**ID2D1RenderTarget:: setTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) -Methode aufrufen. Diese Methode nimmt eine [**D2D1 \_ Matrix \_ 3x2 \_ F-**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) Struktur an, die die Transformation definiert. Sie können diese Struktur initialisieren, indem Sie Methoden für die [**D2D1:: Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse aufrufen. Diese Klasse enthält statische Methoden, die eine Matrix für jede Art von Transformation zurückgeben:

-   [**Matrix3x2F:: Rotation**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F:: Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F:: Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F:: schiefe**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Mit dem folgenden Code wird z. b. eine 20-Grad-Drehung um den Punkt (100, 100) angewendet.


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

Die Transformation wird auf alle späteren Zeichnungsvorgänge angewendet, bis Sie [**setTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) erneut aufrufen. Zum Entfernen der aktuellen Transformation aufrufen Sie **setTransform** mit der Identitätsmatrix. Um die Identitätsmatrix zu erstellen, rufen Sie die [**Matrix3x2F:: Identity**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) -Funktion auf.


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Zeichnen von Takt Händen

Wir setzen Transformationen ein, indem wir unser kreisprogramm in eine analoge Uhr umrechnen. Dies erreichen Sie, indem Sie Zeilen für die Hände hinzufügen.

![ein Screenshot des Programms zur analogen Uhr.](images/graphics18.png)

Anstatt die Koordinaten für die Linien zu berechnen, können wir den Winkel berechnen und dann eine Drehungs Transformation anwenden. Der folgende Code zeigt eine Funktion, die eine Uhr Hand zeichnet. Der *fangle* -Parameter gibt den Winkel der Hand in Grad an.

```C++
void Scene::DrawClockHand(float fHandLength, float fAngle, float fStrokeWidth)
{
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(fAngle, m_ellipse.point)
            );

    // endPoint defines one end of the hand.
    D2D_POINT_2F endPoint = D2D1::Point2F(
        m_ellipse.point.x,
        m_ellipse.point.y - (m_ellipse.radiusY * fHandLength)
        );

    // Draw a line from the center of the ellipse to endPoint.
    m_pRenderTarget->DrawLine(
        m_ellipse.point, endPoint, m_pStroke, fStrokeWidth);
}
```

Dieser Code zeichnet eine vertikale Linie, beginnend ab der Mitte der Uhr und endet am Punkt *Endpunkt*. Die Linie wird um den Mittelpunkt der Ellipse gedreht, indem eine Rotations Transformation angewendet wird. Der Mittelpunkt der Drehung ist der Mittelpunkt der Ellipse, der die Uhr darstellt.

![ein Diagramm, das die Drehung der Uhrzeitangabe anzeigt.](images/graphics19.png)

Der folgende Code zeigt, wie die gesamte Takt Fläche gezeichnet wird.

```C++
void Scene::RenderScene()
{
    m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::SkyBlue));

    m_pRenderTarget->FillEllipse(m_ellipse, m_pFill);
    m_pRenderTarget->DrawEllipse(m_ellipse, m_pStroke);

    // Draw hands
    SYSTEMTIME time;
    GetLocalTime(&time);

    // 60 minutes = 30 degrees, 1 minute = 0.5 degree
    const float fHourAngle = (360.0f / 12) * (time.wHour) + (time.wMinute * 0.5f);
    const float fMinuteAngle =(360.0f / 60) * (time.wMinute);

    DrawClockHand(0.6f,  fHourAngle,   6);
    DrawClockHand(0.85f, fMinuteAngle, 4);

    // Restore the identity transformation.
    m_pRenderTarget->SetTransform( D2D1::Matrix3x2F::Identity() );
}
```

Sie können das komplette Visual Studio-Projekt aus dem [Direct2D Clock-Beispiel](direct2d-clock-sample.md)herunterladen. (Nur zum Spaß fügt die Download Version ein radiales gradiant zum Takt Gesicht hinzu.)

## <a name="combining-transforms"></a>Kombinieren von Transformationen

Die vier grundlegenden Transformationen können kombiniert werden, indem zwei oder mehr Matrizen multipliziert werden. Der folgende Code kombiniert z. b. eine Drehung mit einer Übersetzung.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

Die [**Matrix3x2F**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse stellt [**Operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) für die Matrix Multiplikation bereit. Die Reihenfolge, in der Sie die Matrizen multiplizieren, ist wichtig. Das Festlegen einer Transformation (m × N) bedeutet "m zuerst anwenden, gefolgt von N". Hier sehen Sie beispielsweise die Drehung, gefolgt von der Übersetzung:

![ein Diagramm, das die Drehung anzeigt, gefolgt von der Übersetzung.](images/graphics20.png)

Dies ist der Code für diese Transformation:

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

Vergleichen Sie nun diese Transformation mit einer Transformation in umgekehrter Reihenfolge, Übersetzung und Drehung, gefolgt von der Drehung.

![ein Diagramm, das die Übersetzung anzeigt, gefolgt von der Drehung.](images/graphics21.png)

Die Drehung erfolgt um die Mitte des ursprünglichen Rechtecks. Dies ist der Code für diese Transformation.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Wie Sie sehen können, sind die Matrizen identisch, aber die Reihenfolge der Vorgänge hat sich geändert. Dies liegt daran, dass die Matrix Multiplikation nicht commutative ist: M × N ≠ N × M.

## <a name="next"></a>Nächste

[Anhang: Matrix Transformationen](appendix--matrix-transforms.md)