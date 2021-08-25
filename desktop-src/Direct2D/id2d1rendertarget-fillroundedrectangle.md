---
title: ID2D1RenderTarget FillRoundedRectangle-Methoden (D2d1.h)
description: Zeichnet das Innere des angegebenen abgerundeten Rechtecks.
ms.assetid: 9c4765b0-858f-4a20-b044-0acf87a1f131
keywords:
- FillRoundedRectangle-Methoden Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 8da1a154e7ca0b0b91b23cf067b529281ffa2b96f08f1315c9e8513cb43cb2e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874095"
---
# <a name="id2d1rendertargetfillroundedrectangle-methods"></a>ID2D1RenderTarget::FillRoundedRectangle-Methoden

Zeichnet das Innere des angegebenen abgerundeten Rechtecks.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                                                                                          | BESCHREIBUNG                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**FillRoundedRectangle(D2D1 \_ ROUNDED \_ RECT&,ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush))  | Zeichnet das Innere des angegebenen abgerundeten Rechtecks. <br/> |
| [**FillRoundedRectangle(D2D1 \_ ROUNDED \_ RECT , \* ID2D1Brush \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillroundedrectangle(constd2d1_rounded_rect__id2d1brush)) | Zeichnet das Innere des angegebenen abgerundeten Rechtecks.<br/>  |



## <a name="remarks"></a>Hinweise

Diese Methode gibt bei einem Fehler keinen Fehlercode zurück. Überprüfen Sie das ergebnis, das von den Methoden [**ID2D1RenderTarget::EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) oder [**ID2D1RenderTarget::EndDraw oder ID2D1RenderTarget::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) zurückgegeben wird, um zu bestimmen, ob bei einem Zeichnungsvorgang (z. B. **FillRoundedRectangle)** ein Fehler aufgetreten ist.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel werden die [**Methoden DrawRoundedRectangle**](id2d1rendertarget-drawroundedrectangle.md) und **FillRoundedRectangle** verwendet, um ein abgerundetes Rechteck zu umranden und zu füllen. In diesem Beispiel wird die in der folgenden Abbildung gezeigte Ausgabe erzeugt.

![Abbildung von vier abgerundeten Rechtecke mit unterschiedlichen Strichstilen und Füllungen](images/drawroundedrectangle-scr.png)


```C++
//  Called whenever the application needs to display the client
//  window.
HRESULT DrawAndFillRoundedRectangleExample::OnRender()
{
    HRESULT hr;

    // Create the render target and brushes if they
    // don't already exists.
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

        // Define a rounded rectangle.
        D2D1_ROUNDED_RECT roundedRect = D2D1::RoundedRect(
            D2D1::RectF(20.f, 20.f, 150.f, 100.f),
            10.f,
            10.f
            );

        // Draw the rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f);

        // Apply a translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 0.f));

        // Draw the rounded rectangle again, this time with a dashed stroke.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(0.f, 150.f));

        // Draw, then fill the rounded rectangle.
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);

        // Apply another translation transform.
        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Translation(200.f, 150.f));

        // Fill, then draw the rounded rectangle.
        m_pRenderTarget->FillRoundedRectangle(roundedRect, m_pSilverBrush);
        m_pRenderTarget->DrawRoundedRectangle(roundedRect, m_pBlackBrush, 10.f, m_pStrokeStyle);

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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D2d1.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>D2d1.lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[Zeichnen und Füllen einer einfachen Form](how-to-draw-an-ellipse.md)
</dt> <dt>

[**D2D1::RoundedRect**](/windows/win32/api/d2d1/nf-d2d1-id2d1roundedrectanglegeometry-getroundedrect)
</dt> </dl>

�

�
