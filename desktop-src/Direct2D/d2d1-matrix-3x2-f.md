---
title: D2D1_MATRIX_3X2_F (D2d1.h)
description: Stellt eine 3:2-Matrix dar.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d4e8a50e17c4c740c427d21df27e3c1d9cf8226df5edc1b98f15cbe920c401c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119260490"
---
# <a name="d2d1_matrix_3x2_f"></a>D2D1 \_ MATRIX \_ 3X2 \_ F

Stellt eine 3:2-Matrix dar.


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a>Hinweise

**D2D1 \_ MATRIX \_ 3X2** ist ein neuer Name für die [**D2D \_ MATRIX \_ 3X2 \_ F-Struktur.**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Eine Liste der von der Matrix bereitgestellten Felder finden Sie unter [**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).

Um allgemeine Matrixoperationen zu vereinfachen, stellt Direct2D die [**D2D1::Matrix3x2F-Klasse**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) bereit, die von der [**D2D1 \_ MATRIX \_ 3X2-Struktur**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) abgeleitet wird. Die **Matrix3x2F-Klasse** stellt eine Reihe von Hilfsmethoden zum Ausführen allgemeiner Aufgaben bereit, z. B. das Erstellen einer Übersetzungs- oder Schiefematrix.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die [**D2D1::Matrix3x2F::Rotation-Methode**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) verwendet, um eine Drehungsmatrix zu erstellen, die ein Quadrat im Uhrzeigersinn um 45 Grad um die Mitte des Quadrats dreht und die Matrix an die [**SetTransform-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) des Renderziels übergibt (*m \_ pRenderTarget*).

Die folgende Abbildung zeigt die Auswirkung der Anwendung der vorhergehenden Drehungstransformation auf das Quadrat. Das ursprüngliche Quadrat ist eine gepunktete Kontur, und das gedrehte Quadrat ist eine durchgehende Kontur.

![Abbildung eines Quadrats, das im Uhrzeigersinn um 45 Grad um die Mitte des ursprünglichen Quadrats gedreht wird](images/rotate-ovw.png)


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



Code wurde in diesem Beispiel ausgelassen. Weitere Informationen zu Transformationen finden Sie in der [Übersicht über Transformationen.](direct2d-transforms-overview.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Plattformupdate für UWP-Apps für Windows \[ \| Vista-Desktop-Apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Plattformupdate für Windows Server \[ 2008-Desktop-Apps \| UWP-Apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1- und Windows Runtime-Apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1.h</dt> </dl>                                                        |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[Übersicht über Transformationen](direct2d-transforms-overview.md)
</dt> <dt>

[Drehen eines Objekts](how-to-rotate.md)
</dt> <dt>

[Skalieren eines Objekts](how-to-scale.md)
</dt> <dt>

[Verzerren eines Objekts](how-to-skew.md)
</dt> <dt>

[Übersetzen eines Objekts](how-to-translate.md)
</dt> <dt>

[**D2D \_ MATRIX \_ 3X2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

