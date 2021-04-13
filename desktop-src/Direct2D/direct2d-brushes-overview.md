---
title: Übersicht über Pinsel
description: Beschreibt die verschiedenen Typen von Pinseln, die von Direct2D bereitgestellt werden.
ms.assetid: 7a31d9e7-0521-40ee-b2c1-592dfaf5301e
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 7c8b4c4762a03650f150a74d3207d12767e1fb4e
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104391188"
---
# <a name="brushes-overview"></a>Übersicht über Pinsel

In dieser Übersicht wird beschrieben, wie Sie [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)-, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)-, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)-und [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -Objekte erstellen und verwenden, um Bereiche mit voll Tonfarben, Farbverläufen und Bitmaps zu zeichnen. Der Abschnitt ist wie folgt gegliedert.

## <a name="prerequisites"></a>Voraussetzungen

In dieser Übersicht wird davon ausgegangen, dass Sie mit der Struktur einer grundlegenden Direct2D-Anwendung vertraut sind, wie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)beschrieben.

## <a name="brush-types"></a>Pinseltypen

Ein Pinsel "zeichnet" einen Bereich mit seiner Ausgabe. Verschiedene Pinsel haben unterschiedliche Ausgabetypen. Direct2D bietet vier Pinseltypen: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) zeichnet einen Bereich mit einer voll Tonfarbe, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) mit einem linearen Farbverlauf, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) mit einem radialen Farbverlauf und [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) mit einer Bitmap.

> [!NOTE]  
> Ab Windows 8 können Sie auch [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)verwenden, das einem Bitmap-Pinsel ähnelt, aber Sie können auch primitive verwenden.

Alle Pinsel erben von [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) und geben gemeinsam eine Reihe allgemeiner Features frei (festlegen und erzielen von Deckkraft und Transformieren von Pinsel); Sie werden von [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) erstellt und sind Geräte abhängige Ressourcen: Ihre Anwendung sollte Pinsel erstellen, nachdem Sie das Renderziel initialisiert hat, mit dem die Pinsel verwendet werden, und die Pinsel neu erstellen, wenn das Renderziel neu erstellt werden muss. (Weitere Informationen zu Ressourcen finden Sie unter [Übersicht über Ressourcen](resources-and-resource-domains.md).)

Die folgende Abbildung zeigt Beispiele für jeden der verschiedenen Pinseltypen.

