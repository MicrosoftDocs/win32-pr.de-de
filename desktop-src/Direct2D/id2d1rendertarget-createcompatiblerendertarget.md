---
title: ID2D1RenderTarget CreateCompatibleRenderTarget-Methoden (D2d1.h)
description: Erstellt ein neues Bitmaprenderziel für die Verwendung während der zwischengeschalteten Offscreenzeichnung, die mit dem aktuellen Renderziel kompatibel ist.
ms.assetid: 4a799a7c-0d2f-460f-99f9-24c6cf7c4537
keywords:
- CreateCompatibleRenderTarget-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9015586109ff5015743874d18b604de919a9464a655383cf4d47aabb7b7acf35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432780"
---
# <a name="id2d1rendertargetcreatecompatiblerendertarget-methods"></a>ID2D1RenderTarget::CreateCompatibleRenderTarget-Methoden

Erstellt ein neues Bitmaprenderziel für die Verwendung während der zwischengeschalteten Offscreenzeichnung, die mit dem aktuellen Renderziel kompatibel ist.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                                                                                                        | Beschreibung                                                                                                                                                                                                                                            |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,D2D1 \_ PIXEL \_ FORMAT,D2D1 \_ COMPATIBLE RENDER TARGET \_ \_ \_ OPTIONS,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget))       | Erstellt ein Bitmaprenderingziel zur Verwendung während der zwischengeschalteten Offscreenzeichnung, die mit dem aktuellen Renderziel kompatibel ist.<br/>                                                                                                             |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE F , \_ \* D2D1 \_ SIZE U , \_ \* D2D1 \_ PIXEL FORMAT , \_ \* D2D1 \_ COMPATIBLE RENDER TARGET \_ \_ \_ OPTIONS,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_d2d1_compatible_render_target_options_id2d1bitmaprendertarget)) | Erstellt ein Bitmaprenderingziel zur Verwendung während der zwischengeschalteten Offscreenzeichnung, die mit dem aktuellen Renderziel kompatibel ist. <br/>                                                                                                            |
| [**CreateCompatibleRenderTarget(ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))                                                                                                 | Erstellt ein neues Bitmaprenderingziel für die Verwendung während der zwischengeschalteten Offscreenzeichnung, das mit dem aktuellen Renderziel kompatibel ist und die gleiche Größe, DPI und das gleiche Pixelformat (aber nicht den Alphamodus) wie das aktuelle Renderziel aufweist. <br/>         |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_id2d1bitmaprendertarget))                                                                                   | Erstellt ein neues Bitmaprenderingziel zur Verwendung während der zwischengeschalteten Offscreenzeichnung, das mit dem aktuellen Renderziel kompatibel ist und das gleiche Pixelformat (aber nicht den Alphamodus) wie das aktuelle Renderziel aufweist. <br/>                        |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_id2d1bitmaprendertarget))                                                                     | Erstellt ein Bitmaprenderziel für die Verwendung während der Zwischenzeichnung außerhalb des Bildschirms, das mit dem aktuellen Renderziel kompatibel ist. Das neue Bitmaprenderingziel hat das gleiche Pixelformat (aber nicht den Alphamodus) wie das aktuelle Renderziel. <br/> |
| [**CreateCompatibleRenderTarget(D2D1 \_ SIZE \_ F,D2D1 \_ SIZE \_ U,D2D1 \_ PIXEL \_ FORMAT,ID2D1BitmapRenderTarget \* \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(d2d1_size_f_d2d1_size_u_d2d1_pixel_format_id2d1bitmaprendertarget))                                                 | Erstellt ein Bitmaprenderingziel zur Verwendung während der zwischengeschalteten Offscreenzeichnung, die mit dem aktuellen Renderziel kompatibel ist. <br/>                                                                                                            |



## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **CreateCompatibleRenderTarget-Methode** verwendet, um ein [**ID2D1BitmapRenderTarget-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget) zu erstellen und es zum Zeichnen eines Rastermusters zu verwenden. Das Rastermuster wird als Quelle eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)verwendet.


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



Im folgenden Codebeispiel wird der Pinsel verwendet, um ein Muster zu zeichnen.


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
| Header<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
