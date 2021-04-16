---
title: Text Rendering mit Direct2D und DirectWrite
description: Anders als bei anderen APIs, wie z. b. GDI, GDI+ oder WPF, interagiert Direct2D mit einer anderen API, DirectWrite, um Text zu bearbeiten und zu Rendering. In diesem Thema werden die Vorteile und die Zusammenarbeit dieser separaten Komponenten beschrieben.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c49a8f341377bcf78a9a99699a3bd4852411dd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104549819"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>Text Rendering mit Direct2D und DirectWrite

Anders als bei anderen APIs, wie z. b. [GDI](/windows/desktop/gdi/windows-gdi), GDI+ oder WPF, interagiert [Direct2D](./direct2d-portal.md) mit einer anderen API, [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), um Text zu bearbeiten und zu Rendering. In diesem Thema werden die Vorteile und die Zusammenarbeit dieser separaten Komponenten beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Direct2D ermöglicht inkrementelle Akzeptanz](#direct2d-enables-incremental-adoption)
-   [Text Dienste im Vergleich zum Text Rendering](#text-services-versus-text-rendering)
-   [Symbole im Vergleich zu Text](#glyphs-versus-text)
-   [DirectWrite und Direct2D](#directwrite-and-direct2d)
    -   [DrawText](#drawtextlayout)
    -   [Drawtextlayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Symbol Rendering](#glyph-rendering)
-   [Zusammenfassung](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D ermöglicht inkrementelle Akzeptanz

Das Verschieben einer Anwendung von einer Grafik-API in eine andere kann aus verschiedenen Gründen schwierig oder nicht sinnvoll sein. Dies kann daran liegen, dass Sie Plug-Ins unterstützen müssen, die weiterhin die älteren Schnittstellen verwenden, da die Anwendung selbst zu groß für den Portieren auf eine neue API in einem Release ist oder weil ein Teil der neueren API wünschenswert ist, aber die ältere API für andere Teile der Anwendung ausreichend funktioniert.

Da [Direct2D](./direct2d-portal.md) und [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) als separate Komponenten implementiert werden, können Sie das gesamte 2D-Grafiksystem oder nur den Textzeile des Texts aktualisieren. Beispielsweise können Sie eine Anwendung so aktualisieren, dass Sie DirectWrite für Text verwendet, aber weiterhin [GDI](/windows/desktop/gdi/windows-gdi) oder GDI+ zum Rendern verwenden.

## <a name="text-services-versus-text-rendering"></a>Text Dienste im Vergleich zum Text Rendering

Wenn sich Anwendungen entwickelt haben, haben sich die Anforderungen an die Textverarbeitung immer komplexer. Zunächst war Text in der Regel auf eine statisch gestaltete Benutzeroberfläche beschränkt, und der Text wurde in einem klar definierten Feld, z. b. einer Schaltfläche, gerendert. Da Anwendungen in einer wachsenden Anzahl von Sprachen verfügbar waren, wurde diese Vorgehensweise schwieriger, da sowohl die Breite als auch die Höhe des übersetzten Texts zwischen den Sprachen stark variieren kann. Zum anpassen können Anwendungen ihre Benutzeroberfläche dynamisch anordnen, damit Sie von der tatsächlich gerenderten Größe des Texts abhängig ist, anstatt umgekehrt.

Um Anwendungen bei der Ausführung dieser Aufgabe zu unterstützen, stellt [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) die [**idschreitetextlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle bereit. Diese API ermöglicht es einer Anwendung, Text mit komplexen Merkmalen anzugeben, z. b. unterschiedliche Schriftarten und Schriftgrößen, Unterstriche, Unterstriche, bidirektionaler Text, Effekte, Auslassungs Zeichen und sogar eingebettete nicht-Symbol Zeichen (z. b. ein Bitmap-Emoticon "oder ein Symbol). Die Anwendung kann dann verschiedene Eigenschaften des Texts ändern, während Sie das Benutzeroberflächen Layout iterativ bestimmt. Das [Hallo Welt Beispiel für DirectWrite](/samples/browse/?redirectedfrom=MSDN-samples), das in der folgenden Abbildung dargestellt wird, und im [Tutorial: Einstieg in das DirectWrite](/windows/desktop/DirectWrite/getting-started-with-directwrite) -Thema zeigt viele dieser Auswirkungen.

![Screenshot des "Hello World"-Beispiels.](images/dwrite-hello-world.png)

Das Layout kann entweder die Symbole idealerweise auf Grundlage ihrer breiten (wie WPF) positionieren oder die Glyphen an die nächstgelegenen Pixelpositionen ausrichten (wie [GDI](/windows/desktop/gdi/windows-gdi) ).

Neben der Beschaffung von Text Messungen kann die Anwendung auch verschiedene Teile des Texts testen. Beispielsweise könnte es sein, dass Sie wissen möchten, dass auf einen Link im Text geklickt wird. (Weitere Informationen zu Treffer Tests finden Sie im Thema Gewusst [wie: Ausführen von Treffer Tests für ein Text Layout](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) .)

Die Text Layout-Schnittstelle ist von der Rendering-API entkoppelt, die von der Anwendung verwendet wird, wie im folgenden Diagramm gezeigt:

![Textlayout und Grafik-API-Diagramm.](images/direct2d-directwrite1.png)

Diese Trennung ist möglich, da DirectWrite eine Renderingschnittstelle ([**idschreitetextrenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)) bereitstellt, die von Anwendungen implementiert werden kann, um Text mithilfe der gewünschten Grafik-API zu rendern. Die Anwendung hat [**idschreitetextrenderer implementiert::D rawglyphrun-**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Rückruf Methode wird von DirectWrite aufgerufen, wenn ein Text Layout gerendert wird. Diese Methode ist dafür verantwortlich, die Zeichnungsvorgänge auszuführen oder zu übergeben.

Für Zeichnungs Symbole bietet [Direct2D](./direct2d-portal.md) [**ID2D1RenderTarget::D rawglyphrun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) zum Zeichnen auf eine Direct2D-Oberfläche und [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) stellt [**idschreitebitmaprendertarget bereit::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) zum Zeichnen auf eine GDI-Oberfläche, die dann mithilfe von GDI in ein Fenster übertragen werden kann. " **DrawGlyphRun** " in "Direct2D" und "DirectWrite" haben praktisch kompatible Parameter für die [**DrawGlyphRun-**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) Methode, die von der Anwendung auf " [**idschreitetextrenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)" implementiert wird.

Nach einer ähnlichen Trennung werden textspezifische Funktionen (z. b. Schriftart Enumeration und Verwaltung, Glyphe-Analyse usw.) von [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) anstelle von [Direct2D](./direct2d-portal.md)behandelt. Die DirectWrite-Objekte werden direkt von Direct2D akzeptiert. Damit vorhandene GDI-Anwendungen DirectWrite nutzen können, stellt Sie die [**idwrite tegdiinterop**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) -Methoden Schnittstelle mit Methoden für Folgendes bereit:

-   Erstellen Sie eine [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) -Schriftart aus einer logischen [GDI](/windows/desktop/gdi/windows-gdi) -Schriftart ("[**kreatefontfromlogfont**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)").
-   Konvertieren von einer [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) -Schriftart in eine logische [GDI](/windows/desktop/gdi/windows-gdi) -Schriftart ([**convertfontfacetologfont**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   Rufen Sie die Schriftart der [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) -Schriftart von der Person ab, die in einem hdc ausgewählt ist. ([**Kreatefontfakefromhdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   Erstellen Sie ein [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) - [**Bitmap-Renderziel**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) im Systemspeicher ("[**kreatebitmaprendertarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)").

## <a name="glyphs-versus-text"></a>Symbole im Vergleich zu Text

Bei Text handelt es sich um einen Satz von Unicode-Code Punkten (Zeichen) mit verschiedenen stilmodifiziererzeichen (Schriftarten, Gewichtungen, unterstrichen, Strichen usw.), die in einem Rechteck angeordnet werden. Bei einem Symbol handelt es sich dagegen um einen bestimmten Index in einer bestimmten Schriftart Datei. Ein Symbol definiert eine Reihe von Kurven, die gerendert werden können, aber keine Text Bedeutung haben. Es gibt potenziell eine m:n-Zuordnung zwischen Symbolen und Zeichen. Eine Sequenz von Symbolen, die von der gleichen Schriftart stammen und sequenziell auf einer Baseline angeordnet sind, wird als [GlyphRun](/windows/desktop/DirectWrite/glyphs-and-glyph-runs)bezeichnet. Sowohl [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) als auch [Direct2D](./direct2d-portal.md) nennen ihre präzisere Glyphe-renderingapi [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) und verfügen über sehr ähnliche Signaturen. Folgendes gilt für [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) in Direct2D:


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



Diese Methode wird von [**idschreitebitmaprendertarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) in [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)verwendet:


```
STDMETHOD(DrawGlyphRun)(
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        IDWriteRenderingParams* renderingParams,
        COLORREF textColor,
        __out_opt RECT* blackBoxRect = NULL
        ) PURE;
```



Die [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) -Version behält den Baseline-Ursprung, den Mess Modus und die Symbol Lauf Parameter bei und enthält zusätzliche Parameter.

Mithilfe von [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) können Sie auch einen benutzerdefinierten Renderer für Symbole verwenden, indem Sie die [**idschreitetextrenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) -Schnittstelle implementieren. Diese Schnittstelle verfügt auch über eine **DrawGlyphRun-** Methode, wie im folgenden Codebeispiel gezeigt.


```
STDMETHOD(DrawGlyphRun)(
        __maybenull void* clientDrawingContext,
        FLOAT baselineOriginX,
        FLOAT baselineOriginY,
        DWRITE_MEASURING_MODE measuringMode,
        __in DWRITE_GLYPH_RUN const* glyphRun,
        __in DWRITE_GLYPH_RUN_DESCRIPTION const* glyphRunDescription,
        __maybenull IUnknown* clientDrawingEffect
        ) PURE;
```



Diese Version enthält weitere Parameter, die nützlich sind, wenn Sie einen [benutzerdefinierten TextRenderer](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer)implementieren. Der letzte Parameter wird für Anwendungs implementierte benutzerdefinierte Zeichnungs Effekte verwendet. (Weitere Informationen zu Client Zeichnungs Effekten finden [Sie unter Hinzufügen von Client Zeichnungs Effekten zu einem Text Layout](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Jedes Symbol wird an einem Ursprung gestartet und in eine Zeile eingefügt, beginnend mit diesem Ursprung. Die Symbole werden von der aktuellen Welt Transformation und den ausgewählten Text Rendering-Einstellungen auf dem zugeordneten Renderziel geändert. Diese API wird in der Regel nur direkt von Anwendungen aufgerufen, die ihr eigenes Layout (z. b. ein Textverarbeitungs Tool) oder eine Anwendung, die die [**idschreitetextrenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) -Schnittstelle implementiert hat.

## <a name="directwrite-and-direct2d"></a>DirectWrite und Direct2D

[Direct2D](./direct2d-portal.md) stellt Renderingdienste auf Glyphe über [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun)bereit. Dies erfordert jedoch, dass die Anwendung die Details des Renderings implementiert, das im Grunde die Funktionalität der [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) -API aus GDI selbst neu erstellt.

Daher stellt [Direct2D](./direct2d-portal.md) APIs bereit, die Text anstelle von Glyphen akzeptieren: [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) und [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). Beide Methoden werden auf eine Direct2D-Oberfläche Render. Zum Rendervorgang auf einer GDI-Oberfläche wird [**idschreitebitmaprendertarget::D rawglyphrun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) bereitgestellt. Diese Methode erfordert jedoch, dass ein benutzerdefinierter TextRenderer von der Anwendung implementiert wird. (Weitere Informationen finden Sie im Thema [Rendering zu einer GDI-Oberfläche](/windows/desktop/DirectWrite/render-to-a-gdi-surface) .)

Die Verwendung von Text in einer Anwendung beginnt in der Regel einfach: Legen Sie " **OK** " oder " **Abbrechen** " auf einer Schaltfläche mit festem Layout (z.b.) Im Laufe der Zeit wird Sie jedoch komplexer, wenn Internationalisierung und andere Features hinzugefügt werden. Schließlich müssen viele Anwendungen die textlayoutobjekte [von DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) verwenden und den TextRenderer implementieren.

[Direct2D](./direct2d-portal.md) bietet daher mehrstufige APIs, mit denen eine Anwendung einfach gestartet werden kann, ohne dass Ihr funktionierender Code zurückverfolgt oder abgebrochen werden muss. Eine vereinfachte Ansicht ist im folgenden Diagramm dargestellt:

![DirectWrite-und Direct2D-Anwendungs Diagramm.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>DrawText

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) ist die einfachste der zu verwendenden APIs. Sie benötigt eine Unicode-Zeichenfolge, einen Vordergrund Pinsel, ein einzelnes Format Objekt und ein Ziel Rechteck. Die gesamte Zeichenfolge wird im Layoutrechteck angelegt und dargestellt, und optional wird Sie ausgeblendet. Dies ist hilfreich, wenn Sie einen einfachen Text in einem Teil der Benutzeroberfläche mit festem Layout platzieren.

### <a name="drawtextlayout"></a>Drawtextlayout

Durch das Erstellen eines [**idwrite-Textlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Objekts kann eine Anwendung mit dem Messen und Anordnen des Texts und anderer Benutzeroberflächen Elemente beginnen und mehrere Schriftarten, Stile, Unterstriche und Unterstriche unterstützen. [Direct2D](./direct2d-portal.md) stellt die [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -API bereit, die dieses Objekt direkt annimmt und den Text an einem bestimmten Punkt rendert. (Breite und Höhe werden durch das Layoutobjekt bereitgestellt). Zusätzlich zur Implementierung aller erwarteten textzeitfeatures interpretiert Direct2D jedes Effekt Objekt als Pinsel und wendet diesen Pinsel auf den ausgewählten Bereich von Symbolen an. Außerdem werden alle Inline Objekte aufgerufen. Eine Anwendung kann dann, wenn Sie möchte, nicht--Symbol Zeichen (Symbole) in den Text einfügen. Ein weiterer Vorteil der Verwendung eines textlayoutobjekte besteht darin, dass die Symbol Positionen darin zwischengespeichert werden. Daher ist ein großer Leistungszuwachs möglich, indem das gleiche Layoutobjekt für mehrere Draw-Aufrufe wieder verwendet wird, und es wird vermieden, dass die Symbol Positionen für jeden Aufruf neu berechnet werden. Diese Funktion ist für den GDI- [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))nicht vorhanden.

### <a name="drawglyphrun"></a>DrawGlyphRun

Schließlich kann die Anwendung die [**idwrite tetextrenderer**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) -Schnittstelle selbst implementieren und [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) und [**fillrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) selbst oder eine beliebige andere Rendering-API aufrufen. Alle bestehenden Interaktionen mit dem textlayoutobjekt bleiben unverändert.

Ein Beispiel für das Implementieren eines benutzerdefinierten textrenderers finden Sie im Thema [Rendering using a Custom Text Renderer](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) .

## <a name="glyph-rendering"></a>Symbol Rendering

Durch das Hinzufügen von [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) zu einer vorhandenen GDI-Anwendung kann die Anwendung die [**idwrite-bitmaprendertarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) -API verwenden, um Symbole zu renhen. Die von DirectWrite bereitgestellte [**idwrite-bitmaprendertarget::D rawglyphrun-**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) Methode wird in einer voll Tonfarbe in einen Speicher-DC gerenbt, ohne dass zusätzliche APIs erforderlich sind, wie z. b. [Direct2D](./direct2d-portal.md).

Dadurch kann die Anwendung erweiterte textrenderingfunktionen wie die folgende abrufen:

-   Sub-Pixel ClearType ermöglicht es einer Anwendung, Symbole an untergeordneten Pixelpositionen zu platzieren, um sowohl das Rendern von Symbolen als auch das Symbol Layout zu ermöglichen.
-   Das Antialiasing in Y-Richtung ermöglicht ein glatteres Rendering von Kurven auf größeren Glyphen.

Eine Anwendung, die auf [Direct2D](./direct2d-portal.md) verschoben wird, erhält außerdem die folgenden Features:

-   Hardwarebeschleunigung.
-   Die Möglichkeit, Text mit einem beliebigen [Direct2D](./direct2d-portal.md) -Pinsel (z. b. radiale Farbverläufe, lineare Farbverläufe und Bitmaps) auszufüllen.
-   Weitere Unterstützung für das Schichten und Clipping über die [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))-, [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -und [**die-API**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) -API-Funktion.
-   Die Fähigkeit zur Unterstützung von Graustufen Text Rendering. Dadurch wird der Alphakanal des Ziels ordnungsgemäß mit der Text Pinsel Deckkraft und dem Antialiasing des Texts aufgefüllt.

Zur effizienten Unterstützung der Hardwarebeschleunigung verwendet [Direct2D](./direct2d-portal.md) eine etwas andere Näherung zur Gamma Korrektur namens *Alpha Korrektur*. Dies erfordert keinen Direct2D, um das Renderziel-Farbpixel beim Rendern von Text zu überprüfen.

## <a name="conclusion"></a>Zusammenfassung

In diesem Thema werden die Unterschiede und Ähnlichkeiten zwischen [Direct2D](./direct2d-portal.md) und [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) sowie die architektonischen Beweggründe für die Bereitstellung als separate, kooperative APIs erläutert.

 

 