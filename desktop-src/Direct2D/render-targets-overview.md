---
title: Übersicht über Renderziele
description: Beschreibt die verschiedenen Typen von Direct2D-Renderingzielen und deren Verwendung.
ms.assetid: 8a67babd-20c7-47f4-8dd3-8c0320d89ad6
keywords:
- Direct2D, Renderziele
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 1770447d1468d7a09990696f8d523458bd2d0e46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948868"
---
# <a name="render-targets-overview"></a>Übersicht über Renderziele

Ein Renderziel ist eine Ressource, die von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle erbt. Ein Renderziel erstellt Ressourcen zum Zeichnen und ausführen tatsächlicher Zeichnungsvorgänge. In diesem Thema werden die verschiedenen Typen von Direct2D-Renderingzielen und deren Verwendung beschrieben.

-   [Renderziele](#render-targets-overview)
    -   [Renderzielfeatures](#render-target-features)
    -   [Renderziel Ressourcen](#render-target-resources)
    -   [Zeichnen von Befehlen](#drawing-commands)
    -   [Fehlerbehandlung](#error-handling)
-   [Beispiel: Rendering von Inhalt in einem Fenster](#example-render-content-to-a-window)

## <a name="render-targets"></a>Renderziele

Ein Renderziel ist eine Ressource, die von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle erbt. Ein Renderziel erstellt Ressourcen zum Zeichnen und ausführen tatsächlicher Zeichnungsvorgänge. Es gibt verschiedene Arten von renderzielen, die zum renderinggrafiken auf folgende Weise verwendet werden können:

-   [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekte erzeugen Inhalt in einem Fenster.
-   [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) -Objekte werden in einen GDI-Gerätekontext gerendering.
-   Bitmap-renderzielobjekte renderinginhalte Inhalt zu einer Offscreen-Bitmap.
-   DXGI Renderziel Objekte werden zu einer DXGI-Oberfläche für die Verwendung mit Direct3D.

Da ein Renderziel mit einem bestimmten renderinggerät verknüpft ist, ist es eine Geräte abhängige Ressource und funktioniert nicht mehr, wenn das Gerät entfernt wird.

### <a name="render-target-features"></a>Renderzielfeatures

Sie können angeben, ob ein Renderziel eine Hardwarebeschleunigung verwendet und ob die Remote Anzeige von einem lokalen oder einem Remote Computer gerendert wird. Renderziele können für Alias-oder Antialiasing-Rendering eingerichtet werden. Für renderingszenen mit einer großen Anzahl von primitiven kann ein Entwickler auch 2D-Grafiken im Alias Modus Rendern und D3D Multisampling Antialiasing verwenden, um eine höhere Skalierbarkeit zu erzielen.

Renderziele können auch Zeichnungsvorgänge in Ebenen gruppieren, die durch die [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Schnittstelle dargestellt werden. Ebenen sind nützlich, um Zeichnungsvorgänge zu erfassen, die zusammen zusammengeführt werden, wenn ein Frame gerendert wird. In einigen Szenarien kann dies eine nützliche Alternative zum Rendern in ein Bitmap-Renderziel sein und dann den Bitmapinhalt wieder verwenden, da die Zuordnungs Kosten für die Schichten niedriger sind als bei einem [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Renderziele können neue Renderziele erstellen, die mit sich selbst kompatibel sind. Dies ist für das zwischengeschaltete debuggerrendering nützlich, während die verschiedenen renderzieleigenschaften beibehalten werden, die für den ursprünglichen festgelegt wurden.

Es ist auch möglich, die Verwendung von GDI für ein Direct2D-Renderziel durch Aufrufen von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein Renderziel für [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)zu renderzielen, das über [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) -und [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) -Methoden verfügt, die zum Abrufen eines GDI-Geräte Kontexts verwendet werden können. Das Rendering über GDI ist nur möglich, wenn das Renderziel mit dem festgelegten [**GDI-kompatiblen Flag "D2D1 \_ \_ Renderziel \_ \_ \_ Verwendung**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_usage) " erstellt wurde. Dies ist nützlich für Anwendungen, die in erster Linie mit Direct2D rendern, aber über ein Erweiterbarkeits Modell oder andere Legacy Inhalte verfügen, die die Fähigkeit zum Rendern mit GDI erfordern. Weitere Informationen finden Sie unter [Übersicht über die Zusammenarbeit zwischen Direct2D und GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Renderziel Ressourcen

Wie eine Factory kann ein Renderziel Zeichnungs Ressourcen erstellen. Alle von einem Renderziel erstellten Ressourcen sind Geräte abhängige Ressourcen (genau wie das Renderziel). Mit einem Renderziel können die folgenden Ressourcentypen erstellt werden:

-   Bitmaps
-   Pinsel
-   Ebenen
-   Gittermodelle

### <a name="drawing-commands"></a>Zeichnen von Befehlen

Zum Renderinginhalt verwenden Sie die Zeichnungs Methoden des Renderziels. Bevor Sie mit dem Zeichnen beginnen, wird die [**ID2D1RenderTarget:: beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufgerufen. Nachdem Sie das Zeichnen abgeschlossen haben, können Sie die [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen. Zwischen diesen Aufrufen verwenden Sie Draw-und Fill-Methoden zum Rendering von Zeichnungs Ressourcen. Die meisten Draw-und Fill-Methoden übernehmen eine Form (entweder eine primitive oder eine Geometrie) und einen Pinsel zum ausfüllen oder gliedern der Form.

Renderziele stellen Methoden für das Abschneiden, das Anwenden von Deck Kraft Masken und das Transformieren des Koordinaten Raums bereit.

Direct2D verwendet ein Links händiges Koordinatensystem: positive Werte der x-Achse werden nach rechts fortgesetzt, und die positiven y-Achsen Werte werden nach unten fortgesetzt.

### <a name="error-handling"></a>Fehlerbehandlung

Zeichnungs Befehle des Renderziels geben nicht an, ob der angeforderte Vorgang erfolgreich war. Um herauszufinden, ob Zeichnungs Fehler vorliegen, rufen Sie die Renderziel-Löschmethode oder die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) [**-Methode auf**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) , um ein **HRESULT** zu erhalten.

## <a name="example-render-content-to-a-window"></a>Beispiel: Rendering von Inhalt in einem Fenster

Im folgenden Beispiel wird die Methode " [**kreatehwndrendertarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget)) " verwendet, um eine [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget)zu erstellen.


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



Im nächsten Beispiel wird [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) verwendet, um Text in das Fenster zu zeichnen.


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



Code wurde in diesem Beispiel ausgelassen.

 

 