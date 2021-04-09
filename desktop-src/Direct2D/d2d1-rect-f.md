---
title: D2D1_RECT_F (D2DBaseTypes. h)
description: Stellt ein Rechteck dar, das von den Koordinaten der linken oberen Ecke (Links, oben) und den Koordinaten der unteren rechten Ecke (rechts, unten) definiert wird. | D2D1_RECT_F (D2DBaseTypes. h)
ms.assetid: a961c0e3-fb76-4c07-b76e-47d8c09ada08
keywords:
- D2D1_RECT_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93ce4700e093b9e82fd4334ae9e01485a7fcbb4c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "104050758"
---
# <a name="d2d1_rect_f"></a>D2D1 \_ Rect \_ F

Stellt ein Rechteck dar, das von den Koordinaten der linken oberen Ecke (Links, oben) und den Koordinaten der unteren rechten Ecke (rechts, unten) definiert wird.


```C++
typedef D2D_RECT_F D2D1_RECT_F;
```



## <a name="remarks"></a>Bemerkungen

**D2D1 \_ Rect \_ f** ist ein neuer Name für die bereits definierte [**D2D \_ Rect \_ f**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f) -Struktur.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird ein [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Zeichen verwendet, um mehrere Rechtecke zu zeichnen und auszufüllen. Dieses Beispiel erzeugt eine Ausgabe, wie in der folgenden Abbildung dargestellt.

![Abbildung von zwei Rechtecke in einem Raster Hintergrund](images/drawrectangleexample-small.png)


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
        m_pRenderTarget->FillRectangle(&rectangle1, m_pLightSlateGrayBrush);

        // Draw the outline of a rectangle.
        m_pRenderTarget->DrawRectangle(&rectangle2, m_pCornflowerBlueBrush);

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



Ein verwandtes Tutorial finden Sie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7, Windows Vista mit SP2 und Platt Form Update für Windows Vista \[ -Desktop-Apps \| UWP-apps\]<br/>                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2, Windows Server 2008 mit SP2 und Platt Form Update für Windows Server 2008 \[ Desktop Apps \| UWP-apps\]<br/> |
| Unterstützte Mindestversion (Telefon)<br/>  | Windows Phone 8,1 \[ Windows Phone Silverlight 8,1 und Windows-Runtime apps\]<br/>                                                  |
| Header<br/>                   | <dl> <dt>D2DBaseTypes. h (Include D2d1. h)</dt> </dl>                               |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**D2D \_ Rect \_ F**](/windows/desktop/api/dcommon/ns-dcommon-d2d_rect_f)
</dt> <dt>

[Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)
</dt> </dl>

 

