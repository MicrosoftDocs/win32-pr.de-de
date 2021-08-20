---
title: Verzerren eines Objekts
description: Zeigt, wie ein Objekt verzerrt wird.
ms.assetid: bdc12ca3-eb0d-49ab-8ef7-f42f24fef7ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 849c292221a8b4503cdfd122e08b6f1b2521043b44732c33d851a86693853f2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003499"
---
# <a name="how-to-skew-an-object"></a>Verzerren eines Objekts

Zum Verzerren (oder Verzerren) eines Objekts bedeutet, dass ein Objekt um einen angegebenen Winkel von der x-Achse, der y-Achse oder beidem verzerrt wird. Wenn Sie beispielsweise ein Quadrat neigen, wird es zu einem Parallelogramm.

Die [**Matrix3x2F::Skew-Methode**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-skew) nimmt drei Parameter an:

-   *angleX:* Der Neigungswinkel der x-Achse, der von der y-Achse in Grad gegen den Uhrzeigersinn gemessen wird.
-   *angleY:* Der y-Achsenschiefewinkel, der von der x-Achse im Uhrzeigersinn in Grad gemessen wird.
-   *centerPoint:* Der Punkt, an dem die Schiefe ausgeführt wird.

Um die Auswirkung einer Schiefetransformation vorherzusagen, berücksichtigen Sie, dass *angleX* der Schiefewinkel ist, der in Grad gegen den Uhrzeigersinn von der y-Achse gemessen wird. Wenn *angleX* beispielsweise auf 30 festgelegt ist, verschieft das Objekt 30 Grad gegen den Uhrzeigersinn entlang der y-Achse um *centerPoint.* Die folgende Abbildung zeigt eine horizontale Quadratschiefe um 30 Grad um die linke obere Ecke des Quadrats.

![Abbildung einer quadratischen Schiefe um 30 Grad gegen den Uhrzeigersinn von der y-Achse](images/skewx.png)

Ebenso ist *angleY* ein Neigungswinkel, der im Uhrzeigersinn von der X-Achse in Grad gemessen wird. Wenn *angleY* beispielsweise auf 30 festgelegt ist, verschieft das Objekt 30 Grad im Uhrzeigersinn entlang der x-Achse um *den CenterPoint*. Die folgende Abbildung zeigt eine vertikale Quadratschiefe um 30 Grad um die obere linke Ecke des Quadrats.

![Abbildung einer quadratischen Schiefe um 30 Grad im Uhrzeigersinn von der x-Achse](images/skewy.png)

Wenn Sie sowohl *angleX* als auch *angleY* auf 30 Grad und *centerPoint* auf die obere linke Ecke des Quadrats festlegen, sehen Sie das folgende schiefe Quadrat (durchgezogen umrandet). Beachten Sie, dass das schiefe Quadrat um 30 Grad gegen den Uhrzeigersinn von der y-Achse und 30 Grad im Uhrzeigersinn von der X-Achse verzerrt wird.

![Abbildung einer quadratischen Schiefe um 30 Grad gegen den Uhrzeigersinn von der y-Achse und 30 Grad im Uhrzeigersinn von der x-Achse](images/skewxy.png)

Im folgenden Codebeispiel wird das Quadrat um 45 Grad horizontal um die obere linke Ecke des Quadrats verzerrt.


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



Die folgende Abbildung zeigt die Auswirkung der Anwendung der Verschiebungstransformation auf das Quadrat, wobei das ursprüngliche Quadrat eine gepunktete Kontur und das verzerrte Objekt (Parallelogramm) ein solider Umriss ist. Beachten Sie, dass der Neigungswinkel 45 Grad gegen den Uhrzeigersinn von der y-Achse entfernt ist.

![Abbildung einer quadratischen Schiefe um 45 Grad gegen den Uhrzeigersinn von der y-Achse](images/skew-ovw.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 