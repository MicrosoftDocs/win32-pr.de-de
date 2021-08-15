---
title: Zeichnen einer Bitmap
description: Zeigt, wie Bitmaps mit Direct2D gerendert werden.
ms.assetid: 9c6fc8b1-47ba-46fa-b812-2636cd8ff2b4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c76fb3a956d20f83f4de8beb8431295c86b84cf7e6908fb311ed16ea1ceefa0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119259224"
---
# <a name="how-to-draw-a-bitmap"></a>Zeichnen einer Bitmap

Verwenden Sie zum Rendern einer Bitmap die [**ID2D1RenderTarget::D rawBitmap-Methode.**](id2d1rendertarget-drawbitmap.md) Das folgende Beispiel zeigt, wie sie die **DrawBitmap-Methode** verwenden, um eine [**ID2D1Bitmap zu zeichnen.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) Die in der folgenden Abbildung gezeigte Ausgabe wird erstellt.

![Abbildung einer ursprünglichen Bitmap und resultierenden Bitmaps mit unterschiedlichen Durchlässigkeitseinstellungen und Transformationen](images/drawbitmapexample.png)

Erstellen Sie zunächst eine [**ID2D1Bitmap.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) Im folgenden Beispiel wird eine Bitmap aus der Ressourcendatei der Anwendung geladen und als *m \_ pBitmap gespeichert.* (Informationen dazu, wie die Methode implementiert wird, finden Sie unter Laden einer `LoadResourceBitmap` [Bitmap aus einer Ressource.)](how-to-load-a-bitmap-from-a-resource.md)


```C++
// Create a bitmap from an application resource.
hr = LoadResourceBitmap(
    m_pRenderTarget,
    m_pWICFactory,
    L"SampleImage",
    L"Image",
    200,
    0,
    &m_pBitmap
    );
```



Erstellen Sie [**die ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) in derselben Methode, in der Sie das Renderziel erstellt haben, das Sie zum Zeichnen der Bitmap verwenden, und geben Sie die Bitmap frei, wenn das Renderziel freigegeben wird.

Nachdem die Bitmap erstellt wurde, rendern Sie sie. Im folgenden Beispiel wird die [**DrawBitmap-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f_float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f)) verwendet, um eine Bitmap mehrmals mit unterschiedlichen Größen- und Deckkrafteinstellungen zu rendern.


```C++
HRESULT DrawBitmapExample::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());
        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        // Paint a grid background.
        m_pRenderTarget->FillRectangle(
            D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
            m_pGridPatternBitmapBrush
            );

        // Retrieve the size of the bitmap.
        D2D1_SIZE_F size = m_pBitmap->GetSize();

        D2D1_POINT_2F upperLeftCorner = D2D1::Point2F(100.f, 10.f);

        // Draw a bitmap.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + size.width,
                upperLeftCorner.y + size.height)
            );

        // Draw the next bitmap below the first one.
        upperLeftCorner.y = upperLeftCorner.y + size.height + 10.f;

        // Scale the bitmap to half its size using the linear
        // interoplation mode and draw it.
        float scaledWidth = size.width / 2.f;
        float scaledHeight = size.height / 2.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw the bitmap at half its size and half its opacity.
        upperLeftCorner.y = upperLeftCorner.y + size.height / 2.f + 10.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        // Draw a series of bitmaps with different opacity and
        // rotation angles.
        upperLeftCorner.y = upperLeftCorner.y + scaledHeight + 20.f;
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.5,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        D2D1_POINT_2F lowerLeftCorner = D2D1::Point2F(upperLeftCorner.x, upperLeftCorner.y + scaledHeight);
        D2D1_POINT_2F imageCenter = D2D1::Point2F(
            upperLeftCorner.x + scaledWidth / 2,
            upperLeftCorner.y + scaledHeight / 2
            );

        // Rotate the next bitmap by -20 degrees.
        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-20, imageCenter)
            );

        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            0.75,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        m_pRenderTarget->SetTransform(
            D2D1::Matrix3x2F::Rotation(-45, imageCenter)
            );

        // Make the last bitmap fully opaque.
        m_pRenderTarget->DrawBitmap(
            m_pBitmap,
            D2D1::RectF(
                upperLeftCorner.x,
                upperLeftCorner.y,
                upperLeftCorner.x + scaledWidth,
                upperLeftCorner.y + scaledHeight),
            1.0,
            D2D1_BITMAP_INTERPOLATION_MODE_LINEAR
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



Die [**DrawBitmap-Methode**](id2d1rendertarget-drawbitmap.md) gibt bei einem Fehler keinen Fehlercode zurück. Um zu bestimmen, ob ein Zeichnungsvorgang (z. B. **DrawBitmap)** fehlgeschlagen ist, überprüfen Sie das von der [**ID2D1RenderTarget::EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) zurückgegebene Ergebnis, wie im folgenden Beispiel gezeigt.


```C++
hr = m_pRenderTarget->EndDraw();
```



Code wurde in diesem Beispiel ausgelassen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**DrawBitmap**](id2d1rendertarget-drawbitmap.md)
</dt> <dt>

[**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)
</dt> <dt>

[Laden einer Bitmap aus einer Ressource](how-to-load-a-bitmap-from-a-resource.md)
</dt> </dl>

 

 