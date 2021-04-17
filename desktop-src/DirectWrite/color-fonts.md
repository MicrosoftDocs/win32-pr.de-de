---
title: Farbige Schriftarten
description: In diesem Thema werden Farb Schriftarten, ihre Unterstützung in DirectWrite und Direct2D und deren Verwendung in Ihrer APP beschrieben.
ms.assetid: 74e096c4-9d1c-8854-e9ee-f8b11ac1c71a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6774089cc1f0bed1349edc940c6a1ae715d052c7
ms.sourcegitcommit: 3d9dce1bd6c84e2b51759e940aa95aa9b459cd20
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "104556367"
---
# <a name="color-fonts"></a>Farbige Schriftarten

In diesem Thema werden Farb Schriftarten, ihre Unterstützung in DirectWrite und Direct2D und deren Verwendung in Ihrer APP beschrieben.

Dieses Dokument enthält die folgenden Teile:

-   [Was sind Farb Schriftarten?](#what-are-color-fonts)
-   [Gründe für die Verwendung von Farb Schriftarten](#why-use-color-fonts)
-   [Welche Arten von Farb Schriftarten werden von Windows unterstützt?](#what-kinds-of-color-fonts-does-windows-support)
-   [Verwenden von Farb Schriftarten](#using-color-fonts)
    -   [Verwenden von Farb Schriftarten in einer XAML-App](#using-color-fonts-in-a-xaml-app)
    -   [Verwenden von Farb Schriftarten in Microsoft Edge](#using-color-fonts-in-microsoft-edge)
    -   [Verwenden von Color-Schriftarten mit DirectWrite und Direct2D](#using-color-fonts-with-directwrite-and-direct2d)
    -   [Verwenden von Color Fonts mit Win2D](#using-color-fonts-with-win2d)
-   [Zugehörige Themen](#related-topics)

## <a name="what-are-color-fonts"></a>Was sind Farb Schriftarten?

Farb Schriftarten, auch als mehrfarbige Schriftarten oder als chromatische Schriftarten bezeichnet, sind eine Schriftart Technologie, mit der Schriftart Designer in jedem Symbol mehrere Farben verwenden können. Farb Schriftarten ermöglichen mehrfarbige Text Szenarien in apps und Websites mit weniger Code und stabiler Betriebssystemunterstützung als Ad-hoc-Techniken, die oberhalb des Text Rendering-Systems implementiert werden.

Die Schriftarten, mit denen Sie wahrscheinlich am besten vertraut sind, sind keine Farb Schriftarten. Diese Schriftarten definieren nur die Form der Symbole, die Sie enthalten, entweder mit Vektor Umschlägen oder monochromen Bitmaps. Zur zeichnungszeit füllt ein TextRenderer die Form "Symbol" mit einer einzelnen Farbe (der Schriftfarbe), die durch die zu rendernde APP oder das gerenderte Dokument angegeben wird. Farb Schriftarten enthalten dagegen neben Form Informationen auch Farbinformationen. Bei manchen Ansätzen können Schriftarten Designer mehrere Farbpaletten anbieten, sodass Sie die Farbe für die künstlerische Flexibilität bereitstellen.

Das folgende Beispiel zeigt ein Symbol aus der Segoe UI Emoji Color-Schriftart. Das Symbol wird auf der linken Seite in Monochrom und in Farbe auf der rechten Seite gerendert.

![Zeigt parallele Symbole an, das linke Symbol, das in Monochrom gerendert wird, das Recht in der Schriftart "Bild-auf-der-Farbe I I Emoji Color".](images/color-font-cat.png)

Farb Schriftarten enthalten in der Regel Fall Back Informationen für Plattformen, die keine Farb Schriftarten unterstützen, oder für Szenarios, in denen die Farb Funktionalität deaktiviert wurde. Auf diesen Plattformen werden Farb Schriftarten als reguläre, monochrome Schriftarten gerendert.

## <a name="why-use-color-fonts"></a>Gründe für die Verwendung von Farb Schriftarten

In der Vergangenheit haben Designer und Entwickler eine Reihe von Techniken zum Erreichen von mehrfarbigem Text verwendet. Websites verwenden z. b. häufig Rasterbilder anstelle von Text, um umfangreiche Header anzuzeigen. Diese Vorgehensweise ermöglicht die künstlerische Flexibilität, aber Rastergrafiken können nicht für alle Anzeige Größen skaliert werden, und Sie bieten nicht dieselben Barrierefreiheits Funktionen wie echten Text. Eine andere gängige Methode besteht darin, mehrere monochrome Schriftarten in unterschiedlichen Schriftfarben zu überlagern, dies erfordert jedoch in der Regel zusätzlichen Layoutcode zur Verwaltung.

Farb Schriftarten bieten eine Möglichkeit, diese visuellen Effekte mit der Einfachheit und Funktionalität regulärer Schriftarten zu erzielen. Text, der in einer Farb Schriftart gerendert wird, ist identisch mit dem anderen Text: er kann kopiert und eingefügt werden, er kann durch Barrierefreiheits Tools analysiert werden usw.

## <a name="what-kinds-of-color-fonts-does-windows-support"></a>Welche Arten von Farb Schriftarten werden von Windows unterstützt?

Die [OpenType-Spezifikation](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) definiert mehrere Möglichkeiten, Farbinformationen in eine Schriftart einzubetten. Ab Windows 10 Anniversary Update unterstützen DirectWrite und Direct2D (und die darauf basierenden Windows-Frameworks) all diese Ansätze. Sie werden in der folgenden Tabelle zusammengefasst:



| Verfahren                                                                                                                        | Beschreibung                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Colr](/typography/opentype/spec/colr) / [CPAL](/typography/opentype/spec/cpal) -Tabellen | Verwendet Schichten farbiger Vektoren, deren Formen auf die gleiche Weise definiert sind wie Symbole mit einem Farben Symbol. **Hinweis:** Unterstützt ab Windows 8.1. <br/>                                                                                                                                                 |
| [SVG](/typography/opentype/spec/svg) -Tabelle                                                                 | Verwendet Vektorbilder, die im skalierbaren Vektorgrafik Format erstellt wurden. **Hinweis:** Ab Windows 10 Anniversary Update unterstützt DirectWrite eine Teilmenge der vollständigen SVG-Spezifikation. Nicht alle SVG-Inhalte werden garantiert in einer OpenType SVG-Schriftart dargestellt. Weitere Informationen finden Sie [unter SVG-Unterstützung](../direct2d/svg-support.md) . <br/> |
| [Cbdt](/typography/opentype/spec/cbdt) / [CBLC](/typography/opentype/spec/cblc) -Tabellen | Verwendet eingebettete Farb Bitmap-Bilder.                                                                                                                                                                                                                                                                                |
| [sbix](/typography/opentype/spec/sbix) -Tabelle                                                               | Verwendet eingebettete Farb Bitmap-Bilder.                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a>Verwenden von Farb Schriftarten

Aus Sicht des Benutzers sind Farb Schriftarten nur Schriftarten. Sie können z. b. normalerweise auf die gleiche Weise wie Mono basierte Schriftarten vom System installiert und deinstalliert werden, und Sie werden als regulärer, auswählbarer Text gerendert.

Aus der Perspektive des Entwicklers werden Farb Schriftarten in der Regel auf dieselbe Weise wie Mono basierte Schriftarten verwendet. In den XAML-und Microsoft Edge-Frameworks können Sie Ihren Text mit Farb Schriftarten auf die gleiche Weise wie reguläre Schriftarten formatieren, und der Text wird standardmäßig in Farbe gerendert. Wenn Ihre APP jedoch Direct2D-APIs (oder Win2D-APIs) direkt zum Rendern von Text aufruft, muss Sie explizit das Farb Schriftart Rendering anfordern.

### <a name="using-color-fonts-in-a-xaml-app"></a>Verwenden von Farb Schriftarten in einer XAML-App

Die Textelemente der XAML-Plattform (z. b. [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [richeditbox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphen](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)und [fonticon](/uwp/api/windows.ui.xaml.controls.fonticon)) unterstützen standardmäßig Farb Schriftarten. Formatieren Sie einfach den Text mit einer Farb Schriftart, und alle Farbsymbole werden in Farbe gerendert. Das folgende Codebeispiel zeigt eine Möglichkeit, einen TextBlock mit einer Farb Schriftart zu formatieren, die mit Ihrer APP verpackt ist. Dasselbe Verfahren gilt für reguläre Schriftarten.


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



Wenn Sie nicht möchten, dass das XAML-Textelement mehrfarbigen Text darstellt, legen Sie dessen [iscolorfontenabledproperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) -Eigenschaft auf false fest.

### <a name="using-color-fonts-in-microsoft-edge"></a>Verwenden von Farb Schriftarten in Microsoft Edge

Farb Schriftarten werden standardmäßig in Websites und Web-Apps gerendert, die auf Microsoft Edge ausgeführt werden, einschließlich des XAML- [WebView](/uwp/api/windows.ui.xaml.controls.webview) -Steuer Elements Verwenden Sie einfach HTML und CSS, um Ihren Text mit einer Farb Schriftart zu formatieren, und alle Farbsymbole werden in Farbe gerendert.

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a>Verwenden von Color-Schriftarten mit DirectWrite und Direct2D

Ihre APP kann Direct2D s auf höherer Ebene Text Zeichnungs Methoden ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) und [**drawtextlayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) verwenden, oder es können Methoden auf niedrigerer Ebene verwendet werden, um Glyphe direkt zu zeichnen. In beiden Fällen ist für Ihre APP Codeänderungen erforderlich, damit Farbsymbole ordnungsgemäß verarbeitet werden. Wenn Ihre APP Direct2D s **DrawText** -und **drawtextlayout** -APIs verwendet, beachten Sie, dass diese standardmäßig keine Farbsymbole darstellen. Dadurch werden unerwartete Verhaltensänderungen bei Text Rendering-apps vermieden, die vor der Farb Schriftart Unterstützung entworfen wurden.

Um das Farb Symbol Rendering zu aktivieren, übergeben Sie das Flag " [**D2D1 \_ Draw \_ Text \_ Optionen \_ enable \_ Color \_ Font**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) Options" an die Zeichnungs Methode. Im folgenden Codebeispiel wird gezeigt, wie die DrawText-Methode Direct2D s aufgerufen wird, um eine Zeichenfolge in einer Farb Schriftart zu erzeugen:


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



Wenn Ihre APP APIs auf niedrigerer Ebene verwendet, um Glyphe direkt zu verarbeiten, funktioniert Sie weiterhin, wenn Farb Schriftarten vorhanden sind, aber es ist nicht möglich, Farbsymbole ohne zusätzliche Logik zu zeichnen.

Um Farbsymbole ordnungsgemäß zu verarbeiten, sollte Ihre APP folgende Aktionen ausführen:

1.  Übergeben Sie die Symbol laufinformationen an [**translatecolorglyphrun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), zusammen mit einem [**dwrite-Symbol für \_ \_ Bild \_ Formate**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) , das angibt, welche Typen von Farbsymbolen von der APP verarbeitet werden sollen. Wenn beliebige Farbsymbole vorhanden sind (basierend auf der Schriftart und den angeforderten **dwrite- \_ Glyphe- \_ Bild \_ Formaten**), teilt DirectWrite die Ausführung des primären Symbols in einzelne farbglyphe auf, auf die über das zurückgegebene [**idwrite-colorglyphrunenumerator**](idwritecolorglyphrunenumerator.md) -Objekt in Schritt 4 zugegriffen werden kann.
2.  Überprüfen Sie das von [**translatecolorglyphrun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) zurückgegebene HRESULT, um zu bestimmen, ob farbglyphe erkannt wurden. Ein **HRESULT** von **dwrite \_ E \_ nocolor** gibt an, dass kein anwendbares Farb Symbol ausgeführt werden darf.
3.  Wenn [**translatecolorglyphrun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) gemeldet hat, dass keine Farb Glyphe ausgeführt wird (durch Zurückgeben von **dwrite \_ E \_ nocolor**), wird die ganze Symbol Ausführung als Mono-basiert behandelt, und Ihre APP sollte Sie wie gewünscht zeichnen (z. b. mithilfe von [**ID2D1DeviceContext::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).
4.  Wenn [**translatecolorglyphrun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) das vorhanden sein von Farb Glyphe meldet, sollte Ihre APP das primäre Symbol ausführen und stattdessen die von translatecolorglyphrun zurückgegebenen Farb Symbol Ausführungen verwenden. Zu diesem Zweck durchlaufen Sie das zurückgegebene [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) -Objekt, wobei jedes ausgeführte Farb Symbol abgerufen und nach Bedarf für sein Symbolbild Format gezeichnet wird (Sie können z. b. [**drawcolorbitmapglyphrun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) und [**drawsvgglyphrun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) verwenden, um Farb Bitmap-Symbole bzw. SVG-Symbole zu zeichnen).

Das folgende Codebeispiel zeigt die allgemeine Struktur dieses Verfahrens:


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



### <a name="using-color-fonts-with-win2d"></a>Verwenden von Color Fonts mit Win2D

Ähnlich wie Direct2D werden in Win2D s Text Zeichnungs-APIs standardmäßig keine Farbsymbole dargestellt. Um das Farb Symbol Rendering zu aktivieren, legen Sie das Optionen-Flag [enablecolorfont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) im Textformat-Objekt fest, das Ihre APP an die Text Zeichnungs Methode übergibt. Im folgenden Codebeispiel wird gezeigt, wie eine Zeichenfolge in einer Farb Schriftart mithilfe von Win2D dargestellt wird:


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

[Beispiel für das farbige DirectWrite-Symbol](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[**IDWriteFontFace4-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[**IDWriteFactory4:: translatecolorglyphrun-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[**ID2D1DeviceContext4::D rawtext-Methode**](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

