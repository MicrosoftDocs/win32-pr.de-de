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
# <a name="brushes-overview"></a><span data-ttu-id="3dda3-103">Übersicht über Pinsel</span><span class="sxs-lookup"><span data-stu-id="3dda3-103">Brushes overview</span></span>

<span data-ttu-id="3dda3-104">In dieser Übersicht wird beschrieben, wie Sie [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)-, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)-, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)-und [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -Objekte erstellen und verwenden, um Bereiche mit voll Tonfarben, Farbverläufen und Bitmaps zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-104">This overview describes how to create and use [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) objects to paint areas with solid colors, gradients, and bitmaps.</span></span> <span data-ttu-id="3dda3-105">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="3dda3-105">It contains the following sections.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3dda3-106">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3dda3-106">Prerequisites</span></span>

<span data-ttu-id="3dda3-107">In dieser Übersicht wird davon ausgegangen, dass Sie mit der Struktur einer grundlegenden Direct2D-Anwendung vertraut sind, wie unter [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-107">This overview assumes that you are familiar with the structure of a basic Direct2D application, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span>

## <a name="brush-types"></a><span data-ttu-id="3dda3-108">Pinseltypen</span><span class="sxs-lookup"><span data-stu-id="3dda3-108">Brush types</span></span>

<span data-ttu-id="3dda3-109">Ein Pinsel "zeichnet" einen Bereich mit seiner Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="3dda3-109">A brush "paints" an area with its output.</span></span> <span data-ttu-id="3dda3-110">Verschiedene Pinsel haben unterschiedliche Ausgabetypen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-110">Different brushes have different types of output.</span></span> <span data-ttu-id="3dda3-111">Direct2D bietet vier Pinseltypen: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) zeichnet einen Bereich mit einer voll Tonfarbe, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) mit einem linearen Farbverlauf, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) mit einem radialen Farbverlauf und [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) mit einer Bitmap.</span><span class="sxs-lookup"><span data-stu-id="3dda3-111">Direct2D provides four brush types: [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) paints an area with a solid color, [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) with a linear gradient, [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) with a radial gradient, and [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with a bitmap.</span></span>

> [!NOTE]  
> <span data-ttu-id="3dda3-112">Ab Windows 8 können Sie auch [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush)verwenden, das einem Bitmap-Pinsel ähnelt, aber Sie können auch primitive verwenden.</span><span class="sxs-lookup"><span data-stu-id="3dda3-112">Starting with Windows 8, you can also use [**ID2D1ImageBrush**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1imagebrush), which is similar to a bitmap brush, but you can use primitives, too.</span></span>

<span data-ttu-id="3dda3-113">Alle Pinsel erben von [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) und geben gemeinsam eine Reihe allgemeiner Features frei (festlegen und erzielen von Deckkraft und Transformieren von Pinsel); Sie werden von [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) erstellt und sind Geräte abhängige Ressourcen: Ihre Anwendung sollte Pinsel erstellen, nachdem Sie das Renderziel initialisiert hat, mit dem die Pinsel verwendet werden, und die Pinsel neu erstellen, wenn das Renderziel neu erstellt werden muss.</span><span class="sxs-lookup"><span data-stu-id="3dda3-113">All brushes inherit from [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush) and share a set of common features (setting and getting opacity, and transforming brushes); they are created by [**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget) and are device-dependent resources: your application should create brushes after it initializes the render target with which the brushes will be used, and recreate the brushes whenever the render target needs recreated.</span></span> <span data-ttu-id="3dda3-114">(Weitere Informationen zu Ressourcen finden Sie unter [Übersicht über Ressourcen](resources-and-resource-domains.md).)</span><span class="sxs-lookup"><span data-stu-id="3dda3-114">(For more information about resources, see [Resources Overview](resources-and-resource-domains.md).)</span></span>

<span data-ttu-id="3dda3-115">Die folgende Abbildung zeigt Beispiele für jeden der verschiedenen Pinseltypen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-115">The following illustration shows examples of each of the different brush types.</span></span>

![Abbildung der visuellen Effekte von Pinsel mit voll Tonfarbe, linearen Farbverlaufs Pinsel, radialen Farbverlaufs Pinsel und bitmappinseln](images/brushes-ovw-brushes.png)

## <a name="color-basics"></a><span data-ttu-id="3dda3-117">Grundlagen zu Farben</span><span class="sxs-lookup"><span data-stu-id="3dda3-117">Color basics</span></span>

<span data-ttu-id="3dda3-118">Bevor Sie mit einem [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -oder einem Farbverlaufs Pinsel zeichnen, müssen Sie Farben auswählen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-118">Before you paint with an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) or a gradient brush, you need to choose colors.</span></span> <span data-ttu-id="3dda3-119">In Direct2D werden Farben durch die [**D2D1 \_ Color \_ F**](d2d1-color-f.md) -Struktur dargestellt (bei der es sich eigentlich um einen neuen Namen für die Struktur handelt, die von Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-119">In Direct2D, colors are represented by the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure (which is actually just a new name for the structure that is used by Direct3D, [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)).</span></span>

<span data-ttu-id="3dda3-120">Vor Windows 8 verwendet [**D2D1 \_ Color \_ F**](d2d1-color-f.md) sRGB-Codierung.</span><span class="sxs-lookup"><span data-stu-id="3dda3-120">Prior to Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) uses sRGB encoding.</span></span> <span data-ttu-id="3dda3-121">die sRGB-Codierung teilt Farben in vier Komponenten auf: rot, grün, blau und alpha.</span><span class="sxs-lookup"><span data-stu-id="3dda3-121">sRGB encoding divides colors into four components: red, green, blue, and alpha.</span></span> <span data-ttu-id="3dda3-122">Jede Komponente wird durch einen Gleitkommawert mit einem normalen Bereich von 0,0 bis 1,0 dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-122">Each component is represented by a floating point value with a normal range of 0.0 to 1.0.</span></span> <span data-ttu-id="3dda3-123">Ein Wert von 0,0 gibt das vollständige Fehlen von Farbe an, während der Wert 1,0 angibt, dass die Farbe vollständig vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="3dda3-123">A value of 0.0 indicates the complete absence of that color, while a value of 1.0 indicates that the color is fully present.</span></span> <span data-ttu-id="3dda3-124">In der Alpha-Komponente steht 0,0 für vollständig transparente Farbe und 1,0 für vollständig deckende Farbe.</span><span class="sxs-lookup"><span data-stu-id="3dda3-124">For the alpha component, 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span>

<span data-ttu-id="3dda3-125">Ab Windows 8 akzeptiert [**D2D1 \_ Color \_ F**](d2d1-color-f.md) auch ScRGB-Codierung.</span><span class="sxs-lookup"><span data-stu-id="3dda3-125">Starting in Windows 8, [**D2D1\_COLOR\_F**](d2d1-color-f.md) also accepts scRGB encoding.</span></span> <span data-ttu-id="3dda3-126">ScRGB ist eine supermenge von, die Farb Werte über 1,0 und unter 0,0 zulässt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-126">scRGB is a superset of that allows color values above 1.0 and below 0.0.</span></span>

<span data-ttu-id="3dda3-127">Um eine Farbe zu definieren, können Sie die [**D2D1 \_ Color \_ F**](d2d1-color-f.md) -Struktur verwenden und ihre Felder selbst initialisieren, oder Sie können die [**D2D1:: colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse verwenden, um die Farbe zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-127">To define a color, you can use the [**D2D1\_COLOR\_F**](d2d1-color-f.md) structure and initialize its fields yourself, or you can use the [**D2D1::ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class to help you create the color.</span></span> <span data-ttu-id="3dda3-128">Die **colorf** -Klasse stellt mehrere Konstruktoren zum Definieren von Farben bereit.</span><span class="sxs-lookup"><span data-stu-id="3dda3-128">The **ColorF** class provides several constructors for defining colors.</span></span> <span data-ttu-id="3dda3-129">Wenn der Alpha Wert nicht in den Konstruktoren angegeben ist, wird standardmäßig 1,0 verwendet.</span><span class="sxs-lookup"><span data-stu-id="3dda3-129">If the alpha value is not specified in the constructors, it defaults to 1.0.</span></span>

-   <span data-ttu-id="3dda3-130">Verwenden Sie den colorf-Konstruktor [**(Enum, float)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) , um eine vordefinierte Farbe und einen Alphakanal Wert anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-130">Use the [**ColorF(Enum, FLOAT)**](/previous-versions/windows/desktop/legacy/dd370909(v=vs.85)) constructor to specify a predefined color and an alpha channel value.</span></span> <span data-ttu-id="3dda3-131">Ein Alphakanal Wert reicht von 0,0 bis 1,0, wobei 0,0 eine vollständig transparente Farbe darstellt und 1,0 eine vollständig nicht transparente Farbe darstellt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-131">An alpha channel value ranges from 0.0 to 1.0, where 0.0 represents a fully transparent color and 1.0 represents a fully opaque color.</span></span> <span data-ttu-id="3dda3-132">Die folgende Abbildung zeigt mehrere vordefinierte Farben und ihre hexadezimalen Entsprechungen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-132">The following illustration shows several predefined colors and their hexadecimal equivalents.</span></span> <span data-ttu-id="3dda3-133">Eine komplette Liste der vordefinierten Farben finden Sie im Abschnitt Farb Konstanten der [**colorf**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) -Klasse.</span><span class="sxs-lookup"><span data-stu-id="3dda3-133">For a complete list of predefined colors, see the Color constants section of the [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) class.</span></span>

    ![Abbildung von vordefinierten Farben](images/brushes-ovw-colors.png)

    <span data-ttu-id="3dda3-135">Im folgenden Beispiel wird eine vordefinierte Farbe erstellt und verwendet, um die Farbe eines [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-135">The following example creates a predefined color and uses it to specify the color of an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush).</span></span>

```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```

-   <span data-ttu-id="3dda3-136">Verwenden Sie den colorf-Konstruktor [**(float, float, float, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) , um eine Farbe in der Sequenz von rot, grün, blau und Alpha anzugeben, wobei jedes Element über einen Wert zwischen 0,0 und 1,0 verfügt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-136">Use the [**ColorF(FLOAT, FLOAT, FLOAT, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(float_float_float_float)) constructor to specify a color in the sequence of a red, green, blue, and alpha, where each element has a value between 0.0 and 1.0.</span></span>

    <span data-ttu-id="3dda3-137">Im folgenden Beispiel werden die Werte für Rot, grün, blau und Alpha für eine Farbe angegeben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-137">The following example specifies the red, green, blue, and alpha values for a color.</span></span>

```C++
    ID2D1SolidColorBrush *pGridBrush = NULL;
    hr = pCompatibleRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
        &pGridBrush
        );
```

-   <span data-ttu-id="3dda3-138">Verwenden Sie den colorf-Konstruktor [**(UInt32, float)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) , um den hexadezimalen Wert einer Farbe und einen Alpha Wert anzugeben, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-138">Use the [**ColorF(UINT32, FLOAT)**](/windows/win32/api/d2d1helper/nf-d2d1helper-colorf-colorf(uint32_float)) constructor to specify the hexadecimal value of a color and an alpha value, as shown in the following example.</span></span>
```C++
    hr = m_pRenderTarget->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF(0x9ACD32, 1.0f)),  
        &m_pYellowGreenBrush
        );
```

### <a name="alpha-modes"></a><span data-ttu-id="3dda3-139">Alpha-Modi</span><span class="sxs-lookup"><span data-stu-id="3dda3-139">Alpha modes</span></span>

<span data-ttu-id="3dda3-140">Unabhängig vom Alpha Modus des Renderziels, mit dem Sie einen Pinsel verwenden, werden die Werte von [**D2D1 \_ Color \_ F**](d2d1-color-f.md) immer als gerades Alpha interpretiert.</span><span class="sxs-lookup"><span data-stu-id="3dda3-140">Regardless of the alpha mode of the render target with which you use a brush, [**D2D1\_COLOR\_F**](d2d1-color-f.md) values are always interpreted as straight alpha.</span></span>

## <a name="using-solid-color-brushes"></a><span data-ttu-id="3dda3-141">Verwenden von Pinsel mit voll Tonfarbe</span><span class="sxs-lookup"><span data-stu-id="3dda3-141">Using solid color brushes</span></span>

<span data-ttu-id="3dda3-142">Um einen Pinsel mit voll Tonfarbe zu erstellen, rufen Sie die [**ID2D1RenderTarget::**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) -Methode auf, die ein HRESULT und ein [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) -Objekt zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-142">To create a solid color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method, which returns an HRESULT and an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) object.</span></span> <span data-ttu-id="3dda3-143">Die folgende Abbildung zeigt ein Quadrat, das mit einem schwarzen Farbpinsel gezeichnet ist und mit einem Pinsel mit voll Tonfarbe mit dem Farbwert 0x9acd32 gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-143">The following illustration shows a square that is stroked with a black color brush and painted with a solid color brush that has the color value of 0x9ACD32.</span></span>

![Abbildung eines Quadrats mit einem Pinsel mit voll Tonfarbe](images/brushes-ovw-solidcolor.png)

<span data-ttu-id="3dda3-145">Der folgende Code zeigt, wie ein schwarzer Farben Pinsel und ein Pinsel mit einem Farbwert von 0x9acd32 erstellt und verwendet werden, um dieses Quadrat auszufüllen und zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-145">The following code shows how to create and use a black color brush and a brush with a color value of 0x9ACD32 to fill and draw this square.</span></span>


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



<span data-ttu-id="3dda3-146">Anders als bei anderen Pinseln ist das Erstellen eines [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) ein relativ kostengünstiger Vorgang.</span><span class="sxs-lookup"><span data-stu-id="3dda3-146">Unlike other brushes, creating an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) is a relatively inexpensive operation.</span></span> <span data-ttu-id="3dda3-147">Sie können **ID2D1SolidColorBrush** -Objekte jedes Mal erstellen, wenn Sie mit wenigen oder gar keinen Auswirkungen auf die Leistung erzeugen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-147">You may create **ID2D1SolidColorBrush** objects each time you render with little to no performance impact.</span></span> <span data-ttu-id="3dda3-148">Diese Vorgehensweise wird für Farbverläufe oder Bitmap-Pinsel nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-148">This approach is not recommended for gradient or bitmap brushes.</span></span>

## <a name="using-linear-gradient-brushes"></a><span data-ttu-id="3dda3-149">Verwenden linearer Farbverlaufs Pinsel</span><span class="sxs-lookup"><span data-stu-id="3dda3-149">Using linear gradient brushes</span></span>

<span data-ttu-id="3dda3-150">Ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) zeichnet einen Bereich mit einem linearen Farbverlauf, der entlang einer Linie definiert ist, der Farbverlaufs Achse.</span><span class="sxs-lookup"><span data-stu-id="3dda3-150">An [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) paints an area with a linear gradient defined along a line, the gradient axis.</span></span> <span data-ttu-id="3dda3-151">Sie geben die Farben des Farbverlaufs und deren Position entlang der Farbverlaufs Achse mithilfe von [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) -Objekten an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-151">You specify the gradient's colors and their location along the gradient axis using [**ID2D1GradientStop**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) objects.</span></span> <span data-ttu-id="3dda3-152">Sie können auch die Farbverlaufs Achse ändern, sodass Sie horizontalen und vertikalen Farbverlauf erstellen und die Richtung des Farbverlaufs umkehren können.</span><span class="sxs-lookup"><span data-stu-id="3dda3-152">You may also modify the gradient axis, which enables you to create horizontal and vertical gradient and to reverse the gradient direction.</span></span> <span data-ttu-id="3dda3-153">Zum Erstellen eines linearen Farbverlaufs Pinsels rufen Sie die [**ID2D1RenderTarget:: | atelineargradientbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) -Methode auf.</span><span class="sxs-lookup"><span data-stu-id="3dda3-153">To create a linear gradient brush, call the [**ID2D1RenderTarget::CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method.</span></span>

<span data-ttu-id="3dda3-154">Die folgende Abbildung zeigt ein Quadrat, das mit einem [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) gezeichnet wird, das zwei vordefinierte Farben hat: "Yellow" und "ForestGreen".</span><span class="sxs-lookup"><span data-stu-id="3dda3-154">The following illustration shows a square that is painted with an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) that has two predefined colors, "Yellow" and "ForestGreen".</span></span>

![Abbildung eines Quadrats mit einem linearen Farbverlaufs Pinsel von gelb und Gesamtstruktur grün](images/brushes-ovw-lineargradient.png)

<span data-ttu-id="3dda3-156">Führen Sie die folgenden Schritte aus, um den in der obigen Abbildung gezeigten Farbverlauf zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="3dda3-156">To create the gradient shown in the preceding illustration, complete these steps:</span></span>

1.  <span data-ttu-id="3dda3-157">Deklarieren Sie zwei [**D2D1 \_ Gradient \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) -Objekte.</span><span class="sxs-lookup"><span data-stu-id="3dda3-157">Declare two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="3dda3-158">Jede Farbverlaufs Stopps gibt eine Farbe und eine Position an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-158">Each gradient stop specifies a color and a position.</span></span> <span data-ttu-id="3dda3-159">Eine Position von 0,0 gibt den Anfang des Farbverlaufs an, während eine Position von 1,0 das Ende des Farbverlaufs angibt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-159">A position of 0.0 indicates the beginning of the gradient, while a position of 1.0 indicates the end of the gradient.</span></span>

    <span data-ttu-id="3dda3-160">Der folgende Code erstellt ein Array aus zwei [**D2D1 \_ Gradient \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) -Objekten.</span><span class="sxs-lookup"><span data-stu-id="3dda3-160">The following code creates an array of two [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects.</span></span> <span data-ttu-id="3dda3-161">Der erste Vorgang gibt die Farbe "gelb" an Position 0 an, und der zweite Haltepunkt gibt die Farbe "ForestGreen" an Position 1 an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-161">The first stop specifies the color "Yellow" at a position 0, and the second stop specifies the color "ForestGreen" at position 1.</span></span>

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

    

2.  <span data-ttu-id="3dda3-162">Erstellen Sie eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span><span class="sxs-lookup"><span data-stu-id="3dda3-162">Create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span> <span data-ttu-id="3dda3-163">Im folgenden Beispiel wird " [**kreategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection))" aufgerufen, wobei das Array von [**D2D1- \_ Farbverlaufs \_ Stopp**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) Objekten, die Anzahl der Farbverlaufs Stopps (2), [**D2D1 \_ Gamma \_ 2 \_ 2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) für Interpolationen und die D2D1-Erweiterungs [**Modus- \_ \_ \_ Klammer**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) für den Erweiterungsmodus übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-163">The following example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)), passing in the array of [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) objects, the number of gradient stops (2), [**D2D1\_GAMMA\_2\_2**](/windows/win32/api/d2d1/ne-d2d1-d2d1_gamma) for interpolation, and [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) for the extend mode.</span></span>

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

    

3.  <span data-ttu-id="3dda3-164">Erstellen Sie die [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="3dda3-164">Create the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="3dda3-165">Im nächsten Beispiel wird die Methode " [**samatelineargradientbrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) " aufgerufen und die Eigenschaften des linearen Farbverlaufs Pinsels übergeben, die den Startpunkt bei (0,0) und den Endpunkt bei (150, 150) sowie den im vorherigen Schritt erstellten Farbverlaufs Stopp enthalten.</span><span class="sxs-lookup"><span data-stu-id="3dda3-165">The next example calls the [**CreateLinearGradientBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createlineargradientbrush(constd2d1_linear_gradient_brush_properties__constd2d1_brush_properties__id2d1gradientstopcollection_id2d1lineargradientbrush)) method and passes it the linear gradient brush properties that contain the start point at (0, 0) and the end point at (150, 150), and the gradient stops created in the previous step.</span></span>
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

    

4.  <span data-ttu-id="3dda3-166">Verwenden Sie [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span><span class="sxs-lookup"><span data-stu-id="3dda3-166">Use the [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush).</span></span> <span data-ttu-id="3dda3-167">Im nächsten Codebeispiel wird der Pinsel zum Filtern eines Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="3dda3-167">The next code example uses the brush to fille a rectangle.</span></span>
```C++
    m_pRenderTarget->FillRectangle(&rcBrushRect, m_pLinearGradientBrush);
```

    

## <a name="more-about-gradient-stops"></a><span data-ttu-id="3dda3-168">Weitere Informationen zu Farbverlaufs Stopps</span><span class="sxs-lookup"><span data-stu-id="3dda3-168">More about gradient stops</span></span>

<span data-ttu-id="3dda3-169">Der [**D2D1 \_ Gradient- \_ halte**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) Punkt ist der Grundbaustein eines Farbverlaufs Pinsels.</span><span class="sxs-lookup"><span data-stu-id="3dda3-169">The [**D2D1\_GRADIENT\_STOP**](/windows/win32/api/d2d1/ns-d2d1-d2d1_gradient_stop) is the basic building block of a gradient brush.</span></span> <span data-ttu-id="3dda3-170">Ein Farbverlaufs Ende gibt die Farbe und die Position entlang der Farbverlaufs Achse an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-170">A gradient stop specifies the color and the position along the gradient axis.</span></span> <span data-ttu-id="3dda3-171">Der Wert der Farbverlaufs Position zwischen 0,0 und 1,0.</span><span class="sxs-lookup"><span data-stu-id="3dda3-171">The value of the gradient position ranges between 0.0 and 1.0.</span></span> <span data-ttu-id="3dda3-172">Je näher der Wert 0,0 ist, desto näher ist die Farbe am Anfang des Farbverlaufs. je näher der Wert 1,0 ist, desto näher ist die Farbe am Ende des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="3dda3-172">The closer it is to 0.0, the closer the color is to the start of the gradient; the closer it is to 1.0, the closer the color is to the end of the gradient.</span></span>

<span data-ttu-id="3dda3-173">In der folgenden Abbildung werden die Verlaufs Stopps hervorgehoben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-173">The following illustration highlights the gradient stops.</span></span> <span data-ttu-id="3dda3-174">Der Kreis markiert die Position von Farbverlaufs Stopps, und eine gestrichelte Linie zeigt die Farbverlaufs Achse an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-174">The circle marks the position of gradient stops and a dashed line shows the gradient axis.</span></span>

![Abbildung eines linearen Farbverlaufs Pinsels mit vier Stopps entlang der Achse](images/4stoplineargradient.png)

<span data-ttu-id="3dda3-176">Der erste Farbverlaufs Ende gibt die Farbe Gelb an einer Position von 0,0 an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-176">The first gradient stop specifies the color yellow at a position of 0.0.</span></span> <span data-ttu-id="3dda3-177">Der zweite Farbverlaufs Ende gibt die rote Farbe an der Position 0,25 an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-177">The second gradient stop specifies red color at a position of 0.25.</span></span> <span data-ttu-id="3dda3-178">Von links nach rechts entlang der Farbverlaufs Achse ändern sich die Farben zwischen diesen beiden Haltepunkten allmählich von gelb zu rot.</span><span class="sxs-lookup"><span data-stu-id="3dda3-178">From left to right along the gradient axis, the colors between these two stops gradually change from yellow to red.</span></span> <span data-ttu-id="3dda3-179">Der dritte Farbverlaufs Ende gibt die blaue Farbe an der Position 0,75 an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-179">The third gradient stop specifies blue color at a position of 0.75.</span></span> <span data-ttu-id="3dda3-180">Die Farben zwischen dem zweiten und dritten Farbverlauf werden allmählich von rot in blau geändert.</span><span class="sxs-lookup"><span data-stu-id="3dda3-180">The colors between the second and third gradient stops gradually change from red to blue.</span></span> <span data-ttu-id="3dda3-181">Der vierte Farbverlaufs-Haltepunkt gibt den kalkgrünen an der Position 1,0 an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-181">The fourth gradient stop specifies lime green at a position of 1.0.</span></span> <span data-ttu-id="3dda3-182">Die Farben zwischen dem dritten und vierten Farbverlauf werden allmählich von blau in Kalk Grün geändert.</span><span class="sxs-lookup"><span data-stu-id="3dda3-182">The colors between the third and fourth gradient stops gradually change from blue to lime green.</span></span>

## <a name="the-gradient-axis"></a><span data-ttu-id="3dda3-183">Die Farbverlaufs Achse</span><span class="sxs-lookup"><span data-stu-id="3dda3-183">The gradient axis</span></span>

<span data-ttu-id="3dda3-184">Wie bereits erwähnt, werden Farbverlaufs Stopps eines linearen Farbverlaufs Pinsels entlang einer Linie, der Farbverlaufs Achse, positioniert.</span><span class="sxs-lookup"><span data-stu-id="3dda3-184">As mentioned previously, gradient stops of a linear gradient brush are positioned along a line, the gradient axis.</span></span> <span data-ttu-id="3dda3-185">Beim Erstellen eines linearen Farbverlaufs Pinsels können Sie die Ausrichtung und die Größe der Linie mithilfe der Felder **Startpunkt** und **Endpunkt** der [**\_ \_ \_ \_ Eigenschafts Struktur D2D1 lineare Farbverlaufs Pinsel**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) angeben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-185">You can specify the orientation and size of the line using the **startPoint** and **endPoint** fields of the [**D2D1\_LINEAR\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_linear_gradient_brush_properties) structure when you create a linear gradient brush.</span></span> <span data-ttu-id="3dda3-186">Nachdem Sie einen Pinsel erstellt haben, können Sie die Farbverlaufs Achse anpassen, indem Sie die Methoden [**setstartpoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) und [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) des Pinsels aufrufen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-186">After you've created a brush, you can adjust the gradient axis by calling the brush's [**SetStartPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setstartpoint) and [**SetEndPoint**](/windows/win32/api/d2d1/nf-d2d1-id2d1lineargradientbrush-setendpoint) methods.</span></span> <span data-ttu-id="3dda3-187">Indem Sie den Startpunkt und den Endpunkt des Pinsels bearbeiten, können Sie horizontale und vertikale Farbverläufe erstellen, die Richtung des Farbverlaufs umkehren und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="3dda3-187">By manipulating the brush's start point and end point, you can create horizontal and vertical gradients, reverse the gradient direction, and more.</span></span>

<span data-ttu-id="3dda3-188">In der folgenden Abbildung ist der Startpunkt z. b. auf (0,0) und der Endpunkt auf (150, 50) festgelegt. Dadurch wird ein diagonaler Farbverlauf erstellt, der in der oberen linken Ecke beginnt und sich auf die untere rechte Ecke des Bereichs erstreckt, der gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-188">For example, in the following illustration, the start point is set to (0,0) and the end point to (150, 50); this creates a diagonal gradient that starts at the upper-left corner and extends to the lower-right corner of the area being painted.</span></span> <span data-ttu-id="3dda3-189">Wenn Sie den Anfangspunkt auf (0,0) und den Endpunkt auf (150, 25) festlegen, wird ein horizontaler Farbverlauf erstellt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-189">When you set the start point to (0, 25) and the end point to (150, 25), a horizontal gradient is created.</span></span> <span data-ttu-id="3dda3-190">Entsprechend wird durch das Festlegen des Anfangs Punkts auf (75, 0) und des Endpunkts auf (75, 50) ein vertikaler Farbverlauf erstellt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-190">Similarly, setting the start point to (75, 0) and the end point to (75, 50) creates a vertical gradient.</span></span> <span data-ttu-id="3dda3-191">Wenn Sie den Startpunkt auf (0, 50) und den Endpunkt auf (150, 0) festlegen, wird ein diagonaler Farbverlauf erstellt, der in der unteren linken Ecke beginnt und sich auf die obere rechte Ecke des Bereichs erstreckt, der gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-191">Setting the start point to (0, 50) and the end point to (150, 0) creates a diagonal gradient that starts at the lower-left corner and extends to the upper-right corner of the area being painted.</span></span>

![Abbildung von vier verschiedenen Farbverlaufs Achsen über das gleiche Rechteck](images/linear-gradients.png)

## <a name="using-radial-gradient-brushes"></a><span data-ttu-id="3dda3-193">Verwendung radialer Farbverlaufs Pinsel</span><span class="sxs-lookup"><span data-stu-id="3dda3-193">Using radial gradient brushes</span></span>

<span data-ttu-id="3dda3-194">Im Gegensatz zu einem [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), das zwei oder mehr Farben entlang einer Farbverlaufs Achse kombiniert, zeichnet ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) einen Bereich mit einem radialen Farbverlauf, der zwei oder mehr Farben in eine Ellipse einfügt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-194">Unlike an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), which blends two or more colors along a gradient axis, an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) paints an area with a radial gradient that blends two or more colors across an ellipse.</span></span> <span data-ttu-id="3dda3-195">Während ein **ID2D1LinearGradientBrush** seine Farbverlaufs Achse mit einem Startpunkt und einem Endpunkt definiert, definiert ein **ID2D1RadialGradientBrush** seine Gradient-Ellipse durch Angabe eines Mittelpunkts, horizontalen und vertikalen Radials und eines Verlaufs Ursprungs Offsets.</span><span class="sxs-lookup"><span data-stu-id="3dda3-195">While a **ID2D1LinearGradientBrush** defines its gradient axis with a start point and an end point, a **ID2D1RadialGradientBrush** defines its gradient ellipse by specifying a center, horizontal and vertical radii, and a gradient origin offset.</span></span>

<span data-ttu-id="3dda3-196">Wie bei einem [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)verwendet ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) , um die Farben und Positionen im Farbverlauf anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-196">Like an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) uses an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) to specify the colors and positions in the gradient.</span></span>

<span data-ttu-id="3dda3-197">Die folgende Abbildung zeigt einen Kreis, der mit einem [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-197">The following illustration shows a circle painted with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush).</span></span> <span data-ttu-id="3dda3-198">Der Kreis verfügt über zwei Farbverlaufs Stopps: die erste gibt eine vordefinierte Farbe "gelb" an der Position 0,0 an, und die zweite gibt eine vordefinierte Farbe "ForestGreen" an einer Position von 1,0 an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-198">The circle has two gradient stops: the first specifies a predefined color "Yellow" at a position of 0.0, and the second specifies a predefined color "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="3dda3-199">Der Farbverlauf verfügt über einen Mittelpunkt (75, 75), einen Verlaufs Ursprung Offset von (0,0) und einen x-und y-Radius von 75.</span><span class="sxs-lookup"><span data-stu-id="3dda3-199">The gradient has a center of (75, 75), a gradient origin offset of (0, 0), and an x- and y-radius of 75.</span></span>

![Abbildung eines Kreises, der mit einem radialen Farbverlaufs Pinsel gezeichnet wurde](images/brushes-ovw-radials.png)

<span data-ttu-id="3dda3-201">In den folgenden Codebeispielen wird gezeigt, wie dieser Kreis mit einem [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) gezeichnet wird, der zwei Farb Haltepunkte aufweist: "gelb" an der Position 0,0 und "ForestGreen" an einer Position von 1,0.</span><span class="sxs-lookup"><span data-stu-id="3dda3-201">The following code examples shows how to paint this circle with an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) that has two color stops: "Yellow" at a position of 0.0, and "ForestGreen" at a position of 1.0.</span></span> <span data-ttu-id="3dda3-202">Ähnlich wie bei der Erstellung eines [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)wird im Beispiel " [**kreategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) " aufgerufen, um eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) aus einem Array von Farbverlaufs Stopps zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-202">Similar to creating an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), the example calls [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) from an array of gradient stops.</span></span>


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



<span data-ttu-id="3dda3-203">Verwenden Sie zum Erstellen eines [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)die [**ID2D1RenderTarget::**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3dda3-203">To create an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), use the [**ID2D1RenderTarget::CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush) method.</span></span> <span data-ttu-id="3dda3-204">Der " **kreateradialgradientbrush** " benötigt drei Parameter.</span><span class="sxs-lookup"><span data-stu-id="3dda3-204">The **CreateRadialGradientBrush** takes three parameters.</span></span> <span data-ttu-id="3dda3-205">Der erste Parameter, eine Eigenschaft des [**D2D1 \_ radialen \_ Farbverlaufs \_ Pinsels \_**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) , gibt den Mittelpunkt, den Verlaufs Ursprung Offset und die horizontale und vertikale Radien des Farbverlaufs an.</span><span class="sxs-lookup"><span data-stu-id="3dda3-205">The first parameter, a [**D2D1\_RADIAL\_GRADIENT\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_radial_gradient_brush_properties) specifies the center, gradient origin offset, and the horizontal and vertical radii of the gradient.</span></span> <span data-ttu-id="3dda3-206">Der zweite Parameter ist eine [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) , die die Farben und deren Positionen im Farbverlauf beschreibt, und der dritte Parameter ist die Adresse des Zeigers, der den neuen **ID2D1RadialGradientBrush** -Verweis empfängt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-206">The second parameter is an [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection) that describes the colors and their positions in the gradient, and the third parameter is the address of the pointer that receive the new **ID2D1RadialGradientBrush** reference.</span></span> <span data-ttu-id="3dda3-207">Einige über Ladungen akzeptieren einen zusätzlichen Parameter, eine [**D2D1 \_ Brush \_ Properties**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) -Struktur, die einen Deckkraft Wert und eine Transformation angibt, die auf den neuen Pinsel angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3dda3-207">Some overloads take an additional parameter, a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) structure that specifies an opacity value and a transform to apply to the new brush.</span></span>

<span data-ttu-id="3dda3-208">Im nächsten Beispiel wird " [**kreateradialgradientbrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush)" aufgerufen, wobei das Array von Farbverlaufs Stopps übergeben wird, und die Eigenschaften des radialen Farbverlaufs Pinsels, bei denen der *Mittelwert* auf (75, 75) festgelegt ist, der *gradientoriginoffset* auf (0, 0) festgelegt ist, und *radiin* und *radiin* beide auf 75 festgelegt</span><span class="sxs-lookup"><span data-stu-id="3dda3-208">The next example calls [**CreateRadialGradientBrush**](/windows/win32/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomobjectfactory-createradialgradientbrush), passing in the array of gradient stops, and the radial gradient brush properties that have the *center* value set to (75, 75), the *gradientOriginOffset* set to (0, 0), and *radiusX* and *radiusY* both set to 75.</span></span>


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



<span data-ttu-id="3dda3-209">Im letzten Beispiel wird der Pinsel zum Auffüllen einer Ellipse verwendet.</span><span class="sxs-lookup"><span data-stu-id="3dda3-209">The final example uses the brush to fill an ellipse.</span></span>


```C++
m_pRenderTarget->FillEllipse(ellipse, m_pRadialGradientBrush);
m_pRenderTarget->DrawEllipse(ellipse, m_pBlackBrush, 1, NULL);
```



### <a name="configuring-a-radial-gradient"></a><span data-ttu-id="3dda3-210">Konfigurieren eines radialen Farbverlaufs</span><span class="sxs-lookup"><span data-stu-id="3dda3-210">Configuring a radial gradient</span></span>

<span data-ttu-id="3dda3-211">Unterschiedliche Werte für " *Center*", " *gradientoriginoffset*", " *RADIUS x* " und/oder " *RADIUS* " ergeben verschiedene Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="3dda3-211">Different values for *center*, *gradientOriginOffset*, *radiusX* and/or *radiusY* produce different gradients.</span></span> <span data-ttu-id="3dda3-212">Die folgende Abbildung zeigt mehrere radiale Farbverläufe, die unterschiedliche Farbverlaufs Ursprungs Offsets aufweisen, wodurch die Darstellung der Kreise aus unterschiedlichen Winkeln hervorgeht.</span><span class="sxs-lookup"><span data-stu-id="3dda3-212">The following illustration shows several radial gradients that have different gradient origin offsets, creating the appearance of the light illuminating the circles from different angles.</span></span>

![Abbildung desselben Kreises, der mit radialen Farbverlaufs Pinseln mit unterschiedlichen Ursprungs Offsets gezeichnet wurde](images/radialgradient.png)

## <a name="using-bitmap-brushes"></a><span data-ttu-id="3dda3-214">Verwenden von bitmappinseln</span><span class="sxs-lookup"><span data-stu-id="3dda3-214">Using bitmap brushes</span></span>

<span data-ttu-id="3dda3-215">Ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zeichnet einen Bereich mit einer Bitmap (dargestellt durch ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Objekt).</span><span class="sxs-lookup"><span data-stu-id="3dda3-215">An [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) paints an area with a bitmap (represented by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) object).</span></span>

<span data-ttu-id="3dda3-216">Die folgende Abbildung zeigt ein Quadrat, das mit einer Bitmap einer Anlage gezeichnet wurde.</span><span class="sxs-lookup"><span data-stu-id="3dda3-216">The following illustration shows a square painted with a bitmap of a plant.</span></span>

![Abbildung eines Quadrats, das mit der Werk Bitmap gezeichnet wurde](images/brushes-ovw-bitmap.png)

<span data-ttu-id="3dda3-218">In den folgenden Beispielen wird gezeigt, wie Sie dieses Quadrat mit einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)zeichnen können.</span><span class="sxs-lookup"><span data-stu-id="3dda3-218">The examples that follow shows how to paint this square with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>

<span data-ttu-id="3dda3-219">Im ersten Beispiel wird ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) für die Verwendung mit dem Pinsel initialisiert.</span><span class="sxs-lookup"><span data-stu-id="3dda3-219">The first example initializes an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) for use with the brush.</span></span> <span data-ttu-id="3dda3-220">Der **ID2D1Bitmap** wird von einer Hilfsmethode, loadresourcebitmap, bereitgestellt, die an anderer Stelle im Beispiel definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3dda3-220">The **ID2D1Bitmap** is provided by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


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



