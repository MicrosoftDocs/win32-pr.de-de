---
title: Übersicht über die Direct2D-API
description: Bietet eine Übersicht über das Direct2D-Objektmodell.
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D, Informationen
- Direct2D, Headerdateien
- Direct2D,Objektmodell
- Direct2D, Schnittstellen
- ID2D1Factory-Schnittstelle
- Direct2D, Renderziele
- Renderziele, Informationen
- Direct2D, Zeichnungsbefehle
- Renderziele, Zeichnungsbefehle
- Direct2D, Fehlerbehandlung
- Renderziele,Fehlerbehandlung
- Fehlerbehandlung
- Pinsel
- Renderziele, Pinsel
- geometries
- Direct2D, Geometrien
- Bitmaps für Direct2D
- Direct2D, Bitmaps
- Primitive
- Direct2D, Primitive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54f318e3542d54ee92817193ef6b749a3ba1cf4678407ca7a12f28c6c187ae86
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074994"
---
# <a name="direct2d-api-overview"></a>Übersicht über die Direct2D-API

Direct2D bietet eine API ähnlich wie Direct3D für die Verwendung mit C oder C++. Die API macht eine Vielzahl von zeichnungsbezogenen Funktionen verfügbar:

-   Rendern von Zielen für das Anzeigen und Rendern außerhalb des Bildschirms mit Direct2D, Direct3D oder GDI.
-   Objekte zum Verwalten des Zeichnungszustands, z. B. Koordinatenraumtransformationen und Antialiasingmodi.
-   Darstellungen für geometrische Daten und Funktionen für die Geometrieverarbeitung.
-   Renderingfunktionalität für Bitmaps, Geometrien und Text.
-   Stellen Sie für die Verwendung grafischer Inhalte, die mithilfe von GDI oder Direct3D erstellt wurden, ein.

Dieses Thema bietet eine Übersicht über die Objekte, aus denen die Direct2D-API besteht. Sie enthält die folgenden Abschnitte:

-   [Direct2D-Headerdateien](#direct2d-header-files)
-   [Direct2D-Schnittstellen](#direct2d-interfaces)
-   [Die ID2D1Factory-Schnittstelle](#the-id2d1factory-interface)
-   [Renderziele](#render-targets)
    -   [Renderzielfeatures](#render-target-features)
    -   [Rendern von Zielressourcen](#render-target-resources)
    -   [Zeichnungsbefehle](#drawing-commands)
    -   [Fehlerbehandlung](#error-handling)
-   [Zeichnungsressourcen](#drawing-resources)
    -   [Pinsel](#brushes)
    -   [Geometrien](#geometries)
    -   [Bitmaps](#bitmaps)
-   [Zeichnen von Text](#drawing-text)
-   [Direct2D-Primitive](#direct2d-primitives)
-   [Zugehörige Themen](#related-topics)

## <a name="direct2d-header-files"></a>Direct2D-Headerdateien

Die Direct2D-API wird durch die folgenden Headerdateien definiert.

| Headerdatei         | BESCHREIBUNG                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------|
| d2d1.h              | Definiert C- und C++-Versionen der primären Direct2D-API.                                                                      |
| d2d1helper.h        | Definiert C++-Hilfsfunktionen, -Klassen und -Strukturen.                                                                       |
| d2dbasetypes.h      | Definiert Zeichnungsprimitiven für Direct2D, z. B. Punkte und Rechtecke. Dieser Header ist in d2d1.h enthalten.                 |
| d2derr.h            | Definiert die Fehlercodes für Direct2D. Dieser Header ist in d2d1.h enthalten.                                                   |
| d2d1 \_ 1.h           | Definiert C- und C++-Versionen der primären Direct2D-API für Windows 8 und höher.                                              |
| d2d1 \_ 1helper.h     | Definiert C++-Hilfsfunktionen, -Klassen und -Strukturen für Windows 8 und höher.                                               |
| d2d1effects.h       | Definiert C- und C++-Versionen der Imageeffekte, die Teil der Direct2D-API für Windows 8 und höher sind.                            |
| d2d1effecthelpers.h | Definiert C++-Hilfsfunktionen, Klassen und Strukturen der Bildeffekte, die Teil der Direct2D-API für Windows 8 und höher sind. |



 

Um Direct2D zu verwenden, sollte Ihre Anwendung die Headerdatei d2d1.h enthalten.

Um eine Direct2D-Anwendung zu kompilieren, fügen Sie d2d1.lib zur Liste der Bibliotheken hinzu. Sie finden d2d1.h und d2d1.lib in [Windows Software Development Kit (SDK) für Windows 7.](https://msdn.microsoft.com/windows/bb980924.aspx)

In den folgenden Abschnitten werden einige der allgemeinen Schnittstellen beschrieben, die von der Direct2D-API bereitgestellt werden.

## <a name="direct2d-interfaces"></a>Direct2D-Schnittstellen

Im Stammverzeichnis der Direct2D-API befinden sich die Schnittstellen [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) und [**ID2D1Resource.**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) Ein **ID2D1Factory-Objekt** erstellt **ID2D1Resource-Objekte** und dient als Ausgangspunkt für die Verwendung von Direct2D. Alle anderen Direct2D-Objekte erben von der **ID2D1Resource-Schnittstelle.** Es gibt zwei Arten von Direct2D-Ressourcen: geräteunabhängige Ressourcen und geräteabhängige Ressourcen.

-   Geräteunabhängige Ressourcen sind keinem bestimmten Renderinggerät zugeordnet und können für die Lebensdauer einer Anwendung beibehalten werden.
-   Geräteabhängige Ressourcen werden einem bestimmten Renderinggerät zugeordnet und funktionieren nicht mehr, wenn dieses Gerät entfernt wird.

(Weitere Informationen zu Ressourcen und zur Ressourcenfreigabe finden Sie in der [Ressourcenübersicht.)](resources-and-resource-domains.md)

## <a name="the-id2d1factory-interface"></a>Die ID2D1Factory-Schnittstelle

Die [**ID2D1Factory-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) ist der Ausgangspunkt für die Verwendung von Direct2D. Sie verwenden **eine ID2D1Factory** zum Instanziieren von Direct2D-Ressourcen. Um eine ID2D1Factory zu erstellen, verwenden Sie eine der [**CreateFactory-Methoden.**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory)

Eine Factory definiert einen Satz von Methoden zum Erstellen von *Ressourcen,* die die folgenden Zeichnungsressourcen erzeugen können:

-   Renderziele sind Objekte, die Zeichnungsbefehle rendern.
-   Zeichnungszustandsblöcke sind Objekte, die Zeichnungszustandsinformationen speichern, z. B. die aktuelle Transformation und den Antialiasingmodus.
-   Geometrien sind Objekte, die einfache und potenziell komplexe Formen darstellen.

Eines der nützlichsten Objekte, die eine Factory erstellen kann, ist die [**ID2D1RenderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)die im folgenden Abschnitt beschrieben wird.

## <a name="render-targets"></a>Renderziele

Ein Renderziel ist eine Ressource, die von der [**ID2D1RenderTarget-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) erbt. Ein Renderziel erstellt Ressourcen zum Zeichnen und führt Zeichnungsvorgänge aus. Es gibt verschiedene Arten von Renderzielen, die zum Rendern von Grafiken auf folgende Weise verwendet werden können:

-   [**ID2D1HwndRenderTarget-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) rendern Inhalt in einem Fenster.
-   [**ID2D1DCRenderTarget-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) werden in einem GDI-Gerätekontext gerendert.
-   Bitmap-Renderzielobjekte rendern Inhalt in einer Bitmap außerhalb des Bildschirms.
-   DXGI Renderzielobjekte werden zur Verwendung mit Direct3D auf einer DXGI-Oberfläche gerendert.

Da ein Renderziel einem bestimmten Renderinggerät zugeordnet ist, ist es eine geräteabhängige Ressource und funktioniert nicht mehr, wenn das Gerät entfernt wird.

### <a name="render-target-features"></a>Renderzielfeatures

Sie können angeben, ob ein Renderziel die Hardwarebeschleunigung verwenden soll und ob die Remoteanzeige vom lokalen Oder Remotecomputer gerendert werden soll. Renderziele können für das Rendern mit Alias oder Antialiasing eingerichtet werden. Zum Rendern von Szenen mit einer großen Anzahl von Primitiven kann ein Entwickler auch 2D-Grafiken im Aliasmodus rendern und D3D-Multisample-Antialiasing verwenden, um eine höhere Skalierbarkeit zu erzielen.

Renderziele können zeichnungsvorgänge auch in Ebenen gruppieren, die durch die [**ID2D1Layer-Schnittstelle dargestellt**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) werden. Ebenen sind nützlich für das Sammeln von Zeichnungsvorgängen, die beim Rendern eines Frames zusammengesetzt werden sollen. In einigen Szenarien kann dies eine nützliche Alternative zum Rendern in ein Bitmaprenderingziel und anschließendes Wiederverwendnen des Bitmapinhalts sein, da die Zuordnungskosten für Ebenen niedriger sind als für eine [**ID2D1BitmapRenderTarget.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget)

Renderziele können neue Renderziele erstellen, die mit sich selbst kompatibel sind. Dies ist nützlich für das zwischengeschaltete Off-Screen-Rendering, wobei die verschiedenen Renderzieleigenschaften beibehalten werden, die für das Original festgelegt wurden.

Es ist auch möglich, mithilfe von GDI auf einem Direct2D-Renderziel zu rendern, indem [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) auf einem Renderziel für [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)aufgerufen wird, das [**über GetDC-**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) und [**ReleaseDC-Methoden**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) verfügt, die zum Abrufen eines GDI-Gerätekontexts verwendet werden können. Das Rendern über GDI ist nur möglich, wenn das Renderziel mit dem [**\_ \_ \_ \_ \_ GDI-kompatiblen Flag D2D1 RENDER TARGET USAGE erstellt**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) wurde. Dies ist nützlich für Anwendungen, die in erster Linie mit Direct2D gerendert werden, aber über ein Erweiterbarkeitsmodell oder andere Legacyinhalte verfügen, die die Möglichkeit zum Rendern mit GDI erfordern. Weitere Informationen finden Sie unter [Direct2D und GDI Interoperability Overview (Übersicht über die Direct2D- und GDI-Interoperabilität).](direct2d-and-gdi-interoperation-overview.md)

### <a name="render-target-resources"></a>Rendern von Zielressourcen

Wie eine Factory kann ein Renderziel Zeichnungsressourcen erstellen. Alle von einem Renderziel erstellten Ressourcen sind geräteabhängige Ressourcen (genau wie das Renderziel). Ein Renderziel kann die folgenden Ressourcentypen erstellen:

-   Bitmaps
-   Pinsel
-   Ebenen
-   Gittermodelle

### <a name="drawing-commands"></a>Zeichnungsbefehle

Zum Rendern von Inhalten verwenden Sie die Renderziel-Zeichnungsmethoden. Bevor Sie mit dem Zeichnen beginnen, rufen Sie die [**ID2D1RenderTarget::BeginDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) auf. Nach Abschluss des Zeichnens rufen Sie die [**ID2D1RenderTarget::EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) auf. Zwischen diesen Aufrufen verwenden Sie die Methoden Draw und Fill, um Zeichnungsressourcen zu rendern. Die meisten Draw- und Fill-Methoden nehmen eine Form (entweder eine primitive oder eine Geometrie) und einen Pinsel zum Auffüllen oder Umformn der Form an.

Renderziele bieten auch Methoden zum Ausschneiden, Anwenden von Deckkraftmasken und Transformieren des Koordinatenraums.

Direct2D verwendet ein linkshändiges Koordinatensystem: Positive x-Achsenwerte werden nach rechts und positive Werte der y-Achse nach unten fortgesetzt.

### <a name="error-handling"></a>Fehlerbehandlung

Renderziel-Zeichnungsbefehle geben nicht an, ob der angeforderte Vorgang erfolgreich war. Um herauszufinden, ob Zeichnungsfehler aufgetreten sind, rufen Sie die [**Flush-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) des Renderziels oder die [**EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) auf, um ein **HRESULT zu erhalten.**

## <a name="drawing-resources"></a>Zeichnungsressourcen

In den folgenden Abschnitten werden einige der Ressourcen beschrieben, die von den Renderziel- und Factoryschnittstellen erstellt werden können.

### <a name="brushes"></a>Pinsel

Ein Pinsel, dargestellt durch die [**ID2D1Brush-Schnittstelle,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) ist eine geräteabhängige Ressource, die von einem Renderziel erstellt wird und einen Bereich mit seiner Ausgabe zeichnet. Verschiedene Pinsel haben unterschiedliche Ausgabetypen. Einige Pinsel zeichnen einen Bereich mit einer Volltonfarbe, andere mit einem Farbverlauf oder einem Bild. Direct2D bietet vier Arten von Pinseln:

-   [**ID2D1SolidColorBrush zeichnet**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) einen Bereich mit einer Volltonfarbe.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) zeichnet einen Bereich mit einem linearen Farbverlauf, der zwei oder mehr Farben über eine Linie, die Farbverlaufsachse, kombiniert.
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) zeichnet einen Bereich mit einem radialen Farbverlauf, der zwei oder mehr Farben um eine Ellipse kombiniert.
-   [**ID2D1BitmapBrush zeichnet**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) einen Bereich mit einer Bitmap.

Um einen Pinsel zu erstellen, verwenden Sie eine der [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Create Brush-Methoden, z. B. *<Type>* [**CreateRadialGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush)). Pinsel können mit den Methoden Draw und Fill eines Renderziels verwendet werden, um einen Formstrich oder eine Kontur oder eine Deckkraftmaske zu zeichnen.

Weitere Informationen zu Pinseln finden Sie in der [Übersicht über Pinsel.](direct2d-brushes-overview.md)

### <a name="geometries"></a>Geometrien

Zusätzlich zu grundlegenden Zeichnungsprimitiven wie Punkten, Rechtecke und Ellipsen stellt Direct2D die [**ID2D1Geometry-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) zum Beschreiben einfacher und komplexer Formen bereit. Schnittstellen, die von **ID2D1Geometry** erben, definieren verschiedene Arten von Formen, z. B. [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) zum Darstellen von Rechtecke, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) zum Darstellen abgerundeter Rechtecke und [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) zum Darstellen von Ellipsen.

Komplexere Formen können mithilfe der [**ID2D1GeometrySink-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) erstellt werden, um eine Reihe von Abbildungen anzugeben, die aus Linien, Kurven und Bogen bestehen. **ID2D1GeometrySink** wird an die Open-Methode einer [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) übergeben, um eine komplexe Geometrie zu generieren. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) kann auch mit der DirectWrite-API verwendet werden, um Pfadgliederungen von formatiertem Text für das rendering-Rendering zu extrahieren.

Die Geometrieschnittstellen stellen Methoden zum Bearbeiten von Formen bereit, indem vorhandene Geometrien verbreitert oder vereinfacht werden oder indem die Schnittmenge oder Vereinigung mehrerer Geometrien generiert wird. Sie bieten auch Methoden zum Bestimmen, ob Geometrien sich überschneiden oder überlappen, Begrenzungsinformationen abrufen, den Bereich oder die Länge einer Geometrie berechnen und Positionen entlang einer Geometrie interpolieren. Direct2D bietet auch die Möglichkeit, ein Gitter aus Dreiecken zu erstellen, das aus einer Geometrie mosaikiert ist.

Um eine Geometrie zu erstellen, verwenden Sie eine der [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)::Create Geometry-Methoden, z.B. *<Type>* [**CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry). Eine Geometrie ist eine geräteunabhängige Ressource.

Zum Rendern einer Geometrie verwenden Sie die [**DrawGeometry-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) und [**FillGeometry-Methoden**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) eines Renderziels.

Weitere Informationen zu Geometrien finden Sie in der [Übersicht über Geometrien.](direct2d-geometries-overview.md)

### <a name="bitmaps"></a>Bitmaps

Direct2D stellt keine Methoden zum Laden oder Speichern von Bitmaps zur Verfügung. stattdessen können Sie Bitmaps mithilfe der Windows [Imaging Component (WIC) erstellen.](../wic/-wic-about-windows-imaging-codec.md) Bitmapressourcen können mit WIC geladen und dann zum Erstellen einer [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) über die [**ID2D1RenderTarget::CreateBitmapFromWicBitmap-Methode verwendet**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) werden.

Bitmaps können auch aus In-Memory-Daten erstellt werden, die auf andere Wege eingerichtet wurden. Nachdem eine Bitmap erstellt wurde, kann sie mit der [**DrawBitmap-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) des Renderziels oder mit einem Bitmappinsel gezeichnet werden.

Da das Erstellen von Bitmapressourcen auf Hardwarerenderzielen häufig ein aufwendiger Vorgang ist, kann Direct2D den Inhalt einer Bitmap (oder eines Teils der Bitmap) mithilfe der [**Methoden CopyFromBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap) [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)und [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) aktualisieren. Die Verwendung dieser Methoden kann möglicherweise die Kosten sparen, die mit zusätzlichen GPU-Texturzuordnungen verbunden sind.

## <a name="drawing-text"></a>Zeichnen von Text

Direct2D wurde für die Arbeit mit den Textvorgängen der neuen Text-API entwickelt, DirectWrite. Um die Verwendung der DirectWrite-API zu vereinfachen, stellen Renderziele drei Methoden zum Rendern DirectWrite Textressourcen bereit: [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)), [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)und [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Da Direct2D die GPU für den ClearType-Textrenderingprozess verwendet, bietet Direct2D eine niedrigere CPU-Auslastung als GDI für Textvorgänge und eine bessere Skalierbarkeit, da mehr GPU-Verarbeitungsleistung verfügbar ist.

[**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) ist für die einfachsten Szenarien konzipiert, in denen eine Unicode-Textzeichenfolge mit minimaler Formatierung gerendert wird. Komplexeres Layout und typografische Flexibilität wird durch die [**ID2D1RenderTarget::D rawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) bereitgestellt, die ein [**IDWriteTextLayout-Objekt**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) verwendet, um den Inhalt und die Formatierung anzugeben, die gerendert werden sollen. **Mit IDWriteTextLayout** können Sie individuelle Formatierungen für Teilzeichenfolgen von Text und andere erweiterte Typografieoptionen angeben.

In Szenarien, in denen eine genaue Steuerung des Layouts auf Glyphenebene erforderlich ist, kann die [**ID2D1RenderTarget::D rawGlyphRun-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) in Verbindung mit den von DirectWrite bereitgestellten Messmöglichkeiten verwendet [werden.](../directwrite/direct-write-portal.md)

Um die DirectWrite-API zu verwenden, schließen Sie den dwrite.h-Header ein. Wie Direct2D verwendet DirectWrite eine Factory, [**IDWriteFactory,**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) um Textobjekte zu erstellen. Verwenden Sie [**die DWriteCreateFactory-Funktion,**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) um eine Factory zu erstellen, und verwenden Sie dann deren Create-Methoden, um DirectWrite (z. B. [**IDWriteTextFormat) zu erstellen.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))

Weitere Informationen zu DirectWrite finden Sie im Thema Introducing DirectWrite (Einführung [in DirectWrite).](../directwrite/introducing-directwrite.md)

## <a name="direct2d-primitives"></a>Direct2D-Primitive

Direct2D definiert einen Satz primitiver Typen, die denen ähneln, die von anderen Zeichnungs-APIs bereitgestellt werden. Sie stellt eine Farbstruktur, eine Matrixstruktur zum Ausführen von Transformationen sowie Gleitkomma- und Ganzzahlversionen von Punkten, Rechtecke, Ellipsen und Größenstrukturen zur Verfügung. In der Regel verwenden Sie die Gleitkommaversionen dieser Strukturen.

Sie verwenden keine Factory oder kein Renderziel, um Direct2D-Primitive zu instanziieren. Sie können sie direkt erstellen oder die in d2d1helper.h definierten Hilfsmethoden verwenden, um sie zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> <dt>

[DirectWrite Hallo Welt Beispiel](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Einführung DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Übersicht über Ressourcen](resources-and-resource-domains.md)
</dt> <dt>

[Windows Imaging-Komponente (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 