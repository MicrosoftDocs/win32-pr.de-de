---
title: Vorgehensweise beim Verzerren eines Objekts
description: Zeigt, wie ein Objekt verzerrt wird.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691062e64d4255b1e2f7711b5ff700d72fd90063
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858407"
---
# <a name="how-to-skew-an-object"></a>Vorgehensweise beim Verzerren eines Objekts

Um ein Objekt zu neigen (oder zu scheren), bedeutet dies, dass ein Objekt um einen angegebenen Winkel von der x-Achse, der y-Achse oder beidem verzerrt werden soll. Wenn Sie beispielsweise ein Quadrat neigen, wird es zu einem Parallelogramm.

Die [**Matrix3x2F:: schräw**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) -Methode nimmt 3 Parameter an:

-   *AngleX*: der Neigungswinkel der x-Achse, der in Grad gegen den Uhrzeigersinn von der y-Achse aus gemessen wird.
-   *AngleY*: der Neigungswinkel der y-Achse, der in Grad im Uhrzeigersinn von der x-Achse aus gemessen wird.
-   *CenterPoint*: der Punkt, an dem die Schiefe ausgeführt wird.

Um die Auswirkung einer Neigungs Transformation vorherzusagen, sollten Sie Bedenken, dass *AngleX* der Neigungswinkel in Grad gegen den Uhrzeigersinn von der y-Achse aus gemessen wird. Wenn *AngleX* z. b. auf 30 festgelegt ist, wird das Objekt 30 Grad gegen den Uhrzeigersinn entlang der y-Achse um den Mittel *Punkt* gedreht. In der folgenden Abbildung wird eine eckige eckige Abweichung von 30 Grad in der oberen linken Ecke des Quadrats gezeigt.

![Abbildung einer quadratischen Verzerrung von 30 Grad gegen den Uhrzeigersinn von der y-Achse](images/skewx.png)

Ebenso ist *AngleY* ein Neigungswinkel, der in Grad im Uhrzeigersinn von der x-Achse aus gemessen wird. Wenn *AngleY* z. b. auf 30 festgelegt ist, wird das Objekt 30 Grad im Uhrzeigersinn entlang der x-Achse um den Mittel *Punkt* gerengt. In der folgenden Abbildung wird eine quadratische Breite von 30 Grad in der oberen linken Ecke des Quadrats gezeigt.

![Abbildung einer quadratischen Verzerrung um 30 Grad im Uhrzeigersinn von der x-Achse](images/skewy.png)

Wenn Sie " *AngleX* " und " *AngleY* " auf 30 Grad festgelegt haben und der Mittel *Punkt* auf die linke obere Ecke des Quadrats festgelegt ist, wird das folgende schräge Quadrat angezeigt (durch ein Vollformat dargestellt). Beachten Sie, dass das rechteckige Quadrat 30 Grad gegen den Uhrzeigersinn von der y-Achse und 30 Grad im Uhrzeigersinn von der x-Achse aus verzerrt wird.

![Abbildung einer quadratischen Verzerrung von 30 Grad gegen den Uhrzeigersinn von der y-Achse und 30 Grad im Uhrzeigersinn von der x-Achse](images/skewxy.png)

Im folgenden Codebeispiel wird die Quadrat-45 Grad horizontal um die obere linke Ecke des Quadrats bündig ausgerichtet.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 301.5f, 186.0f, 361.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the skew transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Skew(
            45.0f,
            0.0f,
            D2D1::Point2F(126.0f, 301.5f))
        );

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



In der folgenden Abbildung wird gezeigt, wie sich die Schiefe-Transformation auf das Quadrat auswirkt, wobei das ursprüngliche Quadrat ein gepunkteter Umriss und das schiefe Objekt (Parallelogram) ein voll Bild Umriss ist. Beachten Sie, dass der Neigungswinkel von der y-Achse aus 45 Grad gegen den Uhrzeigersinn liegt.

![Abbildung eines quadratischen verzerrt 45 Grad gegen den Uhrzeigersinn von der y-Achse](images/skew-ovw.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 