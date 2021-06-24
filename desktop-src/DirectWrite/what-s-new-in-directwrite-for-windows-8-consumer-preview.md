---
title: Neues in DirectWrite
description: Im Folgenden finden Sie einige der neuen Ergänzungen zu DirectWrite.
ms.assetid: 2512D222-C6EB-4C2D-80A6-7978FED56F7A
ms.topic: article
ms.date: 09/23/2019
ms.openlocfilehash: ea9e36487477f51179a77b97726b787a0f5da844
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112587890"
---
# <a name="whats-new-in-directwrite"></a>Neues in DirectWrite

In diesem Thema werden die Neuheiten in [DirectWrite](direct-write-portal.md) für verschiedene Releases von Windows 10.

## <a name="windows-app-sdk"></a>Windows-App-SDK

Das [Windows App SDK](/windows/apps/windows-app-sdk/) führt eine neue Version von DirectWrite namens DWriteCore ein. Weitere Informationen finden Sie unter [Übersicht über DWriteCore.](dwritecore-overview.md)

## <a name="windows-10-may-2019-update"></a>Windows 10-Update von Mai 2019

Für Windows 10 Version 1903 (10.0; Build 18362) &mdash; wird auch als Windows 10 May 2019 Update.

## <a name="windows-10-october-2018-update"></a>Windows 10-Update von Oktober 2018

Die folgenden Features und APIs wurden für Windows 10, Version 1809 (10.0; Build 17763) &mdash; auch als Windows 10 October 2018 Update.

### <a name="new"></a>Neu

- [**DWRITE_FONT_SOURCE_TYPE**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_source_type) Enumeration
- [**IDWriteFontSet3-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) und ihre Methoden

## <a name="windows-10-april-2018-update"></a>Windows 10-Update vom April 2018

Die folgenden Features und APIs wurden für Windows 10 Version 1803 (10.0; Build 17134) &mdash; auch als Windows 10 April 2018 Update.

### <a name="new"></a>Neu

- [**IDWriteFactory7-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) und ihre Methoden
- [**IDWriteFontCollection3-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) und ihre Methoden
- [**IDWriteFontSet2-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) und ihre Methoden

## <a name="windows-10-fall-creators-update"></a>Windows 10 Fall Creators Update

Die folgenden Features und APIs wurden für Windows 10 Version 1709 (10.0; Build 16299) &mdash; wird auch als Windows 10 Fall Creators Update.

### <a name="new"></a>Neu

- [**DWRITE_AUTOMATIC_FONT_AXES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_automatic_font_axes) Enumeration
- [**DWRITE_FONT_AXIS_ATTRIBUTES**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_attributes) Enumeration
- [**DWRITE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_axis_tag) Enumeration
- [**DWRITE_FONT_FAMILY_MODEL**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_family_model) Enumeration
- [**IDWriteFactory6-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) und ihre Methoden
- [**IDWriteFontCollection2-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) und ihre Methoden
- [**IDWriteFontFace5-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) und ihre Methoden
- [**IDWriteFontFaceReference1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) und ihre Methoden
- [**IDWriteFontFallback1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfallback1) und ihre Methoden
- [**IDWriteFontFamily2-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) und ihre Methoden
- [**IDWriteFontList2-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) und ihre Methoden
- [**IDWriteFontResource-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) und ihre Methoden
- [**IDWriteFontSet1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) und ihre Methoden
- [**IDWriteFontSetBuilder2-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) und ihre Methoden
- [**IDWriteTextFormat3-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) und ihre Methoden
- [**IDWriteTextLayout4-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextlayout4) und ihre Methoden
- [**DWRITE_MAKE_FONT_AXIS_TAG**](/windows/win32/api/dwrite_3/nf-dwrite_3-dwrite_make_font_axis_tag) Makro
- [**DWRITE_FONT_AXIS_RANGE-Struktur**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)
- [**DWRITE_FONT_AXIS_VALUE-Struktur**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)

### <a name="moved"></a>Verschoben

