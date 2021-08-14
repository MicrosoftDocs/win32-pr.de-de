---
title: Anwenden von Transformationen in Direct2D
description: Anwenden von Transformationen in Direct2D
ms.assetid: 4b54dcfc-f915-4e4a-aa88-ee23c341c2a4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab83cb9a7981ada944de07e362c2f568889a84a4f90f2171150fbab948ab3a6f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118388490"
---
# <a name="applying-transforms-in-direct2d"></a>Anwenden von Transformationen in Direct2D

Beim [Zeichnen mit Direct2D](drawing-with-direct2d.md)haben wir gesehen, dass die [**ID2D1RenderTarget::FillEllipse-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) eine Ellipse zeichnet, die an den x- und y-Achsen ausgerichtet ist. Angenommen, Sie möchten eine Ellipse zeichnen, die in einem Winkel geneigt ist?

![Ein Bild, das eine geneigte Ellipse zeigt.](images/graphics16.png)

Mithilfe von Transformationen können Sie eine Form auf folgende Weise ändern.

-   Drehung um einen Punkt.
-   Skalieren.
-   Übersetzung (Verschiebung in X- oder Y-Richtung).
-   Schiefe (auch als *"Schubar"* bezeichnet).

Eine Transformation ist ein mathematischer Vorgang, bei dem eine Gruppe von Punkten einem neuen Satz von Punkten zugeordnet wird. Das folgende Diagramm zeigt beispielsweise ein Dreieck, das um den Punkt P3 gedreht wird. Nachdem die Drehung angewendet wurde, wird der Punkt P1 " zugeordnet, der Punkt P2 wird P2 zugeordnet, und der Punkt P3 wird sich selbst zugeordnet.

![Ein Diagramm, das die Drehung um einen Punkt zeigt.](images/graphics17.png)

Transformationen werden mithilfe von Matrizen implementiert. Sie müssen jedoch die Mathematik von Matrizen nicht verstehen, um sie verwenden zu können. Weitere Informationen zur Mathematik finden Sie unter [Anhang: Matrixtransformationen.](appendix--matrix-transforms.md)

Um eine Transformation in Direct2D anzuwenden, rufen Sie die [**ID2D1RenderTarget::SetTransform-Methode**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) auf. Diese Methode verwendet eine [**D2D1 \_ MATRIX \_ 3X2 \_ F-Struktur,**](/windows/desktop/Direct2D/d2d1-matrix-3x2-f) die die Transformation definiert. Sie können diese Struktur initialisieren, indem Sie Methoden für die [**D2D1::Matrix3x2F-Klasse**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) aufrufen. Diese Klasse enthält statische Methoden, die eine Matrix für jede Art von Transformation zurückgeben:

-   [**Matrix3x2F::Rotation**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation)
-   [**Matrix3x2F::Scale**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-scale(d2d1_size_f_d2d1_point_2f))
-   [**Matrix3x2F::Translation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f))
-   [**Matrix3x2F::Skew**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew)

Der folgende Code wendet beispielsweise eine Drehung um 20 Grad um den Punkt (100, 100) an.


```C++
pRenderTarget->SetTransform(
    D2D1::Matrix3x2F::Rotation(20, D2D1::Point2F(100,100)));
```

Die Transformation wird auf alle späteren Zeichnungsvorgänge angewendet, bis Sie [**SetTransform**](/windows/desktop/Direct2D/id2d1rendertarget-settransform) erneut aufrufen. Um die aktuelle Transformation zu entfernen, rufen **Sie SetTransform** mit der Identitätsmatrix auf. Um die Identitätsmatrix zu erstellen, rufen Sie die [**Matrix3x2F::Identity-Funktion**](/windows/desktop/api/d2d1helper/nf-d2d1helper-identitymatrix) auf.


```C++
pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
```

## <a name="drawing-clock-hands"></a>Zeichnen von Uhrzeigern

Lassen Sie uns Transformationen verwenden, indem wir unser Circle-Programm in eine analoge Uhr konvertieren. Dazu fügen wir Zeilen für die Hände hinzu.

![Ein Screenshot des analogen Uhrprogramms.](images/graphics18.png)

Anstatt die Koordinaten für die Linien zu berechnen, können wir den Winkel berechnen und dann eine Drehungstransformation anwenden. Der folgende Code zeigt eine Funktion, die eine Uhr hand zeichnet. Der *fAngle-Parameter* gibt den Winkel der Hand in Grad an.

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

Dieser Code zeichnet eine vertikale Linie, beginnend von der Mitte des Uhrzeigers bis zum *Punktendpunkt*. Die Linie wird um die Mitte der Ellipse gedreht, indem eine Drehtransformation angewendet wird. Der Mittelpunkt für die Drehung ist der Mittelpunkt der Ellipse, die das Uhr face bildet.

![Ein Diagramm, das die Drehung der Uhr zeigt.](images/graphics19.png)

Der folgende Code zeigt, wie das gesamte Uhr face gezeichnet wird.

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

Sie können das vollständige Visual Studio Projekt von [Direct2D Clock Sample](direct2d-clock-sample.md)herunterladen. (Aus Spaß fügt die Downloadversion dem Uhr face einen radialen Gradiant hinzu.)

## <a name="combining-transforms"></a>Kombinieren von Transformationen

Die vier grundlegenden Transformationen können kombiniert werden, indem zwei oder mehr Matrizen multipliziert werden. Der folgende Code kombiniert beispielsweise eine Drehung mit einer Übersetzung.

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(20);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(40, 10);

pRenderTarget->SetTransform(rot * trans);
```

Die [**Matrix3x2F-Klasse**](/windows/desktop/api/d2d1helper/nl-d2d1helper-matrix3x2f) stellt [**operator \* ()**](/windows/desktop/api/d2d1helper/nf-d2d1helper-matrix3x2f-operator-mult) für die Matrixmultiplikation bereit. Die Reihenfolge, in der Sie die Matrizen multiplizieren, ist wichtig. Das Festlegen einer Transformation (M × N) bedeutet "Zuerst M anwenden, gefolgt von N". Hier sehen Sie beispielsweise die Drehung gefolgt von der Übersetzung:

![Ein Diagramm, das die Drehung gefolgt von der Übersetzung zeigt.](images/graphics20.png)

Hier ist der Code für diese Transformation:

```C++
const D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
const D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(rot * trans);
```

Vergleichen Sie diese Transformation nun mit einer Transformation in umgekehrter Reihenfolge, der Übersetzung gefolgt von der Drehung.

![Ein Diagramm, das die Übersetzung gefolgt von der Drehung zeigt.](images/graphics21.png)

Die Drehung erfolgt um die Mitte des ursprünglichen Rechtecks. Hier ist der Code für diese Transformation.

```C++
D2D1::Matrix3x2F rot = D2D1::Matrix3x2F::Rotation(45, center);
D2D1::Matrix3x2F trans = D2D1::Matrix3x2F::Translation(x, 0);
pRenderTarget->SetTransform(trans * rot);
```

Wie Sie sehen können, sind die Matrizen identisch, aber die Reihenfolge der Vorgänge hat sich geändert. Dies liegt daran, dass die Matrixmultiplikation nicht kommutativ ist: M × N ≠ N × M.

## <a name="next"></a>Nächste

[Anhang: Matrixtransformationen](appendix--matrix-transforms.md)