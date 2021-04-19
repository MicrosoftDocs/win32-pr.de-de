---
description: In diesem Thema wird beschrieben, wie verschiedene Arten von Pinseln in einem XPS-OM verwendet werden.
ms.assetid: 392ca1d5-283e-4eed-ae21-6477c469014d
title: XPS-OM-Pinsel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0557757bfaf81156b2015525d35897cfb042e44b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356633"
---
# <a name="xps-om-brushes"></a>XPS-OM-Pinsel

In diesem Thema wird beschrieben, wie verschiedene Arten von Pinseln in einem XPS-OM verwendet werden.

Die Pinsel im XPS-OM basieren auf der [**ixpsombrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) und umfassen Folgendes:

<dl> Kachel Pinsel

-   [**Ixpsomtilebrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
-   [**Ixpsomsolidcolorbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
-   [**Ixpsomvisualbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
-   [**Ixpsomimagebrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)

  
Farbverlaufs Pinsel

-   [**Ixpsomgradientbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
-   [**Ixpsomlineargradientbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
-   [**Ixpsomradialgradientbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)

  
</dl>

## <a name="code-examples"></a>Codebeispiele

### <a name="create-a-solid-color-brush"></a>Erstellen eines Pinsel mit voll Tonfarbe

Im folgenden Codebeispiel wird ein vollfarbiger Pinsel aus einem Farbwert erstellt, der im Code definiert ist.


```C++
    HRESULT                hr = S_OK;

    XPS_COLOR              xpsColor;
    IXpsOMSolidColorBrush  *brush;

    // creates a solid red brush
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    hr = xpsFactory->CreateSolidColorBrush(
       &xpsColor, 
       NULL, 
       reinterpret_cast<IXpsOMSolidColorBrush**>(&brush));
    
    // use brush

    // when finished with brush, release pointer
    brush->Release();
```



### <a name="create-a-visual-brush"></a>Erstellen eines visuellen Pinsels

Im folgenden Codebeispiel wird ein Pinsel aus einem visuellen Objekt erstellt.


```C++
    HRESULT                       hr = S_OK;
    IXpsOMVisualBrush             *brush;

    XPS_RECT viewBoxRect = {0,0,0,0};
    XPS_RECT viewPortRect = {0,0,0,0};

    // set viewBoxRect to define the portion of the visual to use
    // as the brush.
    //
    // set viewPortRect to define the location and size of the 
    // the brush in the destination 
    //
    // create the brush
    hr = xpsFactory->CreateVisualBrush (
        &viewBoxRect,
        &viewPortRect,
        reinterpret_cast<IXpsOMVisualBrush**>(&brush));

    // assign the visual object
    //   brushVisual points to a visual
    //   that is defined outside of this example

    hr = brush->SetVisualLocal (brushVisual);
    
    // use brush
    
    // when finished with brush, release pointer
    brush->Release();
    
```



### <a name="create-an-image-brush"></a>Erstellen eines Bild Pinsels

Weitere Informationen finden Sie im Codebeispiel unter [Platzieren von Bildern in einem XPS-OM](place-images-in-an-xps-om.md).

### <a name="create-a-linear-gradient-brush"></a>Erstellen eines Pinsels mit linearem Farbverlauf

Im folgenden Codebeispiel wird ein Pinsel mit linearem Farbverlauf erstellt. Der Farbverlauf weist zwei Farbverlaufs Stopps auf.


```C++
    HRESULT                       hr = S_OK;
    XPS_COLOR                     xpsColorStop;
    IXpsOMGradientStop            *xpsGradientStop1, *xpsGradientStop2;
    IXpsOMLinearGradientBrush     *brush;
    XPS_POINT                     startPoint, endPoint;

    // define the start color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xE4;
    xpsColorStop.value.sRGB.green = 0x3B;
    xpsColorStop.value.sRGB.blue  = 0x2F;
    
    // create a gradient stop by setting the color and location 
    // for the beginning of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop, 
        NULL, 
        0.0f,
        &xpsGradientStop1);
    startPoint.x = 375.75f;
    startPoint.y = 18.0f;

    // define the end color
    xpsColorStop.colorType        = XPS_COLOR_TYPE_SRGB;
    xpsColorStop.value.sRGB.alpha = 0xFF;
    xpsColorStop.value.sRGB.red   = 0xEF;
    xpsColorStop.value.sRGB.green = 0x79;
    xpsColorStop.value.sRGB.blue  = 0x2F;

    // create a gradient stop by setting the color and  location
    //  for the end of the gradient
    hr = xpsFactory->CreateGradientStop(
        &xpsColorStop,
        NULL, 
        1.0f, 
        &xpsGradientStop2);
    endPoint.x   = 375.75f;
    endPoint.y   = 134.6f;

    // create the brush
    hr = xpsFactory->CreateLinearGradientBrush(
        xpsGradientStop1, 
        xpsGradientStop2, 
        &startPoint, 
        &endPoint, 
        &brush);
    // release gradient stops after creating brush
    xpsGradientStop1->Release();
    xpsGradientStop2->Release();

    // when finished with brush, release pointer to brush
    brush->Release();
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Ixpsomgradientbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)
</dt> <dt>

[**Ixpsomimagebrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)
</dt> <dt>

[**Ixpsomlineargradientbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)
</dt> <dt>

[**Ixpsomradialgradientbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)
</dt> <dt>

[**Ixpsomsolidcolorbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**Ixpsomtilebrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)
</dt> <dt>

[**Ixpsomvisualbrush-Schnittstelle**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)
</dt> <dt>

[**XPS- \_ Farbe**](xps-color.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 



