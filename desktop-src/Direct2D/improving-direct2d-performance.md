---
title: Verbessern der Leistung von Direct2D-apps
description: Beschreibt Techniken zum Verbessern der Direct2D-Leistung.
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D, Leistung
- Direct2D, Bitmaps
- Direct2D, Ressourcenverwendung
- Direct2D, Flush-Methode
- Direct2D, statischer Inhalt
- Leistung für Direct2D
- Bitmaps für Direct2D
- Direct2D, GDI-Interoperation
- Direct2D, Interoperabilität
- Interoperabilität, Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- Interoperabilität, Graphics Device Interface (GDI)
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5a413b96e00514b64b3cf1b1ee451a84a9e9ff09
ms.sourcegitcommit: 6eb53540b8d882fd035d428567d7d1c5ec17042c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/12/2020
ms.locfileid: "104474589"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>Verbessern der Leistung von Direct2D-apps

Obwohl [Direct2D](./direct2d-portal.md) Hardware beschleunigt ist und für hohe Leistung vorgesehen ist, müssen Sie die Funktionen zum Maximieren des Durchsatzes ordnungsgemäß verwenden. Die hier vorgestellten Verfahren sind von der Untersuchung allgemeiner Szenarien abgeleitet und gelten möglicherweise nicht für alle App-Szenarios. Daher kann das genaue Verständnis des App-Verhaltens und der Leistungsziele helfen, die gewünschten Ergebnisse zu erzielen.