<span data-ttu-id="3dda3-221">Um den Bitmap-Pinsel zu erstellen, rufen Sie die [**ID2D1RenderTarget:: deatebitmapbrush**](id2d1rendertarget-createbitmapbrush.md) -Methode auf, und geben Sie die [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) an, mit der gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-221">To create the bitmap brush, call the [**ID2D1RenderTarget::CreateBitmapBrush**](id2d1rendertarget-createbitmapbrush.md) method and specify the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with which to paint.</span></span> <span data-ttu-id="3dda3-222">Die-Methode gibt ein **HRESULT** und ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="3dda3-222">The method returns an **HRESULT** and an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) object.</span></span> <span data-ttu-id="3dda3-223">Einige-über Ladungen von "| **atebitmapbrush** " ermöglichen es Ihnen, zusätzliche Optionen anzugeben, indem Sie eine [**D2D1 \_ \_ Brush**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) -Eigenschaft und eine [**D2D1 \_ Bitmap \_ Brush \_ Properties**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) -Struktur akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="3dda3-223">Some **CreateBitmapBrush** overloads enable you to specify additional options by accepting a [**D2D1\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_brush_properties) and a [**D2D1\_BITMAP\_BRUSH\_PROPERTIES**](/windows/win32/api/d2d1/ns-d2d1-d2d1_bitmap_brush_properties) structure.</span></span>


