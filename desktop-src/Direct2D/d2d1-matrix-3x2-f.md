---
title: D2D1_MATRIX_3X2_F (D2D1. h)
description: Stellt eine 3 x 2-Matrix dar.
ms.assetid: f05d7555-6482-4eea-950f-7b443892cc1f
keywords:
- D2D1_MATRIX_3X2_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: beb252e35508c48570c96f251205fc8a54755687
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342192"
---
# <a name="d2d1_matrix_3x2_f"></a>D2D1 \_ Matrix \_ 3x2 \_ F

Stellt eine 3 x 2-Matrix dar.


```C++
typedef D2D_MATRIX_3X2_F D2D1_MATRIX_3X2_F;
```



## <a name="remarks"></a>Bemerkungen

**D2D1 \_ Matrix \_ 3x2** ist ein neuer Name für die [**D2D \_ Matrix \_ 3x2- \_ F-**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Struktur. Eine Liste der Felder, die von der Matrix bereitgestellt werden, finden Sie unter [**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f).

Zum vereinfachen allgemeiner Matrix Vorgänge stellt Direct2D die [**D2D1:: Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f) -Klasse bereit, die aus der [**D2D1 \_ Matrix \_ 3x2-**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f) Struktur abgeleitet ist. Die **Matrix3x2F** -Klasse stellt einen Satz von Hilfsmethoden zum Ausführen allgemeiner Aufgaben bereit, z. b. zum Erstellen einer Übersetzungs-oder schiefe-Matrix.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die [**D2D1:: Matrix3x2F:: Rotation**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-rotation) -Methode verwendet, um eine Rotations Matrix zu erstellen, die einen quadratischen Uhrzeigersinn um 45 Grad um die Mitte des Quadrats dreht und die Matrix an die [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_)) -Methode des Renderziels (*m \_ prendertarget*) übergibt.

Die folgende Abbildung zeigt die Auswirkung der Anwendung der vorangehenden Rotations Transformation auf das Quadrat. Das ursprüngliche Quadrat ist ein gepunkteter Umriss, und das gedrehte Quadrat ist ein voll solider Umriss.

![Abbildung eines Quadrats um 45 Grad im Uhrzeigersinn um die Mitte des ursprünglichen Quadrats gedreht](images/rotate-ovw.png)


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



Code wurde in diesem Beispiel ausgelassen. Weitere Informationen zu Transformationen finden Sie in der [Übersicht über Transformationen](direct2d-transforms-overview.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2d1. h</dt> </dl>                                                        |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D2D1::Matrix3x2F**](/windows/win32/api/d2d1helper/nl-d2d1helper-matrix3x2f)
</dt> <dt>

[Übersicht über Transformationen](direct2d-transforms-overview.md)
</dt> <dt>

[Drehen eines Objekts](how-to-rotate.md)
</dt> <dt>

[Skalieren eines Objekts](how-to-scale.md)
</dt> <dt>

[Vorgehensweise beim Verzerren eines Objekts](how-to-skew.md)
</dt> <dt>

[Übersetzen eines Objekts](how-to-translate.md)
</dt> <dt>

[**D2D \_ Matrix \_ 3x2 \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_matrix_3x2_f)
</dt> </dl>

 

