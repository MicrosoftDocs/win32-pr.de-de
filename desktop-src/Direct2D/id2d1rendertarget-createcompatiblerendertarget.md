---
title: ID2D1RenderTarget-Methode "up-Methode" (D2d1. h)
description: Erstellt ein neues Bitmap-Renderziel zur Verwendung während der zwischengeschalteten Offscreen-Zeichnung, das mit dem aktuellen Renderziel kompatibel ist.
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
keywords:
- Methoden von "Direct2D"
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 0f0de8478d2ab3ee2e7142bd0e197053dc58ac2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367729"
---
# <a name="id2d1rendertargetcreatecompatiblerendertarget-methods"></a>ID2D1RenderTarget::-Methode

Erstellt ein neues Bitmap-Renderziel zur Verwendung während der zwischengeschalteten Offscreen-Zeichnung, das mit dem aktuellen Renderziel kompatibel ist.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreatecompatiblerendertarget" (D2D1 \_ size \_ F, D2D1 \_ size \_ U, D2D1 \_ Pixel \_ Format, D2D1 \_ Compatible \_ \_ renderzieloptionen \_ , ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget))       | Erstellt ein Bitmap-Renderziel zur Verwendung während der zwischengeschalteten Offscreen-Zeichnung, das mit dem aktuellen Renderziel kompatibel ist.<br/>                                                                                                             |
| [**"Kreatecompatiblerendertarget" (D2D1 \_ size \_ F \* , D2D1 \_ size \_ U \* , D2D1 \_ Pixel \_ Format \* , D2D1 \_ Compatible \_ \_ renderzieloptionen \_ , ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)) | Erstellt ein Bitmap-Renderziel zur Verwendung während der zwischengeschalteten Offscreen-Zeichnung, das mit dem aktuellen Renderziel kompatibel ist. <br/>                                                                                                            |
| [**"Kreatecompatiblerendertarget" (ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))                                                                                                 | Erstellt ein neues Bitmap-Renderziel, das während der zwischengeschalteten Offscreen-Zeichnung verwendet werden kann, die mit dem aktuellen Renderziel kompatibel ist und die gleiche Größe, den dpi-Wert und das Pixel Format aufweist (aber nicht der Alpha-Modus) <br/>         |
| [**"Kreatecompatiblerendertarget" (D2D1 \_ size \_ F, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_id2d1bitmaprendertarget))                                                                                   | Erstellt ein neues Bitmap-Renderziel zur Verwendung während der zwischengeschalteten Offscreen-Zeichnung, das mit dem aktuellen Renderziel kompatibel ist und das gleiche Pixel Format (aber nicht den Alpha-Modus) wie das aktuelle Renderziel aufweist. <br/>                        |
| [**"Kreatecompatiblerendertarget" (D2D1 \_ size \_ F, D2D1 \_ size \_ U, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_id2d1bitmaprendertarget))                                                                     | Erstellt ein Bitmap-Renderziel, das während der zwischengeschalteten Bildschirm Zeichnung verwendet werden kann, die mit dem aktuellen Renderziel kompatibel ist. Das neue Bitmap-Renderziel hat das gleiche Pixel Format (aber nicht der Alpha-Modus) wie das aktuelle Renderziel. <br/> |
| [**"Kreatecompatiblerendertarget" (D2D1 \_ size \_ F, D2D1 \_ size \_ U, D2D1 \_ Pixel \_ Format, ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_id2d1bitmaprendertarget))                                                 | Erstellt ein Bitmap-Renderziel zur Verwendung während der zwischengeschalteten Offscreen-Zeichnung, das mit dem aktuellen Renderziel kompatibel ist. <br/>                                                                                                            |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die Methode " **kreatecompatiblerendertarget** " verwendet, um ein [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) zu erstellen und zum Zeichnen eines Raster Musters zu verwenden. Das Raster Muster wird als Quelle eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)verwendet.


```C++
HRESULT DemoApp::CreateGridPatternBrush(
    ID2D1RenderTarget *pRenderTarget,
    ID2D1BitmapBrush **ppBitmapBrush
    )
{
    // Create a compatible render target.
    ID2D1BitmapRenderTarget *pCompatibleRenderTarget = NULL;
    HRESULT hr = pRenderTarget->CreateCompatibleRenderTarget(
        D2D1::SizeF(10.0f, 10.0f),
        &amp;pCompatibleRenderTarget
        );
    if (SUCCEEDED(hr))
    {
        // Draw a pattern.
        ID2D1SolidColorBrush *pGridBrush = NULL;
        hr = pCompatibleRenderTarget->CreateSolidColorBrush(
            D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
            &amp;pGridBrush
            );
        if (SUCCEEDED(hr))
        {
            pCompatibleRenderTarget->BeginDraw();
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.0f, 10.0f, 1.0f), pGridBrush);
            pCompatibleRenderTarget->FillRectangle(D2D1::RectF(0.0f, 0.1f, 1.0f, 10.0f), pGridBrush);
            pCompatibleRenderTarget->EndDraw();

            // Retrieve the bitmap from the render target.
            ID2D1Bitmap *pGridBitmap = NULL;
            hr = pCompatibleRenderTarget->GetBitmap(&amp;pGridBitmap);
            if (SUCCEEDED(hr))
            {
                // Choose the tiling mode for the bitmap brush.
                D2D1_BITMAP_BRUSH_PROPERTIES brushProperties =
                    D2D1::BitmapBrushProperties(D2D1_EXTEND_MODE_WRAP, D2D1_EXTEND_MODE_WRAP);

                // Create the bitmap brush.
                hr = m_pRenderTarget->CreateBitmapBrush(pGridBitmap, brushProperties, ppBitmapBrush);

                pGridBitmap->Release();
            }

            pGridBrush->Release();
        }

        pCompatibleRenderTarget->Release();
    }

    return hr;
}
```



Im folgenden Codebeispiel wird der Pinsel zum Zeichnen eines Musters verwendet.


```C++
// Paint a grid background.
m_pRenderTarget->FillRectangle(
    D2D1::RectF(0.0f, 0.0f, renderTargetSize.width, renderTargetSize.height),
    m_pGridPatternBitmapBrush
    );
```



Code wurde in diesem Beispiel ausgelassen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1. h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
