---
title: Übersicht über Ebenen
description: Beschreibt die Grundlagen von Direct2D-Ebenen.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: ac68ba25d1e8f35c5a41daec4d7a5295235a5d98
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549185"
---
# <a name="layers-overview"></a>Übersicht über Ebenen

In dieser Übersicht werden die Grundlagen der Verwendung von Direct2D-Ebenen beschrieben. Der Abschnitt ist wie folgt gegliedert.

-   [Was sind Ebenen?](#what-are-layers)
-   [Ebenen in Windows 8 und höher](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceContext und PushLayer](#id2d1devicecontext-and-pushlayer)
    -   [D2D1 \_ LAYER \_ PARAMETERS1 und D2D1 \_ LAYER \_ OPTIONS1](/windows)
    -   [Füllmethoden](#blend-modes)
    -   [Interoperation](#interoperation)
-   [Erstellen von Ebenen](#creating-layers)
-   [Inhaltsgrenze](#content-bounds)
-   [Geometrische Masken](#geometric-masks)
-   [Deckkraftmasken](#opacity-masks)
-   [Alternativen zu Ebenen](#alternatives-to-layers)
-   [Beschneiden einer beliebigen Form](#clipping-an-arbitrary-shape)
    -   [An der Achse ausgerichtete Clips](#axis-aligned-clips)
-   [Verwandte Themen](#related-topics)

## <a name="what-are-layers"></a>Was sind Ebenen?

Ebenen, die durch [**ID2D1Layer-Objekte dargestellt**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) werden, ermöglichen es einer Anwendung, eine Gruppe von Zeichnungsvorgängen zu bearbeiten. Sie verwenden eine Ebene, indem Sie sie auf ein Renderziel "pushen". Nachfolgende Zeichnungsvorgänge durch das Renderziel werden an die Ebene weitergeleitet. Nachdem Sie mit der Ebene fertig sind, "popen" Sie die Ebene vom Renderziel, wodurch der Inhalt der Ebene wieder mit dem Renderziel zusammengesetzt wird.

Wie Pinsel sind Ebenen geräteabhängige Ressourcen, die von Renderzielen erstellt werden. Ebenen können auf jedem Renderziel in derselben Ressourcendomäne verwendet werden, die das Renderziel enthält, das es erstellt hat. Eine Ebenenressource kann jedoch jeweils nur von einem Renderziel verwendet werden. Weitere Informationen zu Ressourcen finden Sie in der [Ressourcenübersicht.](resources-and-resource-domains.md)

Obwohl Ebenen ein leistungsstarkes Renderingverfahren zum Erzeugen interessanter Effekte bieten, kann eine übermäßige Anzahl von Ebenen in einer Anwendung aufgrund der verschiedenen Kosten für die Verwaltung von Ebenen und Ebenenressourcen die Leistung beeinträchtigen. Beispielsweise entstehen die Kosten für das Auffüllen oder Löschen der Schicht und das anschließende Zusammensetzen, insbesondere bei höherer Hardware. Dann entstehen die Kosten für die Verwaltung der Ebenenressourcen. Wenn Sie diese häufig neu verteilen, sind die resultierenden Ausfälle bei der GPU das wichtigste Problem. Wenn Sie Ihre Anwendung entwerfen, versuchen Sie, die Wiederverwendung von Ebenenressourcen zu maximieren.

## <a name="layers-in-windows-8-and-later"></a>Ebenen in Windows 8 und höher

Windows 8 wurden neue ebenenbezogene APIs eingeführt, die ebenenbezogene APIs vereinfachen, die Leistung von verbessern und Ebenen Features hinzufügen.

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceContext und PushLayer

Die [**ID2D1DeviceContext-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) wird von der [**ID2D1RenderTarget-Schnittstelle**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) abgeleitet und ist der Schlüssel zum Anzeigen von Direct2D-Inhalten in Windows 8. Weitere Informationen zu dieser Schnittstelle finden Sie unter [Geräte- und Gerätekontexte.](devices-and-device-contexts.md) Mit der Gerätekontextschnittstelle können Sie den Aufruf der [**CreateLayer-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) überspringen und dann NULL an die [**ID2D1DeviceContext::P ushLayer-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) übergeben. Direct2D verwaltet die Ebenenressource automatisch und kann Ressourcen zwischen Ebenen und Effektdiagrammen freigeben.

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>D2D1 \_ LAYER \_ PARAMETERS1 und D2D1 \_ LAYER \_ OPTIONS1

Die [**D2D1 \_ LAYER \_ PARAMETERS1-Struktur**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) ist mit der [**D2D1 \_ LAYER \_ PARAMETERS-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters)identisch, mit der Ausnahme, dass der letzte Member der -Struktur jetzt eine [**D2D1 \_ LAYER \_ OPTIONS1-Enumeration**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) ist.

[**D2D1 \_ LAYER \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) hat keine ClearType-Option und verfügt über zwei verschiedene Optionen, mit denen Sie die Leistung verbessern können:

-   [**D2D1 \_ LAYER \_ OPTIONS1 \_ INITIALIZE \_ FROM \_ BACKGROUND**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D rendert Primitive auf der Ebene, ohne sie mit transparentem Schwarz zu löschen. Dies ist nicht die Standardeinstellung, führt aber in den meisten Fällen zu einer besseren Leistung.

-   [**D2D1 \_ LAYER \_ OPTIONS1 \_ IGNORE \_ ALPHA**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Wenn die zugrunde liegende Oberfläche auf [**D2D1 \_ ALPHA MODE \_ \_ IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)festgelegt ist, kann Direct2D mit dieser Option verhindern, dass der Alphakanal der Ebene geändert wird. Verwenden Sie dies in anderen Fällen nicht.

### <a name="blend-modes"></a>Füllmethoden

Ab Windows 8 verfügt der Gerätekontext über einen [**primitiven Mischungsmodus,**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) der bestimmt, wie die einzelnen Primitiven mit der Zieloberfläche kombiniert werden. Dieser Modus gilt auch für Ebenen, wenn Sie die [**PushLayer-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) aufrufen.

Wenn Sie beispielsweise eine Ebene zum Beschneiden von Primitiven mit Transparenz verwenden, legen Sie den [**D2D1 \_ PRIMITIVE \_ BLEND \_ COPY-Modus**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) für den Gerätekontext fest, um die richtigen Ergebnisse zu erzielen. Der Kopiermodus bewirkt, dass der Gerätekontext linear alle vier Farbkanäle, einschließlich des Alphakanals, jedes Pixels mit dem Inhalt der Zieloberfläche gemäß der geometrischen Maske der Ebene interpoliert.

### <a name="interoperation"></a>Interoperation

Ab Windows 8 unterstützt Direct2D die Interoperation mit Direct3D und GDI, während eine Ebene oder ein Clip gepusht wird. Sie rufen [**ID2D1GdiInteropRenderTarget::GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) auf, während eine Ebene zur Interoperabilität mit GDI gepusht wird. Sie rufen [**ID2D1DeviceContext::Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) auf und rendern dann auf der zugrunde liegenden Oberfläche, um mit Direct3D zu zusammenarbeiten. Es liegt in Ihrer Verantwortung, innerhalb der Ebene oder des Clips mit Direct3D oder GDI zu rendern. Wenn Sie versuchen, außerhalb der Ebene zu rendern oder die Ergebnisse zu beschneiden, sind die Ergebnisse nicht definiert.

## <a name="creating-layers"></a>Erstellen von Ebenen

Das Arbeiten mit Ebenen erfordert Vertrautheit mit den [**Methoden CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))und [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) und der [**Struktur D2D1 \_ LAYER \_ PARAMETERS,**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) die eine Reihe von parametrischen Daten enthält, die definieren, wie die Ebene verwendet werden kann. In der folgenden Liste werden die Methoden und die Struktur beschrieben.

-   Rufen Sie die [**CreateLayer-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) auf, um eine Ebenenressource zu erstellen.
    > [!Note]  
    > Ab Windows 8 können Sie das Aufrufen der [**CreateLayer-Methode**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) überspringen und dann NULL an die [**PushLayer-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) auf der [**ID2D1DeviceContext-Schnittstelle**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) übergeben. Dies ist einfacher und ermöglicht Direct2D die automatische Verwaltung der Ebenenressource und die gemeinsame Nutzung von Ressourcen zwischen Ebenen und Effektdiagrammen.

     

-   Nachdem das Zeichnen des Renderziels begonnen hat (nachdem die [**BeginDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) aufgerufen wurde), können Sie die [**PushLayer-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) verwenden. Die **PushLayer-Methode** fügt dem Renderziel die angegebene Ebene hinzu, sodass das Ziel alle nachfolgenden Zeichnungsvorgänge empfängt, bis [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird. Diese Methode verwendet ein [**ID2D1Layer-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) das durch Aufrufen von [**CreateLayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) zurückgegeben wird, und *ein layerParameters-Objekt* in der [**D2D1 \_ LAYER \_ PARAMETERS-Struktur.**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) In der folgenden Tabelle werden die Felder der -Struktur beschrieben. 

    | Feld                 | Beschreibung|
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | **contentBounds**     | Die Inhaltsgrenze der Ebene. Inhalte außerhalb dieser Grenzen werden garantiert nicht gerendert. Dieser Parameter ist standardmäßig auf [**InfiniteRect festgelegt.**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect) Wenn der Standardwert verwendet wird, werden die Inhaltsgrenze effektiv als Begrenzungen des Renderziels verwendet. |
    | **geometricMask**     | (Optional) Der bereich, der durch eine [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)definiert wird, auf den die Ebene abgeschnitten werden soll. Wird auf **NULL** festgelegt, wenn die Ebene nicht auf eine Geometrie abgeschnitten werden soll. |
    | **maskAntialiasMode** | Ein -Wert, der den Antialiasingmodus für die geometrische Maske angibt, die vom **geometrischen Maskenfeld** angegeben wird. |
    | **maskTransform**     | Ein -Wert, der die Transformation angibt, die beim Erstellen der Ebene auf die geometrische Maske angewendet wird. Dies ist relativ zur Welttransformation.  |
    | **Deckkraft**           | Der Deckkraftwert der Ebene. Die Deckkraft jeder Ressource in der Ebene wird beim Zusammenschalten zum Ziel mit diesem Wert multipliziert.  |
    | **opacityBrush**      | (Optional) Ein Pinsel, der verwendet wird, um die Deckkraft der Ebene zu ändern. Der Pinsel wird der Ebene zugeordnet, und der Alphakanal jedes zugeordneten Pinselpixels wird mit dem entsprechenden Ebenenpixel multipliziert. Legen Sie auf **NULL** fest, wenn die Ebene keine Deckkraftmaske aufweisen soll.   |
    | **layerOptions**      | Ein -Wert, der angibt, ob die Ebene Text mit ClearType-Antialiasing rendern soll. Dieser Parameter ist standardmäßig deaktiviert. Wenn Sie es aktivieren, funktioniert ClearType ordnungsgemäß, führt jedoch zu einer etwas langsameren Renderinggeschwindigkeit.    |

    

     

    > [!Note]  
    > Ab Windows 8 können Sie nicht mit ClearType in einer Ebene rendern. Daher sollte der **layerOptions-Parameter** immer auf [**D2D1 LAYER OPTIONS NONE festgelegt \_ \_ \_ werden.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options)

     

    Der Einfachheit halber stellt Direct2D die [**D2D1::LayerParameters-Methode**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) bereit, um Sie beim Erstellen von [**D2D1 \_ LAYER \_ PARAMETERS-Strukturen**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) zu unterstützen.

-   Rufen Sie die [**PopLayer-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) auf, um den Inhalt der Ebene in das Renderziel zu zusammengesetzt. Sie müssen die **PopLayer-Methode** aufrufen, bevor Sie die [**EndDraw-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufrufen.

Das folgende Beispiel zeigt, wie [**CreateLayer,**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) [**PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))und PopLayer verwendet [**werden.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) Alle Felder in der [**Struktur D2D1 \_ LAYER \_ PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) werden auf ihre Standardwerte festgelegt, mit Ausnahme **von opacityBrush**, das auf [**id2D1RadialGradientBrush festgelegt ist.**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)


```C++
// Create a layer.
ID2D1Layer *pLayer = NULL;
hr = pRT->CreateLayer(NULL, &pLayer);

if (SUCCEEDED(hr))
{
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

    // Push the layer with the content bounds.
    pRT->PushLayer(
        D2D1::LayerParameters(
            D2D1::InfiniteRect(),
            NULL,
            D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
            D2D1::IdentityMatrix(),
            1.0,
            m_pRadialGradientBrush,
            D2D1_LAYER_OPTIONS_NONE),
        pLayer
        );

    pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

    pRT->FillRectangle(
        D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
        m_pSolidColorBrush
        );
    pRT->FillRectangle(
        D2D1::RectF(50.f, 50.f, 75.f, 75.f),
        m_pSolidColorBrush
        ); 
    pRT->FillRectangle(
        D2D1::RectF(75.f, 75.f, 100.f, 100.f),
        m_pSolidColorBrush
        );    
 
    pRT->PopLayer();
}
SafeRelease(&pLayer);
```



Code wurde in diesem Beispiel ausgelassen.

Beachten Sie, dass beim Aufrufen [**von PushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) und [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)sichergestellt ist, dass **jedes PushLayer-Paar** über einen entsprechenden **PopLayer-Aufruf** verfügt. Wenn es mehr **PopLayer-Aufrufe** als **PushLayer-Aufrufe** gibt, wird das Renderziel in einen Fehlerzustand gesetzt. Wenn [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) aufgerufen wird, bevor alle ausstehenden Ebenen aus dem Pop aufgeblendet werden, wird das Renderziel in einen Fehlerzustand gesetzt und gibt einen Fehler zurück. Um den Fehlerzustand zu löschen, verwenden [**Sie EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw).

## <a name="content-bounds"></a>Inhaltsgrenze

**ContentBounds legt** den Grenzwert für das, was auf die Ebene gezeichnet werden soll, fest. Nur die Dinge innerhalb der Inhaltsgrenze werden wieder mit dem Renderziel zusammengesetzt.

Das folgende Beispiel zeigt, wie **contentBounds** angegeben wird, damit das ursprüngliche Bild an die Inhaltsgrenze mit der oberen linken Ecke bei (10, 108) und der unteren rechten Ecke bei (121, 177) abgeschnitten wird. Die folgende Abbildung zeigt das ursprüngliche Bild und das Ergebnis der Beschneidung des Bilds an die Inhaltsgrenze.

![Abbildung der Inhaltsgrenze eines originalen Bilds und des resultierenden abgeschnittenen Bilds](images/layers-contentbounds.png)


```C++
HRESULT DemoApp::RenderWithLayerWithContentBounds(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 0));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::RectF(10, 108, 121, 177)),
            pLayer
            );

        pRT->DrawBitmap(m_pWaterBitmap, D2D1::RectF(0, 0, 128, 192));
        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



Code wurde in diesem Beispiel ausgelassen.

> [!Note]
>
> Das resultierende abgeschnittene Bild wird weiter beeinflusst, wenn Sie eine **geometricMask angeben.** Weitere Informationen [finden Sie im](#geometric-masks) Abschnitt Geometrische Masken.

 

## <a name="geometric-masks"></a>Geometrische Masken

Eine geometrische Maske ist ein Clip oder ein Cutout, definiert durch ein [**ID2D1Geometry-Objekt,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) das eine Ebene maskiert, wenn sie von einem Renderziel gezeichnet wird. Sie können das **feld geometricMask** der [**D2D1 \_ LAYER \_ PARAMETERS-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) verwenden, um die Ergebnisse in einer Geometrie zu maskieren. Wenn Sie beispielsweise ein Bild anzeigen möchten, das durch einen Blockbuchstaben "A" maskiert ist, können Sie zunächst eine Geometrie erstellen, die den Blockbuchstaben "A" darstellt, und diese Geometrie als geometrische Maske für eine Ebene verwenden. Nachdem Sie die Ebene gedrückt haben, können Sie das Bild zeichnen. Wenn Die Ebene per Pop abgeschnitten wird, wird das Bild auf die Form "A" des Blockbuchstabens abgeschnitten.

Das folgende Beispiel zeigt, wie Sie eine [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) erstellen, die eine Form eines Mountain enthält, und dann die Pfadgeometrie an [**pushLayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))übergeben. Anschließend zeichnet er eine Bitmap und Quadrate. Wenn nur eine Bitmap in der Ebene zum Rendern vorhanden ist, verwenden Sie [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem klammerten Bitmappinsel zur Effizienz. Die folgende Abbildung zeigt die Ausgabe des Beispiels.

![Abbildung eines Bilds eines Blatts und des resultierenden Bilds, nachdem eine geometrische Maske eines Mountain angewendet wurde](images/layers-bitmapmask.png)

Im ersten Beispiel wird die Geometrie definiert, die als Maske verwendet werden soll.


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pPathGeometry);
    
if(SUCCEEDED(hr))
{
    ID2D1GeometrySink *pSink = NULL;
    // Write to the path geometry using the geometry sink.
    hr = m_pPathGeometry->Open(&pSink);

    if (SUCCEEDED(hr))
    {
        pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
        pSink->BeginFigure(
            D2D1::Point2F(0, 90),
            D2D1_FIGURE_BEGIN_FILLED
            );

        D2D1_POINT_2F points[7] = {
           D2D1::Point2F(35, 30),
           D2D1::Point2F(50, 50),
           D2D1::Point2F(70, 45),
           D2D1::Point2F(105, 90),
           D2D1::Point2F(130, 90),
           D2D1::Point2F(150, 60),
           D2D1::Point2F(170, 90)
           };

        pSink->AddLines(points, 7);
        pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
        hr = pSink->Close();
    }
    SafeRelease(&pSink);
       }
```



Im nächsten Beispiel wird die Geometrie als Maske für die Ebene verwendet.


```C++
HRESULT DemoApp::RenderWithLayerWithGeometricMask(ID2D1RenderTarget *pRT)
{
    
    HRESULT hr;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 450));

        pRT->PushLayer(
            D2D1::LayerParameters(D2D1::InfiniteRect(), m_pPathGeometry),
            pLayer
            );

        pRT->DrawBitmap(m_pLeafBitmap, D2D1::RectF(0, 0, 198, 132));

        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f), 
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );        

        pRT->PopLayer();
    }

    SafeRelease(&pLayer);

    return hr;
    
}
```



In diesem Beispiel wurde Code ausgelassen.

> [!Note]
>
> Wenn Sie eine **geometrischeMaske** angeben, können Sie im Allgemeinen den Standardwert [**InfiniteRect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)für **contentBounds** verwenden.
>
> Wenn **contentBounds** NULL und **geometricMask** ungleich NULL ist, sind die Inhaltsgrenzen effektiv die Grenzen der geometrischen Maske, nachdem die Maskentransformation angewendet wurde.
>
> Wenn **contentBounds** ungleich NULL und **geometricMask** ungleich NULL ist, wird die transformierte geometrische Maske effektiv an Inhaltsgrenzen abgeschnitten, und es wird davon ausgegangen, dass die Inhaltsgrenzen unendlich sind.

 

## <a name="opacity-masks"></a>Deckkraftmasken

Eine Deckkraftmaske ist eine Maske, die von einem Pinsel oder einer Bitmap beschrieben wird und auf ein anderes Objekt angewendet wird, um dieses Objekt teilweise oder vollständig transparent zu machen. Sie ermöglicht die Verwendung des Alphakanals eines Pinsels als Inhaltsmaske. Beispielsweise können Sie einen radialen Farbverlaufspinsel definieren, der von deckend zu transparent variiert, um einen Effekt zu erzeugen.

Im folgenden Beispiel wird ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pRadialGradientBrush*) als Deckkraftmaske verwendet. Anschließend werden eine Bitmap und Quadrate ge zeichnet. Wenn nur eine Bitmap in der Ebene gerendert werden soll, verwenden Sie [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem geklammerten Bitmappinsel, um die Effizienz zu erhöhen. Die folgende Abbildung zeigt die Ausgabe dieses Beispiels.

![Abbildung eines Bilds von Strukturen und des resultierenden Bilds, nachdem eine Deckkraftmaske angewendet wurde](images/layers-opacitymask.png)


```C++
HRESULT DemoApp::RenderWithLayerWithOpacityMask(ID2D1RenderTarget *pRT)
{   

    HRESULT hr = S_OK;

    // Create a layer.
    ID2D1Layer *pLayer = NULL;
    hr = pRT->CreateLayer(NULL, &pLayer);

    if (SUCCEEDED(hr))
    {
        pRT->SetTransform(D2D1::Matrix3x2F::Translation(300, 250));

        // Push the layer with the content bounds.
        pRT->PushLayer(
            D2D1::LayerParameters(
                D2D1::InfiniteRect(),
                NULL,
                D2D1_ANTIALIAS_MODE_PER_PRIMITIVE,
                D2D1::IdentityMatrix(),
                1.0,
                m_pRadialGradientBrush,
                D2D1_LAYER_OPTIONS_NONE),
            pLayer
            );

        pRT->DrawBitmap(m_pBambooBitmap, D2D1::RectF(0, 0, 190, 127));

        pRT->FillRectangle(
            D2D1::RectF(25.f, 25.f, 50.f, 50.f), 
            m_pSolidColorBrush
            );
        pRT->FillRectangle(
            D2D1::RectF(50.f, 50.f, 75.f, 75.f),
            m_pSolidColorBrush
            ); 
        pRT->FillRectangle(
            D2D1::RectF(75.f, 75.f, 100.f, 100.f),
            m_pSolidColorBrush
            );    
 
        pRT->PopLayer();
    }
    SafeRelease(&pLayer);
   
    return hr;
    
}
```



Code wurde in diesem Beispiel ausgelassen.

> [!Note]  
> In diesem Beispiel wird eine Ebene verwendet, um eine Deckkraftmaske auf ein einzelnes Objekt anzuwenden, um das Beispiel so einfach wie möglich zu halten. Beim Anwenden einer Deckkraftmaske auf ein einzelnes Objekt ist es effizienter, die [**FillOpacityMask-**](id2d1rendertarget-fillopacitymask.md) oder [**FillGeometry-Methoden**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) anstelle einer Ebene zu verwenden.

 

Anweisungen zum Anwenden einer Deckkraftmaske ohne Verwendung einer Ebene finden Sie in der Übersicht über [Deckkraftmasken.](opacity-masks-overview.md)

## <a name="alternatives-to-layers"></a>Alternativen zu Ebenen

Wie bereits erwähnt, kann sich eine übermäßige Anzahl von Ebenen negativ auf die Leistung Ihrer Anwendung auswirken. Um die Leistung zu verbessern, vermeiden Sie die Verwendung von Ebenen, wann immer dies möglich ist. verwenden Sie stattdessen ihre Alternativen. Das folgende Codebeispiel zeigt, wie [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) und [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) verwendet werden, um einen Bereich zu beschneiden, als Alternative zur Verwendung einer Ebene mit Inhaltsgrenze.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



Verwenden Sie auf ähnliche Weise [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem geklammerten Bitmappinsel als Alternative zur Verwendung einer Ebene mit einer Deckkraftmaske, wenn nur ein Inhalt in der Ebene gerendert werden soll, wie im folgenden Beispiel gezeigt.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



Als Alternative zur Verwendung einer Ebene mit einer geometrischen Maske sollten Sie eine Bitmapmaske verwenden, um einen Bereich zu beschneiden, wie im folgenden Beispiel gezeigt.


```C++
// D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask
// to function properly.
m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);

m_pRenderTarget->FillOpacityMask(
    m_pBitmapMask,
    m_pOriginalBitmapBrush,
    D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
    &rcBrushRect,
    NULL
    );

m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);

```



Wenn Sie die Deckkraft auf ein einzelnes Primitiv anwenden möchten, sollten Sie schließlich die Deckkraft in die Pinselfarbe multiplizieren und dann den Primitiv rendern. Sie benötigen keine Ebenen- oder Deckkraftmaskenbitmap.


```C++
float opacity = 0.9f;

ID2D1SolidColorBrush *pBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f * opacity)),
    &pBrush
    );

m_pRenderTarget->FillRectangle(
    D2D1::RectF(50.0f, 50.0f, 75.0f, 75.0f), 
    pBrush
    ); 
```



## <a name="clipping-an-arbitrary-shape"></a>Beschneiden einer beliebigen Form

Die Abbildung zeigt das Ergebnis der Anwendung eines Clips auf ein Bild.

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

> [!Note]  
> In Windows 8 wurden viele Optimierungen an der Verwendung von Ebenen vorgenommen, und es wird empfohlen, nach Möglichkeit die Verwendung von Ebenen-APIs anstelle von [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) zu verwenden.

 

### <a name="axis-aligned-clips"></a>Achsenbündig ausgerichtete Clips

Wenn der zu beschneidende Bereich an der Achse der Zeichnungsoberfläche ausgerichtet ist, anstatt an einer beliebigen. Dieser Fall eignet sich für die Verwendung eines Cliprechtecks anstelle einer Ebene. Der Leistungsgewinn ist eher für gealiaste Geometrie als für Gealiasengeometrie. Weitere Informationen zu achsenbündig ausgerichteten Clips finden Sie im Thema [**PushAxisAlignedClip.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 