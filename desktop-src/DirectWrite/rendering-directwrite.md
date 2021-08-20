---
title: Rendering DirectWrite
description: Rendering DirectWrite
ms.assetid: e8099fac-b5d7-4fb1-b06d-a6e85da0d1dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa640b8963c427b9eaf1d17fd3e4691115a3965d477c5076deb1f5eb05a569db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119070590"
---
# <a name="rendering-directwrite"></a>Rendering DirectWrite

## <a name="rendering-options"></a>Renderingoptionen

Text mit Formatierung, der nur von einem [**IDWriteTextFormat-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) beschrieben wird, kann mit [Direct2D](../direct2d/direct2d-portal.md)gerendert werden. Es gibt jedoch noch einige weitere Optionen zum Rendern eines [**IDWriteTextLayout-Objekts.**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)

Die von einem [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) beschriebene Zeichenfolge kann mit den unten angegebenen Methoden gerendert werden.

## <a name="1-render-using-direct2d"></a>1. Rendern mit Direct2D

Um ein [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mit Direct2D zu rendern, verwenden Sie die [**ID2D1RenderTarget::D rawTextLayout-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) wie im folgenden Code gezeigt.


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



Einen detaillierteren Einblick in das Zeichnen eines [**IDWriteTextLayout-Objekts**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) mit [Direct2D](../direct2d/direct2d-portal.md)finden Sie unter Erste Schritte [mit DirectWrite.](getting-started-with-directwrite.md)

## <a name="2-render-using-a-custom-text-renderer"></a>2. Rendern mit einem benutzerdefinierten Textrenderer.

Sie rendern mit einem benutzerdefinierten Renderer mithilfe der [**IDWriteTextLayout::D raw-Methode,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) die eine von [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) abgeleitete Rückrufschnittstelle als Argument verwendet, wie im folgenden Code gezeigt.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



Die [**IDWriteTextLayout::D raw-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) ruft die Methoden des von Ihnen zur Verfügung stellenden benutzerdefinierten Rendererrückrufs auf. Die [**DrawGlyphRun-,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) [**DrawUnderline-,**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline) [**DrawInlineObject-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)und [**DrawStrikethrough-Methoden**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) führen die Zeichnungsfunktionen aus.

[**IDWriteTextRenderer deklariert**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) Methoden zum Zeichnen eines Glyphenlaufs, einer Unterstreichung, eines Durchstrichs und von Inlineobjekten. Diese Methoden müssen von der Anwendung implementiert werden. Durch das Erstellen eines benutzerdefinierten Textrenderers kann die Anwendung beim Rendern von Text zusätzliche Effekte anwenden, z. B. eine benutzerdefinierte Füllung oder Kontur. Ein benutzerdefinierter Beispieltextrenderer ist im Beispiel DirectWrite Hallo Welt [enthalten.](/samples/browse/?redirectedfrom=MSDN-samples)

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. Rendern von ClearType auf eine GDI-Oberfläche.

Das Rendern auf einer GDI-Oberfläche ist tatsächlich ein Beispiel für die Verwendung eines benutzerdefinierten Textrenderers. Ein Teil der Arbeit wird jedoch in Form der [**IDWriteBitmapRenderTarget-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) für Sie erledigt.

Verwenden Sie zum Erstellen dieser Schnittstelle die [**IDWriteGdiInterop::CreateBitmapRenderTarget-Methode.**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)

Die [**DrawGlyphRun-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Ihres benutzerdefinierten Textrenderers ruft die [**IDWriteBitmapRenderTarget::D rawGlyphRun-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) auf, um die Glyphen zu zeichnen. Das Rendern der Unterstreichungs-, Durchstreich- und Inlineobjekte muss von Ihrem benutzerdefinierten Renderer durchgeführt werden.

Die [**IDWriteBitmapRenderTarget-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) wird in einem Gerätekontext (DC) im Arbeitsspeicher gerendert. Sie erhalten mithilfe der [**IDWriteBitmapRenderTarget::GetMemoryDC-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) ein Handle für diesen DC.


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



Nachdem die Zeichnung durchgeführt wurde, muss der Arbeitsspeicher-DC des [**IDWriteBitmapRenderTarget-Objekts**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) auf die GDI-Zieloberfläche kopiert werden.

> [!Note]  
> Sie haben auch die Möglichkeit, die Bitmap auf eine andere Art von Oberfläche zu übertragen, z. B. GDI+ Oberfläche.

 


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
> Ihre App ist dafür verantwortlich, am Ende alles im Fenster zu rendern. Dies schließt Text und Grafiken ein. Dies hat eine Leistungsstrafe. Darüber hinaus wird das Rendern auf einem Speicherdomänencontroller nicht durch GDI-Hardware beschleunigt.

 

Eine ausführlichere Übersicht über die Interoperabilität mit GDI finden Sie unter [Interoperating with GDI (Interoperabilität mit GDI).](interoperating-with-gdi.md)

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. Transparentes Rendern von Graustufentext auf einer GDI-Oberfläche. (Windows 8 und höher)

Ab Windows 8 können Sie Graustufentext transparent auf einer GDI-Oberfläche rendern, um eine bessere Leistung zu erzielen. Dazu müssen Sie:

1.  Löschen Sie den Arbeitsspeicher-DC in transparent.
2.  Rendern von Text im HDC-Arbeitsspeicher mit Graustufen-Antialiasing (DWRITE \_ TEXT \_ ANTIALIAS \_ MODE \_ GRAYSCALE).
3.  Verwenden Sie [**die AlphaBlend-Funktion,**](/windows/win32/api/wingdi/nf-wingdi-alphablend) um den HDC des Arbeitsspeichers transparent über dem endgültigen HDC-Ziel zu rendern.
4.  Wiederholen Sie sich so oft wie nötig (z. B. einmal pro Glyphenlauf), und dazwischen können andere Grafiken direkt auf dem endgültigen ZIEL-HDC gerendert werden, ohne von der [**AlphaBlend-Funktion überschrieben zu**](/windows/win32/api/wingdi/nf-wingdi-alphablend) werden.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Rendern mit Direct2D](rendering-by-using-direct2d.md)
</dt> <dt>

[Rendern unter Verwendung eines benutzerdefinierten Textrenderers](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[Rendern auf einer GDI-Oberfläche](render-to-a-gdi-surface.md)
</dt> <dt>

[Interoperabilität mit GDI](interoperating-with-gdi.md)
</dt> </dl>

 

 