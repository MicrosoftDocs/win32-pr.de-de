---
title: Übersetzen eines Objekts
description: Zeigt, wie ein-Objekt übersetzt wird.
ms.assetid: 0fc48801-de14-4398-816d-6e7ddf4ffdd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab7921e6de3286f3e1b5cf7e3da8571815848d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316088"
---
# <a name="how-to-translate-an-object"></a>Übersetzen eines Objekts

Wenn Sie ein 2D-Objekt übersetzen möchten, verschieben Sie das Objekt auf die x-Achse, die y-Achse oder beides. Sie können eine der beiden folgenden Methoden zum Erstellen einer Übersetzungs Transformation aufruft.

-   [**Translation (D2D1 \_ size \_ F size)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(d2d1_size_f)): nimmt ein geordnetes Paar an, das den Abstand auf der x-Achse und der y-Achse definiert.
-   [**Übersetzung (float x, float y)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-translation(float_float)): übernimmt den Abstand, der entlang der x-Achse übersetzt werden soll, und die Distanz, die auf der y-Achse übersetzt werden soll.

Der folgende Code erstellt eine Transformationsmatrix für die Konvertierung, die die Quadrat 20 Einheiten entlang der x-Achse nach rechts und 10 Einheiten entlang der y-Achse nach unten verschiebt.


```C++
    // Create a rectangle.
    D2D1_RECT_F rectangle = D2D1::Rect(126.0f, 80.5f, 186.0f, 140.5f);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(
        rectangle,
        m_pOriginalShapeBrush,
        1.0f,
        m_pStrokeStyleDash
        );

    // Apply the translation transform to the render target.
    m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(20, 10));

    // Paint the interior of the rectangle.
    m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);

    // Draw the outline of the rectangle.
    m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



In der folgenden Abbildung werden die Auswirkungen der Anwendung der Translation-Transformation auf das Quadrat dargestellt, wobei das ursprüngliche Quadrat ein gepunkteter Umriss und das übersetzte Quadrat ein voll Bild Umriss ist.

![Abbildung eines Quadrats mit 20 Einheiten nach rechts entlang der x-Achse und 10 Einheiten entlang der y-Achse](images/translation-ovw.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> </dl>

 

 