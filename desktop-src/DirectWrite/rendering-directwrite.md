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
# <a name="rendering-directwrite"></a>Rendern von DirectWrite

## <a name="rendering-options"></a>Renderingoptionen

Text mit Formatierungen, die nur von einem [**idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Objekt beschrieben werden, kann mit [Direct2D](../direct2d/direct2d-portal.md)gerendert werden. es gibt jedoch noch einige weitere Optionen zum Rendern eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts.

Die durch ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt beschriebene Zeichenfolge kann mithilfe der folgenden Methoden gerendert werden.

## <a name="1-render-using-direct2d"></a>1. Rendering mithilfe von Direct2D

Verwenden Sie zum Rendering eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts mithilfe von Direct2D die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode, wie im folgenden Code gezeigt.


```C++
pRT_->DrawTextLayout(
    origin,
    pTextLayout_,
    pBlackBrush_
    );

```



Ausführlichere Informationen zum Zeichnen eines [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts mithilfe von [Direct2D](../direct2d/direct2d-portal.md)finden Sie unter [Getting Started with DirectWrite](getting-started-with-directwrite.md).

## <a name="2-render-using-a-custom-text-renderer"></a>2. renderverwendung eines benutzerdefinierten textrenderers.

Sie werden mit einem benutzerdefinierten Renderer mithilfe der [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode gerengt, die eine von [**idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) abgeleitete Rückruf Schnittstelle als Argument annimmt, wie im folgenden Code gezeigt.


```C++
// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );

```



Die [**idwrite-Textlayout::D RAW**](/windows/win32/api/dwrite/nf-dwrite-idwritetextlayout-draw) -Methode ruft die Methoden des von Ihnen bereitgestellten benutzerdefinierten rendererrückrufs auf. Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun), [**drawunder Line**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawunderline)-, [**drawinlineobject**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawinlineobject)-und [**drawstrikethrough**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawstrikethrough) -Methoden führen die Zeichnungsfunktionen aus.

[**Idwrite tetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) deklariert Methoden zum Zeichnen eines Symbols für das Ausführen, unterstreichen, durchgestrichen und von Inline Objekten. Es ist von der Anwendung bis zur Implementierung dieser Methoden. Wenn Sie einen benutzerdefinierten TextRenderer erstellen, kann die Anwendung beim Rendern von Text zusätzliche Effekte anwenden, z. b. ein benutzerdefiniertes Füll Zeichen Ein Beispiel für einen benutzerdefinierten TextRenderer ist im [DirectWrite-Hallo Welt Beispiel](/samples/browse/?redirectedfrom=MSDN-samples)enthalten.

## <a name="3-render-cleartype-to-a-gdi-surface"></a>3. rendercleartype für eine GDI-Oberfläche.

Das Rendering zu einer GDI-Oberfläche ist ein Beispiel für die Verwendung eines benutzerdefinierten textrenderers. Ein Teil der Arbeit wird jedoch in Form der [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Schnittstelle für Sie ausgeführt.

Um diese Schnittstelle zu erstellen, verwenden Sie die [**idschreitegdiinterop:: deatebitmaprendertarget**](/windows/win32/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget) -Methode.

Die [**DrawGlyphRun-**](/windows/win32/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode Ihres benutzerdefinierten textrenderers Ruft die [**idschreitebitmaprendertarget::D rawglyphrun-**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) Methode auf, um die Symbole zu zeichnen. Das Rendering der unterstrichen, durchgestrichen und Inline Objekte muss von Ihrem benutzerdefinierten Renderer durchgeführt werden.

Die [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Schnittstelle wird in einen Gerätekontext (DC) im Arbeitsspeicher gerendert. Sie erhalten ein Handle für diesen Domänen Controller, indem Sie die [**idschreitebitmaprendertarget:: getmemorydc**](/windows/win32/api/dwrite/nf-dwrite-idwritebitmaprendertarget-getmemorydc) -Methode verwenden.


```C++
memoryHdc = g_pBitmapRenderTarget->GetMemoryDC();
```



Nachdem die Zeichnung ausgeführt wurde, muss der Speicher-DC des [**idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -Objekts auf die Ziel-GDI-Oberfläche kopiert werden.

> [!Note]  
> Sie haben auch die Möglichkeit, die Bitmap auf eine andere Art von Oberfläche zu übertragen, z. b. eine GDI+-Oberfläche.

 


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
> Ihre APP ist dafür verantwortlich, alles im Fenster zu vereinigen. Dies schließt Text und Grafiken ein. Hierfür gibt es eine Leistungs Einbuße. Außerdem ist das Rendering an einen Speicher-DC keine GDI-Hardwarebeschleunigung.

 

Eine ausführlichere Übersicht über die Interaktion mit GDI finden Sie unter Interoperabilität [mit GDI](interoperating-with-gdi.md).

## <a name="4-render-grayscale-text-transparently-to-a-gdi-surface-windows-8-and-later"></a>4. rendersie Graustufen Text transparent auf eine GDI-Oberfläche. (Windows 8 und höher)

Ab Windows 8 können Sie Graustufen Text transparent auf eine GDI-Oberfläche Renderen, um die Leistung zu verbessern. Zu diesem Zweck müssen Sie folgende Schritte ausführen:

1.  Löschen Sie den Speicher-DC zu transparent.
2.  Renderungs Text im Speicher-HDC mithilfe von Graustufen-Antialiasing (dwrite \_ Text \_ Antialias \_ Mode \_ Graustufen).
3.  Verwenden Sie die Funktion [**AlphaBlend**](/windows/win32/api/wingdi/nf-wingdi-alphablend) , um den Speicher-HDC transparent auf dem endgültigen HDC des Ziels zu Renderern.
4.  Wiederholen Sie den Vorgang so oft wie nötig (z. h. einmal pro Glyphe), und zwischen anderen Grafiken können direkt auf den Ziel-HDC gerendert [](/windows/win32/api/wingdi/nf-wingdi-alphablend) werden, ohne dass diese überschrieben werden.


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

[Rendering mithilfe von Direct2D](rendering-by-using-direct2d.md)
</dt> <dt>

[Rendern unter Verwendung eines benutzerdefinierten Textrenderers](how-to-implement-a-custom-text-renderer.md)
</dt> <dt>

[An eine GDI-Oberfläche Renderen](render-to-a-gdi-surface.md)
</dt> <dt>

[Interoperabilität mit GDI](interoperating-with-gdi.md)
</dt> </dl>

 

 