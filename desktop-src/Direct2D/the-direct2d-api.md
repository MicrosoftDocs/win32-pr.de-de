---
title: Übersicht über die Direct2D-API
description: Bietet eine Übersicht über das Direct2D-Objektmodell.
ms.assetid: b1362ef6-40fc-4fa5-ba5b-22c622c39f04
keywords:
- Direct2D, Informationen zu
- Direct2D, Header Dateien
- Direct2D, Objektmodell
- Direct2D, Schnittstellen
- ID2D1Factory-Schnittstelle
- Direct2D, Renderziele
- Renderziele, Informationen
- Direct2D, Zeichnen von Befehlen
- Renderziele, Zeichnen von Befehlen
- Direct2D, Fehlerbehandlung
- Renderziele, Fehlerbehandlung
- Fehlerbehandlung
- Pinsel
- Renderziele, Pinsel
- geometries
- Direct2D, Geometrien
- Bitmaps für Direct2D
- Direct2D, Bitmaps
- Primitives
- Direct2D, primitive
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 858d03f626fe337b174f074d7725dcb1a636b463
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106340920"
---
# <a name="direct2d-api-overview"></a>Übersicht über die Direct2D-API

Direct2D stellt eine API ähnlich wie bei Direct3D für die Verwendung mit C oder C++ bereit. Die API stellt eine Vielzahl von Zeichnungs bezogenen Funktionen bereit:

-   Rendern Sie Ziele für Anzeige-und Offscreen-Rendering mithilfe von Direct2D, Direct3D oder GDI.
-   Objekte zum Verwalten des Zeichnungs Zustands, z. b. Koordinatenraum Transformationen und Antialiasing-Modi.
-   Darstellungen für geometrische Daten und Funktionen für die Geometrie Verarbeitung.
-   Rendering-Funktionalität für Bitmaps, Geometrien und Text.
-   Bereitstellung für die Verwendung grafischer Inhalte, die mit GDI oder Direct3D erstellt wurden.

Dieses Thema enthält eine Übersicht über die Objekte, aus denen die Direct2D-API besteht. Sie enthält die folgenden Abschnitte:

-   [Direct2D-Header Dateien](#direct2d-header-files)
-   [Direct2D-Schnittstellen](#direct2d-interfaces)
-   [Die ID2D1Factory-Schnittstelle](#the-id2d1factory-interface)
-   [Renderziele](#render-targets)
    -   [Renderzielfeatures](#render-target-features)
    -   [Renderziel Ressourcen](#render-target-resources)
    -   [Zeichnen von Befehlen](#drawing-commands)
    -   [Fehlerbehandlung](#error-handling)
-   [Zeichnen von Ressourcen](#drawing-resources)
    -   [Pinsel](#brushes)
    -   [Geometrien](#geometries)
    -   [Bitmaps](#bitmaps)
-   [Zeichnen von Text](#drawing-text)
-   [Direct2D primitive](#direct2d-primitives)
-   [Zugehörige Themen](#related-topics)

## <a name="direct2d-header-files"></a>Direct2D-Header Dateien

Die Direct2D-API wird durch die folgenden Header Dateien definiert.

| Headerdatei         | BESCHREIBUNG                                                                                                                  |
|---------------------|------------------------------------------------------------------------------------------------------------------------------|
| d2d1. h              | Definiert die C-und C++-Versionen der primären Direct2D-API.                                                                      |
| d2d1helper. h        | Definiert C++-Hilfsfunktionen, Klassen und Strukturen.                                                                       |
| d2dbasetypes. h      | Definiert Zeichnungs primitive für Direct2D, z. b. Punkte und Rechtecke. Dieser Header ist in d2d1. h enthalten.                 |
| d2derr. h            | Definiert die Fehlercodes für Direct2D. Dieser Header ist in d2d1. h enthalten.                                                   |
| d2d1 \_ 1. h           | Definiert C-und C++-Versionen der primären Direct2D-API für Windows 8 und höher.                                              |
| d2d1 \_ 1helper. h     | Definiert C++ Helper-Funktionen,-Klassen und-Strukturen für Windows 8 und höher.                                               |
| d2d1effects. h       | Definiert die C-und C++-Versionen der Image Effekte, die Teil der Direct2D-API für Windows 8 und höher sind.                            |
| d2d1effecthelpers. h | Definiert C++-Hilfsfunktionen, Klassen und Strukturen der Bildeffekte, die Teil der Direct2D-API für Windows 8 und höher sind. |



 

Um Direct2D zu verwenden, sollte die Anwendung die Header Datei d2d1. h enthalten.

Fügen Sie der Liste der Bibliotheken d2d1. lib hinzu, um eine Direct2D-Anwendung zu kompilieren. D2d1. h und d2d1. lib finden Sie im [Windows Software Development Kit (SDK) für Windows 7](https://msdn.microsoft.com/windows/bb980924.aspx).

In den folgenden Abschnitten werden einige der allgemeinen Schnittstellen beschrieben, die von der Direct2D-API bereitgestellt werden.

## <a name="direct2d-interfaces"></a>Direct2D-Schnittstellen

Im Stammverzeichnis der Direct2D-API sind die [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -und [**ID2D1Resource**](/windows/win32/api/d2d1/nn-d2d1-id2d1resource) -Schnittstellen. Ein **ID2D1Factory** -Objekt erstellt **ID2D1Resource** -Objekte und dient als Ausgangspunkt für die Verwendung von Direct2D. Alle anderen Direct2D-Objekte erben von der **ID2D1Resource** -Schnittstelle. Es gibt zwei Arten von Direct2D-Ressourcen: geräteunabhängige Ressourcen und Geräte abhängige Ressourcen.

-   Geräteunabhängige Ressourcen sind keinem bestimmten renderinggerät zugeordnet und können für die Lebensdauer einer Anwendung beibehalten werden.
-   Geräte abhängige Ressourcen sind einem bestimmten renderinggerät zugeordnet und funktionieren nicht mehr, wenn das Gerät entfernt wurde.

(Weitere Informationen zu Ressourcen und Ressourcen Freigabe finden Sie in der [Übersicht über Ressourcen](resources-and-resource-domains.md).)

## <a name="the-id2d1factory-interface"></a>Die ID2D1Factory-Schnittstelle

Die [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) -Schnittstelle ist der Ausgangspunkt für die Verwendung von Direct2D. Sie verwenden ein **ID2D1Factory** -, um Direct2D-Ressourcen zu instanziieren. Zum Erstellen eines ID2D1Factory verwenden Sie eine der Methoden " [**kreatefactory**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory) ".

Eine Factory definiert eine Reihe von Methoden zum Erstellen von *Ressourcen* , die die folgenden Zeichnungs Ressourcen erzeugen können:

-   Renderziele sind Objekte, die Zeichnungs Befehle renderingbefehle.
-   Zeichnungs Zustands Blöcke sind Objekte, in denen Zeichnungs Zustandsinformationen gespeichert werden, z. b. die aktuelle Transformation und der Antialiasing-Modus.
-   Geometrien sind Objekte, die einfache und potenziell komplexe Formen darstellen.

Eines der nützlichsten Objekte, die eine Factory erstellen kann, ist die [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), die im folgenden Abschnitt beschrieben wird.

## <a name="render-targets"></a>Renderziele

Ein Renderziel ist eine Ressource, die von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle erbt. Ein Renderziel erstellt Ressourcen zum Zeichnen und Ausführen von Zeichnungs Vorgängen. Es gibt verschiedene Arten von renderzielen, die zum renderinggrafiken auf folgende Weise verwendet werden können:

-   [**ID2D1HwndRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget) -Objekte erzeugen Inhalt in einem Fenster.
-   [**ID2D1DCRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget) -Objekte werden in einen GDI-Gerätekontext gerendering.
-   Bitmap-renderzielobjekte renderinginhalte Inhalt zu einer Offscreen-Bitmap.
-   DXGI Renderziel Objekte werden zu einer DXGI-Oberfläche für die Verwendung mit Direct3D.

Da ein Renderziel mit einem bestimmten renderinggerät verknüpft ist, ist es eine Geräte abhängige Ressource und funktioniert nicht mehr, wenn das Gerät entfernt wird.

### <a name="render-target-features"></a>Renderzielfeatures

Sie können angeben, ob ein Renderziel die Hardwarebeschleunigung verwenden soll und ob die Remote Anzeige vom lokalen Computer oder von einem Remote Computer gerendert werden soll. Renderziele können für Alias-oder Antialiasing-Rendering eingerichtet werden. Für renderingszenen mit einer großen Anzahl von primitiven kann ein Entwickler auch 2D-Grafiken im Alias Modus Rendern und D3D Multisampling Antialiasing verwenden, um eine höhere Skalierbarkeit zu erzielen.

Renderziele können auch Zeichnungsvorgänge in Ebenen gruppieren, die durch die [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Schnittstelle dargestellt werden. Ebenen sind nützlich, um Zeichnungsvorgänge zu erfassen, die zusammen zusammengeführt werden, wenn ein Frame gerendert wird. In einigen Szenarien kann dies eine nützliche Alternative zum Rendern in ein Bitmap-Renderziel sein und dann den Bitmapinhalt wieder verwenden, da die Zuordnungs Kosten für die Schichten niedriger sind als bei einem [**ID2D1BitmapRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget).

Renderziele können neue Renderziele erstellen, die mit sich selbst kompatibel sind. Dies ist für das zwischengeschaltete debuggerrendering nützlich, während die verschiedenen renderzieleigenschaften beibehalten werden, die für den ursprünglichen festgelegt wurden.

Es ist auch möglich, die Verwendung von GDI für ein Direct2D-Renderziel durch Aufrufen von [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) für ein Renderziel für [**ID2D1GdiInteropRenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1gdiinteroprendertarget)zu renderzielen, das über [**GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) -und [**ReleaseDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-releasedc) -Methoden verfügt, die zum Abrufen eines GDI-Geräte Kontexts verwendet werden können. Das Rendering über GDI ist nur möglich, wenn das Renderziel mit dem festgelegten [**GDI-kompatiblen Flag "D2D1 \_ \_ Renderziel \_ \_ \_ Verwendung**](/windows/win32/api/d2d1/ne-d2d1-d2d1_render_target_usage) " erstellt wurde. Dies ist nützlich für Anwendungen, die in erster Linie mit Direct2D Rendering, aber über ein Erweiterbarkeits Modell oder andere Legacy Inhalte verfügen, die die Fähigkeit zum Rendering mit GDI erfordern. Weitere Informationen finden Sie in der [Übersicht über die Interoperabilität zwischen Direct2D und GDI](direct2d-and-gdi-interoperation-overview.md).

### <a name="render-target-resources"></a>Renderziel Ressourcen

Wie eine Factory kann ein Renderziel Zeichnungs Ressourcen erstellen. Alle von einem Renderziel erstellten Ressourcen sind Geräte abhängige Ressourcen (genau wie das Renderziel). Mit einem Renderziel können die folgenden Ressourcentypen erstellt werden:

-   Bitmaps
-   Pinsel
-   Ebenen
-   Gittermodelle

### <a name="drawing-commands"></a>Zeichnen von Befehlen

Zum Renderinginhalt verwenden Sie die Zeichnungs Methoden des Renderziels. Bevor Sie mit dem Zeichnen beginnen, wird die [**ID2D1RenderTarget:: beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufgerufen. Nachdem Sie das Zeichnen abgeschlossen haben, können Sie die [**ID2D1RenderTarget:: EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen. Zwischen diesen Aufrufen verwenden Sie Draw-und Fill-Methoden zum Rendering von Zeichnungs Ressourcen. Die meisten Draw-und Fill-Methoden übernehmen eine Form (entweder eine primitive oder eine Geometrie) und einen Pinsel zum ausfüllen oder gliedern der Form.

Renderziele bieten auch Methoden zum Abschneiden, Anwenden von Deck Kraft Masken und Transformieren des Koordinaten Raums.

Direct2D verwendet ein Links händiges Koordinatensystem: positive Werte der x-Achse werden nach rechts fortgesetzt, und die positiven y-Achsen Werte werden nach unten fortgesetzt.

### <a name="error-handling"></a>Fehlerbehandlung

Zeichnungs Befehle des Renderziels geben nicht an, ob der angeforderte Vorgang erfolgreich war. Um herauszufinden, ob Zeichnungs Fehler aufgetreten sind, rufen Sie die Renderziel-Löschmethode oder die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) [**-Methode auf**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) , um ein **HRESULT** zu erhalten.

## <a name="drawing-resources"></a>Zeichnen von Ressourcen

In den folgenden Abschnitten werden einige der Ressourcen beschrieben, die von den Renderziel-und Factory-Schnittstellen erstellt werden können.

### <a name="brushes"></a>Pinsel

Ein Pinsel, der durch die [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) -Schnittstelle dargestellt wird, ist eine Geräte abhängige Ressource, die von einem Renderziel erstellt wird, die einen Bereich mit der Ausgabe zeichnet. Verschiedene Pinsel haben unterschiedliche Ausgabetypen. Einige Pinsel zeichnen einen Bereich mit einer voll Tonfarbe, andere mit einem Farbverlauf oder einem Bild. Direct2D bietet vier Arten von Pinsel:

-   [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) zeichnet einen Bereich mit einer voll Tonfarbe.
-   [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) zeichnet einen Bereich mit einem linearen Farbverlauf, der zwei oder mehr Farben in einer Linie (der Farbverlaufs Achse) kombiniert.
-   [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) zeichnet einen Bereich mit einem radialen Farbverlauf, der zwei oder mehr Farben um eine Ellipse bindet.
-   [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zeichnet einen Bereich mit einer Bitmap.

Zum Erstellen eines Pinsels verwenden Sie eine der [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)Create *<Type>* Brush-Methoden, wie z. b. " [**kreateradialgradientbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createradialgradientbrush(constd2d1_radial_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1radialgradientbrush))". Pinsel können mit einer renderzielmethode zum Zeichnen und Auffüllen verwendet werden, um einen Form Strich oder eine Gliederung zu zeichnen, oder als Deck Kraft Maske.

Weitere Informationen zu Pinseln finden Sie in der [Übersicht über Pinsel](direct2d-brushes-overview.md).

### <a name="geometries"></a>Geometrien

Zusätzlich zu den grundlegenden Zeichen primitiven wie Punkten, Rechtecke und Ellipsen bietet Direct2D die [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Schnittstelle zum beschreiben einfacher und komplexer Formen. Schnittstellen, die von **ID2D1Geometry** erben, definieren verschiedene Typen von Formen, z. b. [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) zum Darstellen von Rechtecke, [**ID2D1RoundedRectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1roundedrectanglegeometry) für die Darstellung abgerundeter Rechtecke und [**ID2D1EllipseGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1ellipsegeometry) für das darstellen von Ellipsen.

Komplexere Formen können mithilfe der [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) -Schnittstelle erstellt werden, um eine Reihe von Abbildungen anzugeben, die aus Linien, Kurven und Arcs bestehen. Der **ID2D1GeometrySink** wird an die Open-Methode eines [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) -Werts, um eine komplexe Geometrie zu generieren. [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) kann auch mit der DirectWrite-API verwendet werden, um Pfad Gliederungen von formatiertem Text für das künstlerische Rendering zu extrahieren.

Die Geometry-Schnittstellen bieten Methoden zum Bearbeiten von Formen durch Erweiterung oder Vereinfachung vorhandener Geometrien oder durch das Erzeugen der Schnittmenge oder Vereinigung mehrerer Geometrien. Außerdem stellen Sie Methoden bereit, um zu bestimmen, ob Geometrien sich überschneiden oder überlappen, Informationen zu Begrenzungen abrufen, den Bereich oder die Länge einer Geometrie berechnen und Standorte entlang einer Geometrie interpolieren. Direct2D bietet auch die Möglichkeit, ein Gitter von Dreiecken zu erstellen, die aus einer Geometrie in den Mosaik Prozess einbezogen werden.

Zum Erstellen einer Geometrie verwenden Sie eine der [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory):: Create Geometry- *<Type>* Methoden, wie z. b. " [**kreatepathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry)". Eine Geometrie ist eine geräteunabhängige Ressource.

Zum Rendern einer Geometrie verwenden Sie die [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Methode und die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode eines Renderziels.

Weitere Informationen zu Geometrien finden Sie in der [Übersicht über Geometrien](direct2d-geometries-overview.md).

### <a name="bitmaps"></a>Bitmaps

Direct2D stellt keine Methoden zum Laden oder Speichern von Bitmaps bereit. Stattdessen können Sie mit der [Windows Imaging Component (WIC)](../wic/-wic-about-windows-imaging-codec.md)Bitmaps erstellen. Bitmapressourcen können mit WIC geladen und anschließend verwendet werden, um eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) über die [**ID2D1RenderTarget:: createbitmapfromwicbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties_id2d1bitmap)) -Methode zu erstellen.

Bitmaps können auch aus in-Memory-Daten erstellt werden, die auf andere Weise eingerichtet wurden. Nachdem eine Bitmap erstellt wurde, kann Sie von der [**drawbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawbitmap(id2d1bitmap_constd2d1_rect_f__float_d2d1_bitmap_interpolation_mode_constd2d1_rect_f_)) -Methode des Renderziels oder mit einem Bitmap-Pinsel gezeichnet werden.

Da das Erstellen von Bitmap-Ressourcen auf hardwarerrenderzielen häufig ein kostspieliger Vorgang ist, kann Direct2D den Inhalt einer Bitmap (oder eines Teils der Bitmap) mithilfe der [**copyfrombitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)-, [**copyfromrendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)-und [**copyfrommemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory) -Methode aktualisieren. Mithilfe dieser Methoden können möglicherweise die Kosten eingespart werden, die zusätzlichen GPU-Textur Zuordnungen zugeordnet sind.

## <a name="drawing-text"></a>Zeichnen von Text

Direct2D wurde für die Arbeit mit den Text Vorgängen der neuen Text-API, DirectWrite, konzipiert. Um die Verwendung der DirectWrite-API zu vereinfachen, bieten Renderziele drei Methoden zum Rendern von DirectWrite-Textressourcen: [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)), [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout)und [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun). Da Direct2D die GPU für den Klartext-Renderingprozess von ClearType verwendet, bietet Direct2D eine geringere CPU-Auslastung als GDI für Text Vorgänge und eine bessere Skalierbarkeit, da mehr GPU-Verarbeitungsleistung verfügbar ist.

[**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) ist für die einfachsten Szenarien konzipiert, in denen eine Zeichenfolge von Unicode-Text mit minimaler Formatierung gerendert wird. Komplexere Layouts und typografische Flexibilität werden durch die [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode bereitgestellt, die ein [**idwrite-Textlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt verwendet, um den Inhalt und die Formatierung anzugeben, die gerendert werden sollen. Mit **idwrite tetextlayout** können Sie die individuelle Formatierung für Teil Zeichenfolgen von Text und andere erweiterte Typografieoptionen angeben.

Für Szenarien, in denen eine genaue Steuerung des Layouts auf Symbolebene erforderlich ist, kann die [**ID2D1RenderTarget::D rawglyphrun-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) Methode in Verbindung mit den von [DirectWrite](../directwrite/direct-write-portal.md)bereitgestellten Maßeinheiten verwendet werden.

Wenn Sie die DirectWrite-API verwenden möchten, schließen Sie den dwrite. h-Header ein. Wie Direct2D verwendet DirectWrite eine Factory, [**idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) , um Textobjekte zu erstellen. Verwenden Sie die [**dwrite-CreateFactory**](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) -Funktion, um eine Factory zu erstellen, und verwenden Sie dann die Create-Methoden zum Erstellen von DirectWrite-Ressourcen (z. b. [**idschreitetextformat**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))).

Weitere Informationen zu DirectWrite finden Sie im Thema [Einführung in DirectWrite](../directwrite/introducing-directwrite.md) .

## <a name="direct2d-primitives"></a>Direct2D primitive

Direct2D definiert einen Satz primitiver Elemente, die denen von anderen Zeichnungs-APIs ähneln. Sie stellt eine Farbstruktur, eine Matrixstruktur zum Durchführen von Transformationen und Gleit Komma-und ganzzahlige Versionen von Punkten, Rechtecke, Ellipsen und Größen Strukturen bereit. Normalerweise verwenden Sie die Gleit Komma Versionen dieser Strukturen.

Sie verwenden keine Factory oder ein Renderziel, um Direct2D primitive zu instanziieren. Sie können diese direkt erstellen oder die in d2d1helper. h definierten Hilfsmethoden verwenden, um Sie zu erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> <dt>

[Hallo Welt Beispiel für DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples)
</dt> <dt>

[Einführung in DirectWrite](../directwrite/introducing-directwrite.md)
</dt> <dt>

[Ressourcen Übersicht](resources-and-resource-domains.md)
</dt> <dt>

[Windows Imaging-Komponente (WIC)](../wic/-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 