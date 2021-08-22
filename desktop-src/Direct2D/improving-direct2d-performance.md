---
title: Verbessern der Leistung von Direct2D-Apps
description: Beschreibt Techniken zur Verbesserung der Direct2D-Leistung.
ms.assetid: e6b02925-4e75-42b0-b0c4-00f1ddb85e46
keywords:
- Direct2D, Leistung
- Direct2D, Bitmaps
- Direct2D, Ressourcennutzung
- Direct2D,Flush-Methode
- Direct2D, statischer Inhalt
- Leistung für Direct2D
- Bitmaps für Direct2D
- Direct2D,GDI-Interoperation
- Direct2D, Interoperabilität
- Interoperabilität,Direct2D
- Graphics Device Interface (GDI)
- GDI (Graphics Device Interface)
- Interoperabilität, Graphics Device Interface (GDI)
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 34adfd708ef3c1b8d7a6af145d9d1c9505b01beb1ba9b31834e267123ad05b69
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119641500"
---
# <a name="improving-the-performance-of-direct2d-apps"></a>Verbessern der Leistung von Direct2D-Apps

Obwohl [Direct2D](./direct2d-portal.md) hardwarebeschleunigend ist und für hohe Leistung vorgesehen ist, müssen Sie die Features ordnungsgemäß verwenden, um den Durchsatz zu maximieren. Die hier gezeigten Techniken stammen aus der Untersuchung gängiger Szenarien und gelten möglicherweise nicht für alle App-Szenarien. Daher kann ein sorgfältiges Verständnis des App-Verhaltens und der Leistungsziele dazu beitragen, die gewünschten Ergebnisse zu erzielen.

