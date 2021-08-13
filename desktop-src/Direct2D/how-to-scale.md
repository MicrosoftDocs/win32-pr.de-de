---
title: Skalieren eines Objekts
description: Zeigt, wie ein Objekt skaliert wird.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d833ea44e4a38672729dd7647063e8ed9f8de3574d820a3db40d5a848064ef15
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259145"
---
# <a name="how-to-scale-an-object"></a>Skalieren eines Objekts

In diesem Thema wird beschrieben, wie ein Objekt mithilfe der [**Matrix3x2F-Klasse**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) skaliert wird. Das Skalieren eines Objekts bedeutet, dass das Objekt größer oder kleiner wird. Sie können eine der beiden folgenden Methoden aufrufen, um ein Objekt zu skalieren.

-   **Matrix3x2F::Scale(D2D1 \_ SIZE \_ F scalefactor, D2D1 \_ POINT \_ 2F centerpoint)**
-   **Matrix3x2F::Scale(float scalex, float scaley, D2D1 \_ POINT \_ 2F centerpoint)**

Die erste Methode speichert *scalex* und *scaley* als geordnetes Paar von Gleitkommawerten in der [**D2D1 \_ SIZE \_ F-Struktur.**](/windows/desktop/Direct2D/d2d1-size-f) Die zweite Methode definiert *scalex* und *scaley* als einzelne Parameter.

Unabhängig davon, welche Methode Sie verwenden, müssen Sie sowohl *Scalex-* als auch *Skalierungsfaktoren* angeben. Der *scalex-Wert* ist der Skalierungsfaktor in x-Richtung. Beispielsweise wird das Objekt mit einem *scalex-Wert* von 1,5 entlang der x-Achse auf 150 Prozent gestreckt. Auf ähnliche Weise ist der *Skalierungswert* der Skalierungsfaktor in y-Richtung. Beispielsweise verkleinert ein *skalierungswert* von 0,5 die Höhe des Objekts entlang der y-Achse um 50 Prozent.

Verwenden Sie den *Parameter centerpoint,* um einen Punkt als Mittelpunkt des Skalierungsvorgangs anzugeben. Standardmäßig wird ein Objekt um seinen Ursprung (0,0) zentriert.

Der folgende Beispielcode erstellt eine Skalierungstransformation, um die Größe eines Quadrats auf 130 % seiner ursprünglichen Größe zu erhöhen. Der *Mittelpunkt* ist auf die obere linke Ecke des ursprünglichen Quadrats festgelegt.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(438.0f, 80.5f, 498.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the scale transform to the render target.
    m_pRenderTarget->SetTransform(
        D2D1::Matrix3x2F::Scale(
            D2D1::Size(1.3f, 1.3f),
            D2D1::Point2F(438.0f, 80.5f))
        );

    // Paint the rectangle's interior.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);

```



Die folgende Abbildung zeigt die Auswirkungen der Anwendung der Skalierungstransformation auf das Quadrat. Das ursprüngliche Quadrat ist eine gepunktete Kontur, und das skalierte Quadrat ist ein solider Umriss.

![Abbildung der Quadratgröße auf 130 % der ursprünglichen Größe](images/scale-ovw.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 