```C++
if (SUCCEEDED(hr))
{
    hr = m_pRenderTarget->CreateBitmapBrush(
        m_pBitmap,
        &m_pBitmapBrush
        );
}
```



<span data-ttu-id="3dda3-224">Im nächsten Beispiel wird der Pinsel zum Auffüllen eines Rechtecks verwendet.</span><span class="sxs-lookup"><span data-stu-id="3dda3-224">The next example uses the brush to fill a rectangle.</span></span>


```C++
m_pRenderTarget->FillRectangle(&rcBrushRect, m_pBitmapBrush);
```



## <a name="configuring-extend-modes"></a><span data-ttu-id="3dda3-225">Konfigurieren von Erweiterungs Modi</span><span class="sxs-lookup"><span data-stu-id="3dda3-225">Configuring extend modes</span></span>

<span data-ttu-id="3dda3-226">Manchmal füllt der Farbverlauf eines Farbverlaufs Pinsels oder der Bitmap für einen bitmappinsel nicht vollständig den Bereich aus, der gezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-226">Sometimes, the gradient of a gradient brush or the bitmap for a bitmap brush doesn't completely fill the area being painted.</span></span>

-   <span data-ttu-id="3dda3-227">Wenn dies bei einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)geschieht, verwendet Direct2D die horizontalen Einstellungen des Pinsels ("[**abtextendmudex**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)") und "vertikal" ("[**abtextendmodey**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)"), um zu bestimmen, wie der verbleibende Bereich ausgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-227">When this happens for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), Direct2D uses the brush's horizontal ([**SetExtendModeX**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodex)) and vertical ([**SetExtendModeY**](/windows/win32/api/d2d1/nf-d2d1-id2d1bitmapbrush-setextendmodey)) extend mode settings to determine how to fill the remaining area.</span></span>

