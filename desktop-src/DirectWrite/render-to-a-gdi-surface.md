---
title: An eine GDI-Oberfläche Renderen
description: An eine GDI-Oberfläche Renderen
ms.assetid: a6096ff5-1e6e-4edb-b455-ea5d205072ff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ff292feb2250a4dd81abeb62d8ee48ebfb4488b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390932"
---
# <a name="render-to-a-gdi-surface"></a>An eine GDI-Oberfläche Renderen

In einigen Fällen möchten Sie möglicherweise in der Lage sein, [DirectWrite](direct-write-portal.md) -Text auf einer GDI-Oberfläche anzuzeigen. Die [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Schnittstelle kapselt eine Bitmap und einen Gerätekontext zum renderingtext. Sie erstellen ein **idwrite-bitmaprendertarget** -Objekt, indem Sie die [**idschreitegdiinterop:: deatebitmaprendertarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) -Methode verwenden, wie im folgenden Code gezeigt.


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



Um mit [**idwrite-bitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)geresgt werden zu können, müssen Sie eine benutzerdefinierte Rückruf Schnittstelle für TextRenderer implementieren, die von der [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) -Schnittstelle abgeleitet ist. Sie müssen Methoden zum Zeichnen von Symbol Lauf-, unterstrichen, durchgestrichen, Inline Objekten usw. implementieren. Eine umfassende Liste der Methoden finden Sie auf der Referenzseite zu [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) . Nicht jede Methode muss implementiert werden, Sie kann einfach " **E \_ notimpl**" zurückgeben, und das Zeichnen wird fortgesetzt.

Anschließend können Sie den Text mithilfe der [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode zeichnen und die Rückruf Schnittstelle übergeben, die Sie als Parameter implementiert haben. Die **idwrite-Textlayout::D RAW** -Methode ruft die Methoden des von Ihnen bereitgestellten benutzerdefinierten rendererrückrufs auf. Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**drawunder Line**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)-, [**drawinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)-und [**drawstrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) -Methoden führen die Zeichnungsfunktionen aus.

In ihrer Implementierung von [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)können Sie die [**idwrite-bitmaprendertarget::D rawglyphrun-**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) Methode aufrufen, um die Symbole zu zeichnen. Das Rendering des unterstrichen, durchgestrichen und von Inline Objekten muss von Ihrem benutzerdefinierten Renderer erfolgen.

[**Idwrite-bitmaprendertarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) weist einen optionalen Wiederholungs Parameter auf, der die Begrenzungen des Bereichs enthält, in dem der Text gezeichnet wurde. Sie können diese Informationen verwenden, um das Begrenzungs Rechteck für den Gerätekontext mit der [**setboundsrect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) -Funktion festzulegen, die von GDI bereitgestellt wird. Der folgende Code ist ein Beispiel für die Implementierung der [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode eines benutzerdefinierten Renderers.


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



Die [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Schnittstelle wird in einen Gerätekontext (DC) im Arbeitsspeicher gerendert. Sie erhalten ein Handle für diesen Domänen Controller, indem Sie die [**idschreitebitmaprendertarget:: getmemorydc**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) -Methode verwenden. Sobald die Zeichnung ausgeführt wurde, muss der Speicher-DC des Objekts **idschreitebitmaprendertarget** auf die Ziel-GDI-Oberfläche kopiert werden.

Sie können das umschließende Rechteck mithilfe der [**getboundsrect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) -Funktion abrufen und dann das umschließende Rechteck mit der [**BitBLT**](/windows/win32/api/wingdi/nf-wingdi-bitblt) -Funktion verwenden, um den gerenderten [DirectWrite](direct-write-portal.md) -Text aus dem Arbeitsspeicher-DC auf die GDI-Oberfläche zu kopieren, wie im folgenden Code gezeigt.


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



 

 