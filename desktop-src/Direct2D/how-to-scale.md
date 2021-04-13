---
title: Skalieren eines Objekts
description: Zeigt, wie ein Objekt skaliert wird.
ms.assetid: 3da749e2-50d5-4f4e-9ccd-8c230efe3436
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9f46ae37197cb7cbfeb3f86588e1b5298cfc467
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473829"
---
# <a name="how-to-scale-an-object"></a>Skalieren eines Objekts

In diesem Thema wird beschrieben, wie ein Objekt mithilfe der [**Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse skaliert wird. Das Skalieren eines Objekts bedeutet, dass das Objekt größer oder kleiner wird. Sie können eine der beiden folgenden Methoden zum Skalieren eines Objekts aufzurufen.

-   **Matrix3x2F:: Scale (D2D1 \_ size \_ F scalefactor, D2D1 \_ Point \_ 2F Centerpoint)**
-   **Matrix3x2F:: Scale (float ScaleX, float ScaleY, D2D1 \_ Point \_ 2F Centerpoint)**

Die erste Methode speichert *ScaleX* und *ScaleY* als geordnetes Paar von Gleit Komma Werten in der [**D2D1 \_ size \_ F**](/windows/desktop/Direct2D/d2d1-size-f) -Struktur. Mit der zweiten Methode werden *ScaleX* und *ScaleY* als einzelne Parameter definiert.

Unabhängig davon, welche Methode Sie verwenden, müssen Sie sowohl *ScaleX* -als auch *ScaleY* -Faktoren angeben. Der *ScaleX* -Wert ist der Skalierungsfaktor in der x-Richtung. Beispielsweise wird das Objekt von einem *ScaleX* -Wert von 1,5 auf 150 Prozent entlang der x-Achse gestreckt. Ebenso ist der *Skalarwert der Skalierungs* Faktor in der y-Richtung. Beispielsweise verkleinert ein *ScaleY* -Wert von 0,5 die Höhe des Objekts um 50 Prozent entlang der y-Achse.

Um einen Punkt als Mittelpunkt des Skalierungs Vorgangs anzugeben, verwenden Sie den *CenterPoint* -Parameter. Standardmäßig wird ein Objekt über den Ursprung (0, 0) zentriert.

Im folgenden Beispielcode wird eine Skalierungs Transformation erstellt, um die Größe eines Quadrats auf 130% seiner ursprünglichen Größe zu erhöhen. Der Mittel *Punkt* wird auf die obere linke Ecke des ursprünglichen Quadrats festgelegt.


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



Die folgende Abbildung zeigt die Auswirkung der Anwendung der Skalierungs Transformation auf das Quadrat. Das ursprüngliche Quadrat ist eine gepunktete Gliederung, und das skalierte Quadrat ist ein voll solider Umriss.

![Abbildung der Quadrat Größe, die auf 130% der ursprünglichen Größe angepasst wurde](images/scale-ovw.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 