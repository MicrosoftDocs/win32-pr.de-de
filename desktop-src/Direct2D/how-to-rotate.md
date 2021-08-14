---
title: Drehen eines Objekts
description: Zeigt, wie ein Objekt gedreht wird.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babc84c08af759d8484c8ba85db40780f68570d93a0a8b9442e93b960ecac39c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003530"
---
# <a name="how-to-rotate-an-object"></a>Drehen eines Objekts

In diesem Thema wird beschrieben, wie ein Objekt um einen angegebenen Punkt gedreht wird. Um ein Objekt zu drehen, rufen Sie [**die Matrix3x2F::Rotation-Methode**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) auf. Diese Methode verwendet zwei Parameter: den angegebenen Winkel und den Mittelpunkt. Der Winkel ist ein Drehwinkel im Uhrzeigersinn in Grad, und der Mittelpunkt ist der Punkt, um den sich das Objekt dreht. Der Mittelpunkt wird im Koordinatensystem des objekts ausgedrückt, das transformiert wird.

Der folgende Code rotiert z. B. um 45 Grad im Uhrzeigersinn um die Mitte des Quadrats.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 301.5f, 498.0f, 361.5f);

    // Draw the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the rotation transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45.0f,
            D2D1::Point2F(468.0f, 331.5f))
        );

    // Fill the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the transformed rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



Die folgende Abbildung zeigt den Effekt der Anwendung der vorherigen Drehungstransformation auf das Quadrat. Das ursprüngliche Quadrat ist eine gepunktete Kontur, und das gedrehte Quadrat ist ein solider Umriss.

![Abbildung eines quadratischen, um 45 Grad um 45 Grad gedrehten Quadrats um die Mitte des ursprünglichen Quadrats](images/rotate-ovw.png)

Die folgende Abbildung zeigt den Effekt der Drehung um denselben Winkel um einen anderen Mittelpunkt. Beachten Sie, dass sich die gedrehten Objekte relativ zum Original an unterschiedlichen Positionen befinden. Das links umrissene Quadrat ist das Ergebnis der Drehung um die Mitte des ursprünglichen Quadrats, und das recht umrissene Quadrat ist das Ergebnis der Drehung um die linke obere Ecke des ursprünglichen Quadrats.

![Abbildung eines quadratischen, um 45 Grad um 45 Grad gedrehten Quadrats um einen anderen Mittelpunkt](images/translate-rotationcompare.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> </dl>

 

 