![Abbildung der visuellen Effekte von Pinsel mit voll Tonfarbe, linearen Farbverlaufs Pinsel, radialen Farbverlaufs Pinsel und bitmappinseln](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a>Grundlagen zu Farben

Bevor Sie mit einem [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -oder einem Farbverlaufs Pinsel zeichnen, müssen Sie Farben auswählen. In Direct2D werden Farben durch die [**D2D1 \_ Color \_ F**](d2d1-color-f.md) -Struktur dargestellt (bei der es sich eigentlich um einen neuen Namen für die Struktur handelt, die von Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)) verwendet wird.

Vor Windows 8 verwendet [**D2D1 \_ Color \_ F**](d2d1-color-f.md) sRGB-Codierung. die sRGB-Codierung teilt Farben in vier Komponenten auf: rot, grün, blau und alpha. Jede Komponente wird durch einen Gleitkommawert mit einem normalen Bereich von 0,0 bis 1,0 dargestellt. Ein Wert von 0,0 gibt das vollständige Fehlen von Farbe an, während der Wert 1,0 angibt, dass die Farbe vollständig vorhanden ist. In der Alpha-Komponente steht 0,0 für vollständig transparente Farbe und 1,0 für vollständig deckende Farbe.

Ab Windows 8 akzeptiert [**D2D1 \_ Color \_ F**](d2d1-color-f.md) auch ScRGB-Codierung. ScRGB ist eine supermenge von, die Farb Werte über 1,0 und unter 0,0 zulässt.

Um eine Farbe zu definieren, können Sie die [**D2D1 \_ Color \_ F**](d2d1-color-f.md) -Struktur verwenden und ihre Felder selbst initialisieren, oder Sie können die [**D2D1:: colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse verwenden, um die Farbe zu erstellen. Die **colorf** -Klasse stellt mehrere Konstruktoren zum Definieren von Farben bereit. Wenn der Alpha Wert nicht in den Konstruktoren angegeben ist, wird standardmäßig 1,0 verwendet.

-   Verwenden Sie den colorf-Konstruktor [**(Enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) , um eine vordefinierte Farbe und einen Alphakanal Wert anzugeben. Ein Alphakanal Wert reicht von 0,0 bis 1,0, wobei 0,0 eine vollständig transparente Farbe darstellt und 1,0 eine vollständig nicht transparente Farbe darstellt. Die folgende Abbildung zeigt mehrere vordefinierte Farben und ihre hexadezimalen Entsprechungen. Eine komplette Liste der vordefinierten Farben finden Sie im Abschnitt Farb Konstanten der [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse.

    ![Abbildung von vordefinierten Farben](images/brushes-ovw-colors.png)

    Im folgenden Beispiel wird eine vordefinierte Farbe erstellt und verwendet, um die Farbe eines [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)anzugeben.

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   Verwenden Sie den colorf-Konstruktor [**(float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) , um eine Farbe in der Sequenz von rot, grün, blau und Alpha anzugeben, wobei jedes Element über einen Wert zwischen 0,0 und 1,0 verfügt.

    Im folgenden Beispiel werden die Werte für Rot, grün, blau und Alpha für eine Farbe angegeben.

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   Verwenden Sie den colorf-Konstruktor [**(UInt32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) , um den hexadezimalen Wert einer Farbe und einen Alpha Wert anzugeben, wie im folgenden Beispiel gezeigt.
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a>Alpha-Modi

Unabhängig vom Alpha Modus des Renderziels, mit dem Sie einen Pinsel verwenden, werden die Werte von [**D2D1 \_ Color \_ F**](d2d1-color-f.md) immer als gerades Alpha interpretiert.

## <a name="using-solid-color-brushes"></a>Verwenden von Pinsel mit voll Tonfarbe

Um einen Pinsel mit voll Tonfarbe zu erstellen, rufen Sie die [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) -Methode auf, die ein HRESULT und ein [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Objekt zurückgibt. Die folgende Abbildung zeigt ein Quadrat, das mit einem schwarzen Farbpinsel gezeichnet ist und mit einem Pinsel mit voll Tonfarbe mit dem Farbwert 0x9acd32 gezeichnet wird.

![Abbildung eines Quadrats mit einem Pinsel mit voll Tonfarbe](images/brushes-ovw-solidcolor.png)

Der folgende Code zeigt, wie ein schwarzer Farben Pinsel und ein Pinsel mit einem Farbwert von 0x9acd32 erstellt und verwendet werden, um dieses Quadrat auszufüllen und zu zeichnen.


```C++
    ID2D1SolidColorBrush *m_pBlackBrush;
    ID2D1SolidColorBrush *m_pYellowGreenBrush;
```




```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
        &m_pBlackBrush
        );
}

// Create a solid color brush with its rgb value 0x9ACD32.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
}
```




```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pYellowGreenBrush);
m_pRenderTarget->DrawRectangle(&rcBrushRect, m_pBlackBrush, 1, NULL);
```



Anders als bei anderen Pinseln ist das Erstellen eines [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ein relativ kostengünstiger Vorgang. Sie können **ID2D1SolidColorBrush** -Objekte jedes Mal erstellen, wenn Sie mit wenigen oder gar keinen Auswirkungen auf die Leistung erzeugen. Diese Vorgehensweise wird für Farbverläufe oder Bitmap-Pinsel nicht empfohlen.

## <a name="using-linear-gradient-brushes"></a>Verwenden linearer Farbverlaufs Pinsel

Ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) zeichnet einen Bereich mit einem linearen Farbverlauf, der entlang einer Linie definiert ist, der Farbverlaufs Achse. Sie geben die Farben des Farbverlaufs und deren Position entlang der Farbverlaufs Achse mithilfe von [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) -Objekten an. Sie können auch die Farbverlaufs Achse ändern, sodass Sie horizontalen und vertikalen Farbverlauf erstellen und die Richtung des Farbverlaufs umkehren können. Zum Erstellen eines linearen Farbverlaufs Pinsels rufen Sie die [**ID2D1RenderTarget:: | atelineargradientbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) -Methode auf.

Die folgende Abbildung zeigt ein Quadrat, das mit einem [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) gezeichnet wird, das zwei vordefinierte Farben hat: "Yellow" und "ForestGreen".

![Abbildung eines Quadrats mit einem linearen Farbverlaufs Pinsel von gelb und Gesamtstruktur grün](images/brushes-ovw-lineargradient.png)

Führen Sie die folgenden Schritte aus, um den in der obigen Abbildung gezeigten Farbverlauf zu erstellen:

1.  Deklarieren Sie zwei [**D2D1 \_ Gradient \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) -Objekte. Jede Farbverlaufs Stopps gibt eine Farbe und eine Position an. Eine Position von 0,0 gibt den Anfang des Farbverlaufs an, während eine Position von 1,0 das Ende des Farbverlaufs angibt.

    Der folgende Code erstellt ein Array aus zwei [**D2D1 \_ Gradient \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) -Objekten. Der erste Vorgang gibt die Farbe "gelb" an Position 0 an, und der zweite Haltepunkt gibt die Farbe "ForestGreen" an Position 1 an.

```C++
    // Create an array of gradient stops to put in the gradient stop
    // collection that will be used in the gradient brush.
    ID2D1GradientStopCollection *pGradientStops = NULL;

    D2D1_GRADIENT_STOP gradientStops[2];
    gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
    gradientStops[0].position = 0.0f;
    gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
    gradientStops[1].position = 1.0f;
```

    

2.  Erstellen Sie eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection). Im folgenden Beispiel wird " [**kreategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection))" aufgerufen, wobei das Array von [**D2D1- \_ Farbverlaufs \_ Stopp**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) Objekten, die Anzahl der Farbverlaufs Stopps (2), [**D2D1 \_ Gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) für Interpolationen und die D2D1-Erweiterungs [**Modus- \_ \_ \_ Klammer**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) für den Erweiterungsmodus übergeben wird.

```C++
    // Create the ID2D1GradientStopCollection from a previously
    // declared array of D2D1_GRADIENT_STOP structs.
    hr = m_pRenderTarget->CreateGradientStopCollection(
        gradientStops,
        2,
        D2D1_GAMMA_2_2,
        D2D1_EXTEND_MODE_CLAMP,
        &pGradientStops
        );
```

    

3.  Erstellen Sie die [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). Im nächsten Beispiel wird die Methode " [**samatelineargradientbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) " aufgerufen und die Eigenschaften des linearen Farbverlaufs Pinsels übergeben, die den Startpunkt bei (0,0) und den Endpunkt bei (150, 150) sowie den im vorherigen Schritt erstellten Farbverlaufs Stopp enthalten.
```C++
    // The line that determines the direction of the gradient starts at
    // the upper-left corner of the square and ends at the lower-right corner.

    if (SUCCEEDED(hr))
    {
        hr = m_pRenderTarget->CreateLinearGradientBrush(
            D2D1::LinearGradientBrushProperties(
                D2D1::Point2F(0, 0),
                D2D1::Point2F(150, 150)),
            pGradientStops,
            &m_pLinearGradientBrush
            );
    }
```

    

4.  Verwenden Sie [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush). Im nächsten Codebeispiel wird der Pinsel zum Filtern eines Rechtecks verwendet.
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a>Weitere Informationen zu Farbverlaufs Stopps

Der [**D2D1 \_ Gradient- \_ halte**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) Punkt ist der Grundbaustein eines Farbverlaufs Pinsels. Ein Farbverlaufs Ende gibt die Farbe und die Position entlang der Farbverlaufs Achse an. Der Wert der Farbverlaufs Position zwischen 0,0 und 1,0. Je näher der Wert 0,0 ist, desto näher ist die Farbe am Anfang des Farbverlaufs. je näher der Wert 1,0 ist, desto näher ist die Farbe am Ende des Farbverlaufs.

In der folgenden Abbildung werden die Verlaufs Stopps hervorgehoben. Der Kreis markiert die Position von Farbverlaufs Stopps, und eine gestrichelte Linie zeigt die Farbverlaufs Achse an.

![Abbildung eines linearen Farbverlaufs Pinsels mit vier Stopps entlang der Achse](images/4stoplineargradient.png)

Der erste Farbverlaufs Ende gibt die Farbe Gelb an einer Position von 0,0 an. Der zweite Farbverlaufs Ende gibt die rote Farbe an der Position 0,25 an. Von links nach rechts entlang der Farbverlaufs Achse ändern sich die Farben zwischen diesen beiden Haltepunkten allmählich von gelb zu rot. Der dritte Farbverlaufs Ende gibt die blaue Farbe an der Position 0,75 an. Die Farben zwischen dem zweiten und dritten Farbverlauf werden allmählich von rot in blau geändert. Der vierte Farbverlaufs-Haltepunkt gibt den kalkgrünen an der Position 1,0 an. Die Farben zwischen dem dritten und vierten Farbverlauf werden allmählich von blau in Kalk Grün geändert.

## <a name="the-gradient-axis"></a>Die Farbverlaufs Achse

Wie bereits erwähnt, werden Farbverlaufs Stopps eines linearen Farbverlaufs Pinsels entlang einer Linie, der Farbverlaufs Achse, positioniert. Beim Erstellen eines linearen Farbverlaufs Pinsels können Sie die Ausrichtung und die Größe der Linie mithilfe der Felder **Startpunkt** und **Endpunkt** der [**\_ \_ \_ \_ Eigenschafts Struktur D2D1 lineare Farbverlaufs Pinsel**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) angeben. Nachdem Sie einen Pinsel erstellt haben, können Sie die Farbverlaufs Achse anpassen, indem Sie die Methoden [**setstartpoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) und [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) des Pinsels aufrufen. Indem Sie den Startpunkt und den Endpunkt des Pinsels bearbeiten, können Sie horizontale und vertikale Farbverläufe erstellen, die Richtung des Farbverlaufs umkehren und vieles mehr.

In der folgenden Abbildung ist der Startpunkt z. b. auf (0,0) und der Endpunkt auf (150, 50) festgelegt. Dadurch wird ein diagonaler Farbverlauf erstellt, der in der oberen linken Ecke beginnt und sich auf die untere rechte Ecke des Bereichs erstreckt, der gezeichnet wird. Wenn Sie den Anfangspunkt auf (0,0) und den Endpunkt auf (150, 25) festlegen, wird ein horizontaler Farbverlauf erstellt. Entsprechend wird durch das Festlegen des Anfangs Punkts auf (75, 0) und des Endpunkts auf (75, 50) ein vertikaler Farbverlauf erstellt. Wenn Sie den Startpunkt auf (0, 50) und den Endpunkt auf (150, 0) festlegen, wird ein diagonaler Farbverlauf erstellt, der in der unteren linken Ecke beginnt und sich auf die obere rechte Ecke des Bereichs erstreckt, der gezeichnet wird.

![Abbildung von vier verschiedenen Farbverlaufs Achsen über das gleiche Rechteck](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a>Verwendung radialer Farbverlaufs Pinsel

Im Gegensatz zu einem [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), das zwei oder mehr Farben entlang einer Farbverlaufs Achse kombiniert, zeichnet ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) einen Bereich mit einem radialen Farbverlauf, der zwei oder mehr Farben in eine Ellipse einfügt. Während ein **ID2D1LinearGradientBrush** seine Farbverlaufs Achse mit einem Startpunkt und einem Endpunkt definiert, definiert ein **ID2D1RadialGradientBrush** seine Gradient-Ellipse durch Angabe eines Mittelpunkts, horizontalen und vertikalen Radials und eines Verlaufs Ursprungs Offsets.

Wie bei einem [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)verwendet ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) , um die Farben und Positionen im Farbverlauf anzugeben.

Die folgende Abbildung zeigt einen Kreis, der mit einem [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)gezeichnet wird. Der Kreis verfügt über zwei Farbverlaufs Stopps: die erste gibt eine vordefinierte Farbe "gelb" an der Position 0,0 an, und die zweite gibt eine vordefinierte Farbe "ForestGreen" an einer Position von 1,0 an. Der Farbverlauf verfügt über einen Mittelpunkt (75, 75), einen Verlaufs Ursprung Offset von (0,0) und einen x-und y-Radius von 75.

![Abbildung eines Kreises, der mit einem radialen Farbverlaufs Pinsel gezeichnet wurde](images/brushes-ovw-radials.png)

In den folgenden Codebeispielen wird gezeigt, wie dieser Kreis mit einem [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) gezeichnet wird, der zwei Farb Haltepunkte aufweist: "gelb" an der Position 0,0 und "ForestGreen" an einer Position von 1,0. Ähnlich wie bei der Erstellung eines [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)wird im Beispiel " [**kreategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) " aufgerufen, um eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus einem Array von Farbverlaufs Stopps zu erstellen.


```C++
// Create an array of gradient stops to put in the gradient stop
// collection that will be used in the gradient brush.
ID2D1GradientStopCollection *pGradientStops = NULL;

D2D1_GRADIENT_STOP gradientStops[2];
gradientStops[0].color = D2D1::ColorF(D2D1::ColorF::Yellow, 1);
gradientStops[0].position = 0.0f;
gradientStops[1].color = D2D1::ColorF(D2D1::ColorF::ForestGreen, 1);
gradientStops[1].position = 1.0f;
// Create the ID2D1GradientStopCollection from a previously
// declared array of D2D1_GRADIENT_STOP structs.
hr = m_pRenderTarget->CreateGradientStopCollection(
    gradientStops,
    2,
    D2D1_GAMMA_2_2,
    D2D1_EXTEND_MODE_CLAMP,
    &pGradientStops
    );
```



Verwenden Sie zum Erstellen eines [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)die [**ID2D1RenderTarget::**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) -Methode. Der " **kreateradialgradientbrush** " benötigt drei Parameter. Der erste Parameter, eine Eigenschaft des [**D2D1 \_ radialen \_ Farbverlaufs \_ Pinsels \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) , gibt den Mittelpunkt, den Verlaufs Ursprung Offset und die horizontale und vertikale Radien des Farbverlaufs an. Der zweite Parameter ist eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) , die die Farben und deren Positionen im Farbverlauf beschreibt, und der dritte Parameter ist die Adresse des Zeigers, der den neuen **ID2D1RadialGradientBrush** -Verweis empfängt. Einige über Ladungen akzeptieren einen zusätzlichen Parameter, eine [**D2D1 \_ Brush \_ Properties**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) -Struktur, die einen Deckkraft Wert und eine Transformation angibt, die auf den neuen Pinsel angewendet werden soll.

Im nächsten Beispiel wird " [**kreateradialgradientbrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush)" aufgerufen, wobei das Array von Farbverlaufs Stopps übergeben wird, und die Eigenschaften des radialen Farbverlaufs Pinsels, bei denen der *Mittelwert* auf (75, 75) festgelegt ist, der *gradientoriginoffset* auf (0, 0) festgelegt ist, und *radiin* und *radiin* beide auf 75 festgelegt


```C++
// The center of the gradient is in the center of the box.
// The gradient origin offset was set to zero(0, 0) or center in this case.
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateRadialGradientBrush(
        D2D1::RadialGradientBrushProperties(
            D2D1::Point2F(75, 75),
            D2D1::Point2F(0, 0),
            75,
            75),
        pGradientStops,
        &m_pRadialGradientBrush
        );
}
```



Im letzten Beispiel wird der Pinsel zum Auffüllen einer Ellipse verwendet.


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a>Konfigurieren eines radialen Farbverlaufs

Unterschiedliche Werte für " *Center*", " *gradientoriginoffset*", " *RADIUS x* " und/oder " *RADIUS* " ergeben verschiedene Farbverläufe. Die folgende Abbildung zeigt mehrere radiale Farbverläufe, die unterschiedliche Farbverlaufs Ursprungs Offsets aufweisen, wodurch die Darstellung der Kreise aus unterschiedlichen Winkeln hervorgeht.

![Abbildung desselben Kreises, der mit radialen Farbverlaufs Pinseln mit unterschiedlichen Ursprungs Offsets gezeichnet wurde](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a>Verwenden von bitmappinseln

Ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zeichnet einen Bereich mit einer Bitmap (dargestellt durch ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Objekt).

Die folgende Abbildung zeigt ein Quadrat, das mit einer Bitmap einer Anlage gezeichnet wurde.

![Abbildung eines Quadrats, das mit der Werk Bitmap gezeichnet wurde](images/brushes-ovw-bitmap.png)

In den folgenden Beispielen wird gezeigt, wie Sie dieses Quadrat mit einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)zeichnen können.

Im ersten Beispiel wird ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) für die Verwendung mit dem Pinsel initialisiert. Der **ID2D1Bitmap** wird von einer Hilfsmethode, loadresourcebitmap, bereitgestellt, die an anderer Stelle im Beispiel definiert ist.


```C++
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
}
```



Um den Bitmap-Pinsel zu erstellen, rufen Sie die [**ID2D1RenderTarget:: deatebitmapbrush**](id2d1rendertarget-createbitmapbrush.md) -Methode auf, und geben Sie die [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) an, mit der gezeichnet wird. Die-Methode gibt ein **HRESULT** und ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -Objekt zurück. Einige-über Ladungen von "| **atebitmapbrush** " ermöglichen es Ihnen, zusätzliche Optionen anzugeben, indem Sie eine [**D2D1 \_ \_ Brush**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) -Eigenschaft und eine [**D2D1 \_ Bitmap \_ Brush \_ Properties**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) -Struktur akzeptieren.


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



Im nächsten Beispiel wird der Pinsel zum Auffüllen eines Rechtecks verwendet.


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a>Konfigurieren von Erweiterungs Modi

Manchmal füllt der Farbverlauf eines Farbverlaufs Pinsels oder der Bitmap für einen bitmappinsel nicht vollständig den Bereich aus, der gezeichnet wird.

-   Wenn dies bei einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)geschieht, verwendet Direct2D die horizontalen Einstellungen des Pinsels ("[**abtextendmudex**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)") und "vertikal" ("[**abtextendmodey**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)"), um zu bestimmen, wie der verbleibende Bereich ausgefüllt wird.

-   Wenn dies bei einem Farbverlaufs Pinsel geschieht, bestimmt Direct2D, wie der verbleibende Bereich ausgefüllt wird, indem der Wert des Parameters " [**D2D1 \_ Extend \_ Mode**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) " verwendet wird, den Sie beim Aufrufen von " [**deategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) " zum Erstellen des [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)für den Farbverlauf angegeben haben.

Die folgende Abbildung zeigt die Ergebnisse aller möglichen Kombinationen der Erweiterungs Modi für eine [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1 \_ Extended \_ Mode \_ Clamp**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (Clamp), **D2D1 \_ Extend \_ Mode \_ Wrap** (Wrap) und **D2D1 \_ Extend \_ Mirror** (Spiegel).

![Abbildung eines ursprünglichen Bilds und der resultierenden Bilder aus verschiedenen Erweiterungs Modi](images/bitmapwrap-clamp-mirror.png)

Im folgenden Beispiel wird gezeigt, wie die x-und y-Erweiterungs Modi des Bitmap-Pinsels auf [**D2D1 \_ Erweitern des \_ Spiegels**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode)festgelegt werden. Anschließend wird das Rechteck mit dem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)gezeichnet.


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



Sie erzeugt eine Ausgabe, wie in der folgenden Abbildung dargestellt.

![Abbildung eines ursprünglichen Bilds und des resultierenden Bilds nach Spiegelung der x-und y-Richtung](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a>Transformieren von Pinsel

Wenn Sie mit einem Pinsel zeichnen, zeichnet Sie den Koordinaten Bereich des Renderziels. Pinsel positionieren sich nicht automatisch so, dass Sie an dem Objekt ausgerichtet werden, das gezeichnet wird. Standardmäßig beginnen Sie mit dem Zeichnen am Ursprung (0,0) des Renderziels.

Durch Festlegen des Startpunkts und des Endpunkts können Sie den durch ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) definierten Farbverlauf in einen Zielbereich verschieben. Entsprechend können Sie den von einem [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) definierten Farbverlauf durch Ändern seiner Mitte und Radii verschieben.

Um den Inhalt eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) an den Bereich auszurichten, der gezeichnet wird, können Sie die [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) -Methode verwenden, um die Bitmap an die gewünschte Stelle zu übersetzen. Diese Transformation wirkt sich nur auf den Pinsel aus. Er wirkt sich nicht auf andere Inhalte aus, die vom Renderziel gezeichnet werden.

Die folgenden Abbildungen zeigen die Auswirkung der Verwendung eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Auffüllen eines Rechtecks unter (100, 100). Die Abbildung in der linken Abbildung zeigt das Ergebnis der Füllung des Rechtecks ohne Umwandlung des Pinsels: die Bitmap wird am Ursprung des Renderziels gezeichnet. Daher wird nur ein Teil der Bitmap im Rechteck angezeigt. Die Abbildung auf der rechten Seite zeigt das Ergebnis der Transformation des **ID2D1BitmapBrush** , sodass der Inhalt 50 Pixel nach rechts und 50 Pixel nach unten verschoben wird. Die Bitmap füllt nun das Rechteck aus.

![Abbildung eines Quadrats, das mit einem Bitmap-Pinsel gezeichnet wurde, ohne den Pinsel zu transformieren und durch Transformieren des Pinsels](images/brushes-ovw-transform.png)

Der folgende Code zeigt, wie dies erreicht wird. Wenden Sie zuerst eine Übersetzung auf den [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)an, und bewegen Sie den Pinsel 50 Pixel direkt entlang der x-Achse und 50 Pixel entlang der y-Achse. Verwenden Sie dann **ID2D1BitmapBrush** , um das Rechteck mit der linken oberen Ecke bei (100, 100) und der unteren rechten Ecke um (200, 200) auszufüllen.


```cpp
// Create the bitmap to be used by the bitmap brush.
if (SUCCEEDED(hr))
{
    hr = LoadResourceBitmap(
        m_pRenderTarget,
        m_pWICFactory,
        L"FERN",
        L"Image",
        &m_pBitmap
        );
   
}

if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}

D2D1_RECT_F rcTransformedBrushRect = D2D1::RectF(100, 100, 200, 200);

// Demonstrate the effect of transforming a bitmap brush.
m_pBitmapBrush->SetTransform(
     D2D1::Matrix3x2F::Translation(D2D1::SizeF(50,50))
     );

// To see the content of the rcTransformedBrushRect, comment
// out this statement.
m_pRenderTarget->FillRectangle(
     &rcTransformedBrushRect, 
     m_pBitmapBrush
     );

m_pRenderTarget->DrawRectangle(rcTransformedBrushRect, m_pBlackBrush, 1, NULL);
```

## <a name="related-topics"></a>Zugehörige Themen

* [Direct2D-Referenz](reference.md)
* [Erstellen eines Pinsel mit voll Tonfarbe](how-to-create-a-solid-color-brush.md)
* [Erstellen eines linearen Farbverlaufs Pinsels](how-to-create-a-linear-gradient-brush.md)
* [Erstellen eines radialen Farbverlaufs Pinsels](how-to-create-a-radial-gradient-brush.md)
* [Erstellen eines Bitmap-Pinsels](how-to-create-a-bitmap-brush.md)
