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
# <a name="render-to-a-gdi-surface"></a><span data-ttu-id="d17d7-103">An eine GDI-Oberfläche Renderen</span><span class="sxs-lookup"><span data-stu-id="d17d7-103">Render to a GDI Surface</span></span>

<span data-ttu-id="d17d7-104">In einigen Fällen möchten Sie möglicherweise in der Lage sein, [DirectWrite](direct-write-portal.md) -Text auf einer GDI-Oberfläche anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d17d7-104">In some cases, you may want to be able to display [DirectWrite](direct-write-portal.md) text on a GDI surface.</span></span> <span data-ttu-id="d17d7-105">Die [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Schnittstelle kapselt eine Bitmap und einen Gerätekontext zum renderingtext.</span><span class="sxs-lookup"><span data-stu-id="d17d7-105">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface encapsulates a bitmap and device context to render text onto.</span></span> <span data-ttu-id="d17d7-106">Sie erstellen ein **idwrite-bitmaprendertarget** -Objekt, indem Sie die [**idschreitegdiinterop:: deatebitmaprendertarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) -Methode verwenden, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d17d7-106">You create an **IDWriteBitmapRenderTarget** by using the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method, as shown in the following code.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = g_pGdiInterop->CreateBitmapRenderTarget(hdc, r.right, r.bottom, &g_pBitmapRenderTarget);
}
```



<span data-ttu-id="d17d7-107">Um mit [**idwrite-bitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget)geresgt werden zu können, müssen Sie eine benutzerdefinierte Rückruf Schnittstelle für TextRenderer implementieren, die von der [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) -Schnittstelle abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="d17d7-107">To render with an [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget), you must implement a custom text renderer callback interface derived from the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) interface.</span></span> <span data-ttu-id="d17d7-108">Sie müssen Methoden zum Zeichnen von Symbol Lauf-, unterstrichen, durchgestrichen, Inline Objekten usw. implementieren.</span><span class="sxs-lookup"><span data-stu-id="d17d7-108">You must implement methods for drawing a glyph run, underline, strikethrough, inline objects, and so on.</span></span> <span data-ttu-id="d17d7-109">Eine umfassende Liste der Methoden finden Sie auf der Referenzseite zu [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) .</span><span class="sxs-lookup"><span data-stu-id="d17d7-109">For a complete list of the methods, see the [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) reference page.</span></span> <span data-ttu-id="d17d7-110">Nicht jede Methode muss implementiert werden, Sie kann einfach " **E \_ notimpl**" zurückgeben, und das Zeichnen wird fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="d17d7-110">Not every method must be implemented, they can just return **E\_NOTIMPL**, and drawing will continue.</span></span>

<span data-ttu-id="d17d7-111">Anschließend können Sie den Text mithilfe der [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode zeichnen und die Rückruf Schnittstelle übergeben, die Sie als Parameter implementiert haben.</span><span class="sxs-lookup"><span data-stu-id="d17d7-111">You can then draw the text by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method and passing the callback interface that you implemented as a parameter.</span></span> <span data-ttu-id="d17d7-112">Die **idwrite-Textlayout::D RAW** -Methode ruft die Methoden des von Ihnen bereitgestellten benutzerdefinierten rendererrückrufs auf.</span><span class="sxs-lookup"><span data-stu-id="d17d7-112">The **IDWriteTextLayout::Draw** method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="d17d7-113">Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**drawunder Line**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)-, [**drawinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)-und [**drawstrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) -Methoden führen die Zeichnungsfunktionen aus.</span><span class="sxs-lookup"><span data-stu-id="d17d7-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="d17d7-114">In ihrer Implementierung von [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun)können Sie die [**idwrite-bitmaprendertarget::D rawglyphrun-**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) Methode aufrufen, um die Symbole zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="d17d7-114">In your implementation of [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), call the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="d17d7-115">Das Rendering des unterstrichen, durchgestrichen und von Inline Objekten muss von Ihrem benutzerdefinierten Renderer erfolgen.</span><span class="sxs-lookup"><span data-stu-id="d17d7-115">The rendering of the underline, strikethrough and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="d17d7-116">[**Idwrite-bitmaprendertarget::D rawglyphrun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) weist einen optionalen Wiederholungs Parameter auf, der die Begrenzungen des Bereichs enthält, in dem der Text gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="d17d7-116">[**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) has an optional RECT out parameter that contains the bounds of the area where the text was drawn.</span></span> <span data-ttu-id="d17d7-117">Sie können diese Informationen verwenden, um das Begrenzungs Rechteck für den Gerätekontext mit der [**setboundsrect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) -Funktion festzulegen, die von GDI bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="d17d7-117">You can use this information to set the bounding rectangle for the device context with the [**SetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-setboundsrect) function that is provided by GDI.</span></span> <span data-ttu-id="d17d7-118">Der folgende Code ist ein Beispiel für die Implementierung der [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode eines benutzerdefinierten Renderers.</span><span class="sxs-lookup"><span data-stu-id="d17d7-118">The following code is an example implementation of the [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of a custom renderer.</span></span>


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



<span data-ttu-id="d17d7-119">Die [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Schnittstelle wird in einen Gerätekontext (DC) im Arbeitsspeicher gerendert.</span><span class="sxs-lookup"><span data-stu-id="d17d7-119">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="d17d7-120">Sie erhalten ein Handle für diesen Domänen Controller, indem Sie die [**idschreitebitmaprendertarget:: getmemorydc**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="d17d7-120">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span> <span data-ttu-id="d17d7-121">Sobald die Zeichnung ausgeführt wurde, muss der Speicher-DC des Objekts **idschreitebitmaprendertarget** auf die Ziel-GDI-Oberfläche kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="d17d7-121">As soon as the drawing has been performed, the memory DC of the **IDWriteBitmapRenderTarget** object must be copied to the destination GDI surface.</span></span>

<span data-ttu-id="d17d7-122">Sie können das umschließende Rechteck mithilfe der [**getboundsrect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) -Funktion abrufen und dann das umschließende Rechteck mit der [**BitBLT**](/windows/win32/api/wingdi/nf-wingdi-bitblt) -Funktion verwenden, um den gerenderten [DirectWrite](direct-write-portal.md) -Text aus dem Arbeitsspeicher-DC auf die GDI-Oberfläche zu kopieren, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d17d7-122">You can retrieve the bounding rectangle by using the [**GetBoundsRect**](/windows/win32/api/wingdi/nf-wingdi-getboundsrect) function, then use the bounding rectangle with the [**BitBlt**](/windows/win32/api/wingdi/nf-wingdi-bitblt) function to copy the rendered [DirectWrite](direct-write-portal.md) text from the memory DC to the GDI surface as shown in the following code.</span></span>


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



 

 