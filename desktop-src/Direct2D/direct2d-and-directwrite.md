---
title: Textrendering mit Direct2D und DirectWrite
description: Im Gegensatz zu anderen APIs wie GDI, GDI+ oder WPF interoperiert Direct2D mit einer anderen API, DirectWrite, um Text zu bearbeiten und zu rendern. In diesem Thema werden die Vorteile und die Interoperation dieser separaten Komponenten beschrieben.
ms.assetid: 1d5b8deb-34e2-433c-8de3-4ef66fb4e49d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd95e7644b5f429d4dd91d2276213d5b7ffb92b058d8e530bfcf47fee77fea3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698233"
---
# <a name="text-rendering-with-direct2d-and-directwrite"></a>Textrendering mit Direct2D und DirectWrite

Im Gegensatz zu anderen APIs wie [GDI,](/windows/desktop/gdi/windows-gdi)GDI+ oder WPF interoperiert [Direct2D](./direct2d-portal.md) mit einer anderen [API,](/windows/desktop/DirectWrite/direct-write-portal)DirectWrite, um Text zu bearbeiten und zu rendern. In diesem Thema werden die Vorteile und die Interoperation dieser separaten Komponenten beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Direct2D ermöglicht die inkrementelle Einführung](#direct2d-enables-incremental-adoption)
-   [Textdienste im Vergleich zum Textrendering](#text-services-versus-text-rendering)
-   [Glyphen im Vergleich zu Text](#glyphs-versus-text)
-   [DirectWrite und Direct2D](#directwrite-and-direct2d)
    -   [Drawtext](#drawtextlayout)
    -   [DrawTextLayout](#drawtextlayout)
    -   [DrawGlyphRun](#drawglyphrun)
-   [Glyphenrendering](#glyph-rendering)
-   [Zusammenfassung](#conclusion)

## <a name="direct2d-enables-incremental-adoption"></a>Direct2D ermöglicht die inkrementelle Einführung

Das Verschieben einer Anwendung von einer Grafik-API in eine andere kann aus verschiedenen Gründen schwierig oder nicht das sein, was Sie möchten. Dies kann daran liegt, dass Sie Plug-Ins unterstützen müssen, die noch die älteren Schnittstellen verwenden, da die Anwendung selbst zu groß ist, um in einem Release auf eine neue API zu portieren, oder weil ein Teil der neueren API wünschenswert ist, die ältere API aber für andere Teile der Anwendung gut genug funktioniert.

Da [Direct2D](./direct2d-portal.md) und [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) als separate Komponenten implementiert werden, können Sie das gesamte 2D-Grafiksystem oder nur den Textteil davon aktualisieren. Beispielsweise können Sie eine Anwendung aktualisieren, um DirectWrite für Text zu verwenden, aber trotzdem [GDI](/windows/desktop/gdi/windows-gdi) oder GDI+ Rendering verwenden.

## <a name="text-services-versus-text-rendering"></a>Textdienste im Vergleich zum Textrendering

Mit der Entwicklung von Anwendungen sind die Anforderungen an die Textverarbeitung immer komplexer geworden. Zunächst war Text in der Regel auf eine statisch ausgelegte Benutzeroberfläche beschränkt, und der Text wurde in einem klar definierten Feld gerendert, z. B. einer Schaltfläche. Da Anwendungen in einer wachsenden Anzahl von Sprachen verfügbar waren, wurde dieser Ansatz schwieriger zu unterstützen, da sowohl die Breite als auch die Höhe des übersetzten Texts in den verschiedenen Sprachen erheblich variieren können. Um sich anzupassen, begannen Anwendungen, ihre Benutzeroberfläche dynamisch so zu erstellen, dass sie von der tatsächlich gerenderten Größe des Texts abhängig ist, anstatt umgekehrt.

Um Anwendungen beim Abschließen dieser Aufgabe zu [unterstützen,](/windows/desktop/DirectWrite/direct-write-portal) DirectWrite die [**IDWriteTextLayout-Schnittstelle**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) bereit. Diese API ermöglicht es einer Anwendung, einen Textteil mit komplexen Merkmalen wie verschiedenen Schriftarten und Schriftgraden, Unterstreichungen, Durchgestrichenheiten, bidirektionalem Text, Effekten, Auslassungszeichen und sogar eingebetteten Nicht-Glyphenzeichen (z. B. Bitmap-Emoticon oder Symbol) anzugeben. Die Anwendung kann dann verschiedene Merkmale des Texts ändern, da sie das Layout der Benutzeroberfläche iterativ bestimmt. Das [DirectWrite Hallo Welt-Beispiel,](/samples/browse/?redirectedfrom=MSDN-samples)das in der folgenden Abbildung und im Thema [Tutorial: Erste Schritte mit](/windows/desktop/DirectWrite/getting-started-with-directwrite) DirectWrite gezeigt wird, zeigt viele dieser Auswirkungen.

![Screenshot des Beispiels "hello world".](images/dwrite-hello-world.png)

Das Layout kann die Glyphen idealerweise basierend auf ihrer Breite positionieren (wie WPF), oder es kann die Glyphen an den nächsten Pixelpositionen ausrichten (wie [GDI).](/windows/desktop/gdi/windows-gdi)

Zusätzlich zum Abrufen von Textmessungen kann die Anwendung verschiedene Teile des Texts testen. Es kann beispielsweise sein, dass sie wissen möchte, dass auf einen Link im Text geklickt wird. (Weitere Informationen zu Treffertests finden Sie im Thema [How to Perform Hit Testing on a Text Layout](/windows/desktop/DirectWrite/how-to-perform-hit-testing-on-a-text-layout) .)

Die Textlayoutschnittstelle ist von der Rendering-API entkoppelt, die die Anwendung verwendet, wie im folgenden Diagramm dargestellt:

![Textlayout und Grafik-API-Diagramm.](images/direct2d-directwrite1.png)

Diese Trennung ist möglich, da DirectWrite eine Renderingschnittstelle [**(IDWriteTextRenderer)**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)bietet, die Anwendungen implementieren können, um Text mithilfe der von Ihnen verwendeten Grafik-API zu rendern. Die von der Anwendung implementierte [**IDWriteTextRenderer::D rawGlyphRun-Rückrufmethode**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) wird von DirectWrite beim Rendern eines Textlayouts aufgerufen. Es liegt in der Verantwortung dieser Methode, die Zeichnungsvorgänge durchzuführen oder zu übergeben.

Zum Zeichnen von Glyphen stellt [Direct2D](./direct2d-portal.md) [**ID2D1RenderTarget::D rawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) für das Zeichnen auf eine Direct2D-Oberfläche und [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) zum Zeichnen auf eine GDI-Oberfläche zur Anwendung, die dann mithilfe von GDI in ein Fenster übertragen werden kann. Bequemerweise **verfügen DrawGlyphRun** sowohl in Direct2D als auch DirectWrite über genau kompatible Parameter für die [**DrawGlyphRun-Methode,**](/windows/desktop/api/dwrite/nf-dwrite-idwritetextrenderer-drawglyphrun) die die Anwendung in [**IDWriteTextRenderer implementiert.**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer)

Nach einer ähnlichen Trennung werden textspezifische Features (z. B. Schriftartenumeration und [](/windows/desktop/DirectWrite/direct-write-portal) -verwaltung, Glyphenanalyse und ähnliches) von DirectWrite [direct2D behandelt.](./direct2d-portal.md) Die DirectWrite objekte werden direkt von Direct2D akzeptiert. Damit vorhandene GDI-Anwendungen die Vorteile von DirectWrite nutzen können, stellt sie die [**IDWriteGdiInterop-Methodenschnittstelle**](/windows/desktop/api/dwrite/nn-dwrite-idwritegdiinterop) mit Methoden für folgende Aufgaben bereit:

-   Erstellen sie [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) aus einer [logischen GDI-Schriftart](/windows/desktop/gdi/windows-gdi) ([**CreateFontFromLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfromlogfont)).
-   Konvertieren von einem [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) Schriftart in eine [logische GDI-Schriftart](/windows/desktop/gdi/windows-gdi) ([**ConvertFontFaceToLOGFONT**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-convertfontfacetologfont)).
-   Rufen Sie [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) schriftartengesichtige Schriftart aus dem in einem HDC ausgewählten Ab. ([**CreateFontFaceFromHdc**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createfontfacefromhdc))
-   Erstellen eines [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) [**Bitmaprenderingziels**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) im Systemspeicher ([**CreateBitmapRenderTarget**](/windows/desktop/api/dwrite/nf-dwrite-idwritegdiinterop-createbitmaprendertarget)).

## <a name="glyphs-versus-text"></a>Glyphen im Vergleich zu Text

Text ist ein Satz von Unicode-Codepunkten (Zeichen) mit verschiedenen stilischen Modifizierern (Schriftarten, Gewichtungen, Unterstreichungen, Durchgeknstreichungen und so weiter), die in einem Rechteck angeordnet sind. Ein Glyphen hingegen ist ein bestimmter Index in einer bestimmten Schriftartdatei. Ein Glyph definiert eine Reihe von Kurven, die gerendert werden können, hat aber keine textuelle Bedeutung. Möglicherweise gibt es eine n:n-Zuordnung zwischen Glyphen und Zeichen. Eine Sequenz von Glyphen, die aus demselben Schriftartengesicht stammen und sequenziell auf einer Baseline festgelegt werden, wird als [GlyphRun bezeichnet.](/windows/desktop/DirectWrite/glyphs-and-glyph-runs) Sowohl [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) als auch [Direct2D](./direct2d-portal.md) rufen ihre präziseste Glyphenrendering-API [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) auf und haben sehr ähnliche Signaturen. Das folgende Beispiel wird von [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) in Direct2D verwendet:


```
STDMETHOD_(void, DrawGlyphRun)(
        D2D1_POINT_2F baselineOrigin,
        __in CONST DWRITE_GLYPH_RUN *glyphRun,
        __in ID2D1Brush *foregroundBrush,
        DWRITE_MEASURING_MODE measuringMode = DWRITE_MEASURING_MODE_NATURAL 
        ) PURE;
```



Und diese Methode ist von [**IDWriteBitmapRenderTarget**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) in [DirectWrite:](/windows/desktop/DirectWrite/direct-write-portal)


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



Die [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) version behält den Baseline-Ursprung, den Messmodus und die Ausführungsparameter des Glyphen bei und enthält zusätzliche Parameter.

[DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) können Sie auch einen benutzerdefinierten Renderer für Glyphen verwenden, indem Sie die [**IDWriteTextRenderer-Schnittstelle**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) implementieren. Diese Schnittstelle verfügt auch über eine **DrawGlyphRun-Methode,** wie das folgende Codebeispiel zeigt.


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



Diese Version enthält weitere Parameter, die nützlich sind, wenn Sie einen [benutzerdefinierten Textrenderer implementieren.](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer) Der letzte Parameter wird für von der Anwendung implementierte benutzerdefinierte Zeichnungseffekte verwendet. (Weitere Informationen zu Clientzeichnungseffekten finden Sie unter [How to Add Client Drawing Effects to a Text Layout](/windows/desktop/DirectWrite/how-to-add-custom-drawing-efffects-to-a-text-layout).

Jede Glyphen-Ausführung beginnt an einem Ursprung und wird in einer Zeile ab diesem Ursprung ausgeführt. Die Glyphen werden durch die aktuelle Welttransformation und die ausgewählten Textrenderingeinstellungen auf dem zugeordneten Renderziel geändert. Diese API wird im Allgemeinen nur direkt von Anwendungen aufgerufen, die über ein eigenes Layout (z. B. einen Textprozessor) oder durch eine Anwendung, die die [**IDWriteTextRenderer-Schnittstelle implementiert**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) hat.

## <a name="directwrite-and-direct2d"></a>DirectWrite und Direct2D

[Direct2D stellt](./direct2d-portal.md) Renderingdienste auf Glyphenebene über [**DrawGlyphRun zur Verfügung.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) Dies erfordert jedoch, dass die Anwendung die Details des Renderings implementiert, wodurch die Funktionalität der [**DrawText-API**](/windows/desktop/api/winuser/nf-winuser-drawtext) von GDI selbst reproduziert wird.

Daher bietet [Direct2D](./direct2d-portal.md) APIs, die Text anstelle von Glyphen akzeptieren: [**ID2D1RenderTarget::D rawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) und [**ID2D1RenderTarget::D rawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)). Beide Methoden werden auf einer Direct2D-Oberfläche gerendert. Zum Rendern auf einer GDI-Oberfläche wird [**IDWriteBitmapRenderTarget::D rawGlyphRun**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) bereitgestellt. Diese Methode erfordert jedoch, dass ein benutzerdefinierter Textrenderer von der Anwendung implementiert wird. (Weitere Informationen finden Sie im Thema [Rendern auf einer GDI-Oberfläche.)](/windows/desktop/DirectWrite/render-to-a-gdi-surface)

Die Verwendung von Text in einer Anwendung beginnt in der Regel einfach: Legen Sie **ok** oder **Abbrechen** auf einer Schaltfläche mit festem Layout fest, z. B. . Im Laufe der Zeit wird es jedoch komplexer, wenn Internationalisierung und andere Features hinzugefügt werden. Schließlich müssen viele Anwendungen die Textlayoutobjekte [DirectWrite verwenden](/windows/desktop/DirectWrite/direct-write-portal) und den Textrenderer implementieren.

Aus diesem Grund bietet [Direct2D](./direct2d-portal.md) mehrschichtige APIs, die es einer Anwendung ermöglichen, einfach zu starten und komplexer zu werden, ohne ihren Arbeitscode zurückver nachverfolgen oder verdringen zu müssen. Eine vereinfachte Ansicht ist im folgenden Diagramm dargestellt:

![directwrite- und direct2d-Anwendungsdiagramm.](images/direct2d-directwrite2.png)

### <a name="drawtext"></a>Drawtext

[**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) ist die einfachste der zu verwendenden APIs. Dabei werden eine Unicode-Zeichenfolge, ein Vordergrundpinsel, ein einzelnes Formatobjekt und ein Zielrechteck verwendet. Es wird die gesamte Zeichenfolge innerhalb des Layoutrechtecks angeordnet und gerendert und optional abgeschnitten. Dies ist nützlich, wenn Sie einen einfachen Text in einer Benutzeroberfläche mit festem Layout hinzufügen.

### <a name="drawtextlayout"></a>DrawTextLayout

Durch das Erstellen [**eines IDWriteTextLayout-Objekts**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) kann eine Anwendung mit dem Messen und Anordnen des Texts und anderer Benutzeroberflächenelemente beginnen und mehrere Schriftarten, Stile, Unterstreichungen und Durchstreichungen unterstützen. [Direct2D stellt](./direct2d-portal.md) die [**DrawTextLayout-API**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) bereit, die dieses Objekt direkt akzeptiert und den Text an einem bestimmten Punkt rendert. (Breite und Höhe werden vom Layoutobjekt bereitgestellt.) Zusätzlich zur Implementierung aller erwarteten Textlayoutfeatures interpretiert Direct2D jedes Effektobjekt als Pinsel und wenden diesen Pinsel auf den ausgewählten Bereich von Glyphen an. Außerdem werden alle Inlineobjekte aufruft. Eine Anwendung kann dann bei Wunsch Nichtsymbolzeichen (Symbole) in den Text einfügen. Ein weiterer Vorteil der Verwendung eines Textlayoutobjekts besteht in der Zwischenspeicherung der Glyphenpositionen. Daher ist ein großer Leistungsgewinn möglich, indem dasselbe Layoutobjekt für mehrere Zeichnen-Aufrufe wiederverwendbar ist und vermieden wird, dass die Glyphenpositionen für jeden Aufruf neu berechnet werden. Diese Funktion ist für DrawText von GDI [**nicht vorhanden.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode))

### <a name="drawglyphrun"></a>DrawGlyphRun

Schließlich kann die Anwendung die [**IDWriteTextRenderer-Schnittstelle**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer) selbst implementieren und [**DrawGlyphRun**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) und [**FillRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillrectangle(constd2d1_rect_f_id2d1brush)) selbst oder eine andere Rendering-API aufrufen. Alle vorhandenen Interaktionen mit dem Textlayoutobjekt bleiben unverändert.

Ein Beispiel für die Implementierung eines benutzerdefinierten Textrenderers finden Sie im Thema [Rendern mit einem benutzerdefinierten Textrenderer.](/windows/desktop/DirectWrite/how-to-implement-a-custom-text-renderer)

## <a name="glyph-rendering"></a>Glyphenrendering

Durch hinzufügen [von DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) zu einer vorhandenen GDI-Anwendung kann die Anwendung die [**IDWriteBitmapRenderTarget-API**](/windows/desktop/api/dwrite/nn-dwrite-idwritebitmaprendertarget) zum Rendern von Glyphen verwenden. Die [**IDWriteBitmapRenderTarget::D rawGlyphRun-Methode,**](/windows/desktop/api/dwrite/nf-dwrite-idwritebitmaprendertarget-drawglyphrun) die DirectWrite bereitstellt, rendert in Volltonfarbe auf einem Speicherdomänencontroller, ohne dass zusätzliche APIs wie [Direct2D](./direct2d-portal.md)erforderlich sind.

Dadurch kann die Anwendung erweiterte Textrenderingfeatures wie die folgenden abrufen:

-   MitHilfe von Subpixel-ClearType kann eine Anwendung Glyphen an Subpixelpositionen setzen, um das Rendern von spitzen Glyphen und das Layout von Glyphen zu ermöglichen.
-   Antialiasing in Y-Richtung ermöglicht ein reibungsloseres Rendern von Kurven auf größeren Glyphen.

Eine Anwendung, die zu [Direct2D](./direct2d-portal.md) wechselt, erhält auch die folgenden Features:

-   Hardwarebeschleunigung.
-   Die Fähigkeit, Text mit einem beliebigen [Direct2D-Pinsel](./direct2d-portal.md) zu füllen, z. B. radiale Farbverläufe, lineare Farbverläufe und Bitmaps.
-   Weitere Unterstützung für Das Layering und Clipping über die [**APIs PushAxisAlignedClip,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) und [**CreateCompatibleRenderTarget.**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget))
-   Die Möglichkeit zur Unterstützung des Graustufentextrenderings. Dadurch wird der Ziel-Alphakanal entsprechend der Deckkraft des Textpinsels und der Antialiasierung des Texts ordnungsgemäß aufgefüllt.

Um die Hardwarebeschleunigung effizient zu unterstützen, verwendet [Direct2D](./direct2d-portal.md) eine etwas andere Näherung zur Gammakorrektur, die als *Alphakorrektur* bezeichnet wird. Hierfür ist direct2D nicht erforderlich, um das Renderzielfarbpixel beim Rendern von Text zu überprüfen.

## <a name="conclusion"></a>Zusammenfassung

In diesem Thema werden die Unterschiede und Ähnlichkeiten zwischen [Direct2D](./direct2d-portal.md) und [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) sowie die Architekturbeweggründe für die Bereitstellung als separate, kooperative APIs erläutert.

 

 