Die [**DWRITE_GLYPH_IMAGE_FORMATS-Enumeration**](/windows/win32/api/dcommon/ne-dcommon-dwrite_glyph_image_formats) wurde von in `dwrite_3.h` `dcommon.h` verschoben.

## <a name="windows-10-creators-update"></a>Windows 10 Creators Update

Die folgenden Features und APIs wurden für Windows 10 Version 1703 (10.0; Build 15063) &mdash; wird auch als Windows 10 Creators Update.

### <a name="expanded-api-support-for-cloud-fonts-and-custom-font-sets"></a>Erweiterte API-Unterstützung für Cloudschriftarten und benutzerdefinierte Schriftartensätze

Windows 10 enthaltene APIs, die Apps den einfachen Zugriff auf Schriftarten über einen Windows-Schriftartendienst ermöglichen. In der Windows 10 Creators Update apIs für Remoteschriftarten erweitert, um den einfachen Zugriff auf Schriftarten aus anderen Quellen im Web zu ermöglichen, auf die über HTTP oder HTTPS zugegriffen werden kann. 

Die neuen APIs für Remoteschriftart können mit öffentlichen oder privaten Webdiensten verwendet werden. Darüber hinaus können sie für den Zugriff auf Unformatierte, OpenType-Schriftartdateien (TTF, OTF,TTC,FS) oder Schriftarten in [WOFF-](https://www.w3.org/TR/WOFF/) oder [WOFF2-Containerformaten](https://www.w3.org/TR/WOFF2/) verwendet werden. Die neuen APIs werden in Verbindung mit vorhandenen APIs für Warteschlangenanforderungen zum Herunterladen von Remoteschriftartdaten und zum Verarbeiten des eigentlichen Downloadprozesses verwendet.

Andere neue APIs erleichtern Apps die Arbeit mit benutzerdefinierten Schriftarten, die im lokalen Dateisystem gespeichert oder in einen Speicherpuffer geladen werden.

Weitere Informationen zu neuen APIs für die Arbeit mit Remoteschriftarten, benutzerdefinierten Schriftartensätzen oder WOFF/WOFF2-Containerformaten finden Sie im folgenden Thema:

[Benutzerdefinierte Schriftartenkombinationen](custom-font-sets-win10.md)

Siehe auch die Links zu API-Referenzthemen, die in diesem Thema bereitgestellt werden.  Die Verwendung neuer und vorhandener APIs für die Arbeit mit benutzerdefinierten Schriftarten wird auch im [DirectWrite Custom Font Sets-Beispiel veranschaulicht.](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/DirectWriteCustomFontSets/) Dieses Beispiel veranschaulicht die Codeimplementierung für verschiedene Szenarien, einschließlich lokaler Schriftarten auf dem Datenträger, Remoteschriftarten im Web, In-Memory-Schriftartdaten und Schriftarten in gepackten WOFF- oder WOFF2-Formaten.

### <a name="initial-support-for-opentype-font-variations"></a>Anfängliche Unterstützung für OpenType-Schriftartvariationen

In Version 1.8 der OpenType-Schriftartformatspezifikation wurde eine interessante neue Erweiterung für das Format eingeführt, das als OpenType-Schriftartvariationen bezeichnet wird. DirectWrite wurde in der -Windows 10 Creators Update aktualisiert, um benannte Instanzen von variablen Schriftarten zu unterstützen. Weitere Informationen finden Sie in den folgenden Themen:

[OpenType-Variablenschriftarten](opentype-variable-fonts.md)

## <a name="windows-10-anniversary-update"></a>Windows 10 Anniversary Update

Die folgenden Features und APIs wurden für Windows 10 Version 1607 (10.0; Build 14393) &mdash; wird auch als Windows 10 Anniversary Update.

### <a name="improved-support-for-color-fonts"></a>Verbesserte Unterstützung für farbige Schriftarten

Ab Windows 10 Anniversary Update bietet DirectWrite integrierte Unterstützung für eine größere Vielfalt von Farbschriftformaten, sodass Entwickler mehr Schriftarten in ihren DirectWrite-gestützten Apps verwenden können als je zuvor. Unter anderem werden folgende Elemente unterstützt:

-   Die OpenType-Tabelle "COLR", die kompakten Vektorinhalt in Schriftarten ermöglicht. (Unterstützt seit Windows 8.1.)
-   Die OpenType-Tabelle "SVG", die SVG-Inhalt in Schriftarten ermöglicht.
-   Die OpenType-Tabelle 'ÖFFNT', die Farbbitmapinhalt in Schriftarten ermöglicht.
-   Die OpenType-Tabelle "sbix", die Farbbitmapinhalte in Schriftarten ermöglicht.

[Direct2D](../direct2d/direct2d-portal.md), das DirectWrite für das Textrendering verwendet, unterstützt diese Farbschriftformate automatisch, wenn das [**Flag D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options) aktiviert ist. Weitere Informationen finden Sie in den folgenden Themen:

-   [Farbige Schriftarten](color-fonts.md)
-   [DirectWrite-Farbglyphenbeispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="support-for-adobe-typekit-and-other-font-service-clients"></a>Unterstützung für Adobe Typekit und andere Schriftartdienstclients

Einige Schriftartdienste wie Adobe Typekit verfügen über clientseitige Hilfsprogramme, mit denen Benutzer Schriftarten aus dem Dienst laden und in verschiedenen Anwendungen auf ihrem Windows-Computer verwenden können. Diese Hilfsprogramme funktionieren in der Regel durch Laufzeitaufrufe an GDI, um zusätzliche Schriftarten zu laden, anstatt Schriftarten dauerhaft auf dem System zu installieren. Aufgrund dieses Entwurfs können die Schriftarten in früheren Windows-Versionen in GDI-basierten Anwendungen, aber nicht in DirectWrite-Anwendungen verwendet werden. Ab dem Windows 10 Anniversary Update werden Schriftarten, die von solchen Hilfsprogrammen geladen werden, auch in DirectWrite sowie in GDI verfügbar sein.

Schriftarten, die von einem Font-Service-Hilfsprogramm geladen werden, werden in der Auflistung der Systemschriftarten angezeigt, die durch Aufrufen der [**IDWriteFactory::GetSystemFontCollection-Methode erhalten**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-getsystemfontcollection) wurden. Da Schriftartdienste in der Regel einem Lizenzierungsmodell pro Benutzer folgen, werden schriftarten, die von diesen Hilfsprogrammen geladen werden, auf Benutzerbasis verwaltet. Daher können vorhandene DirectWrite-Anwendungen Schriftarten verwenden, die Endbenutzer mithilfe solcher Dienste erhalten haben, ohne dass Codeänderungen in der Anwendung erforderlich sind, was eine nahtlosere Benutzererfahrung bietet.

### <a name="support-for-opentype-collections-using-cff-outlines"></a>Unterstützung für OpenType-Sammlungen mit CFF-Konturen

Die Schriftformate OpenType und TrueType unterstützen seit langem die Möglichkeit, mehrere Schriftarten in einer einzelnen Schriftartdatei zusammen zu packen, die als "Schriftartsammlung" bezeichnet wird. Die OpenType-Spezifikation hat schriftarten immer die Verwendung von TrueType- oder CFF-Formaten für Glyphengliederungsdaten gestattet. Bis vor Kurzem war die Spezifikation jedoch nur für Sammlungen zulässig, in denen Glyphengliederungen das TrueType-Format verwenden. OpenType Version 1.7 ermöglicht sammlungen jetzt die Verwendung von TrueType- oder CFF-Formaten für Gliederungsdaten von Glyphen. Ab der Windows 10 Anniversary Update unterstützt DirectWrite OpenType-Sammlungen mithilfe von CFF-Konturdaten.

## <a name="windows-10"></a>Windows 10

### <a name="windows-font-service-integration"></a>Integration des Windows-Schriftartdiensts

Ab Windows 10 sind Schriftarten, die in Windows enthalten sind, in einem Onlinedienst verfügbar und können über DirectWrite auf jedem gerät Windows 10 werden. Dies gilt für alle Windows 10 Editionen, einschließlich Windows 10 Mobile, Xbox und HoloLens sowie des Desktopclients. Dadurch können Anwendungen Inhalte mit einer beliebigen Windows-Schriftart anzeigen, auch wenn die Schriftart derzeit nicht auf dem Gerät installiert ist.

Die Unterstützung für die DirectWrite-Schriftartdienstmechanismen wurde im XAML-Framework implementiert. Dies bedeutet, dass alle Anwendungen, die XAML verwenden, keine Codeänderungen erfordern, um den Schriftartdienst nutzen zu können. Dies [wird im XAML-Codebeispiel (Downloadable Fonts)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/XamlCloudFontIntegration) veranschaulicht. Anwendungen, die DirectWrite-APIs direkt aufrufen, müssen neue APIs verwenden, um die Font-Service-Mechanismen zu nutzen. Weitere Informationen finden Sie in den folgenden Themen:

-   [**IDWriteFactory3::GetSystemFontCollection-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontcollection)
-   [**IDWriteTextLayout3-Schnittstelle**](idwritetextlayout3.md)
-   [**IDWriteFontDownloadQueue-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue)
-   [**IDWriteFontDownloadListener-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener)

Im [Codebeispiel Downloadable fonts (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteTextLayoutCloudFont) (Herunterladbare Schriftarten (DirectWrite)) wird die Verwendung mehrerer der neuen APIs veranschaulicht.

### <a name="font-set-apis"></a>Schriftartensatz-APIs

Die Schriftartsammlungsschnittstellen von DirectWrite bieten eine Ansicht für eine Auflistung von Schriftarten, die nach Schriftfamilien organisiert ist, und verwenden Gewichtung, Stretching und Stil als Attribute der Unterfamilie. Intern implementiert DirectWrite die Schriftartsammlungsschnittstelle mithilfe einer flachen Liste von Schriftarten mit verschiedenen Attributen. Dieser Ansatz ist flexibler, da in die Enumeration von Gewichtungs-, Stretch-/Stilfamilien unterstützen kann, aber auch Abfragen und Filtern mit anderen Schriftartattributen unterstützen kann.

In Windows 10 wird dieser flexiblere Schriftbehandlungsmechanismus für Anwendungen über IDWriteFontSet und die zugehörigen APIs zur Verfügung gestellt. Die Schriftartensatz-APIs können beispielsweise verwendet werden, um eine benutzerdefinierte Benutzeroberfläche für die Schriftartauswahl zu erstellen, die anwendungsspezifische Schriftarteigenschaften in einem benutzerdefinierten Schriftartensatz nutzt.

Weitere Informationen finden Sie in den folgenden Themen:

-   [**IDWriteFontSet-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset)
-   [**IDWriteFontSetBuilder-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder)
-   [**DWRITE \_ FONT \_ PROPERTY \_ ID-Enumeration**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id)
-   [**IDWriteFontFactory3::GetSystemFontSet-Methode**](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefactory3-getsystemfontset)

### <a name="new-text-layout-line-spacing-modes"></a>Neue Zeilenabstandsmodi für das Textlayout

Die Textformat- und Textlayoutschnittstellen von DirectWrite unterstützen neue Zeilenabstandsmodi. In früheren Versionen war die Textlayoutimplementierung von DirectWrite für den Zeilenabstand zulässig, in dem die Höhe jeder Zeile automatisch basierend auf dem höchsten Element innerhalb einer Zeile (dem Standardmodus) oder dem Zeilenabstand mit allen Zeilen festgelegt wurde, die auf eine von der Anwendung bestimmte einheitliche Höhe festgelegt wurden (der Modus "Uniform"). In Windows 10 wird ein zusätzlicher "proportionaler" Zeilenabstandsmodus unterstützt, der Anwendungen mehr Optionen für das Zeilenabstandsverhalten bietet. Weitere Informationen finden Sie in den folgenden Themen:

-   [**IDWriteTextLayout3-Schnittstelle**](idwritetextlayout3.md)
-   [**IDWriteTextLayout3::SetLineSpacing-Methode**](idwritetextlayout3-setlinespacing.md)
-   [**DWRITE \_ LINE \_ SPACING-Struktur**](/windows/win32/api/Dwrite_3/ns-dwrite_3-dwrite_line_spacing)
-   [**DWRITE \_ LINE \_ SPACING \_ METHOD-Enumeration**](/windows/win32/api/dwrite/ne-dwrite-dwrite_line_spacing_method)
-   [**DWRITE \_ FONT \_ LINE \_ GAP \_ USAGE-Enumeration**](/windows/win32/api/dwrite_3/ne-dwrite_3-dwrite_font_line_gap_usage)
-   [**IDWriteTextLayout3::GetLineMetrics-Methode**](idwritetextlayout3-getlinemetrics.md)
-   [**DWRITE \_ LINE \_ METRICS1-Struktur**](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_line_metrics1)

Das Codebeispiel Line [spacing (DirectWrite)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteLineSpacingModes) veranschaulicht die Verwendung mehrerer der neuen APIs und bietet auch eine Visualisierung aller verschiedenen Zeilenabstandsmodi, die es viel einfacher machen, die verschiedenen verfügbaren Zeilenabstandsoptionen zu verstehen.

### <a name="gdi-interop"></a>GDI-Interop

Seit der Einführung in Windows 7 stellt DirectWrite einen Migrationspfad für Anwendungen zur Verfügung, die ursprünglich mit dem Schriftartmodell, dem Textlayout und dem Rendering von GDI implementiert wurden. Dies wurde über die \[ \[ IDWriteGdiInterop-Schnittstelle \] \] bereitgestellt. In Windows 10 bieten zusätzliche APIs zusätzliche GDI-Interop-Funktionen. Weitere Informationen finden Sie im folgenden Thema:

-   [**IDWriteGdiInterop1-Schnittstelle**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1)

## <a name="windows-81"></a>Windows 8.1

### <a name="rendering-color-fonts"></a>Rendern von Farbschriftarten

Ab Windows Windows 8.1 bietet DirectWrite Unterstützung für Farbschriftarten. [Direct2D,](../direct2d/direct2d-portal.md)das DirectWrite für das Textrendering verwendet, hat den Aufzählwert D2D1 DRAW TEXT OPTIONS ENABLE COLOR FONT hinzugefügt, um dieses Feature beim Zeichnen von \_ \_ Text zu \_ \_ \_ \_ aktivieren. Weitere Informationen finden Sie in den folgenden Themen:

-   [**D2D1 \_ DRAW \_ TEXT \_ OPTIONS-Enumeration**](/windows/win32/api/d2d1/ne-d2d1-d2d1_draw_text_options)
-   [**IDWriteFactory2::TranslateColorGlyphRun-Methode**](/windows/win32/api/dwrite_2/nf-dwrite_2-idwritefactory2-translatecolorglyphrun)

## <a name="windows-8"></a>Windows 8

Eine neue Factoryschnittstelle, [**IDWriteFactory1,**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1)zum Erstellen zusätzlicher verfügbarer Schnittstellen.

Zusätzliche Schriftarteigenschaften, z. B.: Super-/Subscript-, Caretablage-, PANOSE- und Unicode-Bereiche.

-   [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1)
-   [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1)

Verbesserungen beim Abstand, z. B.: Steuerelementzeichenabstand, Legacy-Kerningpaare und Begründung. Weitere Informationen finden Sie im Thema [Begründung, Kerning](justification--kerning--and-spacing.md) und Abstand.

-   [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1)
-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Verbesserte Renderziele und -parameter.

-   [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)
-   [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1)

Verbesserungen bei der Textkomplexitätsanalyse.

-   [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1)

Neue Skripteigenschaften, neue Skriptunterstützung (Unicode 6), Schriftartfallbacker ergänzungen, gekoppelte Klammern und Bidi-Vergrößerung.

Verbesserungen der Leistung des Schriftartcaches. Ab Windows 8 der Schriftartcache global und startet, wenn Der Computer gestartet wird.

Neue Renderingmodi.

Ab Windows 8 [unterstützt DirectWrite](direct-write-portal.md) eine Reihe von Features, mit denen Sie Apps für den Weltmarkt erstellen können.

Im Folgenden finden Sie mehrere Bereiche, mit denen Sie Rich-Text-Apps implementieren können, die auf Kunden auf der ganzen Welt zugeschnitten werden können.

### <a name="chinese-japanese-and-korean-extensions-c--d"></a>Chinesische, japanische und koreanische Erweiterungen C & D

Alle paar Jahre veröffentlicht das Unicode-Konsortium eine standardisierte Liste von Ergänzungen zum Block "Chinesisch", "Japanisch" und "Koreanisch Unified Ideogramm". Mit der Unicode 6.0-Revision haben sie die Erweiterungsblöcke C und D veröffentlicht. Diese Blöcke von Ideogrammen finden Sie auf der Unicode-Website [Erweiterung C](https://www.unicode.org/charts/PDF/U2A700.pdf) und [Erweiterung D](https://www.unicode.org/charts/PDF/U2B740.pdf).

Ab Windows 8 unterstützt [DirectWrite](direct-write-portal.md) die Unicode-Codepunkte für diese neuen Blöcke standardisierter CJK-Ideogramme, sodass Sie sie in DirectWrite-Apps verwenden können.

### <a name="indian-rupee-symbol"></a>Symbol "Indien-Rupie"

Im März 2005 hat die regierung von Indien einen Wettbewerb angekündigt, um ein Symbol für die Währung "Indien, Rupie" zu wählen. Nach viel Wettbewerb wählte die regierung von Indien am 15. Juli 2010 den von D. Ud udmar erstellten Entwurf aus, und [DirectWrite](direct-write-portal.md) unterstützt den an das Symbol gebundenen Unicode-Codepunkt. Daher unterstützen DirectWrite-Apps jetzt dieses Währungssymbol.

### <a name="emoji"></a>Emoji

[DirectWrite](direct-write-portal.md) unterstützt jetzt die Verwendung von Emoji in Apps. In früheren Versionen von DirectWrite wurde ein fehlendes Glyphenfeld angezeigt, wenn Sie versucht haben, ein Emoji-Ideogramm zu rendern. Ab Windows 8 unterstützt DirectWrite den Unicode-Codeblock, der Emoji zugeordnet ist. Wenn Ihre App also die Unicode-Standardcodepunkte für Emoji verwendet, werden die entsprechenden Glyphen angezeigt.

### <a name="myanmar-tiffinagh-and-old-hangul-languages"></a>Die Sprachen "Sollen", "Tiffinagh" und "Old Hangul"

Ab Windows 8 unterstützt [DirectWrite](direct-write-portal.md) den Block von Unicode-Codepunkten, die den Symbolen in den Sprachen "Sollen", "Tiffinagh" und "Old Hangul" entsprechen, sodass Sie Apps erstellen können, die Text aus diesen drei Sprachen enthalten. Zusätzlich zur Unterstützung dieser Zeichen unterstützt DirectWrite die einzigartige Art und Weise, wie Old Hangul Zeilenumbrüche behandelt.

### <a name="new-scripts"></a>Neue Skripts

Ab Windows 8 gibt die [**GetScriptProperties-Methode**](/windows/win32/api/dwrite_1/nf-dwrite_1-idwritetextanalyzer1-getscriptproperties) Informationen für eine Reihe neuer Skripts zurück. Dies ist die Liste der Skripts, [die DirectWrite](direct-write-portal.md) in Windows 8 und danach unterstützt.

-   Avestan
-   Bamum
-   Batak
-   Brahmi
-   Hieroglyphics in DerEndingen
-   Hier wird ein Aicic-Aic-3-
-   Besensisch Pahlavi
-   Parthianisch (Teil 1)
-   Javanisch
-   Kaithi
-   Lisu (Fraser)
-   Mandaisch
-   Meetei Mayek
-   Altes Südosten
-   Altes Türkisch (Orkhon)
-   Samariter
-   Telecom Tham (Lanna)
-   Gegenkn.
