---
title: Übersicht über Durchlässigkeitsmasken
description: In diesem Thema wird beschrieben, wie Bitmaps und Pinsel zum Definieren von Deck Kraft Masken verwendet werden. Der Abschnitt ist wie folgt gegliedert.
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49a4757a30247da465e0ae5226bd923219e3e665
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104556524"
---
# <a name="opacity-masks-overview"></a>Übersicht über Durchlässigkeitsmasken

In diesem Thema wird beschrieben, wie Bitmaps und Pinsel zum Definieren von Deck Kraft Masken verwendet werden. Der Abschnitt ist wie folgt gegliedert.

-   [Voraussetzungen](#prerequisites)
-   [Was ist eine Deck Kraft Maske?](#what-is-an-opacity-mask)
-   [Verwenden einer Bitmap als Deck Kraft Maske mit der fillopacitymask-Methode](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [Verwenden eines Pinsels als Deck Kraft Maske mit der fillgeometry-Methode](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [Verwenden eines linearen Farbverlaufs Pinsels als Deck Kraft Maske](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [Verwenden eines radialen Farbverlaufs Pinsels als Deck Kraft Maske](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [Anwenden einer Deck Kraft Maske auf eine Ebene](#apply-an-opacity-mask-to-a-layer)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

Diese Übersicht setzt voraus, dass Sie mit grundlegenden Direct2D-Zeichnungs Vorgängen vertraut sind, wie in der exemplarischen Vorgehensweise zum [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md) beschrieben. Sie sollten auch mit den verschiedenen Pinseltypen vertraut sein, wie in der [Übersicht über Pinsel](direct2d-brushes-overview.md)beschrieben.

## <a name="what-is-an-opacity-mask"></a>Was ist eine Deck Kraft Maske?

Eine Deck Kraft Maske ist eine Maske, die durch einen Pinsel oder eine Bitmap beschrieben wird, der auf ein anderes Objekt angewendet wird, um dieses Objekt teilweise oder vollständig transparent zu machen. Eine Deck Kraft Maske verwendet Alphakanal Informationen, um anzugeben, wie die Quell Pixel des Objekts in das endgültige Ziel Ziel gemischt werden. Die transparenten Teile der Maske geben die Bereiche an, in denen das zugrunde liegende Bild ausgeblendet ist, während die nicht transparenten Teile der Maske angeben, wo das maskierte Objekt sichtbar ist.

Es gibt mehrere Möglichkeiten, eine Deck Kraft Maske anzuwenden:

-   Verwenden Sie die [**ID2D1RenderTarget:: fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode. Die **fillopacitymask** -Methode zeichnet einen rechteckigen Bereich eines Renderziels und wendet dann eine Deck Kraft Maske an, die durch eine Bitmap definiert wird. Verwenden Sie diese Methode, wenn die Deck Kraft Maske eine Bitmap ist und Sie einen rechteckigen Bereich auffüllen möchten.
-   Verwenden Sie die [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode. Die **fillgeometry** -Methode zeichnet das Innere der Geometrie mit dem angegebenen [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)und wendet dann eine Deckkraft Maske an, die durch einen Pinsel definiert wird. Verwenden Sie diese Methode, wenn Sie eine Deck Kraft Maske auf eine Geometrie anwenden möchten oder wenn Sie einen Pinsel als Deck Kraft Maske verwenden möchten.
-   Verwenden Sie eine [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , um eine Deckkraft Maske anzuwenden. Verwenden Sie diesen Ansatz, wenn Sie eine Deck Kraft Maske auf eine Gruppe von Zeichnungs Inhalten anwenden möchten, nicht nur auf eine einzelne Form oder ein Bild. Weitere Informationen finden Sie in der [Übersicht über Ebenen](direct2d-layers-overview.md).

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>Verwenden einer Bitmap als Deck Kraft Maske mit der fillopacitymask-Methode

Die [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode zeichnet einen rechteckigen Bereich eines Renderziels und wendet dann eine Deck Kraft Maske an, die durch ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)definiert wird. Verwenden Sie diese Methode, wenn Sie über eine Bitmap verfügen, die Sie als Deck Kraft Maske für einen rechteckigen Bereich verwenden möchten.

Das folgende Diagramm zeigt die Auswirkung der Anwendung der Deck Kraft Maske (ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit einem Bild einer Blume) auf eine [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) mit einem Bild einer fern-Anlage. Das resultierende Bild ist eine Bitmap einer Anlage, die auf die Blumenform zugeschnitten ist.

![Diagramm einer Blumen Bitmap, die als Deck Kraft Maske für ein Bild einer fardrource verwendet wird](images/brushes-ovw-bitmapopacity.png)

Die folgenden Codebeispiele zeigen, wie dies erreicht wird.

Im ersten Beispiel wird die folgende Bitmap ( *m \_ pbitmapmask*) für die Verwendung als Bitmap-Maske geladen. Die folgende Abbildung zeigt die Ausgabe, die erstellt wird. Beachten Sie Folgendes: Obwohl der nicht transparente Teil der Bitmap schwarz erscheint, haben die Farbinformationen in der Bitmap keine Auswirkung auf die Deck Kraft Maske. nur die Deckkraft Informationen der einzelnen Pixel in der Bitmap werden verwendet. Die vollständig transparenten Pixel in dieser Bitmap sind nur zu Illustrations Zwecken schwarz gefärbt.

![Abbildung der Blumen Bitmap-Maske](images/bitmapmask.png)

In diesem Beispiel wird das [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Hilfsprogramm von einer Hilfsmethode geladen, die an anderer Stelle im Beispiel als loadresourcebitmap definiert ist.


```C++
            if (SUCCEEDED(hr))
            {
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"BitmapMask",
                    L"Image",
                    &m_pBitmapMask
                    );
            }
```



Im nächsten Beispiel wird der Pinsel " *m \_ pfern bitmapbrush*" definiert, auf den die Deck Kraft Maske angewendet wird. In diesem Beispiel wird ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) verwendet, das ein Bild eines fards enthält, aber Sie können stattdessen eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)oder [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) verwenden. Die folgende Abbildung zeigt die Ausgabe, die erstellt wird.

![Abbildung der Bitmap, die vom bitmappinsel verwendet wird](images/fern.png)


```C++
            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
                hr = m_pRenderTarget->CreateBitmapBrush(
                    m_pFernBitmap,
                    propertiesXClampYClamp,
                    &m_pFernBitmapBrush
                    );


            }
```





Nachdem Sie nun die Deck Kraft Maske und den Pinsel definiert haben, können Sie die [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode in der Rendering-Methode Ihrer Anwendung verwenden. Wenn Sie die **fillopacitymask** -Methode aufzurufen, müssen Sie den Typ der von Ihnen verwendeten Deck Kraft Maske angeben: **\_ \_ \_ Inhalts \_ Grafiken der D2D1 Deck Kraft Mask**, **D2D1 \_ Deck Kraft \_ mask \_ Content \_ Text \_ Natural** und **D2D1 \_ Deck Kraft \_ mask \_ Content \_ Text \_ GDI \_ Compatible**. Die Bedeutung dieser drei Typen finden Sie unter [**D2D1 \_ Opacity \_ mask \_ Content**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).

> [!Note]  
> Ab Windows 8 ist der [**Inhalt der D2D1 \_ Opacity \_ mask \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) nicht erforderlich. Weitere Informationen finden Sie unter der [**ID2D1DeviceContext:: fillopacitymask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) -Methode, die über keinen Content-Parameter der **D2D1 \_ Opacity \_ mask \_** verfügt.

 

Im nächsten Beispiel wird der Antialiasing Modus des Renderziels auf [**D2D1 \_ Antialias \_ Mode \_ Aliasing**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) festgelegt, sodass die Deck Kraft Maske ordnungsgemäß funktioniert. Anschließend ruft er die [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode auf und übergibt ihm die Deck Kraft Maske (*m \_ pbitmapmask*), den Pinsel, auf den die Deck Kraft Maske angewendet wird (*m \_ pfern bitmapbrush*), den Inhaltstyp in der Deck Kraft Maske ([**D2D1 \_ Deck Kraft \_ mask \_ Content \_ graphics**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) und den Bereich, der gezeichnet werden soll. Die folgende Abbildung zeigt die Ausgabe, die erstellt wird.

![Abbildung des fardrwerk Bilds mit angewendeter Deck Kraft Maske](images/opacitymaskoutput.png)


```C++
        D2D1_RECT_F rcBrushRect = D2D1::RectF(5, 5, 155, 155);


        // D2D1_ANTIALIAS_MODE_ALIASED must be set for FillOpacityMask to function properly
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_ALIASED);
        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );
        m_pRenderTarget->SetAntialiasMode(D2D1_ANTIALIAS_MODE_PER_PRIMITIVE);
```





Code wurde in diesem Beispiel ausgelassen.

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a>Verwenden eines Pinsels als Deck Kraft Maske mit der fillgeometry-Methode

Im vorherigen Abschnitt wurde beschrieben, wie ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) als Deck Kraft Maske verwendet wird. Direct2D bietet außerdem die [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode, die es Ihnen ermöglicht, beim Ausfüllen eines [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)optional Pinsel als Deck Kraft Maske anzugeben. Dies ermöglicht es Ihnen, Deck Kraft Masken aus Farbverläufen (mit [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) oder [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) und Bitmaps (mithilfe von **ID2D1Bitmap**) zu erstellen.

Die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode nimmt drei Parameter an:

-   Der erste Parameter, ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), definiert die zu zeichnende Form.
-   Der zweite Parameter, ein [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), gibt den Pinsel an, der zum Zeichnen der Geometrie verwendet wird. Dieser Parameter muss ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) sein, dessen x-und y-Erweiterungs Modi auf die [**D2D1 Erweiterungs \_ Modus \_ - \_ Klammer**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)festgelegt ist.
-   Der dritte Parameter, ein [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), gibt einen Pinsel an, der als Deck Kraft Maske verwendet werden soll. Dieser Pinsel kann ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)oder ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)sein. (Technisch gesehen können Sie eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)verwenden, aber die Verwendung eines voll Tonfarbe-Pinsels als Deck Kraft Maske erzeugt keine interessanten Ergebnisse.)

In den folgenden Abschnitten wird beschrieben, wie [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) -und [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) -Objekte als Deck Kraft Masken verwendet werden.

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>Verwenden eines linearen Farbverlaufs Pinsels als Deck Kraft Maske

Das folgende Diagramm zeigt die Auswirkung der Anwendung eines linearen Farbverlaufs Pinsels auf ein Rechteck, das mit einer Bitmap von Blumen gefüllt ist.

![Diagramm einer Blumen Bitmap, auf die ein linearer Farbverlaufs Pinsel angewendet wird](images/brushes-ovw-lineargradient-opacitymask.png)

In den folgenden Schritten wird beschrieben, wie dieser Effekt neu erstellt wird.

1.  Definieren Sie den Inhalt, der maskiert werden soll. Im folgenden Beispiel wird ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ plinearfadeflowersbitmap*, erstellt. Der Erweiterungs Modus x-und y-für *m \_ plinearfadeflowersbitmap* ist auf [**D2D1 \_ Extend \_ Mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) festgelegt, sodass er mit einer Deckkraft Maske von der [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode verwendet werden kann.

    ```cpp
    if (SUCCEEDED(hr))
    {
        // Create the bitmap to be used by the bitmap brush.
        hr = LoadResourceBitmap(
            m_pRenderTarget,
            m_pWICFactory,
            L"LinearFadeFlowers",
            L"Image",
            &m_pLinearFadeFlowersBitmap
            );
    }
 
    if (SUCCEEDED(hr))
        {
            D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                D2D1::BitmapBrushProperties(
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_EXTEND_MODE_CLAMP,
                D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                );
    ```

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>                if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateBitmapBrush(
                            m_pLinearFadeFlowersBitmap,
                            propertiesXClampYClamp,
                            &m_pLinearFadeFlowersBitmapBrush
                            );
                    }</code></pre></td>
    </tr>
    </tbody>
    </table>

    <span codelanguage="ManagedCPlusPlus"></span>
    <table>
    <colgroup>
    <col style="width: 100%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>C++</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  Definieren Sie die Deckkraft Maske. Im nächsten Codebeispiel wird ein diagonaler linearer Farbverlaufs Pinsel (*m \_ plineargradientbrush*) erstellt, der von vollständig undurchsichtigem schwarz an Position 0 bis vollständig transparent weiß an Position 1 verschwindet.
```C++
                if (SUCCEEDED(hr))
                {
                    ID2D1GradientStopCollection *pGradientStops = NULL;

                    static const D2D1_GRADIENT_STOP gradientStops[] =
                    {
                        {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                        {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                    };

                    hr = m_pRenderTarget->CreateGradientStopCollection(
                        gradientStops,
                        2,
                        &pGradientStops);


                    if (SUCCEEDED(hr))
                    {
                        hr = m_pRenderTarget->CreateLinearGradientBrush(
                            D2D1::LinearGradientBrushProperties(
                                D2D1::Point2F(0, 0),
                                D2D1::Point2F(150, 150)),
                            pGradientStops,
                            &m_pLinearGradientBrush);
                    }

    
                pGradientStops->Release();
                }
```



    

3.  Verwenden Sie die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode. Im letzten Beispiel wird die **fillgeometry** -Methode für den Content-Pinsel verwendet, um ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ prectgeography*) mit einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ plinearfadeflowersbitmap*) zu füllen und eine Deck Kraft Maske (*m \_ plineargradientbrush*) anzuwenden.
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

Code wurde in diesem Beispiel ausgelassen.

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>Verwenden eines radialen Farbverlaufs Pinsels als Deck Kraft Maske

Das folgende Diagramm zeigt den visuellen Effekt der Anwendung eines radialen Farbverlaufs Pinsels auf ein Rechteck, das mit einer Bitmap mit einem Laub gefüllt ist.

![Diagramm einer laubbitmap mit angewendetem radialen Farbverlaufs Pinsel](images/brushes-ovw-radialgradient-opacitymask.png)

Im ersten Beispiel wird ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pradialfadeflowersbitmapbrush*, erstellt. Damit Sie mit einer Deck Kraft Maske von der [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode verwendet werden kann, wird der Erweiterungs Modus x-und y-für *m \_ pradialfadeflowersbitmapbrush* auf [**D2D1 \_ Extend \_ Mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)festgelegt.


```C++
            if (SUCCEEDED(hr))
            {
                // Create the bitmap to be used by the bitmap brush.
                hr = LoadResourceBitmap(
                    m_pRenderTarget,
                    m_pWICFactory,
                    L"RadialFadeFlowers",
                    L"Image",
                    &m_pRadialFadeFlowersBitmap
                    );
            }


            if (SUCCEEDED(hr))
            {
                D2D1_BITMAP_BRUSH_PROPERTIES propertiesXClampYClamp = 
                    D2D1::BitmapBrushProperties(
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_EXTEND_MODE_CLAMP,
                    D2D1_BITMAP_INTERPOLATION_MODE_NEAREST_NEIGHBOR
                    );
```



<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateBitmapBrush(
                        m_pLinearFadeFlowersBitmap,
                        propertiesXClampYClamp,
                        &m_pLinearFadeFlowersBitmapBrush
                        );
                }</code></pre></td>
</tr>
</tbody>
</table>

<span codelanguage="ManagedCPlusPlus"></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



Im nächsten Beispiel wird der radiale Farbverlaufs Pinsel definiert, der als Deck Kraft Maske verwendet wird.


```C++
            if (SUCCEEDED(hr))
            {
                ID2D1GradientStopCollection *pGradientStops = NULL;

                static const D2D1_GRADIENT_STOP gradientStops[] =
                {
                    {   0.f,  D2D1::ColorF(D2D1::ColorF::Black, 1.0f)  },
                    {   1.f,  D2D1::ColorF(D2D1::ColorF::White, 0.0f)  },
                };

                hr = m_pRenderTarget->CreateGradientStopCollection(
                    gradientStops,
                    2,
                    &pGradientStops);




                if (SUCCEEDED(hr))
                {
                    hr = m_pRenderTarget->CreateRadialGradientBrush(
                        D2D1::RadialGradientBrushProperties(
                            D2D1::Point2F(75, 75),
                            D2D1::Point2F(0, 0),
                            75,
                            75),
                        pGradientStops,
                        &m_pRadialGradientBrush);
                }
                pGradientStops->Release();
            }
```





Im letzten Codebeispiel wird das [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pradialfadeflowersbitmapbrush*) und die Deck Kraft Maske (*m \_ pradialgradientbrush*) zum Ausfüllen eines [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ prectbrush*) verwendet.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



Code wurde in diesem Beispiel ausgelassen.

## <a name="apply-an-opacity-mask-to-a-layer"></a>Anwenden einer Deck Kraft Maske auf eine Ebene

Wenn Sie [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) aufzurufen, um ein [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Element auf ein Renderziel zu übertragen, können Sie die [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur verwenden, um einen Pinsel als Deck Kraft Maske zu verwenden. Im folgenden Codebeispiel wird ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) als Deck Kraft Maske verwendet.


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



Weitere Informationen zum Verwenden von Ebenen finden Sie unter [Übersicht über Ebenen](direct2d-layers-overview.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> <dt>

[Übersicht über Schichten](direct2d-layers-overview.md)
</dt> </dl>

 

 