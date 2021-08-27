---
title: Rendern auf einer GDI-Oberfläche
description: Rendern auf einer GDI-Oberfläche
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20df241e379e9a133cb662ea141fa27c86a4bb486c8ffba311423cb9afd83fbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120048490"
---
# <a name="render-to-a-gdi-surface"></a>Rendern auf einer GDI-Oberfläche

In einigen Fällen möchten Sie möglicherweise [](direct-write-portal.md) in der Lage sein, DirectWrite auf einer GDI-Oberfläche anzuzeigen. Die [**IDWriteBitmapRenderTarget-Schnittstelle kapselt**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) eine Bitmap und einen Gerätekontext zum Rendern von Text. Sie erstellen eine **IDWriteBitmapRenderTarget** mithilfe der [**IDWriteGdiInterop::CreateBitmapRenderTarget-Methode,**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) wie im folgenden Code gezeigt.


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



Zum Rendern mit einer [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)müssen Sie eine benutzerdefinierte Textrenderer-Rückrufschnittstelle implementieren, die von der [**IDWriteTextRenderer-Schnittstelle abgeleitet**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) wird. Sie müssen Methoden zum Zeichnen einer Glyphen-Ausführung, einer Unterstreichung, eines Durchstrichs, von Inlineobjekten und so weiter implementieren. Eine vollständige Liste der Methoden finden Sie auf der [**Referenzseite zu IDWriteTextRenderer.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) Nicht jede Methode muss implementiert werden, sie kann einfach **E \_ NOTIMPL zurückgeben,** und das Zeichnen wird fortgesetzt.

Anschließend können Sie den Text zeichnen, indem Sie die [**IDWriteTextLayout::D raw-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) verwenden und die Rückrufschnittstelle übergeben, die Sie als Parameter implementiert haben. Die **IDWriteTextLayout::D raw-Methode** ruft die Methoden des von Ihnen zur Verfügung stellenden benutzerdefinierten Rendererrückrufs auf. Die [**DrawGlyphRun-,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) [**DrawUnderline-,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) [**DrawInlineObject-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)und [**DrawStrikethrough-Methoden**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) führen die Zeichnungsfunktionen aus.

Rufen Sie in Ihrer Implementierung von [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)die [**IDWriteBitmapRenderTarget::D rawGlyphRun-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) auf, um die Glyphen zu zeichnen. Das Rendern der Unterstreichungs-, Durchgestrichen- und Inlineobjekte muss von Ihrem benutzerdefinierten Renderer durchgeführt werden.

[**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) verfügt über einen optionalen RECT out-Parameter, der die Begrenzungen des Bereichs enthält, in dem der Text gezeichnet wurde. Sie können diese Informationen verwenden, um das umgebundene Rechteck für den Gerätekontext mit der Von GDI bereitgestellten [**SetBoundsRect-Funktion**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) zu setzen. Der folgende Code ist eine Beispielimplementierung der [**DrawGlyphRun-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) eines benutzerdefinierten Renderers.


```C++
STDMETHODIMP GdiTextRenderer::DrawGlyphRun(
    __maybenull void* clientDrawingContext,
    FLOAT baselineOriginX,
    FLOAT baselineOriginY,
    DWRITE_MEASURING_MODE measuringMode,
    __in DWRITE_GLYPH_RUN const* glyphRun,
    __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
    IUnknown* clientDrawingEffect
    )
{
    HRESULT hr = S_OK;

    // Pass on the drawing call to the render target to do the real work.
    RECT dirtyRect = {0};

    hr = pRenderTarget_->DrawGlyphRun(
        baselineOriginX,
        baselineOriginY,
        measuringMode,
        glyphRun,
        pRenderingParams_,
        RGB(0,200,255),
        &dirtyRect
        );
    

    return hr;
}
```



Die [**IDWriteBitmapRenderTarget-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) wird in einem Gerätekontext (DC) im Arbeitsspeicher gerendert. Sie erhalten mithilfe der [**IDWriteBitmapRenderTarget::GetMemoryDC-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) ein Handle für diesen DC. Sobald die Zeichnung ausgeführt wurde, muss der Arbeitsspeicher-DC des **IDWriteBitmapRenderTarget-Objekts** auf die GDI-Zieloberfläche kopiert werden.

Sie können das umgebundene Rechteck mithilfe der [**GetBoundsRect-Funktion**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) abrufen und dann das umgebundene Rechteck mit der [**BitBlt-Funktion**](/windows/win32/api/wingdi/nf-wingdi-bitblt) verwenden, um den gerenderten [DirectWrite-Text](direct-write-portal.md) aus dem Speicherdomänencontroller auf die GDI-Oberfläche zu kopieren, wie im folgenden Code gezeigt.


```C++
// Transfer from DWrite's rendering target to the window.
BitBlt(
    hdc,
    0, 0,
    size.cx, size.cy,
    memoryHdc,
    0, 0, 
    SRCCOPY | NOMIRRORBITMAP
    );
```



 

 