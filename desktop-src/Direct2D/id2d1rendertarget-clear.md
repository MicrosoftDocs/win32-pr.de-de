---
title: ID2D1RenderTarget Clear-Methoden
description: Löscht den Zeichenbereich in die angegebene Farbe.
ms.assetid: 3bfec923-17fc-479a-a760-9baab2ff3a56
keywords:
- Methoden löschen Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 346e44e3ce0b59e40577d3207f45faafdc33b367
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369145"
---
# <a name="id2d1rendertargetclear-methods"></a>ID2D1RenderTarget:: Clear-Methoden

Löscht den Zeichenbereich in die angegebene Farbe.

### <a name="overload-list"></a>Überladeliste



| Methode                                                                 | BESCHREIBUNG                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| [**Clear (D2D1 \_ Color \_ F \* )**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) | Löscht den Zeichenbereich in die angegebene Farbe. <br/> |
| [**Clear (D2D1 \_ Color \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))  | Löscht den Zeichenbereich in die angegebene Farbe. <br/> |



## <a name="remarks"></a>Bemerkungen

Direct2D interpretiert den *ClearColor* -Wert als gerades Alpha (nicht vormultipliziert). Wenn der Alpha Modus des Renderziels den [**D2D1 \_ alpha- \_ Modus \_ ignorieren**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)hat, wird der Alphakanal von *ClearColor* ignoriert und durch 1.0 f (vollständig nicht transparent) ersetzt.

Wenn das Renderziel über einen aktiven Clip verfügt (angegeben durch [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), wird der Befehl Clear nur auf den Bereich innerhalb des Ausschneide Bereichs angewendet.

## <a name="examples"></a>Beispiele

Im folgenden Beispiel wird die **Clear** -Methode zum Erstellen eines weißen Hintergrunds verwendet, bevor anderer Inhalt gerendert wird.


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
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



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-------------------------------------------------------------------------------------|
| Bibliothek<br/> | <dl> <dt>D2d1. lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

