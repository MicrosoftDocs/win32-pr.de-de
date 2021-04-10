---
title: Übersicht über Schichten
description: Beschreibt die Grundlagen von Direct2D Ebenen.
ms.assetid: 22d161fb-8470-49cc-a523-309f90643ea9
keywords:
- Direct2D, Ebenen
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0e86b32296718a975ebabccd5fc4ef0ee30cf289
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948945"
---
# <a name="layers-overview"></a>Übersicht über Schichten

In dieser Übersicht werden die Grundlagen der Verwendung von Direct2D Ebenen beschrieben. Der Abschnitt ist wie folgt gegliedert.

-   [Was sind Ebenen?](#what-are-layers)
-   [Schichten in Windows 8 und höher](#layers-in-windows-8-and-later)
    -   [ID2D1DeviceContext und pushlayer](#id2d1devicecontext-and-pushlayer)
    -   [D2D1 \_ Layer \_ PARAMETERS1 und D2D1 \_ Layer \_ OPTIONS1](/windows)
    -   [Füllmethoden](#blend-modes)
    -   [Interoperation](#interoperation)
-   [Erstellen von Ebenen](#creating-layers)
-   [Inhalts Begrenzungen](#content-bounds)
-   [Geometrische Masken](#geometric-masks)
-   [Deck Kraft Masken](#opacity-masks)
-   [Alternativen zu Ebenen](#alternatives-to-layers)
-   [Clipping einer beliebigen Form](#clipping-an-arbitrary-shape)
    -   [Achsen ausgerichtete Clips](#axis-aligned-clips)
-   [Zugehörige Themen](#related-topics)

## <a name="what-are-layers"></a>Was sind Ebenen?

Ebenen, die durch [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Objekte dargestellt werden, ermöglichen es einer Anwendung, eine Gruppe von Zeichnungs Vorgängen zu bearbeiten. Sie verwenden eine Ebene, indem Sie Sie auf ein Renderziel schieben. Nachfolgende Zeichnungsvorgänge durch das Renderziel werden an die Ebene weitergeleitet. Wenn Sie die Ebene fertiggestellt haben, können Sie die Ebene aus dem Renderziel "Pop", das den Inhalt der Ebene an das Renderziel zurückgibt.

Wie bei Pinseln sind Ebenen Geräte abhängige Ressourcen, die durch Renderziele erstellt werden. Ebenen können für alle Renderziele in derselben Ressourcen Domäne verwendet werden, die das Renderziel enthält, von dem Sie erstellt wurde. Eine ebenenressource kann jedoch nur von einem Renderziel gleichzeitig verwendet werden. Weitere Informationen zu Ressourcen finden Sie in der [Übersicht über Ressourcen](resources-and-resource-domains.md).

Obwohl Ebenen eine leistungsstarke renderingtechnik zum erzeugen interessanter Effekte bieten, kann eine übermäßige Anzahl von Ebenen in einer Anwendung sich negativ auf die Leistung auswirken, aufgrund der verschiedenen Kosten bei der Verwaltung von Ebenen und ebenenressourcen. Beispielsweise gibt es die Kosten für das Ausfüllen oder Löschen der Ebene und die anschließende wieder Mischung, insbesondere für die Hardware mit höherem Ende. Dann gibt es die Kosten für die Verwaltung der ebenenressourcen. Wenn Sie diese regelmäßig neu zuordnen, sind die resultierenden Staus gegen die GPU das größte Problem. Wenn Sie die Anwendung entwerfen, versuchen Sie, die Wiederverwendung von ebenenressourcen zu maximieren.

## <a name="layers-in-windows-8-and-later"></a>Schichten in Windows 8 und höher

Mit Windows 8 wurden neue ebenenbezogene APIs eingeführt, die die Leistung von vereinfachen, verbessern und Features zu Ebenen hinzufügen.

### <a name="id2d1devicecontext-and-pushlayer"></a>ID2D1DeviceContext und pushlayer

Die [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Schnittstelle wird von der [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) -Schnittstelle abgeleitet und ist der Schlüssel zum Anzeigen von Direct2D-Inhalten in Windows 8. Weitere Informationen zu dieser Schnittstelle finden Sie unter [Geräte und Geräte Kontexte](devices-and-device-contexts.md). Mit der Gerätekontext Schnittstelle können Sie den Aufruf der [**createlayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) -Methode überspringen und dann NULL an die [**ID2D1DeviceContext::P ushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) -Methode übergeben. Direct2D verwaltet die ebenenressource automatisch und kann Ressourcen zwischen Ebenen und Effekt Diagrammen freigeben.

### <a name="d2d1_layer_parameters1-and-d2d1_layer_options1"></a>D2D1 \_ Layer \_ PARAMETERS1 und D2D1 \_ Layer \_ OPTIONS1

Die [**D2D1 \_ Layer \_ PARAMETERS1**](/windows/desktop/api/d2d1_1/ns-d2d1_1-d2d1_layer_parameters1) -Struktur ist identisch mit [**D2D1 \_ - \_ ebenenparametern**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters), mit dem Unterschied, dass der endgültige Member der-Struktur jetzt eine [**D2D1 \_ Layer \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) -Enumeration ist.

[**D2D1 \_ Layer \_ OPTIONS1**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1) verfügt über keine ClearType-Option und bietet zwei verschiedene Optionen, die Sie verwenden können, um die Leistung zu verbessern:

-   [**D2D1 \_ Ebene \_ OPTIONS1 \_ initialisieren \_ von \_ Background**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Direct2D rendert primitive auf der Ebene, ohne Sie mit transparentem Schwarz zu löschen. Dies ist nicht die Standardeinstellung, aber in den meisten Fällen führt dies zu einer besseren Leistung.

-   [**D2D1 \_ Layer \_ OPTIONS1 \_ \_ Alpha ignorieren**](/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_layer_options1): Wenn die zugrunde liegende Oberfläche auf den [**D2D1 Alpha- \_ \_ Modus \_ ignorieren**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)festgelegt ist, ermöglicht diese Option Direct2D das Ändern des Alphakanals der Ebene zu vermeiden. Verwenden Sie dies nicht in anderen Fällen.

### <a name="blend-modes"></a>Füllmethoden

Ab Windows 8 hat der Gerätekontext einen [**primitiven Blend-Modus**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) , der bestimmt, wie die einzelnen primitiven mit der Ziel Oberfläche gemischt werden. Dieser Modus gilt auch für Ebenen, wenn Sie die [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) -Methode aufzurufen.

Wenn Sie z. b. eine Ebene zum Ausschneiden primitiver Elemente mit Transparenz verwenden, legen Sie den [**D2D1 \_ primitive \_ Blend- \_ Kopier**](/windows/desktop/api/D2d1_1/ne-d2d1_1-d2d1_primitive_blend) Modus im Gerätekontext auf die richtigen Ergebnisse fest. Der Kopiermodus macht den Gerätekontext linear interpolieren alle vier Farbkanäle, einschließlich des Alphakanals, jedes Pixels mit dem Inhalt der Ziel Oberfläche entsprechend der geometrischen Maske der Ebene.

### <a name="interoperation"></a>Interoperation

Ab Windows 8 unterstützt Direct2D die Interaktion mit Direct3D und GDI, während eine Ebene oder ein Clip per Pushvorgang übermittelt wird. Sie können [**ID2D1GdiInteropRenderTarget:: GetDC**](/windows/win32/api/d2d1/nf-d2d1-id2d1gdiinteroprendertarget-getdc) aufrufen, während eine Ebene für die Zusammenarbeit mit GDI per pushübertragung verwendet wird. Sie werden [**ID2D1DeviceContext:: Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) aufgerufen und dann auf der zugrunde liegenden Oberfläche renderzum interagieren mit Direct3D. Es liegt in ihrer Verantwortung, in der Schicht zu werden, oder Sie können mit Direct3D oder GDI Ausschneiden. Wenn Sie versuchen, außerhalb der Ebene zu Rendering oder zu schneiden, sind die Ergebnisse nicht definiert.

## <a name="creating-layers"></a>Erstellen von Ebenen

Das Arbeiten mit Ebenen erfordert Vertrautheit mit [**den Methoden**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))"Methode", " [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))" und " [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) " und der Struktur " [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) ", die einen Satz von parametrischen Daten enthält, die definieren, wie die Ebene verwendet werden kann. In der folgenden Liste werden die Methoden und die Struktur beschrieben.

-   Rufen Sie die Methode " [**kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) " zum Erstellen einer ebenenressource auf.
    > [!Note]  
    > Ab Windows 8 können Sie den Aufruf der [**createlayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) -Methode überspringen und dann NULL an die [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) -Methode der [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -Schnittstelle übergeben. Dies ist einfacher und ermöglicht Direct2D die automatische Verwaltung der ebenenressource und die gemeinsame Nutzung von Ressourcen zwischen Ebenen und Effekt Diagrammen.

     

-   Nachdem das Renderziel mit dem zeichnen begonnen hat (nachdem die [**beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -Methode aufgerufen wurde), können Sie die [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) -Methode verwenden. Die **pushlayer** -Methode fügt die angegebene Ebene zum Renderziel hinzu, sodass das Ziel alle nachfolgenden Zeichnungsvorgänge empfängt, bis [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) aufgerufen wird. Diese Methode nimmt ein [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Objekt an, das durch Aufrufen von [**createlayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer)) und einem *layerparameters* in der [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur zurückgegeben wird. In der folgenden Tabelle werden die Felder der-Struktur beschrieben. 

    | Feld                 | BESCHREIBUNG                                                                                                                                                                                                                                                                 |     |
    |-----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----|
    | **ContentBounds**     | Die Inhalts Begrenzungen der Ebene. Inhalte außerhalb dieser Grenzen werden garantiert nicht angezeigt. Dieser Parameter ist standardmäßig [**infiniterect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect). Wenn der Standardwert verwendet wird, werden die Inhalts Begrenzungen effektiv in die Grenzen des Renderziels übernommen. |     |
    | **geometricmask**     | Optionale Der durch ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)definierte Bereich, auf den die Ebene abgeschnitten werden soll. Auf **null** festgelegt, wenn die Ebene nicht auf eine Geometrie zugeschnitten werden soll.                                                                                           |     |
    | **maskantialiasmode** | Ein-Wert, der den Antialiasing Modus für die geometrische Maske angibt, die durch das **geometricmask** -Feld angegeben wird.                                                                                                                                                               |     |
    | **masktransform**     | Ein-Wert, der die Transformation angibt, die beim Erstellen der Ebene auf die geometrische Maske angewendet wird. Dies ist relativ zur Welt Transformation.                                                                                                                               |     |
    | **Deck Kraft**           | Der Deckkraft Wert der Ebene. Die Deckkraft der einzelnen Ressourcen in der Ebene wird bei der Zusammensetzung mit dem Ziel mit diesem Wert multipliziert.                                                                                                                                     |     |
    | **opacitybrush**      | Optionale Ein Pinsel, der verwendet wird, um die Deckkraft der Ebene zu ändern. Der Pinsel wird der Ebene zugeordnet, und der Alphakanal der einzelnen zugeordneten Pinsel Pixel wird mit dem entsprechenden Ebenenpixel multipliziert. Auf **null** festgelegt, wenn die Ebene keine Deckkraft Maske aufweisen soll.    |     |
    | **layeroptions**      | Ein-Wert, der angibt, ob die Ebene den Text mit ClearType-Antialiasing darstellen soll. Dieser Parameter ist standardmäßig auf OFF eingestellt. Wenn Sie diese Einstellung aktivieren, kann ClearType ordnungsgemäß verwendet werden, was jedoch zu einer etwas langsameren renderinggeschwindigkeit führt.                                          |     |

    

     

    > [!Note]  
    > Ab Windows 8 können Sie nicht mit ClearType in einer Schicht gerenstet werden, daher sollte der **layeroptions** -Parameter immer [**auf \_ D2D1 Layer \_ options \_ None**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_layer_options) festgelegt werden.

     

    Zur einfacheren Bereitstellung stellt Direct2D die [**D2D1:: layerparameters**](/windows/desktop/api/d2d1helper/nf-d2d1helper-layerparameters) -Methode bereit, die Sie beim Erstellen von Strukturen für [**D2D1 \_ Layer- \_ Parameter**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) unterstützt

-   Um den Inhalt der Ebene in das Renderziel zusammenzusetzen, nennen Sie die [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer) -Methode. Sie müssen die **poplayer** -Methode aufrufen, bevor Sie die [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -Methode aufrufen.

Im folgenden Beispiel wird die Verwendung von " [**kreatelayer**](/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-createlayer(id2d1layer))", " [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))" und " [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)" veranschaulicht. Alle Felder in der [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur werden auf ihre Standardwerte festgelegt, mit Ausnahme von **opacitybrush**, die auf eine [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)festgelegt ist.


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

Beachten Sie, dass beim Aufschieben von [**pushlayer**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer)) und [**poplayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)sichergestellt wird, dass jede **pushschicht** über einen passenden **poplayer** -Befehl verfügt. Wenn mehr **poplayer** -Aufrufe als **pushlayer** -Aufrufe vorhanden sind, wird das Renderziel in einen Fehlerzustand versetzt. Wenn [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) vor allen ausstehenden Ebenen aufgerufen wird, wird das Renderziel in einen Fehlerzustand versetzt, und es wird ein Fehler zurückgegeben. Verwenden Sie [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw), um den Fehlerzustand zu löschen.

## <a name="content-bounds"></a>Inhalts Begrenzungen

Die **ContentBounds** legt den Grenzwert fest, der auf die Ebene gezogen werden soll. Nur die Elemente innerhalb der Inhalts Begrenzungen werden wieder zum Renderziel zusammengesetzt.

Im folgenden Beispiel wird gezeigt, wie **ContentBounds** angegeben wird, sodass das ursprüngliche Bild auf die Inhalts Begrenzungen mit der oberen linken Ecke auf (10, 108) und der unteren rechten Ecke um (121, 177) abgeschnitten wird. Die folgende Abbildung zeigt das ursprüngliche Bild und das Ergebnis des Clipping des Bilds auf die Inhalts Begrenzungen.

![Abbildung der Inhalts Begrenzungen auf einem ursprünglichen Bild und dem resultierenden geschnittenen Bild](images/layers-contentbounds.png)


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
> Das resultierende abgeschnitten-Image wird weiter beeinflusst, wenn Sie eine **geometricmask** angeben. Weitere Informationen finden Sie im Abschnitt [geometrische Masken](#geometric-masks) .

 

## <a name="geometric-masks"></a>Geometrische Masken

Eine geometrische Maske ist ein Clip oder ein Ausschnitt, der durch ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) -Objekt definiert wird, das eine Ebene maskiert, wenn Sie von einem Renderziel gezeichnet wird. Sie können das Feld **geomecmask** der [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur verwenden, um die Ergebnisse in einer Geometrie zu maskieren. Wenn Sie z. b. ein Bild anzeigen möchten, das durch den Blockbuchstaben "a" maskiert wird, können Sie zuerst eine Geometrie erstellen, die den Blockbuchstaben "a" darstellt, und diese Geometrie als geometrische Maske für eine Ebene verwenden. Nachdem Sie die Ebene gedrückt haben, können Sie das Bild zeichnen. Das popping der Ebene führt dazu, dass das Bild auf den Blockbuchstaben "A" abgeschnitten wird.

Das folgende Beispiel zeigt, wie ein [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) erstellt wird, das eine Form eines Berges enthält, und dann die Pfad Geometrie an die [**pushschicht**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-pushlayer(constd2d1_layer_parameters1_id2d1layer))übergibt. Anschließend werden eine Bitmap und Quadrate gezeichnet. Wenn in der zu Rendering-Ebene nur eine Bitmap vorhanden ist, verwenden Sie [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem gebundenen Bitmap-Pinsel, um Effizienz zu erzielen. Die folgende Abbildung zeigt die Ausgabe des Beispiels.

![Darstellung eines Bilds und des resultierenden Bilds nach dem Anwenden einer geometrischen Maske eines Berges](images/layers-bitmapmask.png)

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



Code wurde in diesem Beispiel ausgelassen.

> [!Note]
>
> Im Allgemeinen können Sie, wenn Sie eine **geometricmask** angeben, den Standardwert [**infiniterect**](/windows/desktop/api/d2d1Helper/nf-d2d1helper-infiniterect)für die **ContentBounds**-Werte verwenden.
>
> Wenn **ContentBounds** den Wert NULL aufweist und **geometricmask** nicht NULL ist, sind die Inhalts Begrenzungen tatsächlich die Begrenzungen der geometrischen Maske, nachdem die Masken Transformation angewendet wurde.
>
> Wenn **ContentBounds** nicht NULL ist und **geometricmask** nicht NULL ist, wird die transformierte geometrische Maske effektiv auf die Inhalts Begrenzungen zugeschnitten, und die Inhalts Begrenzungen werden als unendlich angenommen.

 

## <a name="opacity-masks"></a>Deck Kraft Masken

Eine Deck Kraft Maske ist eine Maske, die durch einen Pinsel oder eine Bitmap beschrieben wird, der auf ein anderes Objekt angewendet wird, um dieses Objekt teilweise oder vollständig transparent zu machen. Es ermöglicht die Verwendung des Alphakanals eines Pinsels als Inhalts Maske. Sie können z. b. einen radialen Farbverlaufs Pinsel definieren, der von "nicht transparent" zu "transparent" abweicht, um einen

Im folgenden Beispiel wird ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) (*m \_ pradialgradientbrush*) als Deck Kraft Maske verwendet. Anschließend werden eine Bitmap und Quadrate gezeichnet. Wenn in der zu Rendering-Ebene nur eine Bitmap vorhanden ist, verwenden Sie [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem gebundenen Bitmap-Pinsel, um Effizienz zu erzielen. Die folgende Abbildung zeigt die Ausgabe dieses Beispiels.

![Abbildung eines Bilds und des resultierenden Bilds nach dem Anwenden einer Deck Kraft Maske](images/layers-opacitymask.png)


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
> In diesem Beispiel wird eine Ebene verwendet, um eine Deckkraft Maske auf ein einzelnes Objekt anzuwenden, um das Beispiel so einfach wie möglich zu halten. Wenn eine Deck Kraft Maske auf ein einzelnes Objekt angewendet wird, ist es effizienter, die [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode oder die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode anstelle einer Ebene zu verwenden.

 

Anweisungen zum Anwenden einer Deck Kraft Maske ohne Verwendung einer Ebene finden Sie in der [Übersicht über die Deck Kraft Masken](opacity-masks-overview.md).

## <a name="alternatives-to-layers"></a>Alternativen zu Ebenen

Wie bereits erwähnt, kann sich eine übermäßige Anzahl von Ebenen nachteilig auf die Leistung Ihrer Anwendung auswirken. Um die Leistung zu verbessern, sollten Sie möglichst keine Ebenen verwenden. Verwenden Sie stattdessen ihre Alternativen. Im folgenden Codebeispiel wird gezeigt, wie Sie mithilfe von [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f_d2d1_antialias_mode)) und [**popaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip) einen Bereich als Alternative zur Verwendung einer Ebene mit Inhalts Begrenzungen verwenden.


```C++
pRT->PushAxisAlignedClip(
    D2D1::RectF(20, 20, 100, 100),
    D2D1_ANTIALIAS_MODE_PER_PRIMITIVE
    );

pRT->FillRectangle(D2D1::RectF(0, 0, 200, 133), m_pOriginalBitmapBrush);
pRT->PopAxisAlignedClip();
```



Verwenden Sie auch [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit einem gebundenen Bitmap-Pinsel als Alternative zur Verwendung einer Ebene mit einer Deck Kraft Maske, wenn es nur einen Inhalt in der zu Rendering enden Ebene gibt, wie im folgenden Beispiel gezeigt.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo, 
            m_pLinearFadeFlowersBitmapBrush, 
            m_pLinearGradientBrush
            );
```



Als Alternative zur Verwendung einer Ebene mit einer geometrischen Maske sollten Sie die Verwendung einer Bitmap-Maske zum Ausschneiden eines Bereichs in Erwägung gezogen, wie im folgenden Beispiel gezeigt.


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



Wenn Sie die Deckkraft auf ein einzelnes primitiv anwenden möchten, sollten Sie die Deckkraft im in die Pinsel Farbe multiplizieren und dann das primitive Rendering. Sie benötigen keine Ebene oder eine Deck Kraft Maske-Bitmap.


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

> [!Note]  
> In Windows 8 wurden viele Optimierungen an der Verwendung von Ebenen vorgenommen, und es wird empfohlen, die Verwendung von ebenenapis anstelle von [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) zu verwenden, wenn dies möglich ist.

 

### <a name="axis-aligned-clips"></a>Achsen ausgerichtete Clips

, Wenn der Bereich, der abgeschnitten werden soll, an der Achse der Zeichen Oberfläche ausgerichtet ist, anstatt beliebig. Dieser Fall eignet sich für die Verwendung eines Clip Rechtecks anstelle einer Ebene. Der Leistungsgewinn liegt eher bei der Aliasing Geometrie als bei der Geometrie mit Antialiasing. Weitere Informationen zu den Achsen ausgerichteten Clips finden Sie im Thema [**pushaxisalignedclip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) .

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Direct2D-Referenz](reference.md)
</dt> </dl>

 

 