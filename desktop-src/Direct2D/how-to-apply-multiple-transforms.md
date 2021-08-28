---
title: Anwenden mehrerer Transformationen auf ein Objekt
description: Zeigt, wie mehrere Transformationen auf ein Objekt angewendet werden.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d63db7899b79dd07a6a4a14a4efbbfaeefc5723ad09c71a3462ba5d2fd0c042
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259685"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>Anwenden mehrerer Transformationen auf ein Objekt

Das Ausführen mehrerer Transformationen für ein Objekt bedeutet, mehrere Transformationen zu einer Transformation zu kombinieren. Das heißt, die Ausgabe jeder Transformationsmatrix wird als Eingabe für die nächste matrix verwendet, wodurch die kumulativen Auswirkungen aller Matrixtransformationen erhalten werden.

Angenommen, zwei Transformationsmatrizen, Drehung und Übersetzung, werden miteinander multipliziert. Das Ergebnis ist eine neue Matrix, die die Funktionen von Drehung und Übersetzung ausführt. Da die Matrixmultiplikation nicht kommutativ ist, ist eine Drehungstransformation multipliziert mit einer Übersetzungstransformation anders als die Übersetzungstransformation multipliziert mit der Rotationstransformation.

In den folgenden Codebeispielen wird gezeigt, wie die Drehung gefolgt von der Übersetzung und dann der Übersetzung gefolgt von der Drehung angewendet wird. Beachten Sie, dass sich die Renderingergebnisse unterscheiden.


```C++
D2D1_RECT_F rectangle = D2D1::RectF(300.0f, 40.0f, 360.0f, 100.0f);

// Draw the rectangle before transforming the render target.

m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(330.0f, 70.0f)
    );


D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

// First rotate about the center of the square and then move
// 20 pixels to the right along the x-axis
// and 10 pixels downward along the y-axis.
m_pRenderTarget->SetTransform(rotation* translation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush, 1.0f);
```




```C++
D2D1_RECT_F rectangle = D2D1::Rect(40.0f, 40.0f, 100.0f, 100.0f);

// Draw a rectangle without transforming it.
m_pRenderTarget->DrawRectangle(
    rectangle,
    m_pOriginalShapeBrush,
    1.0f,
    m_pStrokeStyleDash
    );

D2D1_MATRIX_3X2_F translation = D2D1::Matrix3x2F::Translation(20.0f, 10.0f);

m_pRenderTarget->SetTransform(translation);

D2D1_MATRIX_3X2_F rotation = D2D1::Matrix3x2F::Rotation(
    45.0f,
    D2D1::Point2F(70.0f, 70.0f)
    );

// First move 20 pixels to the right along the x-axis and
// 10 pixels downward along the y-axis,
// and then rotate about the center of the original square.
m_pRenderTarget->SetTransform(translation * rotation);

// Draw the rectangle in the transformed space.
m_pRenderTarget->FillRectangle(rectangle, m_pFillBrush);
m_pRenderTarget->DrawRectangle(rectangle, m_pTransformedShapeBrush);
```



Der Code erzeugt die in der folgenden Abbildung gezeigte Ausgabe.

![Abbildung eines Rechtecks, das übersetzt und dann gedreht wurde, und eines Rechtecks, das gedreht und dann übersetzt wurde](images/multipletransforms.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> </dl>

 

 