-   [Ressourcenauslastung](#resource-usage)
    -   [Ressourcen wieder verwenden](#reuse-resources)
-   [Beschränken der Verwendung von Flush](#restrict-the-use-of-flush)
-   [Bitmaps](#create-large-bitmaps)
    -   [Erstellen großer Bitmaps](#create-large-bitmaps)
    -   [Erstellen eines Atlas von Bitmaps](#create-an-atlas-of-bitmaps)
    -   [Erstellen von freigegebenen Bitmaps](#create-shared-bitmaps)
    -   [Kopieren von Bitmaps](#copying-bitmaps)
-   [Kachelingbitmap über dashlover verwenden](#use-tiled-bitmap-over-dashing)
-   [Allgemeine Richtlinien zum Rendern komplexer statischer Inhalte](#general-guidelines-for-rendering-complex-static-content)
    -   [Vollständiges Szenen Caching mithilfe einer Farb Bitmap](#full-scene-caching-using-a-color-bitmap)
    -   [Pro primitiver Zwischenspeicherung mithilfe einer A8-Bitmap und der fillopacitymask-Methode](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [Pro primitiver Zwischenspeicherung mithilfe von Geometry-neueinrichtungen](#per-primitive-caching-using-geometry-realizations)
-   [Geometrie Rendering](#geometry-rendering)
    -   [Bestimmtes zeichnen-primitiv überzeichnen-Geometrie verwenden](#use-specific-draw-primitive-over-draw-geometry)
    -   [Rendern statischer Geometrie](#rendering-static-geometry)
    -   [Verwenden eines Multithread-Geräte Kontexts](#use-a-multithreaded-device-context)
-   [Zeichnen von Text mit Direct2D](#use-a-multithreaded-device-context)
    -   [Drawtextlayout im Vergleich zu DrawText](#drawtextlayout-vs-drawtext)
    -   [Auswählen des richtigen textrenderingmodus](#choosing-the-right-text-rendering-mode)
    -   [Zwischenspeichern](#full-scene-caching-using-a-color-bitmap)
-   [Clipping einer beliebigen Form](#clipping-an-arbitrary-shape)
    -   [Pushlayer in Windows 8](#pushlayer-in-windows-8)
    -   [Achsen ausgerichtete Clips](#axis-aligned-clips)
-   [DXGI-Interoperabilität: Vermeiden von häufigen Switches](#dxgi-interoperability-avoid-frequent-switches)
-   [Erkennen Ihres Pixel Formats](#know-your-pixel-format)
-   [Komplexität der Szene](#scene-complexity)
    -   [Verstehen der Komplexität von Szenen](#understand-scene-complexity)
-   [Verbessern der Leistung für Direct2D-Druck-apps](#improving-performance-for-direct2d-printing-apps)
    -   [Festlegen der richtigen Eigenschaftswerte beim Erstellen des D2D-Druck Steuer Elements](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [Vermeiden Sie die Verwendung bestimmter Direct2D-Zeichnungs Muster](#avoid-using-certain-direct2d-drawing-patterns)
    -   [Text direkt und auf einfache Weise zeichnen](#draw-text-in-a-direct-and-plain-way)
    -   [Nach Möglichkeit die ursprünglichen Bitmaps zeichnen](#draw-the-original-bitmaps-when-possible)
-   [Zusammenfassung](#conclusion)

## <a name="resource-usage"></a>Ressourcenauslastung

Eine Ressource ist eine Zuordnung einer beliebigen Art, entweder in Video-oder System Arbeitsspeicher. Bitmaps und Pinsel sind Beispiele für Ressourcen.

In Direct2D können Ressourcen sowohl in der Software als auch in der Hardware erstellt werden. Die Erstellung und Löschung von Ressourcen auf Hardware ist aufwändig, da Sie viel mehr Aufwand für die Kommunikation mit der Grafikkarte benötigen. Sehen wir uns an, wie Direct2D Inhalt in ein Ziel rendert.

In Direct2D werden alle renderingbefehle zwischen einem Aufrufen von [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und einem Aufrufen von [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)eingeschlossen. Diese Aufrufe werden an ein Renderziel durchgeführt. Sie müssen die **beginDraw** -Methode aufrufen, bevor Sie Renderingvorgänge aufrufen. Nachdem Sie **beginDraw** aufgerufen haben, erstellt ein Kontext in der Regel einen Batch von renderingbefehlen, verzögert jedoch die Verarbeitung dieser Befehle, bis eine der folgenden Aussagen zutrifft:

-   [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ist aufgetreten. Wenn **EndDraw** aufgerufen wird, bewirkt dies, dass alle Batch-Zeichnungsvorgänge ausgeführt werden und der Status des Vorgangs zurückgegeben wird.
-   Sie führen einen expliziten aufrufungs Vorgang aus: die **Flush** -Methode [**bewirkt, dass**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)der Batch verarbeitet wird und alle ausstehenden Befehle ausgegeben werden.
-   Der Puffer mit den renderingbefehlen ist voll. Wenn dieser Puffer voll ist, bevor die beiden vorherigen Bedingungen erfüllt sind, werden die renderingbefehle geleert.

Bis die primitiven geleert werden, behält Direct2D interne Verweise auf entsprechende Ressourcen wie Bitmaps und Pinsel bei.

### <a name="reuse-resources"></a>Ressourcen wieder verwenden

Wie bereits erwähnt, ist das Erstellen und Löschen von Ressourcen auf Hardwarekosten aufwendig. Verwenden Sie daher nach Möglichkeit Ressourcen. Sehen Sie sich das Beispiel für die bitmaperstellung bei der Spieleentwicklung an. Normalerweise werden Bitmaps, die eine Szene in einem Spiel bilden, gleichzeitig mit allen verschiedenen Variationen erstellt, die für das spätere Rendering von Frame-to-Frame-Funktionen erforderlich sind. Zum Zeitpunkt des tatsächlichen Renderings und erneuten Renderings werden diese Bitmaps wieder verwendet, anstatt neu erstellt zu werden.

> [!Note]  
> Ressourcen für den Fenstergrößen Änderung können nicht wieder verwendet werden. Wenn die Größe eines Fensters geändert wird, müssen einige Skalierungs abhängige Ressourcen, wie z. b. kompatible Renderziele und möglicherweise einige ebenenressourcen, neu erstellt werden, da der Fensterinhalt neu gezeichnet werden muss. Dies kann wichtig sein, um die Gesamtqualität der gerenderten Szene beizubehalten.

 

## <a name="restrict-the-use-of-flush"></a>Beschränken der Verwendung von Flush

Da die [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) -Methode bewirkt, dass die Batch Rendering-Befehle verarbeitet werden, empfiehlt es sich, Sie nicht zu verwenden. Bei den meisten gängigen Szenarien sollten Sie die Ressourcenverwaltung auf Direct2D überlassen.

## <a name="bitmaps"></a>Bitmaps

Wie bereits erwähnt, sind das Erstellen und Löschen von Ressourcen sehr teure Vorgänge in der Hardware. Eine Bitmap ist eine Art von Ressource, die häufig verwendet wird. Das Erstellen von Bitmaps auf der Grafikkarte ist aufwendig. Mithilfe der Wiederverwendung können Sie die Anwendung schneller machen.

### <a name="create-large-bitmaps"></a>Erstellen großer Bitmaps

Grafikkarten verfügen in der Regel über eine Mindestgröße für die Speicher Belegung. Wenn eine Zuweisung angefordert wird, die kleiner als diese ist, wird eine Ressource dieser Mindestgröße zugeordnet, und der überschüssige Arbeitsspeicher wird verschwendet und ist für andere Dinge nicht verfügbar. Wenn Sie viele kleine Bitmaps benötigen, ist es besser, eine große Bitmap zuzuordnen und den gesamten kleinen Bitmapinhalt in dieser großen Bitmap zu speichern. Dann kann das untergeordnete Element der größeren Bitmap gelesen werden, wenn die kleineren Bitmaps benötigt werden. Häufig sollten Sie zwischen den kleinen Bitmaps Auffüll Zeichen (transparente schwarze Pixel) einschließen, um die Interaktion zwischen den kleineren Bildern während des Vorgangs zu vermeiden. Dies wird auch als *Atlas* bezeichnet und hat den Vorteil, dass der Aufwand der bitmaperstellung und die Arbeitsspeicher Verschwendung von kleinen bitmapzuordnungen verringert werden. Es wird empfohlen, die meisten Bitmaps auf mindestens 64 KB beizubehalten und die Anzahl der Bitmaps, die kleiner als 4 KB sind, einzuschränken.

### <a name="create-an-atlas-of-bitmaps"></a>Erstellen eines Atlas von Bitmaps

Es gibt einige gängige Szenarios, für die ein Bitmap-Atlas sehr gut geeignet ist. Kleine Bitmaps können innerhalb einer großen Bitmap gespeichert werden. Diese kleinen Bitmaps können aus der größeren Bitmap herausgezogen werden, wenn Sie Sie durch Angabe des Ziel Rechtecks benötigen. Beispielsweise muss eine Anwendung mehrere Symbole zeichnen. Alle den Symbolen zugeordneten Bitmaps können im Vordergrund in eine große Bitmap geladen werden. Und zur Renderingzeit können Sie aus der großen Bitmap abgerufen werden.

> [!Note]  
> Eine Direct2D-Bitmap, die im Videospeicher erstellt wurde, ist auf die maximale Bitmapgröße beschränkt, die vom Adapter unterstützt wird, auf dem Sie gespeichert ist. Das Erstellen einer Bitmap, die größer als ist, kann zu einem Fehler führen.

 

> [!Note]  
> Ab Windows 8 umfasst Direct2D einen Atlas- [Effekt](atlas.md) , der diesen Prozess vereinfachen kann.

 

### <a name="create-shared-bitmaps"></a>Erstellen von freigegebenen Bitmaps

Durch das Erstellen von freigegebenen Bitmaps können erweiterte Aufrufer Direct2D Bitmap-Objekte erstellen, die direkt durch ein vorhandenes, mit dem Renderziel kompatibles Objekt unterstützt werden. Dadurch wird das Erstellen mehrerer Oberflächen vermieden, und der Leistungs Aufwand wird reduziert.

> [!Note]  
> Freigegebene Bitmaps sind in der Regel auf Software Ziele oder Ziele beschränkt, die mit DXGI interoperabel sind. Verwenden Sie die Methoden "| [**atebitmapfromdxgisurface**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1))", " [**kreatebitmapfromwicbitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))" und " [**foatesharedbitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) " zum Erstellen von freigegebenen Bitmaps.

 

### <a name="copying-bitmaps"></a>Kopieren von Bitmaps

Das Erstellen einer DXGI-Oberfläche ist ein kostspieliger Vorgang, sodass Sie vorhandene Oberflächen wieder verwenden können. Auch wenn eine Bitmap in der Software größtenteils das gewünschte Formular hat, mit Ausnahme eines kleinen Teils, ist es besser, diesen Teil zu aktualisieren, als die gesamte Bitmap zu lösen und alles neu zu erstellen. Obwohl Sie die gleichen Ergebnisse mithilfe von "" mit "" "" mit "" "" mit "" [**"mit"**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) "mit" "auf das gleiche Ergebnis erzielen können, ist Rendering Der Grund hierfür ist, dass die Hardware zum Verbessern der Cache Lokalität nicht tatsächlich eine Bitmap in derselben Speicher Reihenfolge speichert, in der die Bitmap adressiert ist. Stattdessen wird die Bitmap möglicherweise durch ein-und ausgeblendet. Die schwingenden Elemente werden von der CPU entweder durch den Treiber (der langsam und nur für untere Teile verwendet wird) oder durch den Speicher-Manager auf der GPU ausgeblendet. Aufgrund von Einschränkungen der Art und Weise, wie Daten beim Rendern in ein Renderziel geschrieben werden, werden Renderziele in der Regel nicht mit einem Drilldown oder einem Drilldown auf eine Weise, die weniger optimal ist als möglich, wenn Sie wissen, dass Sie nicht auf die Oberfläche gerendert werden müssen. Aus diesem Grund werden die [CopyFrom](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) - \* Methoden zum Kopieren von Rechtecke aus einer Quelle in die Direct2D-Bitmap bereitgestellt.

CopyFrom kann in einer der drei folgenden Formen verwendet werden:

-   [**Copyfrombitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**Copyfromrendertarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**Copyfrommemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>Kachelingbitmap über dashlover verwenden

Das Rendern einer gestrichelten Linie ist aufgrund der hohen Qualität und Genauigkeit des zugrunde liegenden Algorithmus ein sehr aufwändiger Vorgang. In den meisten Fällen, in denen keine wiederholenden Geometrien beteiligt sind, kann der gleiche Effekt mithilfe von gekachelten Bitmaps schneller generiert werden.

## <a name="general-guidelines-for-rendering-complex-static-content"></a>Allgemeine Richtlinien zum Rendern komplexer statischer Inhalte

Zwischenspeichern von Inhalten, wenn Sie den gleichen Inhalts Frame über Frame darstellen, insbesondere, wenn die Szene Komplex ist.

Es gibt drei Verfahren zum Zwischenspeichern, die Sie verwenden können:

-   Vollständiges Szenen Caching mithilfe einer Farb Bitmap.
-   Pro primitiver Zwischenspeicherung mithilfe einer A8-Bitmap und der [**fillopacitymask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) -Methode.
-   Pro primitiver Zwischenspeicherung mithilfe von Geometry-Vorgängen.

Sehen wir uns diese Details genauer an.

### <a name="full-scene-caching-using-a-color-bitmap"></a>Vollständiges Szenen Caching mithilfe einer Farb Bitmap

Wenn Sie statischen Inhalt in Szenarios wie Animation darstellen, erstellen Sie eine weitere vollfarbige Bitmap, anstatt Sie direkt in die Bildschirm Bitmap zu schreiben. Speichern Sie das aktuelle Ziel, legen Sie Ziel auf die zwischen Bitmap fest, und rendersie den statischen Inhalt. Wechseln Sie dann zurück zur ursprünglichen Bildschirm Bitmap, und zeichnen Sie das zwischenbitmap darauf.

Hier sehen Sie ein Beispiel:


```C++
// Create a bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_B8G8R8A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &sceneBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render static content to the sceneBitmap.
m_d2dContext->SetTarget(sceneBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Render sceneBitmap to oldTarget.
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->DrawBitmap(sceneBitmap.Get());
```



In diesem Beispiel werden zwischen Bitmaps zum Zwischenspeichern verwendet und die Bitmap gewechselt, auf die der Gerätekontext beim Rendern zeigt. Dadurch wird vermieden, dass ein kompatibles Renderziel für denselben Zweck erstellt werden muss.

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>Pro primitiver Zwischenspeicherung mithilfe einer A8-Bitmap und der fillopacitymask-Methode

Wenn die vollständige Szene nicht statisch ist, aber aus Elementen wie Geometrie oder statischem Text besteht, können Sie eine pro primitiver zwischen Speicherungs Methode verwenden. Diese Methode behält die Antialiasing-Merkmale des primitiven bei, das zwischengespeichert wird, und funktioniert mit veränderlichen Pinseltypen. Es wird eine A8-Bitmap verwendet, wobei A8 eine Art von Pixel Format ist, das einen Alphakanal mit 8 Bits darstellt. A8-Bitmaps sind nützlich zum Zeichnen von Geometrie und Text als Maske. Wenn Sie die Deckkraft von statischem Inhalt ändern müssen, anstatt den eigentlichen Inhalt zu bearbeiten, können Sie die Deckkraft der Maske übersetzen, drehen, neigen oder skalieren.

Hier sehen Sie ein Beispiel:


```C++
// Create an opacity bitmap.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

// Preserve the pre-existing target.
ComPtr<ID2D1Image> oldTarget;
m_d2dContext->GetTarget(&oldTarget);

// Render to the opacityBitmap.
m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Call the FillOpacityMask method
// Note: for this call to work correctly the anti alias mode must be D2D1_ANTIALIAS_MODE_ALIASED. 
m_d2dContext->SetTarget(oldTarget.Get());
m_d2dContext->FillOpacityMask(
    opacityBitmap.Get(),
    m_contentBrush().Get(),
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS);
```



## <a name="per-primitive-caching-using-geometry-realizations"></a>Pro primitiver Zwischenspeicherung mithilfe von Geometry-neueinrichtungen

Eine weitere pro primitiver zwischen Speicherungs Technik, die als Geometry-Neuerstellung bezeichnet wird, bietet mehr Flexibilität beim Umgang mit Geometrie. Wenn Sie ein-oder Antialiasing-Geometrien wiederholt zeichnen möchten, ist es schneller, Sie in Geometry-neueinformen zu konvertieren und die Neuerungen zu zeichnen, als Sie wiederholt die Geometrien selbst zeichnen. Geometry-neustellungen verbrauchen in der Regel weniger Speicher als Deck Kraft Masken (insbesondere bei großen Geometrien), und Sie sind weniger sensibel bei Skalierungs Änderungen. Weitere Informationen finden Sie unter [Übersicht über Geometry](geometry-realizations-overview.md)-neueinformationen.

Hier sehen Sie ein Beispiel:


```C++
    // Compute a flattening tolerance based on the scales at which the realization will be used.
    float flatteningTolerance = D2D1::ComputeFlatteningTolerance(...);

    ComPtr<ID2D1GeometryRealization> geometryRealization;

    // Create realization of the filled interior of the geometry.
    m_d2dDeviceContext1->CreateFilledGeometryRealization(
        geometry.Get(),
        flatteningTolerance,
        &geometryRealization
        );

    // In your app's rendering code, draw the geometry realization with a brush.
    m_d2dDeviceContext1->BeginDraw();
    m_d2dDeviceContext1->DrawGeometryRealization(
        geometryRealization.Get(),
        m_brush.Get()
        );
    m_d2dDeviceContext1->EndDraw();
```



## <a name="geometry-rendering"></a>Geometrie Rendering

### <a name="use-specific-draw-primitive-over-draw-geometry"></a>Bestimmtes zeichnen-primitiv überzeichnen-Geometrie verwenden

Verwenden Sie spezifischere zeichnen *primitiver* Aufrufe wie [**drawrechteck**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) über generische [**DrawGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) -Aufrufe. Dies liegt daran, dass die Geometrie mit **drawrechteck** bereits bekannt ist, sodass das Rendering schneller ist.

### <a name="rendering-static-geometry"></a>Rendern statischer Geometrie

In Szenarien, in denen die Geometrie statisch ist, verwenden Sie die oben erläuterten grundlegenden Caching-Techniken. Durch Deck Kraft Masken und Geometrie-Real Messungen kann die renderinggeschwindigkeit von Szenen, die statische Geometrie enthalten, erheblich verbessert werden.

### <a name="use-a-multithreaded-device-context"></a>Verwenden eines Multithread-Geräte Kontexts

Anwendungen, die eine beträchtliche Menge an komplexen geometrischen Inhalten darstellen, sollten beim Erstellen eines [Direct2D](./direct2d-portal.md) -Geräte Kontexts die [**D2D1-Gerätekontext Optionen das Flag zum Aktivieren von \_ \_ \_ \_ \_ \_ \_ multithreadoptimierungen aktivieren**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) . Wenn dieses Flag angegeben ist, verteilt Direct2D das Rendering auf alle logischen Kerne, die auf dem System vorhanden sind. Dies kann die Gesamt Renderingzeit erheblich verringern.

Hinweise:

-   Ab Windows 8.1 wirkt sich dieses Flag nur auf das Rendern von Pfad Geometrie aus. Es hat keine Auswirkung auf Szenen, die nur andere primitive Typen enthalten (z. b. Text, Bitmaps oder Geometrie-neueinrichtungen).
-   Dieses Flag hat auch keine Auswirkung auf das Rendering in Software (d. h. beim Rendern mit einem Warp Direct3D-Gerät). Um das Multithreading von Software zu steuern, sollten Aufrufer \_ \_ \_ \_ \_ \_ beim Erstellen des Warp Direct3D-Geräts das Flag D3D11 Create Device Internal Threading Optimierungen verwenden.
-   Wenn Sie dieses Flag angeben, kann das Workingset beim Rendering erhöht werden, und es können auch Thread Konflikte in Anwendungen erhöht werden, die die Multithreadverarbeitung bereits nutzen.

## <a name="drawing-text-with-direct2d"></a>Zeichnen von Text mit Direct2D

Die Direct2D-Text Rendering-Funktionalität wird in zwei Teilen angeboten. Der erste Teil, der als [**ID2D1RenderTarget::D rawtext**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) -und [**ID2D1RenderTarget::D rawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) -Methode verfügbar gemacht wird, ermöglicht einem Aufrufer, entweder einen Zeichen folgen-und einen Formatierungs Parameter oder ein dwrite-Text Layout-Objekt für mehrere Formate zu übergeben. Dies sollte für die meisten Aufrufer geeignet sein. Die zweite Möglichkeit zum Rendering von Text, der als [**ID2D1RenderTarget::D rawglyphrun-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) Methode verfügbar gemacht wird, bietet eine rasterisierung für Kunden, die bereits die Position der Symbole kennen, die Sie darstellen möchten. Die folgenden beiden allgemeinen Regeln können dabei helfen, die Text Leistung beim Zeichnen in Direct2D zu verbessern.

### <a name="drawtextlayout-vs-drawtext"></a>Drawtextlayout im Vergleich zu DrawText

Sowohl [**DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) als auch [**drawtextlayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) ermöglichen einer Anwendung das einfache Rendering von Text, der von der [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal) -API formatiert wird. **Drawtextlayout** zeichnet ein vorhandenes [**dwrite-Textlayout**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) -Objekt mit [**renderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget), und **DrawText** erstellt basierend auf den Parametern, die übergeben werden, ein DirectWrite-Layout für den Aufrufer. Wenn derselbe Text mehrmals gerendert werden muss, verwenden Sie **drawtextlayout** anstelle von **DrawText**, da **DrawText** jedes Mal, wenn er aufgerufen wird, ein Layout erstellt.

### <a name="choosing-the-right-text-rendering-mode"></a>Auswählen des richtigen textrenderingmodus

Legen Sie für den Text-antialiasmodus den [**D2D1 \_ Text- \_ Antialias Modus \_ \_ Grayscale**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) explizit fest. Die Qualität des Renderings von Graustufen Text ist mit ClearType vergleichbar, aber viel schneller.

### <a name="caching"></a>Zwischenspeicherung

Verwenden Sie die vollständige Szene oder das Zwischenspeichern der primitiven Bitmap, wie z. b. das Zeichnen von

## <a name="clipping-an-arbitrary-shape"></a>Clipping einer beliebigen Form

Die Abbildung zeigt das Ergebnis der Anwendung eines Clips auf ein Bild.

![ein Bild, das ein Beispiel eines Bilds vor und nach einem Clip anzeigt.](images/clip.png)

Sie können dieses Ergebnis mithilfe von Ebenen mit einer Geometrie Maske oder der [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode mit einem Deckkraft Pinsel erhalten.

Im folgenden finden Sie ein Beispiel, in dem eine Ebene verwendet wird:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Es folgt ein Beispiel, in dem die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode verwendet wird:


```C++
// Create an opacity bitmap and render content.
m_d2dContext->CreateBitmap(size, nullptr, 0,
    D2D1::BitmapProperties(
        D2D1_BITMAP_OPTIONS_TARGET,
        D2D1::PixelFormat(
            DXGI_FORMAT_A8_UNORM,
            D2D1_ALPHA_MODE_PREMULTIPLIED),
        dpiX, dpiY),
    &opacityBitmap);

m_d2dContext->SetTarget(opacityBitmap.Get());
m_d2dContext->BeginDraw();
…
m_d2dContext->EndDraw();

// Create an opacity brush from the opacity bitmap.
m_d2dContext->CreateBitmapBrush(opacityBitmap.Get(),
    D2D1::BitmapBrushProperties(),
    D2D1::BrushProperties(),
    &bitmapBrush);

// Call the FillGeometry method and pass in the clip geometry and the opacity brush
m_d2dContext->FillGeometry( 
    clipGeometry.Get(),
    brush.Get(),
    opacityBrush.Get()); 
```



Wenn Sie in diesem Codebeispiel die pushlayer-Methode aufzurufen, übergeben Sie keine von der APP erstellte Ebene. Direct2D erstellt eine Ebene für Sie. Direct2D ist in der Lage, die Zuordnung und Zerstörung dieser Ressource ohne Beteiligung der APP zu verwalten. Dadurch kann Direct2D Ebenen intern wieder verwenden und Ressourcen Verwaltungs Optimierungen anwenden.

In Windows 8 wurden viele Optimierungen an der Verwendung von Ebenen vorgenommen, und es wird empfohlen, die Verwendung von ebenenapis anstelle von [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) zu verwenden, wenn dies möglich ist.

### <a name="pushlayer-in-windows-8"></a>Pushlayer in Windows 8

Die [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Schnittstelle wird von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle abgeleitet und ist der Schlüssel zum Anzeigen von Direct2D-Inhalten in Windows 8. Weitere Informationen zu dieser Schnittstelle finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md). Mit der Gerätekontext Schnittstelle können Sie den Aufruf der [**createlayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) -Methode überspringen und dann NULL an die [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) -Methode übergeben. Direct2D verwaltet die ebenenressource automatisch und kann Ressourcen zwischen Ebenen und Effekt Diagrammen freigeben.

### <a name="axis-aligned-clips"></a>Achsen ausgerichtete Clips

, Wenn der Bereich, der abgeschnitten werden soll, an der Achse der Zeichen Oberfläche ausgerichtet ist, anstatt beliebig. Dieser Fall eignet sich für die Verwendung eines Clip Rechtecks anstelle einer Ebene. Der Leistungsgewinn liegt eher bei der Aliasing Geometrie als bei der Geometrie mit Antialiasing. Weitere Informationen zu den Achsen ausgerichteten Clips finden Sie im Thema [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>DXGI-Interoperabilität: Vermeiden von häufigen Switches

Direct2D kann nahtlos mit Direct3D-Oberflächen zusammenarbeiten. Dies ist sehr nützlich für das Erstellen von Anwendungen, die eine Mischung aus 2D-und 3D-Inhalten darstellen. Jeder Wechsel zwischen Drawing Direct2D und Direct3D-Inhalt wirkt sich jedoch auf die Leistung aus.

Beim Rendern auf eine DXGI-Oberfläche speichert Direct2D den Zustand der Direct3D-Geräte während des Renderings und stellt Sie wieder her, wenn das Rendering abgeschlossen ist. Jedes Mal, wenn ein Batch von Direct2D Rendering abgeschlossen ist, werden die Kosten für diese Speicherung und Wiederherstellung und die Kosten für das leeren aller 2D-Vorgänge bezahlt. das Direct3D-Gerät wird jedoch nicht geleert. Um die Leistung zu erhöhen, beschränken Sie daher die Anzahl der renderingschalter zwischen Direct2D und Direct3D.

## <a name="know-your-pixel-format"></a>Erkennen Ihres Pixel Formats

Wenn Sie ein Renderziel erstellen, können Sie die [**D2D1 \_ Pixel- \_ Format**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) Struktur verwenden, um das Pixel Format und den Alpha Modus anzugeben, die vom Renderziel verwendet werden. Ein Alphakanal ist Teil des Pixel Formats, das den Abdeckungs Wert oder Deck Kraft-Informationen angibt. Wenn ein Renderziel nicht den Alphakanal verwendet, sollte er im Modus " [**D2D1 Alpha Mode \_ \_ \_ Ignore**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) Alpha" erstellt werden. Dadurch wird die Zeit, die für das Rendern eines Alphakanals aufgewendet wird, der nicht benötigt wird, gespart.

Weitere Informationen zu Pixel Formaten und Alpha Modi finden Sie [unter Unterstützte Pixel Formate und Alpha-Modi](supported-pixel-formats-and-alpha-modes.md).

## <a name="scene-complexity"></a>Komplexität der Szene

Wenn Sie Leistungs-Hotspots in einer Szene analysieren, die gerendert wird, kann es hilfreich sein, wenn Sie wissen, ob die Szene an die Füllrate gebunden ist oder Vertex-gebunden ist.

-   Füllrate: die Füllrate bezieht sich auf die Anzahl der Pixel, die eine Grafikkarte Renderingvorgänge und in den Videospeicher pro Sekunde schreiben kann.
-   Vertex-gebunden: eine Szene ist Scheitelpunkt gebunden, wenn Sie viele komplexe Geometrie enthält.

### <a name="understand-scene-complexity"></a>Verstehen der Komplexität von Szenen

Sie können die Komplexität der Szene analysieren, indem Sie die Größe des Renderziels ändern. Wenn Leistungssteigerungen für eine proportionale Reduzierung der Größe des Renderziels sichtbar sind, wird die Füllrate der Anwendung aufgehoben. Andernfalls ist die Komplexität der Szene der Leistungsengpass.

Wenn eine Szene in der Füllrate gebunden ist, kann die Leistung durch eine Verringerung der Größe des Renderziels verbessert werden. Dies liegt daran, dass die Anzahl der zu rendernden Pixel proportional zur Größe des Renderziels reduziert wird.

Wenn eine Szene Scheitelpunkt gebunden ist, verringern Sie die Komplexität der Geometrie. Beachten Sie jedoch, dass dies auf Kosten der Bildqualität erfolgt. Daher sollte eine sorgfältige Kompromiss Entscheidung zwischen der gewünschten Qualität und der erforderlichen Leistung getroffen werden.

## <a name="improving-performance-for-direct2d-printing-apps"></a>Verbessern der Leistung für Direct2D-Druck-apps

[Direct2D](./direct2d-portal.md) bietet Kompatibilität mit dem Drucken. Sie können dieselben Direct2D-Zeichnungs Befehle (in Form von Direct2D-Befehlslisten) zum Drucken an das Direct2D-Druck Steuerelement senden, wenn Sie nicht wissen, auf welche Geräte Sie sich beziehen, oder wie die Zeichnung in das Drucken übersetzt wird.

Sie können die Verwendung des [Direct2D](./direct2d-portal.md) -Druck Steuer Elements und ihrer Direct2D-Zeichnungs Befehle weiter optimieren, um Druckergebnisse mit besserer Leistung zu liefern.

Das Druck Steuerelement [Direct2D](./direct2d-portal.md) gibt Debugmeldungen aus, wenn ein Direct2D-Code Muster angezeigt wird, das zu einer niedrigeren Druckqualität oder-Leistung führt (z. b. Code muster weiter unten in diesem Thema), um Sie daran zu erinnern, wo Sie Leistungsprobleme vermeiden können Um diese Debugmeldungen anzuzeigen, müssen Sie [Direct2D Debug Layer](direct2ddebuglayer-portal.md) in Ihrem Code aktivieren. Anweisungen zum Aktivieren der Ausgabe der Debugmeldung finden Sie unter [Debug Messages](direct2ddebuglayer-debugmessages.md) .

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>Festlegen der richtigen Eigenschaftswerte beim Erstellen des D2D-Druck Steuer Elements

Es gibt drei Eigenschaften, die Sie festlegen können, wenn Sie das [Direct2D](./direct2d-portal.md) -Druck Steuerelement erstellen. Zwei dieser Eigenschaften beeinflussen, wie das Direct2D-Druck Steuerelement bestimmte Direct2D-Befehle behandelt und sich wiederum auf die Gesamtleistung auswirkt.

-   Font Subset Mode: das [Direct2D](./direct2d-portal.md) -Druck Steuerelement unterteilt Schriftart Ressourcen, die auf jeder Seite verwendet werden, bevor die zu druckende Seite gesendet wird. Dieser Modus reduziert die Größe der zum Drucken benötigten Seiten Ressourcen. Abhängig von der Schriftart Verwendung auf der Seite können Sie verschiedene Schriftart Teilmengen-Modi auswählen, um die beste Leistung zu erzielen.
    -   [**D2D1 \_ Der \_ Standardwert für Schriftart- \_ Untermenge \_ \_ Drucken**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) bietet in den meisten Fällen die beste Druckleistung. Wenn dieser Modus festgelegt ist, verwendet das [Direct2D](./direct2d-portal.md) -Druck Steuerelement eine heuristische Strategie, um zu entscheiden, wann Schriftarten unterteilt werden sollen.
    -   Für kurze Druckaufträge mit 1 oder 2 Seiten wird empfohlen, [**den \_ Schriftart-Teilmengen \_ \_ \_ Modus \_ D2D1 zu drucken**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) , bei dem das [Direct2D](./direct2d-portal.md) -Druck Steuerelement die Schriftarten Ressourcen auf jeder Seite einrichtet und die Schriftart in den einzelnen Seiten einbettet. diese Schriftart wird dann verworfen, nachdem die Seite gedruckt wurde. Mit dieser Option wird sichergestellt, dass jede Seite sofort gedruckt werden kann, nachdem Sie generiert wurde, aber die Größe der Seiten Ressourcen, die für den Druck benötigt werden (normalerweise große Schriftart Teilmengen), etwas erhöht
    -   Für Druckaufträge mit vielen Seiten von Texten und kleinen Schrift Graden (z. b. 100 Textseiten, die eine einzelne Schriftart verwenden) Es wird empfohlen, den Schrift Schnitt für Schriftart in [](./direct2d-portal.md) [**D2D1 drucken zu lassen, wobei das Direct2D-Druck Steuerelement keine Schriftart Ressourcen unter \_ \_ \_ \_ \_**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode)teilt, sondern die ursprünglichen Schriftart Ressourcen zusammen mit der Seite sendet, die zuerst die Schriftart verwendet, und die Schriftart Ressourcen für spätere Seiten erneut verwendet, ohne Sie erneut zu senden.
-   Rasterisierungsdpi: Wenn das [Direct2D](./direct2d-portal.md) -Druck Steuerelement während der Direct2D-XPS-Konvertierung Direct2D-Befehle Rasterisieren muss, wird dieser dpi-Wert für die rasterisierung verwendet. Anders ausgedrückt: Wenn die Seite keinen gerastererten Inhalt hat, wird durch das Festlegen eines beliebigen dpi-Wert die Leistung und Qualität nicht geändert. Abhängig von der rasterisierungsverwendung auf der Seite können Sie unterschiedliche rasterisierungsdpis auswählen, um ein optimales Gleichgewicht zwischen Treue und Leistung zu erzielen.
    -   150 ist der Standardwert, wenn Sie keinen Wert angeben, wenn Sie das [Direct2D](./direct2d-portal.md) -Druck Steuerelement erstellen. Dies ist in den meisten Fällen das beste Gleichgewicht der Druckqualität und der Druckleistung.
    -   Höhere dpi-Werte führen in der Regel zu einer besseren Druckqualität (da weitere Details beibehalten werden), aber zu einer geringeren Leistung aufgrund der größeren Bitmaps, die Sie generiert. Wir empfehlen keinen dpi-Wert größer als 300, da dadurch keine zusätzlichen Informationen, die von Menschen Augen visuell sichtbar sind, eingeführt werden.
    -   Niedrigerer dpi-Wert kann eine bessere Leistung bedeuten, kann jedoch auch zu einer niedrigeren Qualität führen

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>Vermeiden Sie die Verwendung bestimmter Direct2D-Zeichnungs Muster

Es gibt Unterschiede zwischen dem, was [Direct2D](./direct2d-portal.md) visuell darstellen kann, und dem, was das Druck Subsystem in der gesamten Druck Pipeline behalten und transportieren kann. Das Druck Steuerelement Direct2D Bridges diese Lücken durch das Anfügen oder rasterieren von Direct2D-primitiven, die vom Druck Subsystem nicht nativ unterstützt werden. Diese Näherung führt in der Regel zu einer geringeren Druck Treue, geringeren Druckleistung oder beidem. Daher ist es in allen Fällen nicht ideal, auch wenn ein Kunde die gleichen Zeichnungs Muster für Bildschirm-und Druck Rendering verwenden kann. Es empfiehlt sich, solche Direct2D-primitive und-Muster nicht so weit wie möglich für den Druckpfad zu verwenden, oder Sie verwenden eine eigene rasterisierung, bei der Sie vollständige Kontrolle über die Qualität und die Größe der gerasterten Bilder verfügen.

Im folgenden finden Sie eine Liste der Fälle, in denen die Druckleistung und-Qualität nicht ideal sind und Sie ggf. den Codepfad für eine optimale Druckleistung unterscheiden möchten.

-   Vermeiden Sie die Verwendung des primitiven Blend-Modus außer [**D2D1 \_ primitiver \_ Blend \_ sourceover**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend).
-   Vermeiden Sie die Verwendung von Kompositions Modi, wenn Sie ein anderes Bild als den D2D1-Modus für den zusammen [**\_ gesetzten \_ Modus \_ \_ über**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) und den **D2D1- \_ Verbund \_ Modus \_ \_**
-   Vermeiden Sie das Zeichnen einer GDI-Metadatendatei.
-   Vermeiden Sie das Übertragen einer ebenenressource, die den Quell Hintergrund kopiert ( [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) wird aufgerufen, wobei [**D2D1 \_ Layer \_ OPTIONS1 \_ Initialize \_ von \_ Background**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) an die **D2D1 \_ Layer \_ PARAMETERS1** -Struktur übergeben wird).
-   Vermeiden Sie das Erstellen eines Bitmap-Pinsels oder Bild Pinsels mit der D2D1-Pinsel \_ Erweiterung \_ \_ Es wird empfohlen, dass Sie D2D1 extendermodusspiegelung verwenden \_ \_ , wenn Sie sich \_ keine Gedanken über Pixel außerhalb des Bilds machen (z. b., wenn das Bild, das an den Pinsel angefügt ist, größer als der gefüllte Zielbereich ist).
-   Vermeiden Sie das Zeichnen von Bitmaps mit [Perspektiven Transformationen](3d-perspective-transform.md).

### <a name="draw-text-in-a-direct-and-plain-way"></a>Text direkt und auf einfache Weise zeichnen

Direct2D verfügt über mehrere Optimierungen beim Rendern von Texten, die für eine bessere Leistung und/oder eine bessere visuelle Qualität angezeigt werden. Aber nicht alle Optimierungen verbessern die Druckleistung und-Qualität, da der Druck auf dem Papier in der Regel eine viel höhere dpi-Menge hat, und das Drucken muss keine Szenarios wie Animation aufnehmen. Daher wird empfohlen, dass Sie den ursprünglichen Text oder die Symbole direkt zeichnen und eine der folgenden Optimierungen vermeiden, wenn Sie die Befehlsliste zum Drucken erstellen.

-   Vermeiden Sie das Zeichnen von Text mit der [**fillopacitymask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask) -Methode.
-   Vermeiden Sie das Zeichnen von Text im Alias Modus.

### <a name="draw-the-original-bitmaps-when-possible"></a>Nach Möglichkeit die ursprünglichen Bitmaps zeichnen

Wenn die Ziel Bitmap ein JPEG ist, PNG, TIFF oder JPEG-XR Sie können eine WIC-Bitmap entweder aus einer Datenträger Datei oder aus einem in-Memory-Stream erstellen. Anschließend können Sie eine [Direct2D](./direct2d-portal.md) -Bitmap aus der WIC-Bitmap mithilfe von [**ID2D1DeviceContext:: depfromwicbitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))und schließlich direkt an das Direct2D-Druck Steuerelement übergeben, ohne weitere Manipulationen durchführen zu müssen. Auf diese Weise kann das Direct2D-Druck Steuerelement den bitmapStream wieder verwenden, was in der Regel zu einer besseren Druckleistung führt (durch das Überspringen der redundante Bitmap-Codierung und-Decodierung) und eine bessere Druckqualität (wenn Metadaten, z. b. Farbprofile, in der Bitmap beibehalten werden).

Das Zeichnen der ursprünglichen Bitmap bietet die folgenden Vorteile für-Anwendungen.

-   Im Allgemeinen behält [Direct2D](./direct2d-portal.md) Print die ursprünglichen Informationen (ohne Verlust oder Rauschen) bis zum späten Zeitpunkt in der Pipeline bei, insbesondere dann, wenn Apps die Details der Druck Pipeline nicht kennen (bzw. nicht wissen möchten), insbesondere dann, wenn die Drucker Pipeline die Details der Druck Pipeline kennt
-   In vielen Fällen bedeutet eine verzögerte Bitmap-rasterisierung eine bessere Leistung (z. b. beim Drucken eines 96dpi-Fotos auf einen 600 dpi-Drucker).
-   In bestimmten Fällen ist das übergeben der ursprünglichen Bilder die einzige Möglichkeit, hohe Genauigkeit zu beachten (wie z. b. eingebettete Farbprofile).

Eine solche Optimierung kann jedoch aufgrund der folgenden Aktionen nicht deaktiviert werden:

-   Durch Abfragen von Drucker Informationen und der frühen rasterisierung können Sie Inhalte selbst mit vollständiger Kontrolle über die endgültige Darstellung auf dem Papier verkleinern.
-   In bestimmten Fällen kann die frühe Vergrößerung tatsächlich die End-to-End-Leistung einer APP verbessern (z. b. das Drucken von Fotos in der Größe von Fotos).
-   In bestimmten Fällen erfordert das übergeben der ursprünglichen Bitmaps eine bedeutende Änderung der vorhandenen Code Architektur (z. b. das Laden von Bildern und Ressourcen Update Pfaden in bestimmten Anwendungen).

## <a name="conclusion"></a>Zusammenfassung

Obwohl Direct2D Hardware beschleunigt ist und für hohe Leistung vorgesehen ist, müssen Sie die Funktionen zum Maximieren des Durchsatzes ordnungsgemäß verwenden. Die hier vorgestellten Verfahren sind von der Untersuchung allgemeiner Szenarien abgeleitet und gelten möglicherweise nicht für alle Anwendungsszenarien.

 

 