-   <span data-ttu-id="3dda3-228">Wenn dies bei einem Farbverlaufs Pinsel geschieht, bestimmt Direct2D, wie der verbleibende Bereich ausgefüllt wird, indem der Wert des Parameters " [**D2D1 \_ Extend \_ Mode**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) " verwendet wird, den Sie beim Aufrufen von " [**deategradientstopcollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) " zum Erstellen des [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection)für den Farbverlauf angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-228">When this happens for a gradient brush, Direct2D determines how to fill the remaining area by using the value of the [**D2D1\_EXTEND\_MODE**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) parameter that you specified when you called the [**CreateGradientStopCollection**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-creategradientstopcollection(constd2d1_gradient_stop_uint32_d2d1_gamma_d2d1_extend_mode_id2d1gradientstopcollection)) to create the gradient brush's [**ID2D1GradientStopCollection**](/windows/win32/api/d2d1/nn-d2d1-id2d1gradientstopcollection).</span></span>

<span data-ttu-id="3dda3-229">Die folgende Abbildung zeigt die Ergebnisse aller möglichen Kombinationen der Erweiterungs Modi für eine [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1 \_ Extended \_ Mode \_ Clamp**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (Clamp), **D2D1 \_ Extend \_ Mode \_ Wrap** (Wrap) und **D2D1 \_ Extend \_ Mirror** (Spiegel).</span><span class="sxs-lookup"><span data-stu-id="3dda3-229">The following illustration shows the results from every possible combination of the extend modes for an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush): [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode) (CLAMP), **D2D1\_EXTEND\_MODE\_WRAP** (WRAP), and **D2D1\_EXTEND\_MIRROR** (MIRROR).</span></span>

![Abbildung eines ursprünglichen Bilds und der resultierenden Bilder aus verschiedenen Erweiterungs Modi](images/bitmapwrap-clamp-mirror.png)

<span data-ttu-id="3dda3-231">Im folgenden Beispiel wird gezeigt, wie die x-und y-Erweiterungs Modi des Bitmap-Pinsels auf [**D2D1 \_ Erweitern des \_ Spiegels**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode)festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3dda3-231">The following example shows how to set the bitmap brush's x- and y-extend modes to [**D2D1\_EXTEND\_MIRROR**](/windows/win32/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span> <span data-ttu-id="3dda3-232">Anschließend wird das Rechteck mit dem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3dda3-232">It then paints the rectangle with the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span>


```C++
m_pBitmapBrush->SetExtendModeX(D2D1_EXTEND_MODE_MIRROR);
m_pBitmapBrush->SetExtendModeY(D2D1_EXTEND_MODE_MIRROR);

m_pRenderTarget->FillRectangle(exampleRectangle, m_pBitmapBrush);
```



<span data-ttu-id="3dda3-233">Sie erzeugt eine Ausgabe, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-233">It produces output as shown in the following illustration.</span></span>

![Abbildung eines ursprünglichen Bilds und des resultierenden Bilds nach Spiegelung der x-und y-Richtung](images/brushes-ovw-bitmapmirrormirror.png)

## <a name="transforming-brushes"></a><span data-ttu-id="3dda3-235">Transformieren von Pinsel</span><span class="sxs-lookup"><span data-stu-id="3dda3-235">Transforming brushes</span></span>

<span data-ttu-id="3dda3-236">Wenn Sie mit einem Pinsel zeichnen, zeichnet Sie den Koordinaten Bereich des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="3dda3-236">When you paint with a brush, it paints in the coordinate space of the render target.</span></span> <span data-ttu-id="3dda3-237">Pinsel positionieren sich nicht automatisch so, dass Sie an dem Objekt ausgerichtet werden, das gezeichnet wird. Standardmäßig beginnen Sie mit dem Zeichnen am Ursprung (0,0) des Renderziels.</span><span class="sxs-lookup"><span data-stu-id="3dda3-237">Brushes do not automatically position themselves to align with the object being painted; by default, they begin painting at the origin (0, 0) of the render target.</span></span>

<span data-ttu-id="3dda3-238">Durch Festlegen des Startpunkts und des Endpunkts können Sie den durch ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) definierten Farbverlauf in einen Zielbereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-238">You can "move" the gradient defined by an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) to a target area by setting its start point and end point.</span></span> <span data-ttu-id="3dda3-239">Entsprechend können Sie den von einem [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) definierten Farbverlauf durch Ändern seiner Mitte und Radii verschieben.</span><span class="sxs-lookup"><span data-stu-id="3dda3-239">Likewise, you can move the gradient defined by an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) by changing its center and radii.</span></span>

<span data-ttu-id="3dda3-240">Um den Inhalt eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) an den Bereich auszurichten, der gezeichnet wird, können Sie die [**setTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) -Methode verwenden, um die Bitmap an die gewünschte Stelle zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-240">To align the content of an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to the area being painted, you can use the [**SetTransform**](/windows/win32/api/d2d1/nf-d2d1-id2d1brush-settransform(constd2d1_matrix_3x2_f)) method to translate the bitmap to the desired location.</span></span> <span data-ttu-id="3dda3-241">Diese Transformation wirkt sich nur auf den Pinsel aus. Er wirkt sich nicht auf andere Inhalte aus, die vom Renderziel gezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="3dda3-241">This transform only affects the brush; it does not affect any other content drawn by the render target.</span></span>

<span data-ttu-id="3dda3-242">Die folgenden Abbildungen zeigen die Auswirkung der Verwendung eines [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) zum Auffüllen eines Rechtecks unter (100, 100).</span><span class="sxs-lookup"><span data-stu-id="3dda3-242">The following illustrations shows the effect of using an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) to fill a rectangle located at (100, 100).</span></span> <span data-ttu-id="3dda3-243">Die Abbildung in der linken Abbildung zeigt das Ergebnis der Füllung des Rechtecks ohne Umwandlung des Pinsels: die Bitmap wird am Ursprung des Renderziels gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3dda3-243">The illustration on the left illustration shows the result of filling the rectangle without transforming the brush: the bitmap is drawn at the render target's origin.</span></span> <span data-ttu-id="3dda3-244">Daher wird nur ein Teil der Bitmap im Rechteck angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3dda3-244">As a result, only a portion of the bitmap appears in the rectangle.</span></span> <span data-ttu-id="3dda3-245">Die Abbildung auf der rechten Seite zeigt das Ergebnis der Transformation des **ID2D1BitmapBrush** , sodass der Inhalt 50 Pixel nach rechts und 50 Pixel nach unten verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-245">The illustration on the right shows the result of transforming the **ID2D1BitmapBrush** so that its content is shifted 50 pixels to the right and 50 pixels down.</span></span> <span data-ttu-id="3dda3-246">Die Bitmap füllt nun das Rechteck aus.</span><span class="sxs-lookup"><span data-stu-id="3dda3-246">The bitmap now fills the rectangle.</span></span>

![Abbildung eines Quadrats, das mit einem Bitmap-Pinsel gezeichnet wurde, ohne den Pinsel zu transformieren und durch Transformieren des Pinsels](images/brushes-ovw-transform.png)

<span data-ttu-id="3dda3-248">Der folgende Code zeigt, wie dies erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="3dda3-248">The following code shows how to accomplish this.</span></span> <span data-ttu-id="3dda3-249">Wenden Sie zuerst eine Übersetzung auf den [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)an, und bewegen Sie den Pinsel 50 Pixel direkt entlang der x-Achse und 50 Pixel entlang der y-Achse.</span><span class="sxs-lookup"><span data-stu-id="3dda3-249">First apply a translation to the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), moving the brush 50 pixels right along the x-axis and 50 pixels down along the y-axis.</span></span> <span data-ttu-id="3dda3-250">Verwenden Sie dann **ID2D1BitmapBrush** , um das Rechteck mit der linken oberen Ecke bei (100, 100) und der unteren rechten Ecke um (200, 200) auszufüllen.</span><span class="sxs-lookup"><span data-stu-id="3dda3-250">Then use the **ID2D1BitmapBrush** to fill the rectangle that has the upper-left corner at (100, 100) and the lower-right corner at (200, 200).</span></span>


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

## <a name="related-topics"></a><span data-ttu-id="3dda3-251">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3dda3-251">Related topics</span></span>

* [<span data-ttu-id="3dda3-252">Direct2D-Referenz</span><span class="sxs-lookup"><span data-stu-id="3dda3-252">Direct2D reference</span></span>](reference.md)
* [<span data-ttu-id="3dda3-253">Erstellen eines Pinsel mit voll Tonfarbe</span><span class="sxs-lookup"><span data-stu-id="3dda3-253">How to create a solid color brush</span></span>](how-to-create-a-solid-color-brush.md)
* [<span data-ttu-id="3dda3-254">Erstellen eines linearen Farbverlaufs Pinsels</span><span class="sxs-lookup"><span data-stu-id="3dda3-254">How to create a linear gradient brush</span></span>](how-to-create-a-linear-gradient-brush.md)
* [<span data-ttu-id="3dda3-255">Erstellen eines radialen Farbverlaufs Pinsels</span><span class="sxs-lookup"><span data-stu-id="3dda3-255">How to create a radial gradient brush</span></span>](how-to-create-a-radial-gradient-brush.md)
* [<span data-ttu-id="3dda3-256">Erstellen eines Bitmap-Pinsels</span><span class="sxs-lookup"><span data-stu-id="3dda3-256">How to create a bitmap brush</span></span>](how-to-create-a-bitmap-brush.md)
