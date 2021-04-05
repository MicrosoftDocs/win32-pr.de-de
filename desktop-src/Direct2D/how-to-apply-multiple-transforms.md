---
title: Anwenden mehrerer Transformationen auf ein Objekt
description: Zeigt, wie mehrere Transformationen auf ein Objekt angewendet werden.
ms.assetid: a3875072-bb73-4698-944e-102ab5539d80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e031a46545c59513767ed4d260be9dc677b3fb77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708363"
---
# <a name="how-to-apply-multiple-transforms-to-an-object"></a>Anwenden mehrerer Transformationen auf ein Objekt

Das Ausführen mehrerer Transformationen für ein Objekt bedeutet, dass mehrere Transformationen in einem Objekt kombiniert werden. Das heißt, die Ausgabe jeder Transformationsmatrix zu verwenden und Sie als Eingabe für die nächste zu verwenden, wodurch die kumulativen Auswirkungen aller Matrix Transformationen erhalten werden.

Angenommen, es werden zwei Transformations Matrizen, Drehung und Übersetzung, multipliziert. Das Ergebnis ist eine neue Matrix, die die Funktionen sowohl der Drehung als auch der Übersetzung ausführt. Da die Matrix Multiplikation nicht kommutativ ist, unterscheidet sich die Transformation für Rotation multipliziert mit einer Übersetzungs Transformation von der Transformations Transformation, multipliziert mit der Transformation für Rotation.

In den folgenden Codebeispielen wird veranschaulicht, wie die Drehung, gefolgt von der Übersetzung, gefolgt von der Drehung angewendet wird. Beachten Sie, dass die renderingergebnisse verschieden sind.


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

![Abbildung eines Rechtecks, das übersetzt und dann gedreht wurde, und ein Rechteck, das gedreht und dann übersetzt wurde](images/multipletransforms.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> <dt>

[Übersicht über Direct2D-Transformationen](direct2d-transforms-overview.md)
</dt> </dl>

 

 




