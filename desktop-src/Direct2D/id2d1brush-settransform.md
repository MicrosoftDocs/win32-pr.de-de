---
title: ID2D1Brush SetTransform-Methoden (D2d1 \_ 1.h)
description: Legt die auf den Pinsel angewendete Transformation fest.
ms.assetid: 57afadc1-88c9-4a5b-a83f-63c4c69182a7
keywords:
- SetTransform-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: a5a30d4051303667402fdd1143f5a813d7515223c8093a5913294e6dd1722273
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119918035"
---
# <a name="id2d1brushsettransform-methods"></a>ID2D1Brush::SetTransform-Methoden

Legt die auf den Pinsel angewendete Transformation fest.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                       | Beschreibung                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | Legt die auf den Pinsel angewendete Transformation fest.<br/> |
| [**SetTransform(D2D1 \_ MATRIX \_ 3X2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | Legt die auf den Pinsel angewendete Transformation fest.<br/> |



## <a name="remarks"></a>Hinweise

Wenn Sie mit einem Pinsel zeichnen, zeichnet er im Koordinatenbereich des Renderziels. Pinsel positionieren sich nicht automatisch so, dass sie dem gezeichneten Objekt entsprechen. standardmäßig beginnen sie mit dem Zeichnen am Ursprung (0, 0) des Renderziels.

Sie können den durch einen [**ID2D1LinearGradientBrush definierten**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) Farbverlauf in einen Zielbereich "verschieben", indem Sie dessen Startpunkt und Endpunkt festlegen. Ebenso können Sie den durch einen [**ID2D1RadialGradientBrush definierten**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) Farbverlauf verschieben, indem Sie seinen Mittelpunkt und seine Radien ändern.

Um den Inhalt eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) an den gezeichneten Bereich auszurichten, können Sie die **SetTransform-Methode** verwenden, um die Bitmap an die gewünschte Position zu übersetzen. Diese Transformation wirkt sich nur auf den Pinsel aus. sie wirkt sich nicht auf andere Inhalte aus, die vom Renderziel gezeichnet werden.

Die folgenden Abbildungen zeigen die Auswirkung der Verwendung eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Ausfüllen eines Rechtecks unter (100, 100). Die Abbildung auf der linken Abbildung zeigt das Ergebnis der Füllung des Rechtecks ohne Transformation des Pinsels: Die Bitmap wird am Ursprung des Renderziels gezeichnet. Daher wird nur ein Teil der Bitmap im Rechteck angezeigt.

Die Abbildung auf der rechten Seite zeigt das Ergebnis der Transformation des [**ID2D1BitmapBrush, sodass**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) der Inhalt um 50 Pixel nach rechts und 50 Pixel nach unten verschoben wird. Die Bitmap füllt nun das Rechteck aus.

![Abbildung von zwei Quadraten, eines mit einer Bitmap ohne transformierten Pinsel und eines mit einem transformierten Pinsel gezeichnet](images/brushes-ovw-transform.png)

## <a name="examples"></a>Beispiele

Die folgenden Codebeispiele zeigen, wie sie die Transformation erstellen, die im rechten Diagramm in der vorherigen Abbildung gezeigt wird. Wenden Sie zunächst eine Übersetzung auf den [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)an, und verschieben Sie den Pinsel um 50 Pixel rechts entlang der x-Achse und 50 Pixel nach unten entlang der y-Achse. Verwenden Sie dann **id2D1BitmapBrush,** um das Rechteck mit der linken oberen Ecke bei (100, 100) und der unteren rechten Ecke bei (200, 200) auszufüllen.


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &amp;m_pBitmap
        );
   
}
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &amp;m_pBitmapBrush
        );
}
```




```C++
D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);



 // Demonstrate the effect of transforming a bitmap brush.
 m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

 // To see the content of the rcTransformedBrushRect, comment
 // out this statement.
 m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

 m_pRenderTarget-&gt;DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```





## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1.h (einschließlich D2d1.h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
