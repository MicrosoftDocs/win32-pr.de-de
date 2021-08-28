---
title: ID2D1RenderTarget FillRectangle-Methoden (D2d1 \_ 1.h)
description: Zeichnet das Innere des angegebenen Rechtecks.
ms.assetid: 08e498f9-b564-4da6-ba9b-bff08964ce08
keywords:
- FillRectangle-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 3ae33b1d63633361b43ff61cd7ff0297ac3b8a6553c6218f0fc093f566c31742
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874110"
---
# <a name="id2d1rendertargetfillrectangle-methods"></a>ID2D1RenderTarget::FillRectangle-Methoden

Zeichnet das Innere des angegebenen Rechtecks.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                               | BESCHREIBUNG                                                 |
|:---------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------|
| [**FillRectangle(D2D1 \_ RECT \_ F&,ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush))  | Zeichnet das Innere des angegebenen Rechtecks. <br/> |
| [**FillRectangle(D2D1 \_ RECT \_ F \* ,ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f__id2d1brush)) | Zeichnet das Innere des angegebenen Rechtecks. <br/> |



## <a name="remarks"></a>Hinweise

Diese Methode gibt keinen Fehlercode zurück, wenn ein Fehler auftritt. Überprüfen Sie das von den Methoden [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegebene Ergebnis, um zu ermitteln, ob ein Zeichnungsvorgang (z. B. **FillRectangle)** fehlgeschlagen ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird [**id2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) verwendet, um mehrere Rechtecke zu zeichnen und zu füllen. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung von zwei Rechtecke auf einem Rasterhintergrund](images/drawrectangleexample-small.png)


```C++
// This method discards device-specific
// resources if the Direct3D device dissapears during execution and
// recreates the resources the next time it's invoked.
HRESULT DemoApp::OnRender()
{
    HRESULT hr = S_OK;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();

        // Draw a grid background.
        int width = static_cast<int>(rtSize.width);
        int height = static_cast<int>(rtSize.height);

        for (int x = 0; x < width; x += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(static_cast<FLOAT>(x), 0.0f),
                D2D1::Point2F(static_cast<FLOAT>(x), rtSize.height),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        for (int y = 0; y < height; y += 10)
        {
            m_pRenderTarget->DrawLine(
                D2D1::Point2F(0.0f, static_cast<FLOAT>(y)),
                D2D1::Point2F(rtSize.width, static_cast<FLOAT>(y)),
                m_pLightSlateGrayBrush,
                0.5f
                );
        }

        // Draw two rectangles.
        D2D1_RECT_F rectangle1 = D2D1::RectF(
            rtSize.width/2 - 50.0f,
            rtSize.height/2 - 50.0f,
            rtSize.width/2 + 50.0f,
            rtSize.height/2 + 50.0f
            );

        D2D1_RECT_F rectangle2 = D2D1::RectF(
            rtSize.width/2 - 100.0f,
            rtSize.height/2 - 100.0f,
            rtSize.width/2 + 100.0f,
            rtSize.height/2 + 100.0f
            );


        // Draw a filled rectangle.
        m_pRenderTarget->FillRectangle(&amp;rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&amp;rectangle2, m_pCornflowerBlueBrush);

        hr = m_pRenderTarget->EndDraw();
    }

    if (hr == D2DERR_RECREATE_TARGET)
    {
        hr = S_OK;
        DiscardDeviceResources();
    }

    return hr;
}
```



Ein verwandtes Tutorial finden Sie unter [Erstellen einer einfachen Direct2D-Anwendung.](direct2d-quickstart.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1 \_ 1.h (einschließlich D2d1.h)</dt> </dl> |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)
</dt> </dl>

�

�
