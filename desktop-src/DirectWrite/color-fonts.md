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
# <a name="color-fonts"></a><span data-ttu-id="46173-103">Farbige Schriftarten</span><span class="sxs-lookup"><span data-stu-id="46173-103">Color Fonts</span></span>

<span data-ttu-id="46173-104">In diesem Thema werden Farb Schriftarten, ihre Unterstützung in DirectWrite und Direct2D und deren Verwendung in Ihrer APP beschrieben.</span><span class="sxs-lookup"><span data-stu-id="46173-104">This topic describes color fonts, their support in DirectWrite and Direct2D, and how to use them in your app.</span></span>

<span data-ttu-id="46173-105">Dieses Dokument enthält die folgenden Teile:</span><span class="sxs-lookup"><span data-stu-id="46173-105">This document contains the following parts:</span></span>

-   [<span data-ttu-id="46173-106">Was sind Farb Schriftarten?</span><span class="sxs-lookup"><span data-stu-id="46173-106">What are color fonts?</span></span>](#what-are-color-fonts)
-   [<span data-ttu-id="46173-107">Gründe für die Verwendung von Farb Schriftarten</span><span class="sxs-lookup"><span data-stu-id="46173-107">Why use color fonts?</span></span>](#why-use-color-fonts)
-   [<span data-ttu-id="46173-108">Welche Arten von Farb Schriftarten werden von Windows unterstützt?</span><span class="sxs-lookup"><span data-stu-id="46173-108">What kinds of color fonts does Windows support?</span></span>](#what-kinds-of-color-fonts-does-windows-support)
-   [<span data-ttu-id="46173-109">Verwenden von Farb Schriftarten</span><span class="sxs-lookup"><span data-stu-id="46173-109">Using color fonts</span></span>](#using-color-fonts)
    -   [<span data-ttu-id="46173-110">Verwenden von Farb Schriftarten in einer XAML-App</span><span class="sxs-lookup"><span data-stu-id="46173-110">Using color fonts in a XAML app</span></span>](#using-color-fonts-in-a-xaml-app)
    -   [<span data-ttu-id="46173-111">Verwenden von Farb Schriftarten in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="46173-111">Using color fonts in Microsoft Edge</span></span>](#using-color-fonts-in-microsoft-edge)
    -   [<span data-ttu-id="46173-112">Verwenden von Color-Schriftarten mit DirectWrite und Direct2D</span><span class="sxs-lookup"><span data-stu-id="46173-112">Using color fonts with DirectWrite and Direct2D</span></span>](#using-color-fonts-with-directwrite-and-direct2d)
    -   [<span data-ttu-id="46173-113">Verwenden von Color Fonts mit Win2D</span><span class="sxs-lookup"><span data-stu-id="46173-113">Using color fonts with Win2D</span></span>](#using-color-fonts-with-win2d)
-   [<span data-ttu-id="46173-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46173-114">Related topics</span></span>](#related-topics)

## <a name="what-are-color-fonts"></a><span data-ttu-id="46173-115">Was sind Farb Schriftarten?</span><span class="sxs-lookup"><span data-stu-id="46173-115">What are color fonts?</span></span>

<span data-ttu-id="46173-116">Farb Schriftarten, auch als mehrfarbige Schriftarten oder als chromatische Schriftarten bezeichnet, sind eine Schriftart Technologie, mit der Schriftart Designer in jedem Symbol mehrere Farben verwenden können.</span><span class="sxs-lookup"><span data-stu-id="46173-116">Color fonts, also referred to as  multicolored fonts  or  chromatic fonts,  are a font technology that allows font designers to use multiple colors within each glyph.</span></span> <span data-ttu-id="46173-117">Farb Schriftarten ermöglichen mehrfarbige Text Szenarien in apps und Websites mit weniger Code und stabiler Betriebssystemunterstützung als Ad-hoc-Techniken, die oberhalb des Text Rendering-Systems implementiert werden.</span><span class="sxs-lookup"><span data-stu-id="46173-117">Color fonts enable multicolored text scenarios in apps and websites with less code and more robust operating system support than ad-hoc techniques implemented above the text rendering system.</span></span>

<span data-ttu-id="46173-118">Die Schriftarten, mit denen Sie wahrscheinlich am besten vertraut sind, sind keine Farb Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="46173-118">The fonts you are probably most familiar with are not color fonts.</span></span> <span data-ttu-id="46173-119">Diese Schriftarten definieren nur die Form der Symbole, die Sie enthalten, entweder mit Vektor Umschlägen oder monochromen Bitmaps.</span><span class="sxs-lookup"><span data-stu-id="46173-119">These fonts define only the shape of the glyphs they contain, either with vector outlines or monochromatic bitmaps.</span></span> <span data-ttu-id="46173-120">Zur zeichnungszeit füllt ein TextRenderer die Form "Symbol" mit einer einzelnen Farbe (der Schriftfarbe), die durch die zu rendernde APP oder das gerenderte Dokument angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="46173-120">At draw time, a text renderer fills the glyph shape using a single color (the  font color ) specified by the app or document being rendered.</span></span> <span data-ttu-id="46173-121">Farb Schriftarten enthalten dagegen neben Form Informationen auch Farbinformationen.</span><span class="sxs-lookup"><span data-stu-id="46173-121">Color fonts, on the other hand, contain color information in addition to shape information.</span></span> <span data-ttu-id="46173-122">Bei manchen Ansätzen können Schriftarten Designer mehrere Farbpaletten anbieten, sodass Sie die Farbe für die künstlerische Flexibilität bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="46173-122">Some approaches allow font designers to offer multiple color palettes, giving the color font artistic flexibility.</span></span>

<span data-ttu-id="46173-123">Das folgende Beispiel zeigt ein Symbol aus der Segoe UI Emoji Color-Schriftart.</span><span class="sxs-lookup"><span data-stu-id="46173-123">The following example shows a glyph from the Segoe UI Emoji color font.</span></span> <span data-ttu-id="46173-124">Das Symbol wird auf der linken Seite in Monochrom und in Farbe auf der rechten Seite gerendert.</span><span class="sxs-lookup"><span data-stu-id="46173-124">The glyph is rendered in monochrome on the left, and in color on the right.</span></span>

![Zeigt parallele Symbole an, das linke Symbol, das in Monochrom gerendert wird, das Recht in der Schriftart "Bild-auf-der-Farbe I I Emoji Color".](images/color-font-cat.png)

<span data-ttu-id="46173-126">Farb Schriftarten enthalten in der Regel Fall Back Informationen für Plattformen, die keine Farb Schriftarten unterstützen, oder für Szenarios, in denen die Farb Funktionalität deaktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="46173-126">Color fonts typically include fallback information for platforms that do not support color fonts or for scenarios in which color functionality has been disabled.</span></span> <span data-ttu-id="46173-127">Auf diesen Plattformen werden Farb Schriftarten als reguläre, monochrome Schriftarten gerendert.</span><span class="sxs-lookup"><span data-stu-id="46173-127">On those platforms, color fonts are rendered as regular monochromatic fonts.</span></span>

## <a name="why-use-color-fonts"></a><span data-ttu-id="46173-128">Gründe für die Verwendung von Farb Schriftarten</span><span class="sxs-lookup"><span data-stu-id="46173-128">Why use color fonts?</span></span>

<span data-ttu-id="46173-129">In der Vergangenheit haben Designer und Entwickler eine Reihe von Techniken zum Erreichen von mehrfarbigem Text verwendet.</span><span class="sxs-lookup"><span data-stu-id="46173-129">Historically, designers and developers have used a variety of techniques to achieve multicolored text.</span></span> <span data-ttu-id="46173-130">Websites verwenden z. b. häufig Rasterbilder anstelle von Text, um umfangreiche Header anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="46173-130">For example, websites often use raster images instead of text in order to display rich headers.</span></span> <span data-ttu-id="46173-131">Diese Vorgehensweise ermöglicht die künstlerische Flexibilität, aber Rastergrafiken können nicht für alle Anzeige Größen skaliert werden, und Sie bieten nicht dieselben Barrierefreiheits Funktionen wie echten Text.</span><span class="sxs-lookup"><span data-stu-id="46173-131">This approach enables artistic flexibility, but raster graphics do not scale well to all display sizes, nor do they provide the same accessibility features as real text.</span></span> <span data-ttu-id="46173-132">Eine andere gängige Methode besteht darin, mehrere monochrome Schriftarten in unterschiedlichen Schriftfarben zu überlagern, dies erfordert jedoch in der Regel zusätzlichen Layoutcode zur Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="46173-132">Another common technique is to overlay multiple monochromatic fonts in different font colors, but this typically requires extra layout code to manage.</span></span>

<span data-ttu-id="46173-133">Farb Schriftarten bieten eine Möglichkeit, diese visuellen Effekte mit der Einfachheit und Funktionalität regulärer Schriftarten zu erzielen.</span><span class="sxs-lookup"><span data-stu-id="46173-133">Color fonts offer a way to achieve these visual effects with all the simplicity and functionality of regular fonts.</span></span> <span data-ttu-id="46173-134">Text, der in einer Farb Schriftart gerendert wird, ist identisch mit dem anderen Text: er kann kopiert und eingefügt werden, er kann durch Barrierefreiheits Tools analysiert werden usw.</span><span class="sxs-lookup"><span data-stu-id="46173-134">Text rendered in a color font is the same as other text: it can be copied and pasted, it can be parsed by accessibility tools, and so forth.</span></span>

## <a name="what-kinds-of-color-fonts-does-windows-support"></a><span data-ttu-id="46173-135">Welche Arten von Farb Schriftarten werden von Windows unterstützt?</span><span class="sxs-lookup"><span data-stu-id="46173-135">What kinds of color fonts does Windows support?</span></span>

<span data-ttu-id="46173-136">Die [OpenType-Spezifikation](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) definiert mehrere Möglichkeiten, Farbinformationen in eine Schriftart einzubetten.</span><span class="sxs-lookup"><span data-stu-id="46173-136">The [OpenType specification](https://www.microsoft.com/Typography/OpenTypeSpecification.aspx) defines several ways to embed color information in a font.</span></span> <span data-ttu-id="46173-137">Ab Windows 10 Anniversary Update unterstützen DirectWrite und Direct2D (und die darauf basierenden Windows-Frameworks) all diese Ansätze.</span><span class="sxs-lookup"><span data-stu-id="46173-137">Starting in Windows 10 Anniversary Update, DirectWrite and Direct2D (and the Windows frameworks built on them) support all of these approaches.</span></span> <span data-ttu-id="46173-138">Sie werden in der folgenden Tabelle zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="46173-138">They are summarized in the table below:</span></span>



| <span data-ttu-id="46173-139">Verfahren</span><span class="sxs-lookup"><span data-stu-id="46173-139">Technique</span></span>                                                                                                                        | <span data-ttu-id="46173-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="46173-140">Description</span></span>                                                                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="46173-141">[Colr](/typography/opentype/spec/colr) / [CPAL](/typography/opentype/spec/cpal) -Tabellen</span><span class="sxs-lookup"><span data-stu-id="46173-141">[COLR](/typography/opentype/spec/colr)/[CPAL](/typography/opentype/spec/cpal) tables</span></span> | <span data-ttu-id="46173-142">Verwendet Schichten farbiger Vektoren, deren Formen auf die gleiche Weise definiert sind wie Symbole mit einem Farben Symbol.</span><span class="sxs-lookup"><span data-stu-id="46173-142">Uses layers of colored vectors, whose shapes are defined in the same way as single-color glyph outlines.</span></span> <span data-ttu-id="46173-143">**Hinweis:** Unterstützt ab Windows 8.1.</span><span class="sxs-lookup"><span data-stu-id="46173-143">**Note:** Supported starting in Windows 8.1.</span></span> <br/>                                                                                                                                                 |
| <span data-ttu-id="46173-144">[SVG](/typography/opentype/spec/svg) -Tabelle</span><span class="sxs-lookup"><span data-stu-id="46173-144">[SVG](/typography/opentype/spec/svg) table</span></span>                                                                 | <span data-ttu-id="46173-145">Verwendet Vektorbilder, die im skalierbaren Vektorgrafik Format erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="46173-145">Uses vector images authored in the Scalable Vector Graphics format.</span></span> <span data-ttu-id="46173-146">**Hinweis:** Ab Windows 10 Anniversary Update unterstützt DirectWrite eine Teilmenge der vollständigen SVG-Spezifikation. Nicht alle SVG-Inhalte werden garantiert in einer OpenType SVG-Schriftart dargestellt.</span><span class="sxs-lookup"><span data-stu-id="46173-146">**Note:** As of Windows 10 Anniversary Update, DirectWrite supports a subset of the full SVG spec. Not all SVG content is guaranteed to render in an OpenType SVG font.</span></span> <span data-ttu-id="46173-147">Weitere Informationen finden Sie [unter SVG-Unterstützung](../direct2d/svg-support.md) .</span><span class="sxs-lookup"><span data-stu-id="46173-147">See [SVG Support](../direct2d/svg-support.md) for more details.</span></span> <br/> |
| <span data-ttu-id="46173-148">[Cbdt](/typography/opentype/spec/cbdt) / [CBLC](/typography/opentype/spec/cblc) -Tabellen</span><span class="sxs-lookup"><span data-stu-id="46173-148">[CBDT](/typography/opentype/spec/cbdt)/[CBLC](/typography/opentype/spec/cblc) tables</span></span> | <span data-ttu-id="46173-149">Verwendet eingebettete Farb Bitmap-Bilder.</span><span class="sxs-lookup"><span data-stu-id="46173-149">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="46173-150">[sbix](/typography/opentype/spec/sbix) -Tabelle</span><span class="sxs-lookup"><span data-stu-id="46173-150">[sbix](/typography/opentype/spec/sbix) table</span></span>                                                               | <span data-ttu-id="46173-151">Verwendet eingebettete Farb Bitmap-Bilder.</span><span class="sxs-lookup"><span data-stu-id="46173-151">Uses embedded color bitmap images.</span></span>                                                                                                                                                                                                                                                                                |



 

## <a name="using-color-fonts"></a><span data-ttu-id="46173-152">Verwenden von Farb Schriftarten</span><span class="sxs-lookup"><span data-stu-id="46173-152">Using color fonts</span></span>

<span data-ttu-id="46173-153">Aus Sicht des Benutzers sind Farb Schriftarten nur Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="46173-153">From the user s perspective, color fonts are  just fonts .</span></span> <span data-ttu-id="46173-154">Sie können z. b. normalerweise auf die gleiche Weise wie Mono basierte Schriftarten vom System installiert und deinstalliert werden, und Sie werden als regulärer, auswählbarer Text gerendert.</span><span class="sxs-lookup"><span data-stu-id="46173-154">For example, they can usually be installed and uninstalled from the system in the same way as monochromatic fonts, and they are rendered as regular, selectable text.</span></span>

<span data-ttu-id="46173-155">Aus der Perspektive des Entwicklers werden Farb Schriftarten in der Regel auf dieselbe Weise wie Mono basierte Schriftarten verwendet.</span><span class="sxs-lookup"><span data-stu-id="46173-155">From the developer s perspective too, color fonts are usually used the same way as monochromatic fonts.</span></span> <span data-ttu-id="46173-156">In den XAML-und Microsoft Edge-Frameworks können Sie Ihren Text mit Farb Schriftarten auf die gleiche Weise wie reguläre Schriftarten formatieren, und der Text wird standardmäßig in Farbe gerendert.</span><span class="sxs-lookup"><span data-stu-id="46173-156">In the XAML and Microsoft Edge frameworks, you can style your text with color fonts the same way as regular fonts, and by default your text will be rendered in color.</span></span> <span data-ttu-id="46173-157">Wenn Ihre APP jedoch Direct2D-APIs (oder Win2D-APIs) direkt zum Rendern von Text aufruft, muss Sie explizit das Farb Schriftart Rendering anfordern.</span><span class="sxs-lookup"><span data-stu-id="46173-157">However, if your app directly calls Direct2D APIs (or Win2D APIs) to render text, it must explicitly request color font rendering.</span></span>

### <a name="using-color-fonts-in-a-xaml-app"></a><span data-ttu-id="46173-158">Verwenden von Farb Schriftarten in einer XAML-App</span><span class="sxs-lookup"><span data-stu-id="46173-158">Using color fonts in a XAML app</span></span>

<span data-ttu-id="46173-159">Die Textelemente der XAML-Plattform (z. b. [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [richeditbox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphen](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396)und [fonticon](/uwp/api/windows.ui.xaml.controls.fonticon)) unterstützen standardmäßig Farb Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="46173-159">The XAML platform s text elements (such as [TextBlock](/uwp/api/windows.ui.xaml.controls.textblock), [TextBox](/uwp/api/windows.ui.xaml.controls.textbox), [RichEditBox](/uwp/api/windows.ui.xaml.controls.richeditbox), [Glyphs](/uwp/api/windows.ui.xaml.documents.glyphs?f=255&MSPPError=-2147217396), and [FontIcon](/uwp/api/windows.ui.xaml.controls.fonticon)) support color fonts by default.</span></span> <span data-ttu-id="46173-160">Formatieren Sie einfach den Text mit einer Farb Schriftart, und alle Farbsymbole werden in Farbe gerendert.</span><span class="sxs-lookup"><span data-stu-id="46173-160">Simply style your text with a color font, and any color glyphs will be rendered in color.</span></span> <span data-ttu-id="46173-161">Das folgende Codebeispiel zeigt eine Möglichkeit, einen TextBlock mit einer Farb Schriftart zu formatieren, die mit Ihrer APP verpackt ist.</span><span class="sxs-lookup"><span data-stu-id="46173-161">The following code example shows one way to style a TextBlock with a color font packaged with your app.</span></span> <span data-ttu-id="46173-162">Dasselbe Verfahren gilt für reguläre Schriftarten.</span><span class="sxs-lookup"><span data-stu-id="46173-162">The same technique applies to regular fonts.</span></span>


```XML
<TextBlock FontFamily="Assets/TMyColorFont.otf#MyFontFamilyName">Here is some text.</TextBlock>
```



<span data-ttu-id="46173-163">Wenn Sie nicht möchten, dass das XAML-Textelement mehrfarbigen Text darstellt, legen Sie dessen [iscolorfontenabledproperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) -Eigenschaft auf false fest.</span><span class="sxs-lookup"><span data-stu-id="46173-163">If you never want your XAML text element to render multicolored text, set its [IsColorFontEnabledProperty](/uwp/api/windows.ui.xaml.controls.textblock.iscolorfontenabledproperty) property to false.</span></span>

### <a name="using-color-fonts-in-microsoft-edge"></a><span data-ttu-id="46173-164">Verwenden von Farb Schriftarten in Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="46173-164">Using color fonts in Microsoft Edge</span></span>

<span data-ttu-id="46173-165">Farb Schriftarten werden standardmäßig in Websites und Web-Apps gerendert, die auf Microsoft Edge ausgeführt werden, einschließlich des XAML- [WebView](/uwp/api/windows.ui.xaml.controls.webview) -Steuer Elements</span><span class="sxs-lookup"><span data-stu-id="46173-165">Color fonts are rendered by default in websites and web apps running on Microsoft Edge, including the XAML [WebView](/uwp/api/windows.ui.xaml.controls.webview) control.</span></span> <span data-ttu-id="46173-166">Verwenden Sie einfach HTML und CSS, um Ihren Text mit einer Farb Schriftart zu formatieren, und alle Farbsymbole werden in Farbe gerendert.</span><span class="sxs-lookup"><span data-stu-id="46173-166">Simply use HTML and CSS to style your text with a color font, and any color glyphs will be rendered in color.</span></span>

### <a name="using-color-fonts-with-directwrite-and-direct2d"></a><span data-ttu-id="46173-167">Verwenden von Color-Schriftarten mit DirectWrite und Direct2D</span><span class="sxs-lookup"><span data-stu-id="46173-167">Using color fonts with DirectWrite and Direct2D</span></span>

<span data-ttu-id="46173-168">Ihre APP kann Direct2D s auf höherer Ebene Text Zeichnungs Methoden ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) und [**drawtextlayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) verwenden, oder es können Methoden auf niedrigerer Ebene verwendet werden, um Glyphe direkt zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="46173-168">Your app can use Direct2D s higher-level text drawing methods ([**DrawText**](../direct2d/id2d1devicecontext4-drawtext-overload.md) and [**DrawTextLayout**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawtextlayout)) or it can use lower-level techniques to draw glyph runs directly.</span></span> <span data-ttu-id="46173-169">In beiden Fällen ist für Ihre APP Codeänderungen erforderlich, damit Farbsymbole ordnungsgemäß verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="46173-169">In either case, your app requires code changes in order to handle color glyphs correctly.</span></span> <span data-ttu-id="46173-170">Wenn Ihre APP Direct2D s **DrawText** -und **drawtextlayout** -APIs verwendet, beachten Sie, dass diese standardmäßig keine Farbsymbole darstellen.</span><span class="sxs-lookup"><span data-stu-id="46173-170">If your app uses Direct2D s **DrawText** and **DrawTextLayout** APIs, note that these do not render color glyphs by default.</span></span> <span data-ttu-id="46173-171">Dadurch werden unerwartete Verhaltensänderungen bei Text Rendering-apps vermieden, die vor der Farb Schriftart Unterstützung entworfen wurden.</span><span class="sxs-lookup"><span data-stu-id="46173-171">This is to avoid unexpected behavior changes in text rendering apps that were designed prior to color font support.</span></span>

<span data-ttu-id="46173-172">Um das Farb Symbol Rendering zu aktivieren, übergeben Sie das Flag " [**D2D1 \_ Draw \_ Text \_ Optionen \_ enable \_ Color \_ Font**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) Options" an die Zeichnungs Methode.</span><span class="sxs-lookup"><span data-stu-id="46173-172">To opt in to color glyph rendering, pass the [**D2D1\_DRAW\_TEXT\_OPTIONS\_ENABLE\_COLOR\_FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) options flag to the drawing method.</span></span> <span data-ttu-id="46173-173">Im folgenden Codebeispiel wird gezeigt, wie die DrawText-Methode Direct2D s aufgerufen wird, um eine Zeichenfolge in einer Farb Schriftart zu erzeugen:</span><span class="sxs-lookup"><span data-stu-id="46173-173">The following code example shows how to call Direct2D s DrawText method to render a string in a color font:</span></span>


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



<span data-ttu-id="46173-174">Wenn Ihre APP APIs auf niedrigerer Ebene verwendet, um Glyphe direkt zu verarbeiten, funktioniert Sie weiterhin, wenn Farb Schriftarten vorhanden sind, aber es ist nicht möglich, Farbsymbole ohne zusätzliche Logik zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="46173-174">If your app uses lower-level APIs to handle glyph runs directly, then it will continue to function in the presence of color fonts, but it will not be able to draw color glyphs without additional logic.</span></span>

<span data-ttu-id="46173-175">Um Farbsymbole ordnungsgemäß zu verarbeiten, sollte Ihre APP folgende Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="46173-175">To correctly handle color glyphs, your app should:</span></span>

1.  <span data-ttu-id="46173-176">Übergeben Sie die Symbol laufinformationen an [**translatecolorglyphrun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), zusammen mit einem [**dwrite-Symbol für \_ \_ Bild \_ Formate**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) , das angibt, welche Typen von Farbsymbolen von der APP verarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="46173-176">Pass the glyph run information to [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun), along with a [**DWRITE\_GLYPH\_IMAGE\_FORMATS**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) parameter that indicates which type(s) of color glyph the app is prepared to handle.</span></span> <span data-ttu-id="46173-177">Wenn beliebige Farbsymbole vorhanden sind (basierend auf der Schriftart und den angeforderten **dwrite- \_ Glyphe- \_ Bild \_ Formaten**), teilt DirectWrite die Ausführung des primären Symbols in einzelne farbglyphe auf, auf die über das zurückgegebene [**idwrite-colorglyphrunenumerator**](idwritecolorglyphrunenumerator.md) -Objekt in Schritt 4 zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="46173-177">If any color glyphs are present (based on the font and the requested **DWRITE\_GLYPH\_IMAGE\_FORMATS**), then DirectWrite will split the primary glyph run into individual  color glyph runs  which can be accessed through the returned [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) object in Step 4.</span></span>
2.  <span data-ttu-id="46173-178">Überprüfen Sie das von [**translatecolorglyphrun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) zurückgegebene HRESULT, um zu bestimmen, ob farbglyphe erkannt wurden.</span><span class="sxs-lookup"><span data-stu-id="46173-178">Check the HRESULT returned by [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) to determine whether any color glyph runs were detected.</span></span> <span data-ttu-id="46173-179">Ein **HRESULT** von **dwrite \_ E \_ nocolor** gibt an, dass kein anwendbares Farb Symbol ausgeführt werden darf.</span><span class="sxs-lookup"><span data-stu-id="46173-179">An **HRESULT** of **DWRITE\_E\_NOCOLOR** indicates no applicable color glyph run.</span></span>
3.  <span data-ttu-id="46173-180">Wenn [**translatecolorglyphrun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) gemeldet hat, dass keine Farb Glyphe ausgeführt wird (durch Zurückgeben von **dwrite \_ E \_ nocolor**), wird die ganze Symbol Ausführung als Mono-basiert behandelt, und Ihre APP sollte Sie wie gewünscht zeichnen (z. b. mithilfe von [**ID2D1DeviceContext::D rawglyphrun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span><span class="sxs-lookup"><span data-stu-id="46173-180">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) reported no color glyph runs (by returning **DWRITE\_E\_NOCOLOR**), then the whole glyph run is treated as monochromatic, and your app should draw it as desired (for example, using [**ID2D1DeviceContext::DrawGlyphRun**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawglyphrun)).</span></span>
4.  <span data-ttu-id="46173-181">Wenn [**translatecolorglyphrun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) das vorhanden sein von Farb Glyphe meldet, sollte Ihre APP das primäre Symbol ausführen und stattdessen die von translatecolorglyphrun zurückgegebenen Farb Symbol Ausführungen verwenden.</span><span class="sxs-lookup"><span data-stu-id="46173-181">If [**TranslateColorGlyphRun**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun) does report the presence of color glyph runs, then your app should ignore the primary glyph run and instead use the color glyph run(s) returned by TranslateColorGlyphRun.</span></span> <span data-ttu-id="46173-182">Zu diesem Zweck durchlaufen Sie das zurückgegebene [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) -Objekt, wobei jedes ausgeführte Farb Symbol abgerufen und nach Bedarf für sein Symbolbild Format gezeichnet wird (Sie können z. b. [**drawcolorbitmapglyphrun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) und [**drawsvgglyphrun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) verwenden, um Farb Bitmap-Symbole bzw. SVG-Symbole zu zeichnen).</span><span class="sxs-lookup"><span data-stu-id="46173-182">To do so, iterate through the returned [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) object, retrieving each color glyph run and drawing it as appropriate for its glyph image format (for example, you can use [**DrawColorBitmapGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawcolorbitmapglyphrun) and [**DrawSvgGlyphRun**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext4-drawsvgglyphrun) to draw color bitmap glyphs and SVG glyphs, respectively).</span></span>

<span data-ttu-id="46173-183">Das folgende Codebeispiel zeigt die allgemeine Struktur dieses Verfahrens:</span><span class="sxs-lookup"><span data-stu-id="46173-183">The following code example shows the general structure of this procedure:</span></span>


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



### <a name="using-color-fonts-with-win2d"></a><span data-ttu-id="46173-184">Verwenden von Color Fonts mit Win2D</span><span class="sxs-lookup"><span data-stu-id="46173-184">Using color fonts with Win2D</span></span>

<span data-ttu-id="46173-185">Ähnlich wie Direct2D werden in Win2D s Text Zeichnungs-APIs standardmäßig keine Farbsymbole dargestellt.</span><span class="sxs-lookup"><span data-stu-id="46173-185">Similar to Direct2D, Win2D s text drawing APIs do not render color glyphs by default.</span></span> <span data-ttu-id="46173-186">Um das Farb Symbol Rendering zu aktivieren, legen Sie das Optionen-Flag [enablecolorfont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) im Textformat-Objekt fest, das Ihre APP an die Text Zeichnungs Methode übergibt.</span><span class="sxs-lookup"><span data-stu-id="46173-186">To opt in to color glyph rendering, set the [EnableColorFont](https://microsoft.github.io/Win2D/html/T_Microsoft_Graphics_Canvas_Text_CanvasDrawTextOptions.htm) options flag in the text format object your app passes to the text drawing method.</span></span> <span data-ttu-id="46173-187">Im folgenden Codebeispiel wird gezeigt, wie eine Zeichenfolge in einer Farb Schriftart mithilfe von Win2D dargestellt wird:</span><span class="sxs-lookup"><span data-stu-id="46173-187">The following code example shows how to render a string in a color font using Win2D:</span></span>


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

## <a name="related-topics"></a><span data-ttu-id="46173-188">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="46173-188">Related topics</span></span>

[<span data-ttu-id="46173-189">Beispiel für das farbige DirectWrite-Symbol</span><span class="sxs-lookup"><span data-stu-id="46173-189">DirectWrite colored glyph sample</span></span>](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)


[<span data-ttu-id="46173-190">**IDWriteFontFace4-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="46173-190">**IDWriteFontFace4 interface**</span></span>](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4)


[<span data-ttu-id="46173-191">**IDWriteFactory4:: translatecolorglyphrun-Methode**</span><span class="sxs-lookup"><span data-stu-id="46173-191">**IDWriteFactory4::TranslateColorGlyphRun method**</span></span>](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory4-translatecolorglyphrun)


[<span data-ttu-id="46173-192">**ID2D1DeviceContext4::D rawtext-Methode**</span><span class="sxs-lookup"><span data-stu-id="46173-192">**ID2D1DeviceContext4::DrawText method**</span></span>](../direct2d/id2d1devicecontext4-drawtext-overload.md)


 

