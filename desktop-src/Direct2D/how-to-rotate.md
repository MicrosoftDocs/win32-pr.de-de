---
title: Drehen eines Objekts
description: Zeigt, wie ein Objekt gedreht wird.
ms.assetid: 468e29b6-941b-4cf8-8649-9e513326ccb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b69cd900a78ba4d81919df91b85fd97723172eba
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948938"
---
# <a name="how-to-rotate-an-object"></a>Drehen eines Objekts

In diesem Thema wird beschrieben, wie ein Objekt um einen angegebenen Punkt gedreht wird. Um ein Objekt zu drehen, nennen Sie die [**Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) -Methode. Diese Methode erfordert zwei Parameter, den angegebenen Winkel und den Mittelpunkt. Der Winkel ist ein Drehungs Winkel im Uhrzeigersinn in Grad, und der Mittelpunkt ist der Punkt, an dem sich das Objekt dreht. Der Mittelpunkt wird im Koordinatensystem des Objekts ausgedrückt, das transformiert wird.

Der folgende Code dreht z. b. einen quadratischen Uhrzeigersinn um 45 Grad um die Mitte des Quadrats.


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



Die folgende Abbildung zeigt die Auswirkung der Anwendung der vorangehenden Rotations Transformation auf das Quadrat. Das ursprüngliche Quadrat ist ein gepunkteter Umriss, und das gedrehte Quadrat ist ein voll solider Umriss.

![Abbildung eines Quadrats um 45 Grad im Uhrzeigersinn um die Mitte des ursprünglichen Quadrats gedreht](images/rotate-ovw.png)

In der folgenden Abbildung wird gezeigt, wie sich die Drehung mit dem gleichen Winkel an einem anderen Mittelpunkt dreht. Beachten Sie, dass sich die gedrehten Objekte in Relation zum ursprünglichen an verschiedenen Positionen befinden. Das linke eckige Quadrat ist das Ergebnis der Drehung über den Mittelpunkt des ursprünglichen Quadrats, und das Recht Umriss Quadrat ist das Ergebnis der Rotation der oberen linken Ecke des ursprünglichen Quadrats.

![Abbildung eines Quadrats um 45 Grad im Uhrzeigersinn um einen anderen Mittelpunkt gedreht](images/translate-rotationcompare.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> </dl>

 

 