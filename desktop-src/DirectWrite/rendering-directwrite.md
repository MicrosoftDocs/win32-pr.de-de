---
title: Rendern von DirectWrite
description: Rendern von DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc7012bc4861a8befc9beb97c945dc0b03b4e761
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390626"
---
# <a name="rendering-directwrite"></a><span data-ttu-id="2d69a-103">Rendern von DirectWrite</span><span class="sxs-lookup"><span data-stu-id="2d69a-103">Rendering DirectWrite</span></span>

## <a name="rendering-options"></a><span data-ttu-id="2d69a-104">Renderingoptionen</span><span class="sxs-lookup"><span data-stu-id="2d69a-104">Rendering Options</span></span>

<span data-ttu-id="2d69a-105">Text mit Formatierungen, die nur von einem [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt beschrieben werden, kann mit [Direct2D](../direct2d/direct2d-portal.md)gerendert werden. es gibt jedoch noch einige weitere Optionen zum Rendern eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts.</span><span class="sxs-lookup"><span data-stu-id="2d69a-105">Text with formatting described by only an [**IDWriteTextFormat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) object can be rendered with [Direct2D](../direct2d/direct2d-portal.md), however, there are a few more options for rendering an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object.</span></span>

<span data-ttu-id="2d69a-106">Die durch ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt beschriebene Zeichenfolge kann mithilfe der folgenden Methoden gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="2d69a-106">The string described by an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object can be rendered using the methods below.</span></span>

## <a name="1-render-using-direct2d"></a><span data-ttu-id="2d69a-107">1. Rendering mithilfe von Direct2D</span><span class="sxs-lookup"><span data-stu-id="2d69a-107">1. Render using Direct2D</span></span>

<span data-ttu-id="2d69a-108">Verwenden Sie zum Rendering eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts mithilfe von Direct2D die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d69a-108">To render an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using Direct2D, use the [**ID2D1RenderTarget::DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) method, as shown in the following code.</span></span>


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



<span data-ttu-id="2d69a-109">Ausführlichere Informationen zum Zeichnen eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts mithilfe von [Direct2D](../direct2d/direct2d-portal.md)finden Sie unter [Getting Started with DirectWrite](getting-started-with-directwrite.md).</span><span class="sxs-lookup"><span data-stu-id="2d69a-109">For a more in depth look at drawing an [**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) object using [Direct2D](../direct2d/direct2d-portal.md), see [Getting Started with DirectWrite](getting-started-with-directwrite.md).</span></span>

## <a name="2-render-using-a-custom-text-renderer"></a><span data-ttu-id="2d69a-110">2. renderverwendung eines benutzerdefinierten textrenderers.</span><span class="sxs-lookup"><span data-stu-id="2d69a-110">2. Render using a custom text renderer.</span></span>

<span data-ttu-id="2d69a-111">Sie werden mit einem benutzerdefinierten Renderer mithilfe der [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode gerengt, die eine von [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) abgeleitete Rückruf Schnittstelle als Argument annimmt, wie im folgenden Code gezeigt.</span><span class="sxs-lookup"><span data-stu-id="2d69a-111">You render with a custom renderer by using the [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method, which takes a callback interface derived from [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) as an argument, as shown in the following code.</span></span>


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



<span data-ttu-id="2d69a-112">Die [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode ruft die Methoden des von Ihnen bereitgestellten benutzerdefinierten rendererrückrufs auf.</span><span class="sxs-lookup"><span data-stu-id="2d69a-112">The [**IDWriteTextLayout::Draw**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) method calls the methods of the custom renderer callback you provide.</span></span> <span data-ttu-id="2d69a-113">Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**drawunder Line**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)-, [**drawinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)-und [**drawstrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) -Methoden führen die Zeichnungsfunktionen aus.</span><span class="sxs-lookup"><span data-stu-id="2d69a-113">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**DrawUnderline**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline), [**DrawInlineObject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject), and [**DrawStrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) methods perform the drawing functions.</span></span>

<span data-ttu-id="2d69a-114">[**Idwrite tetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) deklariert Methoden zum Zeichnen eines Symbols für das Ausführen, unterstreichen, durchgestrichen und von Inline Objekten.</span><span class="sxs-lookup"><span data-stu-id="2d69a-114">[**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) declares methods for drawing a glyph run, underline, strikethrough, and inline objects.</span></span> <span data-ttu-id="2d69a-115">Es ist von der Anwendung bis zur Implementierung dieser Methoden.</span><span class="sxs-lookup"><span data-stu-id="2d69a-115">It is up to the application to implement these methods.</span></span> <span data-ttu-id="2d69a-116">Wenn Sie einen benutzerdefinierten TextRenderer erstellen, kann die Anwendung beim Rendern von Text zusätzliche Effekte anwenden, z. b. ein benutzerdefiniertes Füll Zeichen</span><span class="sxs-lookup"><span data-stu-id="2d69a-116">Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.</span></span> <span data-ttu-id="2d69a-117">Ein Beispiel für einen benutzerdefinierten TextRenderer ist im [DirectWrite-Hallo Welt Beispiel](/samples/browse/?redirectedfrom=MSDN-samples)enthalten.</span><span class="sxs-lookup"><span data-stu-id="2d69a-117">A sample custom text renderer is included in the [DirectWrite Hello World Sample](/samples/browse/?redirectedfrom=MSDN-samples).</span></span>

## <a name="3-render-cleartype-to-a-gdi-surface"></a><span data-ttu-id="2d69a-118">3. rendercleartype für eine GDI-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="2d69a-118">3. Render ClearType to a GDI surface.</span></span>

<span data-ttu-id="2d69a-119">Das Rendering zu einer GDI-Oberfläche ist ein Beispiel für die Verwendung eines benutzerdefinierten textrenderers.</span><span class="sxs-lookup"><span data-stu-id="2d69a-119">Rendering to a GDI surface is actually an example of using a custom text renderer.</span></span> <span data-ttu-id="2d69a-120">Ein Teil der Arbeit wird jedoch in Form der [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Schnittstelle für Sie ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2d69a-120">However, some of the work is done for you in the form of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface.</span></span>

<span data-ttu-id="2d69a-121">Um diese Schnittstelle zu erstellen, verwenden Sie die [**idschreitegdiinterop:: deatebitmaprendertarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) -Methode.</span><span class="sxs-lookup"><span data-stu-id="2d69a-121">To create this interface, use the [**IDWriteGdiInterop::CreateBitmapRenderTarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) method.</span></span>

<span data-ttu-id="2d69a-122">Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode Ihres benutzerdefinierten textrenderers Ruft die [**idschreitebitmaprendertarget::D rawglyphrun-**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) Methode auf, um die Symbole zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="2d69a-122">The [**DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) method of your custom text renderer calls the [**IDWriteBitmapRenderTarget::DrawGlyphRun**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) method to draw the glyphs.</span></span> <span data-ttu-id="2d69a-123">Das Rendering der unterstrichen, durchgestrichen und Inline Objekte muss von Ihrem benutzerdefinierten Renderer durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="2d69a-123">The rendering of the underline, strikethrough, and inline objects must be done by your custom renderer.</span></span>

<span data-ttu-id="2d69a-124">Die [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Schnittstelle wird in einen Gerätekontext (DC) im Arbeitsspeicher gerendert.</span><span class="sxs-lookup"><span data-stu-id="2d69a-124">The [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) interface renders to a device context (DC) in memory.</span></span> <span data-ttu-id="2d69a-125">Sie erhalten ein Handle für diesen Domänen Controller, indem Sie die [**idschreitebitmaprendertarget:: getmemorydc**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) -Methode verwenden.</span><span class="sxs-lookup"><span data-stu-id="2d69a-125">You get a handle to this DC by using the [**IDWriteBitmapRenderTarget::GetMemoryDC**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) method.</span></span>


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



<span data-ttu-id="2d69a-126">Nachdem die Zeichnung ausgeführt wurde, muss der Speicher-DC des [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Objekts auf die Ziel-GDI-Oberfläche kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="2d69a-126">Once the drawing has been performed, the memory DC of the [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) object must be copied to the destination GDI surface.</span></span>

> [!Note]  
> <span data-ttu-id="2d69a-127">Sie haben auch die Möglichkeit, die Bitmap auf eine andere Art von Oberfläche zu übertragen, z. b. eine GDI+-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="2d69a-127">You also have the option of transferring the bitmap to another type of surface, such as a GDI+ surface.</span></span>

 


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



> [!Note]  
> <span data-ttu-id="2d69a-128">Ihre APP ist dafür verantwortlich, alles im Fenster zu vereinigen.</span><span class="sxs-lookup"><span data-stu-id="2d69a-128">Your app has the responsibility to render everything to the window in the end.</span></span> <span data-ttu-id="2d69a-129">Dies schließt Text und Grafiken ein.</span><span class="sxs-lookup"><span data-stu-id="2d69a-129">This includes text and graphics.</span></span> <span data-ttu-id="2d69a-130">Hierfür gibt es eine Leistungs Einbuße.</span><span class="sxs-lookup"><span data-stu-id="2d69a-130">There is a performance penalty to this.</span></span> <span data-ttu-id="2d69a-131">Außerdem ist das Rendering an einen Speicher-DC keine GDI-Hardwarebeschleunigung.</span><span class="sxs-lookup"><span data-stu-id="2d69a-131">Additionally, rendering to a memory DC is not GDI hardware accelerated.</span></span>

 

<span data-ttu-id="2d69a-132">Eine ausführlichere Übersicht über die Interaktion mit GDI finden Sie unter Interoperabilität [mit GDI](interoperating-with-gdi.md).</span><span class="sxs-lookup"><span data-stu-id="2d69a-132">For a more detailed overview of interoperating with GDI see [Interoperating with GDI](interoperating-with-gdi.md).</span></span>

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a><span data-ttu-id="2d69a-133">4. rendersie Graustufen Text transparent auf eine GDI-Oberfläche.</span><span class="sxs-lookup"><span data-stu-id="2d69a-133">4. Render Grayscale Text Transparently to a GDI Surface.</span></span> <span data-ttu-id="2d69a-134">(Windows 8 und höher)</span><span class="sxs-lookup"><span data-stu-id="2d69a-134">(Windows 8 and later)</span></span>

<span data-ttu-id="2d69a-135">Ab Windows 8 können Sie Graustufen Text transparent auf eine GDI-Oberfläche Renderen, um die Leistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="2d69a-135">Starting in Windows 8, you can render grayscale text transparently to a GDI surface for better performance.</span></span> <span data-ttu-id="2d69a-136">Zu diesem Zweck müssen Sie folgende Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="2d69a-136">To do this you need to:</span></span>

1.  <span data-ttu-id="2d69a-137">Löschen Sie den Speicher-DC zu transparent.</span><span class="sxs-lookup"><span data-stu-id="2d69a-137">Clear the memory DC to transparent.</span></span>
2.  <span data-ttu-id="2d69a-138">Renderungs Text im Speicher-HDC mithilfe von Graustufen-Antialiasing (dwrite \_ Text \_ Antialias \_ Mode \_ Graustufen).</span><span class="sxs-lookup"><span data-stu-id="2d69a-138">Render text to the memory HDC using grayscale antialiasing (DWRITE\_TEXT\_ANTIALIAS\_MODE\_GRAYSCALE).</span></span>
3.  <span data-ttu-id="2d69a-139">Verwenden Sie die Funktion [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) , um den Speicher-HDC transparent auf dem endgültigen HDC des Ziels zu Renderern.</span><span class="sxs-lookup"><span data-stu-id="2d69a-139">Use the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function to render the memory HDC transparently on top of the final target HDC.</span></span>
4.  <span data-ttu-id="2d69a-140">Wiederholen Sie den Vorgang so oft wie nötig (z. h. einmal pro Glyphe), und zwischen anderen Grafiken können direkt auf den Ziel-HDC gerendert [](/windows/win32/api/wingdi/nf-wingdi-alphablend) werden, ohne dass diese überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="2d69a-140">Repeat as many times as necessary (say, once per glyph run) and in between other graphics may be rendered directly to the final target HDC without being overwritten by the [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) function.</span></span>


```C++
pRT_->SetTextAntialiasMode(DWRITE_TEXT_ANTIALIAS_MODE_GRAYSCALE);

pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

BLENDFUNCTION blendFunction = { 0 };  
blendFunction.BlendOp = AC_SRC_OVER;  
blendFunction.SourceConstantAlpha = 255;  
blendFunction.AlphaFormat = AC_SRC_ALPHA;

AlphaBlend(  
        hdc,  
        0, 0,  
        width, height,  
        pRT_->GetMemoryDC(),  
        0, 0,  
        width, height,  
        blendFunction  
        );

```



## <a name="related-topics"></a><span data-ttu-id="2d69a-141">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2d69a-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d69a-142">Rendering mithilfe von Direct2D</span><span class="sxs-lookup"><span data-stu-id="2d69a-142">Render Using Direct2D</span></span>](rendering-by-using-direct2d.md)
</dt> <dt>

[<span data-ttu-id="2d69a-143">Rendern unter Verwendung eines benutzerdefinierten Textrenderers</span><span class="sxs-lookup"><span data-stu-id="2d69a-143">Render Using a Custom Text Renderer</span></span>](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[<span data-ttu-id="2d69a-144">An eine GDI-Oberfläche Renderen</span><span class="sxs-lookup"><span data-stu-id="2d69a-144">Render to a GDI surface</span></span>](render-to-a-gdi-surface.md)
</dt> <dt>

[<span data-ttu-id="2d69a-145">Interoperabilität mit GDI</span><span class="sxs-lookup"><span data-stu-id="2d69a-145">Interoperating with GDI</span></span>](interoperating-with-gdi.md)
</dt> </dl>

 

 