---
title: Übersicht über Durchlässigkeitsmasken
description: In diesem Thema wird beschrieben, wie Bitmaps und Pinsel verwendet werden, um Deckkraftmasken zu definieren. Der Abschnitt ist wie folgt gegliedert.
ms.assetid: 869821b0-6ebe-46c2-aab6-93177d8a92c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2050cccd37012028e2a86fbf77cd071671ce7201
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626556"
---
# <a name="opacity-masks-overview"></a>Übersicht über Durchlässigkeitsmasken

In diesem Thema wird beschrieben, wie Bitmaps und Pinsel verwendet werden, um Deckkraftmasken zu definieren. Der Abschnitt ist wie folgt gegliedert.

-   [Voraussetzungen](#prerequisites)
-   [Was ist eine Deckkraftmaske?](#what-is-an-opacity-mask)
-   [Verwenden einer Bitmap als Deckkraftmaske mit der FillOpacityMask-Methode](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [Verwenden eines Pinsels als Deckkraftmaske mit der FillGeometry-Methode](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [Verwenden eines Pinsels mit linearem Farbverlauf als Deckkraftmaske](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [Verwenden eines Radialverlaufspinsels als Deckkraftmaske](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [Anwenden einer Deckkraftmaske auf eine Ebene](#apply-an-opacity-mask-to-a-layer)
-   [Zugehörige Themen](#related-topics)

## <a name="prerequisites"></a>Voraussetzungen

In dieser Übersicht wird davon ausgegangen, dass Sie mit den grundlegenden Direct2D-Zeichnungsvorgängen vertraut sind, wie in der exemplarischen Vorgehensweise Erstellen einer einfachen [Direct2D-Anwendung](direct2d-quickstart.md) beschrieben. Sie sollten auch mit den verschiedenen Pinseltypen vertraut sein, wie in [Übersicht über Pinsel beschrieben.](direct2d-brushes-overview.md)

## <a name="what-is-an-opacity-mask"></a>Was ist eine Deckkraftmaske?

Eine Deckkraftmaske ist eine Maske, die von einem Pinsel oder einer Bitmap beschrieben wird und auf ein anderes Objekt angewendet wird, um dieses Objekt teilweise oder vollständig transparent zu machen. Eine Deckkraftmaske verwendet Alphakanalinformationen, um anzugeben, wie die Quellpixel des Objekts in das endgültige Zielziel gemischt werden. Die transparenten Teile der Maske geben die Bereiche an, in denen das zugrunde liegende Bild ausgeblendet ist, während die nicht transparenten Teile der Maske angeben, wo das maskierte Objekt sichtbar ist.

Es gibt mehrere Möglichkeiten, eine Deckkraftmaske anzuwenden:

-   Verwenden Sie [**die ID2D1RenderTarget::FillOpacityMask-Methode.**](id2d1rendertarget-fillopacitymask.md) Die **FillOpacityMask-Methode** zeichnet einen rechteckigen Bereich eines Renderziels und wendet dann eine Deckkraftmaske an, die durch eine Bitmap definiert wird. Verwenden Sie diese Methode, wenn ihre Deckkraftmaske eine Bitmap ist und Sie einen rechteckigen Bereich ausfüllen möchten.
-   Verwenden Sie [**die ID2D1RenderTarget::FillGeometry-Methode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) Die **FillGeometry-Methode** zeichnet das Innere der Geometrie mit dem angegebenen [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)und wendet dann eine Deckkraftmaske an, die durch einen Pinsel definiert wird. Verwenden Sie diese Methode, wenn Sie eine Deckkraftmaske auf eine Geometrie anwenden oder einen Pinsel als Deckkraftmaske verwenden möchten.
-   Verwenden Sie [**einen ID2D1Layer,**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) um eine Deckkraftmaske anzuwenden. Verwenden Sie diesen Ansatz, wenn Sie eine Deckkraftmaske auf eine Gruppe von Zeichnungsinhalten anwenden möchten, nicht nur auf eine einzelne Form oder ein einzelnes Bild. Weitere Informationen finden Sie in der [Übersicht über Ebenen.](direct2d-layers-overview.md)

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a>Verwenden einer Bitmap als Deckkraftmaske mit der FillOpacityMask-Methode

Die [**FillOpacityMask-Methode**](id2d1rendertarget-fillopacitymask.md) zeichnet einen rechteckigen Bereich eines Renderziels und wendet dann eine Deckkraftmaske an, die durch eine [**ID2D1Bitmap definiert wird.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) Verwenden Sie diese Methode, wenn Sie über eine Bitmap verfügen, die Sie als Deckkraftmaske für einen rechteckigen Bereich verwenden möchten.

Das folgende Diagramm zeigt einen Effekt der Anwendung der Deckkraftmaske (eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit einem Bild einer Blume) auf einen [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) mit einem Bild einer Far-Anlage. Das resultierende Bild ist eine Bitmap einer Anlage, die auf die Form der Blume abgeschnitten ist.

![Diagramm einer Als Deckkraftmaske auf einem Bild einer Farn-Anlage verwendeten Bitmap](images/brushes-ovw-bitmapopacity.png)

Die folgenden Codebeispiele zeigen, wie dies erreicht wird.

Im ersten Beispiel wird die folgende Bitmap , *\_ m pBitmapMask,* zur Verwendung als Bitmapmaske geladen. Die folgende Abbildung zeigt die erzeugte Ausgabe. Beachten Sie, dass die Farbinformationen in der Bitmap keine Auswirkungen auf die Deckkraftmaske haben, obwohl der nicht transparente Teil der Bitmap schwarz erscheint. es werden nur die Deckkraftinformationen jedes Pixels in der Bitmap verwendet. Die vollständig deckenden Pixel in dieser Bitmap wurden nur zur Veranschaulichung schwarz einfärbt.

![Abbildung der Bitmapmaske für Die Blume](images/bitmapmask.png)

In diesem Beispiel wird die [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) von der Hilfsmethode LoadResourceBitmap geladen, die an anderer Stelle im Beispiel definiert ist.


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



Im nächsten Beispiel wird der Pinsel *m \_ pFernBitmapBrush* definiert, auf den die Deckkraftmaske angewendet wird. In diesem Beispiel wird ein [**ID2D1BitmapBrush-Objekt**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) verwendet, das ein Bild eines Farns enthält. Sie können jedoch stattdessen [**id2D1SolidColorBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)oder [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) verwenden. Die folgende Abbildung zeigt die erzeugte Ausgabe.

![Abbildung der vom Bitmappinsel verwendeten Bitmap](images/fern.png)


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





Nachdem die Deckkraftmaske und der Pinsel definiert wurden, können Sie die [**FillOpacityMask-Methode**](id2d1rendertarget-fillopacitymask.md) in der Renderingmethode Ihrer Anwendung verwenden. Wenn Sie die **FillOpacityMask-Methode** aufrufen, müssen Sie den Typ der verwendeten Deckkraftmaske angeben: **D2D1 \_ OPACITY \_ MASK CONTENT \_ \_ GRAPHICS**, **D2D1 \_ OPACITY \_ MASK CONTENT TEXT \_ \_ \_ NATURAL** und **D2D1 \_ OPACITY \_ MASK CONTENT TEXT \_ \_ \_ GDI \_ COMPATIBLE**. Die Bedeutungen dieser drei Typen finden Sie unter [**D2D1 \_ OPACITY \_ MASK \_ CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).

> [!Note]  
> Ab Windows 8 ist [**der D2D1-OPACITY \_ \_ \_ MASK-INHALT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) nicht mehr erforderlich. Weitere Informationen finden Sie unter der [**ID2D1DeviceContext::FillOpacityMask-Methode,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) die keinen **D2D1 \_ OPACITY \_ MASK \_ CONTENT-Parameter** hat.

 

Im nächsten Beispiel wird der Antialiasingmodus des Renderziels auf [**D2D1 \_ ANTIALIAS \_ MODE \_ ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) gesetzt, damit die Deckkraftmaske ordnungsgemäß funktioniert. Anschließend ruft sie die [**FillOpacityMask-Methode**](id2d1rendertarget-fillopacitymask.md) auf und übergibt ihr die Deckkraftmaske (*m \_ pBitmapMask*), den Pinsel, auf den die Deckkraftmaske angewendet wird (*m \_ pFernBitmapBrush*), den Inhaltstyp innerhalb der Deckkraftmaske ([**D2D1 \_ OPACITY \_ MASK CONTENT \_ \_ GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) und den zu zeichnenden Bereich. Die folgende Abbildung zeigt die erzeugte Ausgabe.

![Abbildung des Fern-Pflanzenbilds mit angewendeter Deckkraftmaske](images/opacitymaskoutput.png)


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





Code wurde in diesem Beispiel weggelassen.

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a>Verwenden eines Pinsels als Deckkraftmaske mit der FillGeometry-Methode

Im vorherigen Abschnitt wurde beschrieben, wie Sie eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) als Deckkraftmaske verwenden. Direct2D bietet auch die [**ID2D1RenderTarget::FillGeometry-Methode,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) mit der Sie optional einen Pinsel als Deckkraftmaske angeben können, wenn Sie eine [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)ausfüllen. Dadurch können Sie Deckkraftmasken aus Farbverläufen (mit [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) oder [**ID2D1RadialGradientBrush)**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)und Bitmaps (mit **ID2D1Bitmap)** erstellen.

Die [**FillGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) verwendet drei Parameter:

-   Der erste Parameter, eine [**ID2D1Geometry,**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)definiert die zu zeichnende Form.
-   Der zweite Parameter, ein [**ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)gibt den Pinsel an, der zum Zeichnen der Geometrie verwendet wird. Dieser Parameter muss ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) sein, für den die Modi x und y-extend auf [**D2D1 \_ EXTEND MODE CLAMP festgelegt \_ \_ sind.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)
-   Der dritte Parameter, ein [**ID2D1Brush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush)gibt einen Pinsel an, der als Deckkraftmaske verwendet werden soll. Dieser Pinsel kann ein [**ID2D1LinearGradientBrush,**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)oder [**ein ID2D1BitmapBrush sein.**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (Technisch gesehen können Sie einen [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)verwenden, aber die Verwendung eines Volltonfarbpinsels als Deckkraftmaske führt nicht zu interessanten Ergebnissen.)

In den folgenden Abschnitten wird beschrieben, wie [**Id2D1LinearGradientBrush-**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) und [**ID2D1RadialGradientBrush-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) als Deckkraftmasken verwendet werden.

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a>Verwenden eines Pinsels mit linearem Farbverlauf als Deckkraftmaske

Das folgende Diagramm zeigt die Auswirkung der Anwendung eines Pinsels mit linearem Farbverlauf auf ein Rechteck, das mit einer Bitmap von Pflanzen gefüllt ist.

![Diagramm einer Bitmap mit einem angewendeten linearen Farbverlaufspinsel](images/brushes-ovw-lineargradient-opacitymask.png)

In den folgenden Schritten wird beschrieben, wie Sie diesen Effekt neu erstellen.

1.  Definieren Sie den inhalt, der maskiert werden soll. Im folgenden Beispiel wird [**id2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pLinearFadeFlowersBitmap erstellt.* Der Erweiterungsmodus x- und y- für *\_ m pLinearFadeFlowersBitmap* wird auf D2D1 EXTEND MODE CLAMP festgelegt, sodass er mit einer Deckkraftmaske von der [**FillGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) verwendet werden [**\_ \_ \_ kann.**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)

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
    <col  />
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
    <col  />
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

    

2.  Definieren Sie die Deckkraftmaske. Im nächsten Codebeispiel wird ein diagonaler linearer Farbverlaufspinsel (*m \_ pLinearGradientBrush*) erstellt, der von vollständig deckend schwarz an Position 0 zu vollständig transparentem Weiß an Position 1 ausblendet.
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



    

3.  Verwenden Sie [**die FillGeometry-Methode.**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) Im letzten Beispiel wird die **FillGeometry-Methode** zum Inhaltspinsel verwendet, um eine [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) mit einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pLinearFadeFlowersBitmap*) zu füllen und eine Deckkraftmaske (*m \_ pLinearGradientBrush*) zu verwenden.
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

Code wurde in diesem Beispiel weggelassen.

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a>Verwenden eines Radialverlaufspinsels als Deckkraftmaske

Das folgende Diagramm zeigt den visuellen Effekt der Anwendung eines radialen Farbverlaufspinsels auf ein Rechteck, das mit einer Bitmap von Foliage gefüllt ist.

![Diagramm einer Foliagebitmap mit angewendetem Radialverlaufspinsel](images/brushes-ovw-radialgradient-opacitymask.png)

Im ersten Beispiel wird [**id2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pRadialFadeFlowersBitmapBrush erstellt.* Damit sie mit einer Deckkraftmaske von [**der FillGeometry-Methode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) verwendet werden kann, werden die Erweiterungsmodus x- und y- für *m \_ pRadialFadeFlowersBitmapBrush* auf [**D2D1 \_ EXTEND MODE \_ \_ CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)festgelegt.


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
<col  />
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
<col  />
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



Im nächsten Beispiel wird der Radialverlaufspinsel definiert, der als Deckkraftmaske verwendet wird.


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





Im letzten Codebeispiel werden [**id2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pRadialFadeFlowersBitmapBrush*) und die Deckkraftmaske (*m \_ pRadialGradientBrush*) verwendet, um [**id2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ pRectGeo*) zu füllen.


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



Code wurde in diesem Beispiel weggelassen.

## <a name="apply-an-opacity-mask-to-a-layer"></a>Anwenden einer Deckkraftmaske auf eine Ebene

Wenn Sie [**PushLayer aufrufen,**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) um einen [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) auf ein Renderziel zu pushen, können Sie die [**D2D1 \_ LAYER \_ PARAMETERS-Struktur**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) verwenden, um einen Pinsel als Deckkraftmaske anzuwenden. Im folgenden Codebeispiel wird [**id2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) als Deckkraftmaske verwendet.


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



Weitere Informationen zur Verwendung von Ebenen finden Sie in der [Übersicht über Ebenen.](direct2d-layers-overview.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über Pinsel](direct2d-brushes-overview.md)
</dt> <dt>

[Übersicht über Ebenen](direct2d-layers-overview.md)
</dt> </dl>

 

 