-   [Ressourcennutzung](#resource-usage)
    -   [Wiederverwenden von Ressourcen](#reuse-resources)
-   [Einschränken der Verwendung der Leerung](#restrict-the-use-of-flush)
-   [Bitmaps](#create-large-bitmaps)
    -   [Erstellen großer Bitmaps](#create-large-bitmaps)
    -   [Erstellen eines Atlas von Bitmaps](#create-an-atlas-of-bitmaps)
    -   [Erstellen freigegebener Bitmaps](#create-shared-bitmaps)
    -   [Kopieren von Bitmaps](#copying-bitmaps)
-   [Verwenden von gekachelten Bitmaps über Bindestriche](#use-tiled-bitmap-over-dashing)
-   [Allgemeine Richtlinien zum Rendern komplexer statischer Inhalte](#general-guidelines-for-rendering-complex-static-content)
    -   [Vollständige Szenenzwischenspeicherung mit einer Farbbitmap](#full-scene-caching-using-a-color-bitmap)
    -   [Pro primitivem Zwischenspeichern mit einer A8-Bitmap und der FillOpacityMask-Methode](#per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method)
-   [Zwischenspeichern pro Primitiven mit geometriebasierten Realisierungen](#per-primitive-caching-using-geometry-realizations)
-   [Geometrierendering](#geometry-rendering)
    -   [Verwenden eines bestimmten Primitiven zeichnen über zeichnende Geometrie](#use-specific-draw-primitive-over-draw-geometry)
    -   [Rendern von statischer Geometrie](#rendering-static-geometry)
    -   [Verwenden eines Multithreadgerätekontexts](#use-a-multithreaded-device-context)
-   [Zeichnen von Text mit Direct2D](#use-a-multithreaded-device-context)
    -   [DrawTextLayout im Vergleich zu DrawText](#drawtextlayout-vs-drawtext)
    -   [Auswählen des richtigen Textrenderingmodus](#choosing-the-right-text-rendering-mode)
    -   [Zwischenspeichern](#full-scene-caching-using-a-color-bitmap)
-   [Beschneiden einer beliebigen Form](#clipping-an-arbitrary-shape)
    -   [PushLayer in Windows 8](#pushlayer-in-windows-8)
    -   [An der Achse ausgerichtete Clips](#axis-aligned-clips)
-   [DXGI-Interoperabilität: Vermeiden häufiger Switches](#dxgi-interoperability-avoid-frequent-switches)
-   [Kennen Ihres Pixelformats](#know-your-pixel-format)
-   [Szenenkomplexität](#scene-complexity)
    -   [Verstehen der Komplexität von Szenen](#understand-scene-complexity)
-   [Verbessern der Leistung für Direct2D-Druck-Apps](#improving-performance-for-direct2d-printing-apps)
    -   [Festlegen der richtigen Eigenschaftswerte beim Erstellen des D2D-Drucksteuerelements](#set-the-right-property-values-when-you-create-the-d2d-print-control)
    -   [Vermeiden der Verwendung bestimmter Direct2D-Zeichnungsmuster](#avoid-using-certain-direct2d-drawing-patterns)
    -   [Direktes und einfaches Zeichnen von Text](#draw-text-in-a-direct-and-plain-way)
    -   [Zeichnen der ursprünglichen Bitmaps nach Möglichkeit](#draw-the-original-bitmaps-when-possible)
-   [Zusammenfassung](#conclusion)

## <a name="resource-usage"></a>Ressourcenauslastung

Eine Ressource ist eine Zuordnung einer Art, entweder im Video- oder Systemspeicher. Bitmaps und Pinsel sind Beispiele für Ressourcen.

In Direct2D können Ressourcen sowohl in Software als auch in Hardware erstellt werden. Die Erstellung und Löschung von Ressourcen auf Hardware sind teure Vorgänge, da sie viel Aufwand für die Kommunikation mit der Grafikkarte erfordern. Sehen wir uns an, wie Direct2D Inhalte auf ein Ziel rendert.

In Direct2D werden alle Renderingbefehle zwischen einem Aufruf von [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und einem Aufruf von [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)eingeschlossen. Diese Aufrufe werden an ein Renderziel vorgenommen. Sie müssen die **BeginDraw-Methode** aufrufen, bevor Sie Renderingvorgänge aufrufen. Nachdem Sie **BeginDraw** aufgerufen haben, erstellt ein Kontext in der Regel einen Batch von Renderingbefehlen, verzögert jedoch die Verarbeitung dieser Befehle, bis eine dieser Anweisungen zutrifft:

-   [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) ist aufgetreten. Wenn **EndDraw** aufgerufen wird, werden alle Batchzeichnungsvorgänge abgeschlossen, und der Status des Vorgangs wird zurückgegeben.
-   Sie rufen [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)explizit auf: Die **Flush-Methode** bewirkt, dass der Batch verarbeitet und alle ausstehenden Befehle ausgegeben werden.
-   Der Puffer mit den Renderingbefehlen ist voll. Wenn dieser Puffer voll wird, bevor die beiden vorherigen Bedingungen erfüllt sind, werden die Renderingbefehle geleert.

Bis die Primitiven geleert werden, behält Direct2D interne Verweise auf entsprechende Ressourcen wie Bitmaps und Pinsel bei.

### <a name="reuse-resources"></a>Wiederverwenden von Ressourcen

Wie bereits erwähnt, ist die Erstellung und Löschung von Ressourcen auf der Hardware teuer. Verwenden Sie also nach Möglichkeit Ressourcen wieder. Nehmen Sie das Beispiel für die Bitmaperstellung bei der Spieleentwicklung. Normalerweise werden Bitmaps, die eine Szene in einem Spiel bilden, gleichzeitig mit allen verschiedenen Variationen erstellt, die für das spätere Frame-to-Frame-Rendering erforderlich sind. Zum Zeitpunkt des tatsächlichen Renderns und erneuten Renderns von Szenen werden diese Bitmaps wiederverwendet, anstatt neu erstellt zu werden.

> [!Note]  
> Sie können keine Ressourcen für den Vorgang zum Ändern der Fenstergröße wiederverwenden. Wenn die Größe eines Fensters geändert wird, müssen einige skalierungsabhängige Ressourcen wie kompatible Renderziele und möglicherweise einige Ebenenressourcen neu erstellt werden, da der Fensterinhalt neu gezeichnet werden muss. Dies kann wichtig sein, um die Gesamtqualität der gerenderten Szene aufrechtzuerhalten.

 

## <a name="restrict-the-use-of-flush"></a>Einschränken der Verwendung der Leerung

Da die [**Flush-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) bewirkt, dass die Batchrenderingbefehle verarbeitet werden, wird empfohlen, sie nicht zu verwenden. Für die meisten gängigen Szenarien belassen Sie die Ressourcenverwaltung auf Direct2D.

## <a name="bitmaps"></a>Bitmaps

Wie bereits erwähnt, sind das Erstellen und Löschen von Ressourcen sehr kostspielige Vorgänge in der Hardware. Eine Bitmap ist eine Art von Ressource, die häufig verwendet wird. Das Erstellen von Bitmaps auf der Grafikkarte ist teuer. Die Wiederverwendung kann dazu beitragen, die Anwendung schneller zu machen.

### <a name="create-large-bitmaps"></a>Erstellen großer Bitmaps

Grafikkarten weisen in der Regel eine minimale Speicherbelegungsgröße auf. Wenn eine Zuordnung angefordert wird, die kleiner als diese ist, wird eine Ressource dieser Mindestgröße zugeordnet, und der überschüssige Arbeitsspeicher wird verschwendet und ist für andere Dinge nicht verfügbar. Wenn Sie viele kleine Bitmaps benötigen, ist es besser, eine große Bitmap zuzuordnen und alle kleinen Bitmapinhalte in dieser großen Bitmap zu speichern. Dann können Unterbereiche der größeren Bitmap gelesen werden, wo die kleineren Bitmaps benötigt werden. Häufig sollten Sie die Auffüllung (transparente schwarze Pixel) zwischen den kleinen Bitmaps einschließen, um eine Interaktion zwischen den kleineren Bildern während der Vorgänge zu vermeiden. Dies wird auch als *Atlas* bezeichnet und hat den Vorteil, dass der Aufwand für die Bitmaperstellung und die Verschwendung von Arbeitsspeicher durch kleine Bitmapzuordnungen reduziert werden. Es wird empfohlen, die meisten Bitmaps auf mindestens 64 KB beizubehalten und die Anzahl von Bitmaps zu begrenzen, die kleiner als 4 KB sind.

### <a name="create-an-atlas-of-bitmaps"></a>Erstellen eines Atlas von Bitmaps

Es gibt einige gängige Szenarien, für die ein Bitmapat atlas sehr gut eingesetzt werden kann. Kleine Bitmaps können in einer großen Bitmap gespeichert werden. Diese kleinen Bitmaps können aus der größeren Bitmap abgerufen werden, wenn Sie sie benötigen, indem Sie das Zielrechteck angeben. Beispielsweise muss eine Anwendung mehrere Symbole zeichnen. Alle Bitmaps, die den Symbolen zugeordnet sind, können vorab in eine große Bitmap geladen werden. Und zur Renderingzeit können sie aus der großen Bitmap abgerufen werden.

> [!Note]  
> Eine im Videospeicher erstellte Direct2D-Bitmap ist auf die maximale Bitmapgröße beschränkt, die vom Adapter unterstützt wird, auf dem sie gespeichert wird. Das Erstellen einer Bitmap, die größer als diese ist, kann zu einem Fehler führen.

 

> [!Note]  
> Ab Windows 8 enthält Direct2D einen [Atlas-Effekt,](atlas.md) der diesen Prozess vereinfachen kann.

 

### <a name="create-shared-bitmaps"></a>Erstellen freigegebener Bitmaps

Durch das Erstellen freigegebener Bitmaps können erweiterte Aufrufer Direct2D-Bitmapobjekte erstellen, die direkt von einem vorhandenen Objekt unterstützt werden, das bereits mit dem Renderziel kompatibel ist. Dies vermeidet das Erstellen mehrerer Oberflächen und trägt zur Verringerung des Leistungsaufwands bei.

> [!Note]  
> Freigegebene Bitmaps sind in der Regel auf Softwareziele oder auf Ziele beschränkt, die mit DXGI interoperabel sind. Verwenden Sie die Methoden [**CreateBitmapFromDxgiSurface,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromdxgisurface(idxgisurface_constd2d1_bitmap_properties1_id2d1bitmap1)) [**CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))und [**CreateSharedBitmap,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsharedbitmap) um freigegebene Bitmaps zu erstellen.

 

### <a name="copying-bitmaps"></a>Kopieren von Bitmaps

Das Erstellen einer DXGI-Oberfläche ist ein aufwendiger Vorgang, sodass vorhandene Oberflächen nach Möglichkeit wiederverwendet werden können. Selbst in der Software ist es besser, diesen Teil zu aktualisieren, als die gesamte Bitmap wegzuwerfen und alles neu zu erstellen, wenn eine Bitmap größtenteils in der gewünschten Form vorliegt, mit Ausnahme eines kleinen Teils. Obwohl Sie [**CreateCompatibleRenderTarget**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createcompatiblerendertarget(id2d1bitmaprendertarget)) verwenden können, um die gleichen Ergebnisse zu erzielen, ist das Rendern im Allgemeinen ein viel teurerer Vorgang als das Kopieren. Dies liegt daran, dass die Hardware zur Verbesserung der Cachelokalität keine Bitmap in derselben Speicherreihenfolge speichert, in der die Bitmap adressiert ist. Stattdessen kann die Bitmap swizzled sein. Der Swizzling wird entweder durch den Treiber (der langsam ist und nur in unteren Endteilen verwendet wird) oder durch den Speicher-Manager auf der GPU vor der CPU ausgeblendet. Aufgrund von Einschränkungen hinsichtlich der Art und Weise, wie Daten beim Rendern in ein Renderziel geschrieben werden, werden Renderziele in der Regel entweder nicht mit swizzled oder auf eine Weise wischt, die weniger optimal ist, als erreicht werden kann, wenn Sie wissen, dass Sie nie auf die Oberfläche rendern müssen. Daher werden die [CopyFrom-Methoden](/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap) \* zum Kopieren von Rechtecke aus einer Quelle in die Direct2D-Bitmap bereitgestellt.

CopyFrom kann in jeder seiner drei Formen verwendet werden:

-   [**CopyFromBitmap**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrombitmap)
-   [**CopyFromRenderTarget**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfromrendertarget)
-   [**CopyFromMemory**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmap-copyfrommemory)

## <a name="use-tiled-bitmap-over-dashing"></a>Verwenden von gekachelten Bitmaps über Bindestriche

Das Rendern einer gestrichelten Linie ist aufgrund der hohen Qualität und Genauigkeit des zugrunde liegenden Algorithmus ein sehr aufwendiger Vorgang. In den meisten Fällen, die keine relinearen Geometrien betreffen, kann der gleiche Effekt mithilfe von gekachelten Bitmaps schneller generiert werden.

## <a name="general-guidelines-for-rendering-complex-static-content"></a>Allgemeine Richtlinien zum Rendern komplexer statischer Inhalte

Zwischenspeichern von Inhalten, wenn Sie denselben Inhaltsrahmen über Frame rendern, insbesondere, wenn die Szene komplex ist.

Es gibt drei Methoden zum Zwischenspeichern, die Sie verwenden können:

-   Vollständige Szenenzwischenspeicherung mit einer Farbbitmap.
-   Pro primitivem Zwischenspeichern mit einer A8-Bitmap und der [**FillOpacityMask-Methode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f))
-   Zwischenspeicherung pro Grundtyp mit geometriebasierten Realisierungen.

Sehen wir uns die einzelnen Details genauer an.

### <a name="full-scene-caching-using-a-color-bitmap"></a>Vollständige Szenenzwischenspeicherung mit einer Farbbitmap

Erstellen Sie beim Rendern statischer Inhalte in Szenarien wie Animationen eine weitere Vollfarbbitmap, anstatt direkt in die Bildschirmbitmap zu schreiben. Speichern Sie das aktuelle Ziel, legen Sie das Ziel auf die Zwischenbitmap fest, und rendern Sie den statischen Inhalt. Wechseln Sie dann zurück zur ursprünglichen Bildschirmbitmap, und zeichnen Sie die Zwischenbitmap darauf.

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



In diesem Beispiel werden Zwischenbitmaps zum Zwischenspeichern verwendet und die Bitmap, auf die der Gerätekontext zeigt, beim Rendern umgeschaltet. Dadurch wird vermieden, dass ein kompatibles Renderziel für den gleichen Zweck erstellt werden muss.

### <a name="per-primitive-caching-using-an-a8-bitmap-and-the-fillopacitymask-method"></a>Pro primitivem Zwischenspeichern mit einer A8-Bitmap und der FillOpacityMask-Methode

Wenn die vollständige Szene nicht statisch ist, sondern aus Elementen wie Geometrie oder statischem Text besteht, können Sie eine methode pro primitivem Caching verwenden. Diese Technik behält die Antialiasingmerkmale des zwischengespeicherten Primitives bei und funktioniert mit sich ändernden Pinseltypen. Es wird eine A8-Bitmap verwendet, wobei A8 eine Art Pixelformat ist, das einen Alphakanal mit 8 Bits darstellt. A8-Bitmaps sind nützlich, um Geometrie/Text als Maske zu zeichnen. Wenn Sie die Deckkraft statischer Inhalte ändern müssen, anstatt den Inhalt selbst zu bearbeiten, können Sie die Deckkraft der Maske übersetzen, drehen, verzerren oder skalieren.

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



## <a name="per-primitive-caching-using-geometry-realizations"></a>Zwischenspeichern pro Primitiven mit geometriebasierten Realisierungen

Eine weitere Technik für die primitive Zwischenspeicherung, die als Geometrierealisierungen bezeichnet wird, bietet mehr Flexibilität beim Umgang mit Geometrie. Wenn Sie wiederholt Alias- oder Antialiasedgeometrien zeichnen möchten, ist es schneller, sie in Geometrierealisierungen zu konvertieren und die Realisierungen wiederholt zu zeichnen, als die Geometrien selbst wiederholt zu zeichnen. Geometrierealisierungen verbrauchen im Allgemeinen auch weniger Arbeitsspeicher als Deckkraftmasken (insbesondere bei großen Geometrien), und sie sind weniger empfindlich auf Skalierungsänderungen. Weitere Informationen finden Sie unter [Geometry Realizations Overview](geometry-realizations-overview.md).

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



## <a name="geometry-rendering"></a>Geometrierendering

### <a name="use-specific-draw-primitive-over-draw-geometry"></a>Verwenden eines bestimmten Primitiven zeichnen über zeichnende Geometrie

Verwenden Sie *spezifischere primitive* Draw-Aufrufe wie [**DrawRectangle**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawrectangle(constd2d1_rect_f__id2d1brush_float_id2d1strokestyle)) über generische [**DrawGeometry-Aufrufe.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawgeometry) Dies liegt daran, dass bei **DrawRectangle** die Geometrie bereits bekannt ist, sodass das Rendern schneller ist.

### <a name="rendering-static-geometry"></a>Rendern von statischer Geometrie

Verwenden Sie in Szenarien, in denen die Geometrie statisch ist, die oben beschriebenen Methoden für die primitive Zwischenspeicherung. Deckkraftmasken und Geometrierealisierungen können die Renderinggeschwindigkeit von Szenen, die statische Geometrie enthalten, erheblich verbessern.

### <a name="use-a-multithreaded-device-context"></a>Verwenden eines Multithreadgerätekontexts

Anwendungen, die große Mengen komplexer geometrischer Inhalte rendern möchten, sollten beim Erstellen eines [Direct2D-Gerätekontexts](./direct2d-portal.md) das Flag [**D2D1 \_ DEVICE CONTEXT OPTIONS ENABLE MULTI \_ \_ \_ \_ \_ THREADED \_ OPTIMIZATIONS**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_device_context_options) angeben. Wenn dieses Flag angegeben wird, verteilt Direct2D das Rendering auf alle logischen Kerne im System, was die Gesamtrenderingzeit erheblich verkürzen kann.

Hinweise:

-   Ab Windows 8.1 wirkt sich dieses Flag nur auf das Rendern der Pfadgeometrie aus. Sie hat keine Auswirkungen auf Szenen, die nur andere primitive Typen enthalten (z. B. Text, Bitmaps oder Geometrierealisierungen).
-   Dieses Flag hat auch keine Auswirkungen beim Rendern in Software (d. h. beim Rendern mit einem WARP Direct3D-Gerät). Zum Steuern des Multithreadings von Software sollten Aufrufer beim Erstellen des \_ \_ \_ \_ \_ \_ WARP Direct3D-Geräts das Flag D3D11 CREATE DEVICE PREVENT INTERNAL THREADING OPTIMIZATIONS verwenden.
-   Die Angabe dieses Flags kann den Spitzenarbeitssatz während des Renderings erhöhen und auch Threadinhalte in Anwendungen erhöhen, die bereits die Multithreadverarbeitung nutzen.

## <a name="drawing-text-with-direct2d"></a>Zeichnen von Text mit Direct2D

Direct2D-Textrenderingfunktionen werden in zwei Teilen angeboten. Der erste Teil, der als [**ID2D1RenderTarget::D rawText-**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) und [**ID2D1RenderTarget::D rawTextLayout-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) verfügbar gemacht wird, ermöglicht einem Aufrufer, entweder eine Zeichenfolge und Formatierungsparameter oder ein DWrite-Textlayoutobjekt für mehrere Formate zu übergeben. Dies sollte für die meisten Aufrufer geeignet sein. Die zweite Möglichkeit zum Rendern von Text, der als [**ID2D1RenderTarget::D rawGlyphRun-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawglyphrun) verfügbar gemacht wird, ermöglicht die Rasterung für Kunden, die die Position der zu renderenden Glyphen bereits kennen. Die folgenden beiden allgemeinen Regeln können helfen, die Textleistung beim Zeichnen in Direct2D zu verbessern.

### <a name="drawtextlayout-vs-drawtext"></a>DrawTextLayout im Vergleich zu DrawText

[**Sowohl DrawText**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtext(constwchar_uint32_idwritetextformat_constd2d1_rect_f__id2d1brush_d2d1_draw_text_options_dwrite_measuring_mode)) als auch [**DrawTextLayout**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout) ermöglichen einer Anwendung das einfache Rendern von Text, der von der [DirectWrite-API](/windows/desktop/DirectWrite/direct-write-portal) formatiert wird. **DrawTextLayout** zeichnet ein vorhandenes [**DWriteTextLayout-Objekt**](/windows/desktop/api/dwrite/nn-dwrite-idwritetextlayout) in [**renderTarget,**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)und **DrawText** erstellt basierend auf den übergebenen Parametern ein DirectWrite Layout für den Aufrufer. Wenn der gleiche Text mehrmals gerendert werden muss, verwenden **Sie DrawTextLayout** anstelle von **DrawText**, da **DrawText** bei jedem Aufruf ein Layout erstellt.

### <a name="choosing-the-right-text-rendering-mode"></a>Auswählen des richtigen Textrenderingmodus

Legen Sie den Text-Antialiasmodus explizit auf [**D2D1 \_ TEXT \_ ANTIALIAS \_ MODE \_ GRAYSCALE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_text_antialias_mode) fest. Die Qualität des Renderns von Graustufentext ist vergleichbar mit ClearType, ist aber viel schneller.

### <a name="caching"></a>Caching

Verwenden Sie die vollständige Szene oder das zwischenspeichern von primitiven Bitmaps wie beim Zeichnen anderer Primitive.

## <a name="clipping-an-arbitrary-shape"></a>Beschneiden einer beliebigen Form

Die folgende Abbildung zeigt das Ergebnis der Anwendung eines Clips auf ein Bild.

![Ein Bild, das ein Beispiel für ein Bild vor und nach einem Clip zeigt.](images/clip.png)

Sie können dieses Ergebnis erzielen, indem Sie Ebenen mit einer Geometriemaske oder die [**FillGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem Deckkraftpinsel verwenden.

Hier sehen Sie ein Beispiel, in dem eine Ebene verwendet wird:


```C++
// Call PushLayer() and pass in the clipping geometry.
m_d2dContext->PushLayer(
    D2D1::LayerParameters(
        boundsRect,
        geometricMask));
```



Hier sehen Sie ein Beispiel, in dem die [**FillGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) verwendet wird:


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



Wenn Sie in diesem Codebeispiel die PushLayer-Methode aufrufen, übergeben Sie keine von der App erstellte Ebene. Direct2D erstellt eine Ebene für Sie. Direct2D kann die Zuordnung und Zerstörung dieser Ressource ohne Beteiligung der App verwalten. Dadurch kann Direct2D Ebenen intern wiederverwenden und Ressourcenverwaltungsoptimierungen anwenden.

In Windows 8 wurden viele Optimierungen an der Verwendung von Ebenen vorgenommen, und es wird empfohlen, nach Möglichkeit zu versuchen, Ebenen-APIs anstelle von [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) zu verwenden.

### <a name="pushlayer-in-windows-8"></a>PushLayer in Windows 8

Die [**ID2D1DeviceContext-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) wird von der [**ID2D1RenderTarget-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) abgeleitet und ist der Schlüssel zum Anzeigen von Direct2D-Inhalten in Windows 8. Weitere Informationen zu dieser Schnittstelle finden Sie unter [Geräte- und Gerätekontexte.](devices-and-device-contexts.md) Mit der Gerätekontextschnittstelle können Sie den Aufruf der [**CreateLayer-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) überspringen und dann NULL an die [**ID2D1DeviceContext::P ushLayer-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) übergeben. Direct2D verwaltet die Ebenenressource automatisch und kann Ressourcen zwischen Ebenen und Effektdiagrammen freigeben.

### <a name="axis-aligned-clips"></a>An der Achse ausgerichtete Clips

Wenn der zu beschneidende Bereich an der Achse der Zeichnungsoberfläche ausgerichtet ist, anstatt an einer beliebigen. Dieser Fall eignet sich für die Verwendung eines Cliprechtecks anstelle einer Ebene. Die Leistungssteigerung ist bei Gealiasgeometrie höher als bei Geometrie mit Antialiasing. Weitere Informationen zu an der Achse ausgerichteten Clips finden Sie im [**Thema PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))

## <a name="dxgi-interoperability-avoid-frequent-switches"></a>DXGI-Interoperabilität: Vermeiden häufiger Switches

Direct2D kann nahtlos mit Direct3D-Oberflächen zusammenarbeiten. Dies ist sehr nützlich beim Erstellen von Anwendungen, die eine Mischung aus 2D- und 3D-Inhalt rendern. Jeder Wechsel zwischen dem Zeichnen von Direct2D- und Direct3D-Inhalten wirkt sich jedoch auf die Leistung aus.

Beim Rendern auf einer DXGI-Oberfläche speichert Direct2D den Zustand der Direct3D-Geräte während des Renderings und stellt ihn wieder auf, wenn das Rendering abgeschlossen ist. Jedes Mal, wenn ein Batch des Direct2D-Renderings abgeschlossen ist, werden die Kosten für diese Einsparungen und Wiederherstellungen und die Kosten für das Leeren aller 2D-Vorgänge bezahlt, und das Direct3D-Gerät wird noch nicht geleert. Um die Leistung zu erhöhen, beschränken Sie daher die Anzahl der Renderingwechsel zwischen Direct2D und Direct3D.

## <a name="know-your-pixel-format"></a>Kennen Des Pixelformats

Wenn Sie ein Renderziel erstellen, können Sie die [**D2D1 \_ PIXEL \_ FORMAT-Struktur**](/windows/desktop/api/dcommon/ns-dcommon-d2d1_pixel_format) verwenden, um das Pixelformat und den Alphamodus anzugeben, die vom Renderziel verwendet werden. Ein Alphakanal ist Teil des Pixelformats, das den Abdeckungswert oder die Deckkraftinformationen angibt. Wenn ein Renderziel den Alphakanal nicht verwendet, sollte es mit dem [**Alphamodus D2D1 \_ ALPHA MODE \_ \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode) erstellt werden. Dadurch wird die Zeit zum Rendern eines alphanumerten Kanals erspart, der nicht benötigt wird.

Weitere Informationen zu Pixelformaten und Alphamodi finden Sie unter [Unterstützte Pixelformate und Alphamodi.](supported-pixel-formats-and-alpha-modes.md)

## <a name="scene-complexity"></a>Komplexität der Szene

Wenn Sie leistungsorientierte Hotspots in einer Szene analysieren, die gerendert wird, kann das Wissen, ob die Szene Füllraten- oder Scheitelpunkt gebunden ist, nützliche Informationen liefern.

-   Füllrate: Die Füllrate bezieht sich auf die Anzahl von Pixeln, die eine Grafikkarte rendern und in den Videospeicher pro Sekunde schreiben kann.
-   Scheitelpunkt gebunden: Eine Szene ist vertexgebunden, wenn sie viele komplexe Geometrien enthält.

### <a name="understand-scene-complexity"></a>Verstehen der Komplexität von Szenen

Sie können die Komplexität Ihrer Szene analysieren, indem Sie die Größe des Renderziels ändern. Wenn Leistungssteigerungen für eine proportionale Verringerung der Größe des Renderziels sichtbar sind, ist die Anwendung an die Füllrate gebunden. Andernfalls ist die Komplexität der Szene der Leistungsengpass.

Wenn eine Szene mit einer Füllrate gebunden ist, kann eine Verringerung der Größe des Renderziels die Leistung verbessern. Dies liegt daran, dass die Anzahl der zu rendernden Pixel proportional zur Größe des Renderziels reduziert wird.

Wenn eine Szene scheitel gebunden ist, verringern Sie die Komplexität der Geometrie. Denken Sie jedoch daran, dass dies auf Kosten der Imagequalität erfolgt. Daher sollte eine sorgfältige Kompromissentscheidung zwischen der gewünschten Qualität und der erforderlichen Leistung getroffen werden.

## <a name="improving-performance-for-direct2d-printing-apps"></a>Verbessern der Leistung für Direct2D-Druck-Apps

[Direct2D bietet](./direct2d-portal.md) Kompatibilität mit dem Drucken. Sie können dieselben Direct2D-Zeichnungsbefehle (in Form von Direct2D-Befehlslisten) zum Drucken an das Direct2D-Drucksteuerelemente senden, wenn Sie nicht wissen, auf welche Geräte Sie zeichnen oder wie die Zeichnung in den Druck übersetzt wird.

Sie können die Verwendung des Direct2D-Drucksteuersteuerblatts und Ihrer [Direct2D-Zeichnungsbefehle](./direct2d-portal.md) weiter optimieren, um Druckergebnisse mit besserer Leistung zu liefern.

Das [Direct2D-Drucksteuer](./direct2d-portal.md) steuerelement gibt Debugmeldungen aus, wenn es ein Direct2D-Codemuster erkennt, das zu einer geringeren Druckqualität oder -leistung führt (z. B. code patterns listed later in this topic), um Sie daran zu erinnern, wo Sie Leistungsprobleme vermeiden können. Um diese Debugmeldungen anzeigen zu können, müssen Sie [die Direct2D-Debugebene](direct2ddebuglayer-portal.md) im Code aktivieren. Anweisungen [zum Aktivieren der Ausgabe](direct2ddebuglayer-debugmessages.md) von Debugnachrichten finden Sie unter Debugmeldungen.

### <a name="set-the-right-property-values-when-you-create-the-d2d-print-control"></a>Festlegen der richtigen Eigenschaftswerte beim Erstellen des D2D-Drucksteuer steuerelements

Es gibt drei Eigenschaften, die Sie beim Erstellen des [Direct2D-Drucksteuer steuerelements](./direct2d-portal.md) festlegen können. Zwei dieser Eigenschaften wirken sich auf die Art und Weise aus, wie das Direct2D-Drucksteuermodul bestimmte Direct2D-Befehle verarbeitet und sich wiederum auf die Gesamtleistung auswirken kann.

-   Schriftteilmengenmodus: Das Direct2D-Drucksteuersteuerteilmengen-Steuerelement verwendet schriftartenressourcen, die auf jeder Seite verwendet werden, bevor die zu druckende Seite versendet wird. [](./direct2d-portal.md) Dieser Modus reduziert die Größe der Seitenressourcen, die zum Drucken benötigt werden. Abhängig von der Schriftartverwendung auf der Seite können Sie verschiedene Schriftartteilmengenmodi auswählen, um die beste Leistung zu erzielen.
    -   [**D2D1 \_ PRINT \_ FONT SUBSET MODE \_ \_ \_ DEFAULT**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) bietet in den meisten Fällen die beste Druckleistung. Wenn dieses Steuerelement auf diesen Modus festgelegt ist, verwendet das [Direct2D-Drucksteuersystem](./direct2d-portal.md) eine heuristische Strategie, um zu entscheiden, wann Schriftarten als Teilmenge verwendet werden.
    -   Für kurze Druckaufträge mit 1 oder 2 Seiten empfehlen wir [**D2D1 \_ PRINT FONT SUBSET MODE \_ \_ \_ \_ EACHPAGE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode) , wobei das Direct2D-Drucksteuersteuerteilmengen und -ressourcen auf jeder Seite einbettet und diese Schriftartteilmenge dann verwirft, nachdem die Seite gedruckt wurde. [](./direct2d-portal.md) Mit dieser Option wird sichergestellt, dass jede Seite direkt nach ihrer Generiert gedruckt werden kann, aber die Größe der für das Drucken benötigten Seitenressourcen (mit in der Regel großen Teilmengen von Schriftarten) leicht erhöht wird.
    -   Für Druckaufträge mit vielen Seiten mit Texten und kleinen Schriftgraden (z. B. 100 Seiten text, die eine einzelne Schriftart verwenden) empfehlen wir [**D2D1 \_ PRINT FONT SUBSET MODE \_ \_ \_ \_ NONE**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_print_font_subset_mode), wobei das [Direct2D-Drucksteuerfeld](./direct2d-portal.md) überhaupt keine Schriftartressourcen unterteilt. Stattdessen sendet es die ursprünglichen Schriftartressourcen zusammen mit der Seite, die zuerst die Schriftart verwendet, und verwendet die Schriftartressourcen für spätere Seiten erneut, ohne sie erneut zu senden.
-   Rasterungs-DPI: Wenn das [Direct2D-Drucksteuer](./direct2d-portal.md) steuerelement Direct2D-Befehle während der Direct2D-XPS-Konvertierung rastern muss, verwendet es diesen DPI für die Rasterung. Anders ausgedrückt: Wenn die Seite keine rasterisierten Inhalte enthält, ändert das Festlegen eines DPI-Werts die Leistung und Qualität nicht. Je nach Rasterungsverwendung auf der Seite können Sie verschiedene Rasterungs-DPIs auswählen, um das beste Gleichgewicht zwischen Genauigkeit und Leistung zu erzielen.
    -   150 ist der Standardwert, wenn Sie beim Erstellen des [Direct2D-Drucksteuer](./direct2d-portal.md) steuerelements keinen Wert angeben. Dies ist in den meisten Fällen die beste Balance zwischen Druckqualität und Druckleistung.
    -   Höhere DPI-Werte führen in der Regel zu einer besseren Druckqualität (wie in mehr Details beibehalten), aber eine geringere Leistung aufgrund der größeren Bitmaps, die sie generiert. Es wird kein DPI-Wert von mehr als 300 empfohlen, da dies keine zusätzlichen Informationen enthält, die für menschliche Augen visuell sichtbar sind.
    -   Ein niedrigerer DPI-Wert kann zu einer besseren Leistung führen, aber auch zu einer niedrigeren Qualität führen.

### <a name="avoid-using-certain-direct2d-drawing-patterns"></a>Vermeiden der Verwendung bestimmter Direct2D-Zeichnungsmuster

Es gibt Unterschiede zwischen [dem, was Direct2D](./direct2d-portal.md) visuell darstellen kann, und dem, was das Drucksubsystem während der gesamten Druckpipeline verwalten und transporten kann. Das Direct2D-Drucksteuersystem überbrückt diese Lücken, indem es direct2D-Primitive, die vom Drucksubsystem nicht nativ unterstützt werden, entweder anfügst oder rastert. Eine solche Näherung führt in der Regel zu geringerer Druckgenauigkeit, geringerer Druckleistung oder beidem. Obwohl ein Kunde dieselben Zeichnungsmuster sowohl für das Bildschirm- als auch für das Druckrendering verwenden kann, ist es daher nicht in allen Fällen ideal. Es ist am besten, solche Direct2D-Primitive und -Muster nicht so weit wie möglich für den Druckpfad zu verwenden oder eine eigene Rasterung zu verwenden, bei der Sie die vollständige Kontrolle über die Qualität und Größe der rasterisierten Bilder haben.

Im Folgenden finden Sie eine Liste der Fälle, in denen die Druckleistung und -qualität nicht ideal ist und Sie erwägen sollten, den Codepfad für eine optimale Druckleistung zu variieren.

-   Vermeiden Sie es, einen anderen primitiven Überblendmodus [**als D2D1 \_ PRIMITIVE BLEND \_ \_ SOURCEOVER zu verwenden.**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend)
-   Vermeiden Sie die Verwendung von Kompositionsmodi, wenn Sie ein anderes Bild als [**D2D1 \_ COMPOSITE MODE SOURCE \_ \_ \_ OVER**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_composite_mode) und **D2D1 \_ COMPOSITE MODE DESTINATION OVER \_ \_ \_ zeichnen.**
-   Vermeiden Sie das Zeichnen einer GDI-Metadatei.
-   Vermeiden Sie das Pushen einer Ebenenressource, die den Quellhintergrund kopiert (Aufrufen von [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-pushlayer) mit Übergabe von [**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE FROM \_ \_ BACKGROUND**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) an die **Struktur D2D1 \_ LAYER \_ PARAMETERS1).**
-   Vermeiden Sie das Erstellen eines Bitmappinsels oder Bildpinsels mit D2D1 \_ EXTEND \_ MODE \_ CLAMP. Es wird empfohlen, D2D1 EXTEND MODE MIRROR zu verwenden, wenn Pixel außerhalb des Bilds überhaupt nicht wichtig sind (z. B. ist bekannt, dass das an den Pinsel angefügte Bild größer als der ausgefüllte Zielbereich \_ \_ \_ ist).
-   Vermeiden Sie das Zeichnen von Bitmaps mit [Perspektiventransformationen.](3d-perspective-transform.md)

### <a name="draw-text-in-a-direct-and-plain-way"></a>Direktes und einfaches Zeichnen von Text

Direct2D verfügt über mehrere Optimierungen beim Rendern von Texten, um eine bessere Leistung und/oder bessere visuelle Qualität zu erzielen. Aber nicht alle Optimierungen verbessern die Druckleistung und -qualität, da sich der Druck auf Papier in der Regel in einem viel höheren DPI-Wert befindet und der Druck keine Szenarien wie Animationen aufnehmen muss. Daher wird empfohlen, den ursprünglichen Text oder die Glyphen direkt zu zeichnen und beim Erstellen der Befehlsliste für das Drucken die folgenden Optimierungen zu vermeiden.

-   Vermeiden Sie das Zeichnen von Text mit der [**FillOpacityMask-Methode.**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1commandsink-fillopacitymask)
-   Vermeiden Sie das Zeichnen von Text im Aliasmodus.

### <a name="draw-the-original-bitmaps-when-possible"></a>Zeichnen der ursprünglichen Bitmaps nach Möglichkeit

Wenn es sich bei der Zielbitmap um eine JPEG-, PNG-, TIFF- oder JPEG-XR-Bitmap handelt, können Sie eine WIC-Bitmap entweder aus einer Datenträgerdatei oder aus einem In-Memory-Stream erstellen und dann mithilfe von [**ID2D1DeviceContext::CreateBitmapFromWicBitmap**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createbitmapfromwicbitmap(iwicbitmapsource_constd2d1_bitmap_properties1_id2d1bitmap1))eine Direct2D-Bitmap aus dieser WIC-Bitmap erstellen und schließlich diese [Direct2D-Bitmap](./direct2d-portal.md) ohne weitere Bearbeitung direkt an das Direct2D-Drucksteuergerät übergeben. Dadurch kann das Direct2D-Drucksteuerelemente den Bitmapstream wiederverwenden. Dies führt in der Regel zu einer besseren Druckleistung (durch Überspringen redundanter Bitmapcodierung und -decodierung) und einer besseren Druckqualität (wenn Metadaten wie Farbprofile in der Bitmap beibehalten werden).

Das Zeichnen der ursprünglichen Bitmap bietet den folgenden Vorteil für Anwendungen.

-   Im Allgemeinen behält [der Direct2D-Druck](./direct2d-portal.md) die ursprünglichen Informationen (ohne Verlust oder Rauschen) bis spät in der Pipeline bei, insbesondere, wenn Apps die Details der Druckpipeline nicht kennen (oder nicht wissen möchten) (z. B. den Drucker, auf den er druckt, welcher DPI-Drucker der Zieldrucker ist, und so weiter).
-   In vielen Fällen bedeutet das Verzögern der Bitmap-Rasterung eine bessere Leistung (z. B. beim Drucken eines 96dpi-Fotos auf einen 600dpi-Drucker).
-   In bestimmten Fällen ist die Übergabe der originalen Bilder die einzige Möglichkeit, die Hohe Genauigkeit zu verwenden (z. B. eingebettete Farbprofile).

Eine solche Optimierung kann jedoch nicht verwendet werden, da:

-   Durch Abfragen von Druckerinformationen und frühzeitiger Rasterung können Sie Inhalte selbst mit vollständiger Kontrolle über die endgültige Darstellung auf Papier rastern.
-   In bestimmten Fällen kann die frühe Rasterung tatsächlich die End-to-End-Leistung einer App verbessern (z. B. das Drucken von Fotos in Walletsgröße).
-   In bestimmten Fällen erfordert die Übergabe der ursprünglichen Bitmaps eine erhebliche Änderung der vorhandenen Codearchitektur (z. B. das verzögerte Laden von Bildern und Ressourcenaktualisierungspfade in bestimmten Anwendungen).

## <a name="conclusion"></a>Zusammenfassung

Obwohl Direct2D hardwarebeschleunigt ist und für hohe Leistung bestimmt ist, müssen Sie die Features ordnungsgemäß verwenden, um den Durchsatz zu maximieren. Die hier beschriebenen Techniken stammen aus der Untersuchung gängiger Szenarien und gelten möglicherweise nicht für alle Anwendungsszenarien.

 

 
