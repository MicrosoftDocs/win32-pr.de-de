---
title: Neues in Direct2D
description: Im Folgenden finden Sie einige der neuen Ergänzungen zu Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 595a0833e88948585622d79907c81a1465e3fa7b11d1ebc8d6bbd697312509bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119430470"
---
# <a name="whats-new-in-direct2d"></a>Neues in Direct2D

Im Folgenden finden Sie einige der neuen Ergänzungen zu Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>Neues bei Windows 10 Creators Update

Die folgenden Features und APIs wurden hinzugefügt oder für Windows 10 Creators Update.

### <a name="support-for-svg-image-rendering"></a>Unterstützung für SVG-Bildrendering

Ab Windows 10 Creators Update bietet Direct2D Unterstützung für das Analyse- und Zeichnen von SVG-Bildern, sodass Entwickler Objekte rendern können, die in ihren bevorzugten Vektorarttools erzeugt wurden, ohne sie zuerst in Rasterbilder zu konvertieren. Verwenden Sie dieses Feature, um den Datenträgerbedarf und das Skalierungsverhalten Ihrer In-App-Symbolografie zu verbessern, und verwenden Sie die neuen SVG-Objektmodell-APIs von Direct2D, um programmgesteuerte Änderungen am SVG Ihrer App vorzunehmen. Beachten Sie, dass Direct2D nur eine begrenzte Teilmenge von SVG unterstützt, die für Bilder geeignet ist, und nicht alle SVG-Zeichnungsfeatures unterstützt. Wenn Sie browserbasierte SVG-Kompatibilität oder die weborientierten Features von SVG benötigen, sollten Sie stattdessen das [XAML-WebView-Steuerelement](/uwp/api/Windows.UI.Xaml.Controls.WebView) verwenden. Weitere Informationen finden Sie in den folgenden Themen:

-   [Direct2D-SVG-Bildrenderingbeispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [SVG-Unterstützung](svg-support.md)
-   [**ID2D1DeviceContext5::CreateSvgDocument-Methode**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument)
-   [**ID2D1DeviceContext5::D rawSvgDocument-Methode**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument)
-   [**ID2D1SvgElement-Schnittstelle**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement)

### <a name="improved-support-for-color-management"></a>Verbesserte Unterstützung für die Farbverwaltung

Ab Windows 10 Creators Update bietet Direct2D verbesserte Farbverwaltungsfunktionen. Entwickler benötigen keinÄT-Profil mehr, um den Direct2D-Farbverwaltungseffekt zu verwenden. Sie können jetzt DXGI-Farbräume verwenden oder ihre eigene parametrisierte Farbraumdefinition erstellen. Weitere Informationen finden Sie in den folgenden Themen:

-   [Farbverwaltungseffekt](color-management.md)
-   [**ID2D1DeviceContext5::CreateColorContextFromDxgiColorSpace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5::CreateColorContextFromSimpleColorProfile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>Neues bei Windows 10 Anniversary Update

Die folgenden Features und APIs wurden für Windows 10 Anniversary Update hinzugefügt oder aktualisiert.

### <a name="improved-support-for-color-fonts"></a>Verbesserte Unterstützung für farbige Schriftarten

Ab Windows 10 Anniversary Update unterstützt Direct2D jetzt das Rendern einer größeren Vielfalt von Farbschriftarten, sodass Entwickler mehr Schriftarten in ihren Direct2D-gestützten Apps verwenden können als je zuvor. Unter anderem werden folgende Elemente unterstützt:

-   Die OpenType-Tabelle "COLR", die kompakten Vektorinhalt in Schriftarten ermöglicht. (Unterstützt seit Windows 8.1.)
-   Die OpenType-Tabelle "SVG", die SVG-Inhalt in Schriftarten ermöglicht.
-   Die OpenType-Tabelle 'ÖFFNT', die Farbbitmapinhalt in Schriftarten ermöglicht.
-   Die OpenType-Tabelle "sbix", die Farbbitmapinhalt in Schriftarten aktiviert.

Direct2D unterstützt diese Farbschriftformate automatisch, wenn das [**Flag D2D1 \_ DRAW TEXT OPTIONS ENABLE COLOR \_ \_ \_ \_ \_ FONT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) aktiviert ist. Weitere Informationen finden Sie in den folgenden Themen:

-   [Farbige Schriftarten](/windows/desktop/DirectWrite/color-fonts)
-   [DirectWrite eines Farbglyphenbeispiels](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Neue Bildeffekte

Ab Windows 10 Anniversary Update enthält Direct2D die Effekte AlphaMask, CrossFade, Opacity und Tönung. Diese Funktionalität war zuvor in bestimmten Konfigurationen von Composite-, ArithmeticComposite- und ColorMatrix-Effekten verfügbar, aber die neuen integrierten Effekte erleichtern die Arbeit mit diesen gängigen Vorgängen.

## <a name="whats-new-for-windows-10"></a>Neues bei Windows 10

Die folgenden Features und APIs wurden hinzugefügt oder für Windows 10.

### <a name="sprite-batches"></a>Sprite-Batches

Ab Windows 10 bietet Direct2D Unterstützung für das Erstellen und Rendern von Sprite-Batches. Im Vergleich zur allgemeinen [**DrawImage-Methode**](id2d1devicecontext-drawimage-overload.md) verursachen Sprite-Batches erheblich weniger CPU-Mehraufwand pro Bild. Dies macht sie ideal für Szenarien mit Hunderten oder Tausenden von gleichzeitigen Bildern, z. B. Spiel-Sprites oder Partikelsysteme. Weitere Informationen finden Sie in den folgenden Themen:

-   [**ID2D1DeviceContext3::CreateSpriteBatch-Methode**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch)
-   [**ID2D1DeviceContext3::D rawSpriteBatch-Methoden**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options))
-   [**ID2D1SpriteBatch-Schnittstelle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch)

### <a name="gradient-meshes"></a>Farbverlaufsgitter

Ab Windows 10 bietet Direct2D ein neues Primitiv für Farbverlaufsgitter. Farbverlaufsgitter werden häufig von Professionellen in Grafikentwurfssoftware verwendet und ermöglichen es Denkgrafiken, komplexe (sogar fotorealistische) mehrfarbige Formen mit allen Speicher- und Skalierbarkeitsvorteilen von Vektoren zu rendern. Weitere Informationen finden Sie in den folgenden Themen:

-   [Beispiel für ein Direct2D-Farbverlaufsgitter](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2D1 \_ GRADIENT \_ MESH \_ PATCH-Struktur**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch)
-   [**ID2D1DeviceContext2::D rawGradientMesh-Methode**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh)

### <a name="improved-image-loading-apis"></a>Verbesserte ApIs zum Laden von Images

Ab Windows 10 bietet Direct2D eine neue API zum Laden von Bildern, ID2D1ImageSource. Die Bildquelle verbessert vorhandene Bildlade-APIs, einschließlich CreateBitmapFromWicBitmap, des Bitmap Source-Effekts und des YCbCr-Effekts. Die Direct2D-Bildquelle kombiniert die Funktionen dieser APIs mit Unterstützung für beliebig große Bilder, einfache Integration in Drucken und Effekte und zahlreiche Optimierungen, einschließlich YCbCr JPEG und indizierter JPEG. Weitere Informationen finden Sie in den folgenden Themen:

-   [Direct2D Photo Adjustment SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [IWICJpegFrameDecode::SetIndexing](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Verbesserte Unterstützung für das Rendern von Ink-Daten

Ab Windows 10 stellt Direct2D ein neues Primitiv für die Darstellung von Ink-Strichen dar. Direct2D-Ink-Striche werden durch Bézierkurven definiert, unterstützen verschiedene Nib-Formen und Transformationen und können eine feste oder variable Stärke aufweisen. Die integrierte Unterstützung für Ink-Striche von Direct2D ermöglicht Apps das einfache Rendern schneller und besserer Ink als bei vorherigen Ansätzen, bei denen Apps in der Regel Selbstverwalten von Ink als eine Reihe von Ellipsen und Quadrieren benötigten. Weitere Informationen finden Sie in den folgenden Themen:

-   [**ID2D1Ink-Schnittstelle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**ID2D1DeviceContext2::D rawInk-Methode**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**ID2D1InkStyle-Schnittstelle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Verknüpfen von Effekt-Shadern

Direct2D-Effekte werden mithilfe von HLSL-Pixel-, Scheitelpunkt- und/oder Compute-Shadern implementiert. Ab Windows 10 analysiert Direct2D automatisch Effektdiagramme auf Möglichkeiten, einzelne Shader zu kombinieren und auszuführen. Dies kann zu einer erheblichen Erhöhung des tatsächlichen Durchsatzes führen. Benutzer integrierter Effekte müssen nichts tun, um von Effekt-Shader-Verknüpfungen zu profitieren. Entwickler, die eigene benutzerdefinierte Effekte erstellen, sollten jedoch aktualisierte bewährte Methoden für die Nutzung von Effekt-Shaderverknüpfungen befolgen. Weitere Informationen finden Sie in den folgenden Themen:

-   [Effektshader-Verknüpfung](effect-shader-linking.md)
-   [Direct2D HLSL Helpers](hlsl-helpers.md)
-   [Direct2D Custom Effects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

Effekt-Shaderverknüpfungen sind so konzipiert, dass sie sich nicht auf die visuelle Ausgabe von Effekten auswirken. Dies ist jedoch nicht immer aufgrund eines bestimmten Verhaltens im Bereich der Effektgenauigkeit und numerischen Beschneidung möglich. Weitere Informationen zum Steuern dieser Verhaltensweisen finden Sie unter:

-   [Steuern der Genauigkeit und numerischen Beschneidung in Effektdiagrammen](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Neue integrierte Effekte

Ab Windows 10 bietet Direct2D eine umfangreiche Reihe von neuen integrierten Effekten, die die wichtigsten Entwickleranforderungen adressieren und neue Arten von visuellen Szenarien ermöglichen. Die neuen Auswirkungen sind:

### <a name="color"></a>Farbe:

-   [RGB-zu-Hue-Effekt](rgb-to-hue-effect.md)
-   [Hue-zu-RGB-Effekt](hue-to-rgb-effect.md)
-   [3D-Lookuptabelleneffekt](3d-lookup-table-effect.md)

### <a name="photo"></a>Foto:

-   [Kontrasteffekt](contrast-effect.md)
-   [Belichtungseffekt](exposure-effect.md)
-   [Graustufeneffekt](grayscale-effect.md)
-   [Highlights und Schatteneffekt](highlights-and-shadows-effect.md)
-   [Invert-Effekt](invert-effect.md)
-   [Sepia-Effekt](sepia-effect.md)
-   [Schärfen des Effekts](sharpen-effect.md)
-   [Begradigungseffekt](straighten-effect.md)
-   [Temperatur- und Tönungseffekt](temperature-and-tint-effect.md)
-   [Effekt "Effect"](vignette-effect.md)

### <a name="filter"></a>Filter:

-   [Auswirkung der Edgeerkennung](edge-detection-effect.md)

### <a name="stylize"></a>Stilisieren:

-   [Emboss-Effekt](emboss-effect.md)
-   [Effekt "Posterize"](posterize-effect.md)

### <a name="transparency"></a>Transparenz:

-   [Effekt "Tastenknöte"](chromakey-effect.md)

Die Effekte für Geraden, Sättigung, Kontrast, Highlights und Schatten sowie Temperatur- und Tönungseffekte werden im [Direct2D Photo Adjustment SDK-Beispiel gezeigt.](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)

## <a name="whats-new-for-windows-81"></a>Neues bei Windows 8.1

Die folgenden Features und APIs wurden hinzugefügt oder für Windows 8.1.

Ab Windows 8.1 basiert Direct2D auf Direct3D 11.2.

### <a name="geometry-realizations"></a>Geometrierealisierungen

Ab Windows 8.1 bietet Direct2D Geometrierealisierungen. Geometrierealisierungen ermöglichen Es Anwendungen, die Leistung des Geometrierenderings in bestimmten Situationen zu verbessern, ohne einige der Nachteile der Rasterung der Geometrie in eine Bitmap zu vermeiden. Weitere Informationen finden Sie in den folgenden Themen:

-   [**ID2D1Device1-Schnittstelle**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1)
-   [**ID2D1DeviceContext1::D rawGeometryRealization-Methode**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization)

### <a name="support-for-jpeg-ycbcr-images"></a>Unterstützung für JPEG-YCbCr-Bilder

Ab Windows 8.1 bietet Direct2D Unterstützung für das Rendern von Bilddaten im JPEG Y'CbCr-Format. Apps können JPEG-Inhalte in ihrer nativen Y'CbCr-Darstellung rendern, anstatt in BGRA zu dekomprimieren. Dies kann den Grafikspeicherverbrauch und die Zeit für die Ressourcenerstellung erheblich reduzieren. Weitere Informationen finden Sie in den folgenden Themen:

-   [Direct2D-YCbCr-Effekt](ycbcr-effect.md)
-   [**IWICPlanarBitmapSourceTransform-Schnittstelle**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform)

### <a name="support-for-block-compressed-formats-dds-files"></a>Unterstützung für blockkomprimierte Formate (DDS-Dateien)

Ab Windows 8.1 bietet Direct2D Unterstützung für Bitmaps, die DXGI \_ FORMAT \_ BC1 \_ UNORM-, DXGI \_ FORMAT \_ BC2 UNORM- und \_ DXGI FORMAT \_ \_ BC3 \_ UNORM-Pixeldaten enthalten. Apps können ihre Bildressourcen durch blockkomprimierte DDS-Images ersetzen. Dies kann den Grafikspeicherverbrauch und die Zeit für die Ressourcenerstellung erheblich reduzieren. Weitere Informationen finden Sie in den folgenden Themen:

-   [**ID2D1DeviceContext::CreateBitmapFromWicBitmap-Methode**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md)
-   [**IWICDdsFrameDecode-Schnittstelle**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode)

### <a name="rendering-priority"></a>Renderingpriorität

Ab Windows 8.1 bietet Direct2D Unterstützung für die Renderingpriorität pro Gerät. Mit diesem neuen Feature können Apps ein Gerät zwischen normaler Renderingpriorität (Standard) und niedriger Renderingpriorität (bei der das Gerät keine anderen Renderingaufgaben auf dem System blockiert) wechseln. Es wird empfohlen, dass Apps eine niedrige Renderingpriorität für Aufgaben verwenden, die für die Reaktionsfähigkeit des Benutzers nicht entscheidend sind, z. B. Vorabrendering von Inhalten, Rendering, minimiertes Rendering und andere Vorgänge, die in der Regel im Hintergrund ausgeführt werden. Weitere Informationen finden Sie in den folgenden Themen:

-   [**ID2D1Device1::SetRenderingPriority-Methode**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority)
-   [**D2D1 \_ RENDERING \_ PRIORITY-Enumeration**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority)

## <a name="whats-new-for-windows-8"></a>Neues bei Windows 8

Die folgenden Features und APIs wurden hinzugefügt oder für Windows 8.

Die neuen Direct2D-Schnittstellen werden auf Windows 7 mit installierter [Plattformupdate für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) unterstützt.

Die Semantik von Direct2D für Geräte und Gerätekontexte wurde aktualisiert, um der von Direct3D verwendeten Semantik stärker zu ähneln und eine präzise Operation für Windows Store bereitstellen. Weitere [Informationen finden Sie unter](devices-and-device-contexts.md) Geräte und Gerätekontexte.

Ausgewählte verwandte APIs:

-   [**ID2D1Geräte**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

Mit der Befehlslisten-API können Sie den Renderingpfad für beim Rendern und Drucken auf dem Bildschirm freigeben. Außerdem können Sie primitive Typen verwenden, um einen Bildpinsel zum Auffüllen von Primitiven zu erstellen.

Ausgewählte verwandte APIs:

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Direct2D-Effekte](effects-overview.md) sind eine Reihe von APIs, die neu in Windows 8 sind, um qualitativ hochwertige Effekte auf Bilder anwenden zu können. Sie enthält auch APIs, mit denen Sie eigene benutzerdefinierte Effekte erstellen können.

Ausgewählte verwandte APIs:

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

Ab Windows 8 enthält Direct2D zusätzliche APIs zum Erstellen von Multithread-Apps. Weitere Informationen finden Sie unter [Multithread-Direct2D-Apps.](multi-threaded-direct2d-apps.md)

Ausgewählte verwandte APIs:

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**\_D2D1-FACTORYTYP \_ \_ \_ MULTITHREADING**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 