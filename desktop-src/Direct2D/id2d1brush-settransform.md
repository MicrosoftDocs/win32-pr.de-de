---
title: ID2D1Brush setTransform-Methoden (D2d1 \_ 1. h)
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
ms.openlocfilehash: 89d0da76368fac2d2335cabda1f6d0a6130b499f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367132"
---
# <a name="id2d1brushsettransform-methods"></a>ID2D1Brush:: setTransform-Methoden

Legt die auf den Pinsel angewendete Transformation fest.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                       | BESCHREIBUNG                                              |
|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------|
| [**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f_))  | Legt die auf den Pinsel angewendete Transformation fest.<br/> |
| [**SetTransform (D2D1 \_ Matrix \_ 3x2 \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) | Legt die auf den Pinsel angewendete Transformation fest.<br/> |



## <a name="remarks"></a>Bemerkungen

Wenn Sie mit einem Pinsel zeichnen, zeichnet Sie den Koordinaten Bereich des Renderziels. Pinsel positionieren sich nicht automatisch so, dass Sie an dem Objekt ausgerichtet werden, das gezeichnet wird. Standardmäßig beginnen Sie mit dem Zeichnen am Ursprung (0,0) des Renderziels.

Durch Festlegen des Startpunkts und des Endpunkts können Sie den durch ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) definierten Farbverlauf in einen Zielbereich verschieben. Entsprechend können Sie den von einem [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) definierten Farbverlauf durch Ändern seiner Mitte und Radii verschieben.

Um den Inhalt eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) an den Bereich auszurichten, der gezeichnet wird, können Sie die **setTransform** -Methode verwenden, um die Bitmap an die gewünschte Stelle zu übersetzen. Diese Transformation wirkt sich nur auf den Pinsel aus. Er wirkt sich nicht auf andere Inhalte aus, die vom Renderziel gezeichnet werden.

Die folgenden Abbildungen zeigen die Auswirkung der Verwendung eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Auffüllen eines Rechtecks, das sich unter (100, 100) befindet. Die Abbildung in der linken Abbildung zeigt das Ergebnis der Füllung des Rechtecks ohne Umwandlung des Pinsels: die Bitmap wird am Ursprung des Renderziels gezeichnet. Daher wird nur ein Teil der Bitmap im Rechteck angezeigt.

Die Abbildung auf der rechten Seite zeigt das Ergebnis der Transformation des [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) , sodass der Inhalt 50 Pixel nach rechts und 50 Pixel nach unten verschoben wird. Die Bitmap füllt nun das Rechteck aus.

![Abbildung von zwei Quadraten, eine mit einer Bitmap ohne transformierten Pinsel und eine mit einem transformierten Pinsel gezeichnet](images/brushes-ovw-transform.png)

## <a name="examples"></a>Beispiele

In den folgenden Codebeispielen wird veranschaulicht, wie die Transformation erstellt wird, die im rechten Diagramm in der obigen Abbildung gezeigt wird. Wenden Sie zuerst eine Übersetzung auf den [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)an, und bewegen Sie den Pinsel 50 Pixel direkt entlang der x-Achse und 50 Pixel entlang der y-Achse. Verwenden Sie dann **ID2D1BitmapBrush** , um das Rechteck mit der linken oberen Ecke bei (100, 100) und der unteren rechten Ecke um (200, 200) auszufüllen.


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
| Header<br/>  | <dl> <dt>D2d1 \_ 1. h (Include D2d1. h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> <dt>

[**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)
</dt> </dl>

�

�
