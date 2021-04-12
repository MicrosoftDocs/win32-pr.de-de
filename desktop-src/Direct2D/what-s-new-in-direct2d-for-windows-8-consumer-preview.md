---
title: Neues in Direct2D
description: Im folgenden finden Sie einige der neuen Ergänzungen zu Direct2D.
ms.assetid: BA459FF0-9457-4652-A97C-BD4EC57EC8E2
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 9208ded926bda197baf41d9195c13cacd8f7079b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315651"
---
# <a name="whats-new-in-direct2d"></a>Neues in Direct2D

Im folgenden finden Sie einige der neuen Ergänzungen zu Direct2D.

## <a name="whats-new-for-windows-10-creators-update"></a>Neuerungen bei Windows 10 Creators Update

Die folgenden Features und APIs wurden für Windows 10 Creators Update hinzugefügt oder aktualisiert.

### <a name="support-for-svg-image-rendering"></a>Unterstützung für das SVG-Image Rendering

Ab Windows 10 Creators Update bietet Direct2D Unterstützung für das Durchsuchen und Zeichnen von SVG-Bildern, sodass Entwickler Assets in Ihren bevorzugten vektorkunst Tools Rendering können, ohne Sie zuerst in Rasterbilder zu wandeln. Verwenden Sie diese Funktion, um den Datenträger Bedarf und das Skalierungs Verhalten ihrer in-App-iconographie zu verbessern, und verwenden Sie renderingkonventionen New SVG Object Model-APIs, um programmgesteuerte Änderungen am SVG Ihrer APP vorzunehmen. Beachten Sie, dass Direct2D nur eine begrenzte Teilmenge von SVG unterstützt, die für Images geeignet ist und nicht alle SVG-Zeichnungs Features unterstützt. Wenn Sie die SVG-Kompatibilität von Browser Stufen oder die weborientierten SVG-Features von SVG benötigen, sollten Sie stattdessen das [XAML-WebView-Steuer](/uwp/api/Windows.UI.Xaml.Controls.WebView) Element verwenden. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Direct2D SVG-Bild Rendering (Beispiel)](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DSvgImage)
-   [SVG-Unterstützung](svg-support.md)
-   [**ID2D1DeviceContext5:: kreatesvgdocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createsvgdocument) -Methode
-   [**ID2D1DeviceContext5::D rawsvgdocument**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-drawsvgdocument) -Methode
-   [**ID2D1SvgElement**](/windows/win32/api/d2d1svg/nn-d2d1svg-id2d1svgelement) -Schnittstelle

### <a name="improved-support-for-color-management"></a>Verbesserte Unterstützung für die Farbverwaltung

Ab Windows 10 Creators Update bietet Direct2D verbesserte Farb Verwaltungsfunktionen. Entwickler benötigen kein ICC-Profil mehr, um den renderingkonventionen Color Management Effect zu verwenden. Sie können jetzt DXGI-Farbbereiche verwenden oder eine eigene parametrisierte Farbraum-Definition erstellen. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Farb Verwaltungs Effekt](color-management.md)
-   [**ID2D1DeviceContext5:: kreatecolorcontextfromdxgicolorspace**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromdxgicolorspace)
-   [**ID2D1DeviceContext5:: kreatecolorcontextfromsimplecolorprofile**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext5-createcolorcontextfromsimplecolorprofile(constd2d1_simple_color_profile_id2d1colorcontext1))

## <a name="whats-new-for-windows-10-anniversary-update"></a>Neuerungen bei Windows 10 Anniversary Update

Die folgenden Features und APIs wurden für Windows 10 Anniversary Update hinzugefügt oder aktualisiert.

### <a name="improved-support-for-color-fonts"></a>Verbesserte Unterstützung für farbige Schriftarten

Ab Windows 10 Anniversary Update unterstützt Direct2D jetzt das Rendern einer größeren Vielzahl von Farb Schriftart Formaten, sodass Entwickler mehr Arten von Schriftarten in ihren Direct2D-gestützten Apps als je zuvor verwenden können. Unter anderem werden folgende Elemente unterstützt:

-   Die OpenType-Tabelle "colr", die kompakten Vektor Inhalte in Schriftarten ermöglicht. (Wird seit Windows 8.1 unterstützt.)
-   Die OpenType-Tabelle "SVG", die SVG-Inhalte in Schriftarten ermöglicht.
-   Die Tabelle "cbdt" OpenType, die Farb Bitmapinhalt in Schriftarten ermöglicht.
-   Die OpenType-Tabelle "sbix", die Farb Bitmapinhalt in Schriftarten ermöglicht.

Direct2D unterstützt diese Farb Schriftart Formate automatisch, wenn das Flag zum [**\_ Aktivieren der \_ \_ \_ \_ Farb \_ Schriftart für D2D1-zeichnen**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_draw_text_options) aktiviert ist. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Farbige Schriftarten](/windows/desktop/DirectWrite/color-fonts)
-   [Beispiel für DirectWrite-Farb Glyphe](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/DWriteColorGlyph)

### <a name="new-image-effects"></a>Neue Bildeffekte

Ab Windows 10 Anniversary Update umfasst Direct2D die Alpha amask-, Crossfade-, Deckkraft-und tint-Effekte. Diese Funktionalität war zuvor über bestimmte Konfigurationen von zusammengesetzten, arithmeticcomposite-und ColorMatrix-Effekten verfügbar, aber die neuen integrierten Effekte vereinfachen das Ausführen dieser gängigen Vorgänge.

## <a name="whats-new-for-windows-10"></a>Neuerungen in Windows 10

Die folgenden Features und APIs wurden für Windows 10 hinzugefügt oder aktualisiert.

### <a name="sprite-batches"></a>Sprite-Batches

Ab Windows 10 bietet Direct2D Unterstützung für das Erstellen und Rendern von Sprite-Batches. Im Vergleich zur allgemeinen [**DrawImage**](id2d1devicecontext-drawimage-overload.md) -Methode verursachen Sprite-Batches erheblich weniger CPU-Aufwand pro Bild. Dadurch eignen Sie sich ideal für Szenarien, in denen Hunderte oder Tausende gleichzeitige Images, z. b. Spiel Sprite oder Partikelsysteme, beteiligt sind. Weitere Informationen finden Sie unter den folgenden Themen:

-   [**ID2D1DeviceContext3:: kreatespritebatch**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-createspritebatch) -Methode
-   [**ID2D1DeviceContext3::D rawspritebatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-id2d1devicecontext3-drawspritebatch(id2d1spritebatch_id2d1bitmap_d2d1_bitmap_interpolation_mode_d2d1_sprite_options)) -Methoden
-   [**ID2D1SpriteBatch**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1spritebatch) -Schnittstelle

### <a name="gradient-meshes"></a>Farbverlaufs Netze

Ab Windows 10 stellt Direct2D einen neuen primitiven für Farbverlaufs Netze bereit. Farbverlaufs Netze werden häufig von professionellen Illustratoren in Grafik Entwurfs Software verwendet und ermöglichen es Künstlern, komplexe (sogar fotorealistische) mehrfarbige Formen mit sämtlichen Speicher-und Skalierbarkeits Vorteilen von Vektoren zu Renderern. Weitere Informationen finden Sie in den folgenden Themen:

-   [Beispiel für ein Direct2D-Farbverlaufsgitter](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DGradientMesh)
-   [**D2D1 \_ \_ \_ Patchstruktur des Farbverlaufs Netzes**](/windows/desktop/api/d2d1_3/ns-d2d1_3-d2d1_gradient_mesh_patch)
-   [**ID2D1DeviceContext2::D rawgradientmesh**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawgradientmesh) -Methode

### <a name="improved-image-loading-apis"></a>Verbessertes Laden von Image-APIs

Ab Windows 10 bietet Direct2D eine neue API zum Laden von Images: ID2D1ImageSource. Die Bildquelle verbessert die vorhandenen Images zum Laden von Images, einschließlich "kreatebitmapfromwicbitmap", "Bitmap Source Effect" und "YCbCr". Die Direct2D-Image Quelle kombiniert die Funktionen dieser APIs mit Unterstützung für beliebig große Bilder, einfache Integration in Druck und Effekte und zahlreiche Optimierungen einschließlich YCbCr JPEG und indiziertes JPEG. Weitere Informationen finden Sie in den folgenden Themen:

-   [Direct2D-SDK-Beispiel für Foto Anpassung](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)
-   [**ID2D1ImageSource**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesource)
-   [**ID2D1ImageSourceFromWic**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1imagesourcefromwic)
-   [Iwicjpgframedecode:: setindizierung](/windows/desktop/api/wincodec/nf-wincodec-iwicjpegframedecode-setindexing)

### <a name="improved-support-for-ink-rendering"></a>Verbesserte Unterstützung für das frei Hand Rendering

Ab Windows 10 stellt Direct2D einen neuen primitiven zum Darstellen von Hand Strichen dar. Direct2D Ink-Striche werden von Bezier-Kurven definiert, unterstützen unterschiedliche NIB-Formen und-Transformationen und verfügen möglicherweise über eine fest-oder Variablen Stärke. Renderingkonventionen die integrierte Unterstützung für frei Hand Eingaben ermöglicht apps das einfache Rendering schneller und komplexer frei Hand Eingaben als vorherige Ansätze, bei denen es in der Regel erforderlich war, dass apps frei Hand Eingaben selbst verwalten, als eine Reihe von Ellipsen und vier eckalen. Weitere Informationen finden Sie unter den folgenden Themen:

-   [**ID2D1Ink-Schnittstelle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1ink)
-   [**ID2D1DeviceContext2::D rawink-Methode**](/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1devicecontext2-drawink)
-   [**ID2D1InkStyle-Schnittstelle**](/windows/win32/api/d2d1_3/nn-d2d1_3-id2d1inkstyle)

### <a name="effect-shader-linking"></a>Effekt-Shader-Verknüpfung

Direct2D Effekte werden mithilfe von HLSL Pixel, Vertex und/oder COMPUTE-Shadern implementiert. Ab Windows 10 analysiert Direct2D nun automatisch die Auswirkungen von Diagrammen auf Möglichkeiten zum kombinieren und ausführen einzelner Shader. Dies kann zu einer deutlichen Steigerung des Wirkungs Durchsatzes führen. Consumer integrierter Effekte müssen nichts Unternehmen, um von der shaderverknüpfung des Shaders profitieren zu können. Entwickler, die ihre eigenen benutzerdefinierten Effekte erstellen, sollten jedoch die aktualisierten bewährten Methoden befolgen, um den Effekt-Shader-Link zu nutzen. Weitere Informationen finden Sie unter den folgenden Themen:

-   [Effektshader-Verknüpfung](effect-shader-linking.md)
-   [Direct2D HLSL-Hilfsprogramme](hlsl-helpers.md)
-   [Direct2D Custom Effects SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects)

Der Effekt der shaderverknüpfung ist so konzipiert, dass sich keine Auswirkungen auf die visuelle Ausgabe der Effekte haben. Dies ist jedoch aufgrund eines bestimmten Verhaltens bei der Auswirkung auf die Genauigkeit und das numerische Clipping nicht immer möglich. Weitere Informationen zur Steuerung dieser Verhaltensweisen finden Sie unter:

-   [Steuern der Genauigkeit und des numerischen Clipping in Effekt Diagrammen](precision-and-clipping-in-effect-graphs.md)

### <a name="new-built-in-effects"></a>Neue integrierte Effekte

Ab Windows 10 umfasst Direct2D einen umfangreichen Satz neuer integrierter Effekte, die die wichtigsten Entwickler Anfragen erfüllen und neue Arten von visuellen Szenarios ermöglichen. Die neuen Effekte lauten:

### <a name="color"></a>Farbe:

-   [RGB-zu-Hue-Effekt](rgb-to-hue-effect.md)
-   [Effekt von Hue auf RGB](hue-to-rgb-effect.md)
-   [3D-Such Tabellen Effekt](3d-lookup-table-effect.md)

### <a name="photo"></a>Foto

-   [Kontrast Effekt](contrast-effect.md)
-   [Expositions Effekt](exposure-effect.md)
-   [Graustufen Effekt](grayscale-effect.md)
-   [Highlights und Schatteneffekte](highlights-and-shadows-effect.md)
-   [Effekt umkehren](invert-effect.md)
-   [* Pia-Effekt](sepia-effect.md)
-   [Schärfe Effekt](sharpen-effect.md)
-   [Auswirkung](straighten-effect.md)
-   [Temperatur-und Tönungs-Effekt](temperature-and-tint-effect.md)
-   [Vigffekt](vignette-effect.md)

### <a name="filter"></a>Filter:

-   [Edge-Erkennungs Effekt](edge-detection-effect.md)

### <a name="stylize"></a>Farbig

-   [Emboss-Effekt](emboss-effect.md)
-   [Auswirkung auf die Folge](posterize-effect.md)

### <a name="transparency"></a>Transparenz:

-   [Chroma-Schlüssel Effekt](chromakey-effect.md)

Das [Direct2D Photo-Anpassungs-SDK-Beispiel](https://github.com/Microsoft/Windows-universal-samples/tree/master/Samples/D2DPhotoAdjustment)zeigt, wie sich die Ergebnisse, Sättigung, Kontrast, Hervorhebung und Schatten sowie Temperatur und Tönungs auswirken.

## <a name="whats-new-for-windows-81"></a>Neuerungen bei Windows 8.1

Die folgenden Features und APIs wurden für Windows 8.1 hinzugefügt oder aktualisiert.

Beginnend mit Windows 8.1 baut Direct2D auf Direct3D 11,2 auf.

### <a name="geometry-realizations"></a>Geometrie-Neumessungen

Ab Windows 8.1 bietet Direct2D Geometrie-Neustarts. Geometry-Anpassungen ermöglichen es Anwendungen, die Leistung von Geometrie Rendering in bestimmten Situationen zu verbessern, ohne dass einige Nachteile der rasterierung von Geometrie auf eine Bitmap auftreten. Weitere Informationen finden Sie unter den folgenden Themen:

-   [**ID2D1Device1**](/windows/win32/api/d2d1_2/nn-d2d1_2-id2d1device1) -Schnittstelle
-   [**ID2D1DeviceContext1::D rawgeometryrealisation**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1devicecontext1-drawgeometryrealization) -Methode

### <a name="support-for-jpeg-ycbcr-images"></a>Unterstützung für JPEG YCbCr-Bilder

Ab Windows 8.1 bietet Direct2D Unterstützung für das Rendern von Bilddaten im CbCr-Format. Apps können JPEG-Inhalte in ihrer nativen ' CbCr '-Darstellung darstellen, anstatt Sie in BGRA zu komprimieren. Dadurch kann die Auslastung des Grafik Speichers und die Ressourcen Erstellung erheblich reduziert werden. Weitere Informationen finden Sie unter den folgenden Themen:

-   Direct2D [YCbCr-Effekt](ycbcr-effect.md)
-   [**Iwicplanarbitmapsourcetransform**](/windows/desktop/api/wincodec/nn-wincodec-iwicplanarbitmapsourcetransform) -Schnittstelle

### <a name="support-for-block-compressed-formats-dds-files"></a>Unterstützung für Block komprimierte Formate (DDS-Dateien)

Ab Windows 8.1 bietet Direct2D Unterstützung für Bitmaps, die das DXGI- \_ Format \_ BC1 \_ unorm, DXGI \_ \_ -Format BC2 \_ unorm und DXGI-Format \_ \_ BC3 \_ unorm Pixeldaten enthalten. Apps können Ihre Image Ressourcen durch Block komprimierte DDS-Images ersetzen. Dadurch kann die Auslastung des Grafik Speichers und die Ressourcen Erstellung erheblich reduziert werden. Weitere Informationen finden Sie unter den folgenden Themen:

-   [**ID2D1DeviceContext:: kreatebitmapfromwicbitmap**](id2d1devicecontext-createbitmapfromwicbitmap-overload.md) -Methode
-   [**Iwicddsframedecode**](/windows/desktop/api/wincodec/nn-wincodec-iwicddsframedecode) -Schnittstelle

### <a name="rendering-priority"></a>Renderingpriorität

Ab Windows 8.1 bietet Direct2D Unterstützung für Geräte basierte renderingpriorität. Mit dieser neuen Funktion können apps zwischen normaler renderingpriorität (Standardeinstellung) und niedriger renderingpriorität wechseln (in der das Gerät keine anderen renderingtasks auf dem System blockiert). Es wird empfohlen, dass apps eine niedrige renderingpriorität für Aufgaben verwenden, die für die Benutzer Reaktionsfähigkeit nicht relevant sind, z. b. das vorab Rendering von Inhalten, das Rendering während der Minimierung und andere Vorgänge, die in der Regel im Hintergrund ausgeführt werden. Weitere Informationen finden Sie unter den folgenden Themen:

-   [**ID2D1Device1:: strenderingpriority**](/windows/win32/api/d2d1_2/nf-d2d1_2-id2d1device1-setrenderingpriority) -Methode
-   [**D2D1 \_ \_Renderprioritätsenumeration**](/windows/desktop/api/D2D1_2/ne-d2d1_2-d2d1_rendering_priority)

## <a name="whats-new-for-windows-8"></a>Neuerungen in Windows 8

Die folgenden Features und APIs wurden für Windows 8 hinzugefügt oder aktualisiert.

Die neuen Direct2D-Schnittstellen werden unter Windows 7 unterstützt, wobei das [Platt Form Update für Windows 7](/windows/desktop/direct3darticles/platform-update-for-windows-7) installiert ist.

Die renderingkonventionen-Semantik für Geräte und Geräte Kontexte wurde so aktualisiert, dass Sie der von Direct3D verwendeten Semantik ähnelt und einen präzisen Vorgang für Windows Store-Apps bereitstellt. Weitere Informationen finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md) .

Ausgewählte Verwandte APIs:

-   [**ID2D1Device**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1device)
-   [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext)

Mit der Befehlslisten-API können Sie den Renderingpfad für auf Bildschirm Rendering und-Druck freigeben. Außerdem können Sie mithilfe von primitiven einen Bild Pinsel zum Auffüllen primitiver Elemente erstellen.

Ausgewählte Verwandte APIs:

-   [**ID2D1CommandList**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1commandlist)
-   [**ID2D1PrintControl**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1printcontrol)
-   [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)

[Direct2D Effects](effects-overview.md) ist ein Satz von APIs, die neu in Windows 8 sind, um hochwertige Effekte auf Bilder anzuwenden. Sie enthält auch APIs, mit denen Sie eigene benutzerdefinierte Effekte erstellen können.

Ausgewählte Verwandte APIs:

-   [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
-   [**ID2D1EffectImpl**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectimpl)
-   [**ID2D1EffectContext**](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext)

Ab Windows 8 umfasst Direct2D zusätzliche APIs zum Entwickeln von Multithread-apps. Weitere Informationen finden Sie unter [Multithreaded Direct2D-apps](multi-threaded-direct2d-apps.md) .

Ausgewählte Verwandte APIs:

-   [**ID2D1MultiThread**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1multithread)
-   [**D2D1 \_ Factory \_ - \_ Typ \_ Multithread**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_factory_type)

 

 