---
title: Farbige Schriftarten
description: In diesem Thema werden Farbschriftarten, ihre Unterstützung in DirectWrite und Direct2D und deren Verwendung in Ihrer App beschrieben.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5c0154e528ab8471d40f4771db5479ca9233320177386adbbd849162dbcd598
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119329524"
---
# <a name="color-fonts"></a>Farbige Schriftarten

In diesem Thema werden Farbschriftarten, ihre Unterstützung in DirectWrite und Direct2D und deren Verwendung in Ihrer App beschrieben.

Dieses Dokument enthält die folgenden Teile:

-   [Was sind Farbschriftarten?](#what-are-color-fonts)
-   [Gründe für die Verwendung von Farbschriftarten](#why-use-color-fonts)
-   [Welche Arten von Farbschriftarten werden Windows unterstützt?](#what-kinds-of-color-fonts-does-windows-support)
-   [Verwenden von Farbschriftarten](#using-color-fonts)
    -   [Verwenden von Farbschriftarten in einer XAML-App](#using-color-fonts-in-a-xaml-app)
    -   [Verwenden von Farbschriftarten in Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Verwenden von Farbschriftarten mit DirectWrite und Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Verwenden von Farbschriftarten mit Win2D](#using-color-fonts-with-win2d)
-   [Zugehörige Themen](#related-topics)

## <a name="what-are-color-fonts"></a>Was sind Farbschriftarten?

Farbschriftarten, die auch als mehrfarbige schriftarten odertic-Schriftarten bezeichnet werden, sind eine Schriftarttechnologie, die es Schriftart-Designern ermöglicht, mehrere Farben in jedem Glyphen zu verwenden. Farbschriftarten ermöglichen mehrfarbige Textszenarien in Apps und Websites mit weniger Code und stabilerer Betriebssystemunterstützung als Ad-hoc-Techniken, die über dem Textrenderingsystem implementiert sind.

Die Schriftarten, mit der Sie wahrscheinlich am besten vertraut sind, sind keine Farbschriftarten. Diese Schriftarten definieren nur die Form der Glyphen, die sie enthalten, entweder mit Vektorgliederungen oder monoischen Bitmaps. Zur Zeichnen-Zeit füllt ein Textrenderer die Glyphenform mit einer einzelnen Farbe (die Schriftfarbe) aus, die von der app oder dem Dokument angegeben wird, die gerendert wird. Farbschriftarten enthalten dagegen zusätzlich zu Forminformationen Farbinformationen. Bei einigen Ansätzen können Schriftart-Designer mehrere Farbpaletten anbieten, was der Farbschriftart Flexibilität gibt.

Das folgende Beispiel zeigt ein Glyphen aus der Segoe UI Emoji-Farbschriftart. Das Glyphen wird links monofarbig und rechts in Farbe gerendert.

![Zeigt nebeneinander glyphen, das linke Glyph in monofarbig gerendert, die rechte in der Segoe U I Emoji-Farbschriftart.](images/color-font-cat.png)

Farbschriftarten enthalten in der Regel Fallbackinformationen für Plattformen, die keine Farbschriftarten unterstützen, oder für Szenarien, in denen die Farbfunktionalität deaktiviert wurde. Auf diesen Plattformen werden Farbschriftarten als reguläre monotone Schriftarten gerendert.

## <a name="why-use-color-fonts"></a>Gründe für die Verwendung von Farbschriftarten

In der Vergangenheit haben Designer und Entwickler eine Vielzahl von Techniken verwendet, um mehrfarbigen Text zu erzielen. Websites verwenden z. B. häufig Rasterbilder anstelle von Text, um umfangreiche Header anzuzeigen. Dieser Ansatz ermöglicht flexibilität, aber Rastergrafiken werden nicht gut auf alle Anzeigegrößen skaliert und bieten auch nicht die gleichen Barrierefreiheitsfeatures wie echter Text. Eine weitere gängige Methode ist das Überlagern mehrerer monotoner Schriftarten in verschiedenen Schriftfarben, aber dies erfordert in der Regel zusätzlichen Layoutcode für die Verwaltung.

Farbschriftarten bieten eine Möglichkeit, diese visuellen Effekte mit der Einfachheit und Funktionalität regulärer Schriftarten zu erzielen. Text, der in einer Farbschriftart gerendert wird, ist identisch mit anderem Text: Er kann kopiert und eingefügt, von Barrierefreiheitstools analysiert werden usw.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>Welche Arten von Farbschriftarten werden Windows unterstützt?

Die [OpenType-Spezifikation](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) definiert mehrere Möglichkeiten zum Einbetten von Farbinformationen in eine Schriftart. Ab Windows 10 Anniversary Update unterstützen DirectWrite und Direct2D (und die darauf erstellten Windows-Frameworks) alle diese Ansätze. Sie sind in der folgenden Tabelle zusammengefasst:



| Verfahren                                                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [COLR](/typography/opentype/spec/colr) / [CPAL-Tabellen](/typography/opentype/spec/cpal) | Verwendet Ebenen von farbigen Vektoren, deren Formen auf die gleiche Weise definiert werden wie einfarbige Glyphengliederungen. **Hinweis:** Unterstützt ab Windows 8.1. <br/>                                                                                                                                                 |
| [SVG-Tabelle](/typography/opentype/spec/svg)                                                                 | Verwendet Vektorbilder, die im Format Scalable Vector Graphics erstellt wurden. **Hinweis:** Ab dem Windows 10 Anniversary Update unterstützt DirectWrite eine Teilmenge der vollständigen SVG-Spezifikation. Nicht alle SVG-Inhalte werden garantiert in einer OpenType SVG-Schriftart gerendert. Weitere [Informationen finden Sie unter SVG-Unterstützung.](../direct2d/svg-support.md) <br/> |
| [BESENT](/typography/opentype/spec/cbdt) / [CBLC-Tabellen](/typography/opentype/spec/cblc) | Verwendet eingebettete Farbbitmapbilder.                                                                                                                                                                                                                                                                                |
| [sbix-Tabelle](/typography/opentype/spec/sbix)                                                               | Verwendet eingebettete Farbbitmapbilder.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Verwenden von Farbschriftarten

Aus Sicht des Benutzers sind Farbschriftarten nur Schriftarten. Beispielsweise können sie in der Regel auf die gleiche Weise wie monotone Schriftarten installiert und aus dem System deinstalliert werden, und sie werden als regulärer, auswählbarer Text gerendert.

Auch aus Entwicklersicht werden Farbschriftarten in der Regel auf die gleiche Weise wie monotone Schriftarten verwendet. In den XAML- und Microsoft Edge-Frameworks können Sie Ihren Text mit Farbschriftarten auf die gleiche Weise formatieren wie reguläre Schriftarten, und Ihr Text wird standardmäßig in Farbe gerendert. Wenn Ihre App jedoch Direct2D-APIs (oder Win2D-APIs) direkt aufruft, um Text zu rendern, muss sie explizit Farbschriftartrendering anfordern.

### <a name="using-color-fonts-in-a-xaml-app"></a>Verwenden von Farbschriftarten in einer XAML-App

Die Textelemente der XAML-Plattform (z. B. [TextBlock,](/uwp/api/windows.ui.xaml.controls.textblock) [TextBox,](/uwp/api/windows.ui.xaml.controls.textbox) [RichEditBox,](/uwp/api/windows.ui.xaml.controls.richeditbox) [Glyphen](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)und [FontIcon)](/uwp/api/windows.ui.xaml.controls.fonticon)unterstützen standardmäßig Farbschriftarten. Formatieren Sie Ihren Text einfach mit einer Farbschriftart, und alle Farbstriche werden in Farbe gerendert. Das folgende Codebeispiel zeigt eine Möglichkeit zum Formatieren eines TextBlock mit einer Farbschriftart, die mit Ihrer App gepackt ist. Das gleiche Verfahren gilt für reguläre Schriftarten.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Wenn Ihr XAML-Textelement niemals mehrfarbigen Text rendern soll, legen Sie dessen [IsColorFontEnabledProperty-Eigenschaft](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) auf FALSE fest.

### <a name="using-color-fonts-in-microsoft-edge"></a>Verwenden von Farbschriftarten in Microsoft Edge

Farbschriftarten werden standardmäßig in Websites und Web-Apps gerendert, die auf Microsoft Edge ausgeführt werden, einschließlich des [XAML-WebView-Steuerelements.](/uwp/api/windows.ui.xaml.controls.webview) Verwenden Sie einfach HTML und CSS, um Ihren Text mit einer Farbschriftart zu formatieren, und alle Farbstriche werden in Farbe gerendert.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Verwenden von Farbschriftarten mit DirectWrite und Direct2D

Ihre App kann direct2D-Textzeichnungsmethoden auf höherer Ebene ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) und [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) oder Techniken auf niedrigerer Ebene verwenden, um Glyphenläufe direkt zu zeichnen. In beiden Fällen erfordert Ihre App Codeänderungen, um Farbglyphen ordnungsgemäß zu behandeln. Wenn Ihre App Die **DrawText-** und **DrawTextLayout-APIs** von Direct2D verwendet, beachten Sie, dass diese standardmäßig keine Farbstriche rendern. Dadurch werden unerwartete Verhaltensänderungen in Textrendering-Apps vermieden, die vor der Unterstützung der Farbschriftart entworfen wurden.

Um das Farbglyphenrendering zu aktivieren, übergeben Sie das [**Optionsflag D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) an die Zeichnungsmethode. Das folgende Codebeispiel zeigt, wie die DrawText-Methode von Direct2D zum Rendern einer Zeichenfolge in einer Farbschriftart aufruft:


```C++
// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_defaultFillBrush. 
m_deviceContext->DrawText( 
    m_string->Data(), 
    m_string->Length(), 
    m_textFormat.Get(), 
    m_layoutRect, 
    m_defaultFillBrush.Get(), 
    D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT 
    );  
    
```



Wenn Ihre App APIs auf niedrigerer Ebene verwendet, um Glyphenläufe direkt zu verarbeiten, funktioniert sie weiterhin bei Vorhandensein von Farbschriftarten, kann aber ohne zusätzliche Logik keine Farbglyphen zeichnen.

Um farbliche Glyphen ordnungsgemäß zu verarbeiten, sollte Ihre App:

1.  Übergeben Sie die Ausführungsinformationen des Glyphen an [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)zusammen mit einem [**DWRITE \_ GLYPH \_ IMAGE \_ FORMATS-Parameter,**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) der angibt, für welche Typen von Farbglyphen die App vorbereitet ist. Wenn Farbglyphen vorhanden sind (basierend auf der Schriftart und den angeforderten **\_ DWRITE-GLYPH-BILDFORMATen), \_ \_** teilt DirectWrite die primäre Glyphe in einzelne Farbglyphenläufe auf, auf die über das zurückgegebene [**IDWriteColorGlyphRunEnumerator-Objekt**](idwritecolorglyphrunenumerator.md) in Schritt 4 zugegriffen werden kann.
2.  Überprüfen Sie das von [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) zurückgegebene HRESULT, um zu ermitteln, ob Farbglyphenläufe erkannt wurden. Ein **HRESULT von** **DWRITE E \_ \_ NOCOLOR** gibt an, dass keine anwendbaren Farbstriche ausgeführt werden.
3.  Wenn [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) keine Farbglyphenläufe gemeldet hat (durch Zurückgeben von **DWRITE \_ E \_ NOCOLOR**), wird die gesamte Glyphen-Ausführung als monolypisch behandelt, und Ihre App sollte sie wie gewünscht zeichnen (z. B. mit [**ID2D1DeviceContext::D rawGlyphRun).**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)
4.  Wenn [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) das Vorhandensein von Farbglyphenläufen berichtet, sollte Ihre App die Ausführung des primären Glyphen ignorieren und stattdessen die von TranslateColorGlyphRun zurückgegebenen Farbglyphenläufe verwenden. Iterieren Sie dazu das zurückgegebene [**IDWriteColorGlyphRunEnumerator1-Objekt,**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) indem Sie die einzelnen Farbglyphenläufe abrufen und entsprechend dem Glyphenbildformat zeichnen (Sie können z. B. [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) und [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) verwenden, um Farbbitmap-Glyphen bzw. SVG-Glyphen zu zeichnen).

Das folgende Codebeispiel zeigt die allgemeine Struktur dieser Prozedur:


```C++
// An example code snippet demonstrating how to use TranslateColorGlyphRun 
// to handle different kinds of color glyphs. This code does not make any 
// actual drawing calls. 
HRESULT DrawGlyphRun( 
    FLOAT baselineOriginX, 
    FLOAT baselineOriginY, 
    DWRITE_MEASURING_MODE measuringMode, 
    _In_ DWRITE_GLYPH_RUN const* glyphRun, 
    _In_ DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription, 
) 
{ 
    // Specify the color glyph formats your app supports. In this example, 
    // the app requests only glyphs defined with PNG or SVG. 
    DWRITE_GLYPH_IMAGE_FORMATS requestedFormats = 
        DWRITE_GLYPH_IMAGE_FORMATS_PNG | DWRITE_GLYPH_IMAGE_FORMATS_SVG; 

    ComPtr<IDWriteColorGlyphRunEnumerator1> glyphRunEnumerator; 
    HRESULT hr = m_dwriteFactory->TranslateColorGlyphRun( 
        D2D1::Point2F(baselineOriginX, baselineOriginY), 
        glyphRun, 
        glyphRunDescription, 
        requestedFormats, // the glyph formats supported by this renderer 
        measuringMode, 
        nullptr, 
        0, 
        &glyphRunEnumerator // on return, may contain color glyph runs 
        ); 

    if (hr == DWRITE_E_NOCOLOR) 
    { 
        // The glyph run has no color glyphs. Draw it as a monochrome glyph 
        // run, for example using the DrawGlyphRun method on a Direct2D 
        // device context. 
    } 
    else 
    { 
        // The glyph run has one or more color glyphs. 
        DX::ThrowIfFailed(hr); 

        // Iterate through the color glyph runs and draw them. 
        for (;;) 
        { 
            BOOL haveRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->MoveNext(&haveRun)); 
            if (!haveRun) 
            { 
                break; 
            } 

            // Retrieve the color glyph run. 
            DWRITE_COLOR_GLYPH_RUN1 const* colorRun; 
            DX::ThrowIfFailed(glyphRunEnumerator->GetCurrentRun(&colorRun)); 

            // Draw the color glyph run depending on its format. 
            switch (colorRun->glyphImageFormat) 
            { 
            case DWRITE_GLYPH_IMAGE_FORMATS_PNG: 
                // Draw the PNG glyph, for example with 
                // ID2D1DeviceContext4::DrawColorBitmapGlyphRun. 
                break; 

            case DWRITE_GLYPH_IMAGE_FORMATS_SVG: 
                // Draw the SVG glyph, for example with 
                // ID2D1DeviceContext4::DrawSvgGlyphRun. 
                break; 

                // ...etc. 
            } 
        } 
    } 

    return hr; 
} 
```



### <a name="using-color-fonts-with-win2d"></a>Verwenden von Farbschriftarten mit Win2D

Ähnlich wie Direct2D rendern Die Textzeichnungs-APIs von Win2D standardmäßig keine Farbstriche. Um das Farbglyphenrendering zu aktivieren, legen Sie das [Optionsflag EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) im Textformatobjekt fest, das Ihre App an die Textzeichnungsmethode übergibt. Das folgende Codebeispiel zeigt, wie sie eine Zeichenfolge mit win2D in einer Farbschriftart rendert:


```C++
// The text format that will be used to draw the text. (Declared elsewhere 
// and initialized elsewhere by the app to point to a color font.) 
CanvasTextFormat m_textFormat; 

// Set the EnableColorFont option. 
m_textFormat.Options = CanvasDrawTextOptions.EnableColorFont; 

// If m_textFormat points to a font with color glyphs, then the following  
// call will render m_string using the color glyphs available in that font. 
// Any monochromatic glyphs will be rendered with m_color. 
args.DrawingSession.DrawText( 
    m_string, 
    m_point, 
    m_color, 
    m_textFormat 
    ); 
```

## <a name="related-topics"></a>Zugehörige Themen

[DirectWrite eines farbigen Glyphenbeispiels](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**IDWriteFontFace4-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**IDWriteFactory4::TranslateColorGlyphRun-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**ID2D1DeviceContext4::D rawText-Methode**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

