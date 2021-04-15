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
# <a name="opacity-masks-overview"></a><span data-ttu-id="3c431-104">Übersicht über Durchlässigkeitsmasken</span><span class="sxs-lookup"><span data-stu-id="3c431-104">Opacity Masks Overview</span></span>

<span data-ttu-id="3c431-105">In diesem Thema wird beschrieben, wie Bitmaps und Pinsel zum Definieren von Deck Kraft Masken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c431-105">This topic describes how to use bitmaps and brushes to define opacity masks.</span></span> <span data-ttu-id="3c431-106">Der Abschnitt ist wie folgt gegliedert.</span><span class="sxs-lookup"><span data-stu-id="3c431-106">It contains the following sections.</span></span>

-   [<span data-ttu-id="3c431-107">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3c431-107">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="3c431-108">Was ist eine Deck Kraft Maske?</span><span class="sxs-lookup"><span data-stu-id="3c431-108">What Is an Opacity Mask?</span></span>](#what-is-an-opacity-mask)
-   [<span data-ttu-id="3c431-109">Verwenden einer Bitmap als Deck Kraft Maske mit der fillopacitymask-Methode</span><span class="sxs-lookup"><span data-stu-id="3c431-109">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>](#use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method)
-   [<span data-ttu-id="3c431-110">Verwenden eines Pinsels als Deck Kraft Maske mit der fillgeometry-Methode</span><span class="sxs-lookup"><span data-stu-id="3c431-110">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>](#use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method)
    -   [<span data-ttu-id="3c431-111">Verwenden eines linearen Farbverlaufs Pinsels als Deck Kraft Maske</span><span class="sxs-lookup"><span data-stu-id="3c431-111">Use an Linear Gradient Brush as an Opacity Mask</span></span>](#use-an-linear-gradient-brush-as-an-opacity-mask)
    -   [<span data-ttu-id="3c431-112">Verwenden eines radialen Farbverlaufs Pinsels als Deck Kraft Maske</span><span class="sxs-lookup"><span data-stu-id="3c431-112">Use a Radial Gradient Brush as an Opacity Mask</span></span>](#use-a-radial-gradient-brush-as-an-opacity-mask)
-   [<span data-ttu-id="3c431-113">Anwenden einer Deck Kraft Maske auf eine Ebene</span><span class="sxs-lookup"><span data-stu-id="3c431-113">Apply an Opacity Mask to a Layer</span></span>](#apply-an-opacity-mask-to-a-layer)
-   [<span data-ttu-id="3c431-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c431-114">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="3c431-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="3c431-115">Prerequisites</span></span>

<span data-ttu-id="3c431-116">Diese Übersicht setzt voraus, dass Sie mit grundlegenden Direct2D-Zeichnungs Vorgängen vertraut sind, wie in der exemplarischen Vorgehensweise zum [Erstellen einer einfachen Direct2D-Anwendung](direct2d-quickstart.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3c431-116">This overview assumes that you are familiar with basic Direct2D drawing operations, as described in the [Creating a Simple Direct2D Application](direct2d-quickstart.md) walkthrough.</span></span> <span data-ttu-id="3c431-117">Sie sollten auch mit den verschiedenen Pinseltypen vertraut sein, wie in der [Übersicht über Pinsel](direct2d-brushes-overview.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3c431-117">You should also be familiar with the different types of brushes, as described in the [Brushes Overview](direct2d-brushes-overview.md).</span></span>

## <a name="what-is-an-opacity-mask"></a><span data-ttu-id="3c431-118">Was ist eine Deck Kraft Maske?</span><span class="sxs-lookup"><span data-stu-id="3c431-118">What Is an Opacity Mask?</span></span>

<span data-ttu-id="3c431-119">Eine Deck Kraft Maske ist eine Maske, die durch einen Pinsel oder eine Bitmap beschrieben wird, der auf ein anderes Objekt angewendet wird, um dieses Objekt teilweise oder vollständig transparent zu machen.</span><span class="sxs-lookup"><span data-stu-id="3c431-119">An opacity mask is a mask, described by a brush or bitmap, that is applied to another object to make that object partially or completely transparent.</span></span> <span data-ttu-id="3c431-120">Eine Deck Kraft Maske verwendet Alphakanal Informationen, um anzugeben, wie die Quell Pixel des Objekts in das endgültige Ziel Ziel gemischt werden.</span><span class="sxs-lookup"><span data-stu-id="3c431-120">An opacity mask uses alpha channel information to specify how the source pixels of the object are blended into the final destination target.</span></span> <span data-ttu-id="3c431-121">Die transparenten Teile der Maske geben die Bereiche an, in denen das zugrunde liegende Bild ausgeblendet ist, während die nicht transparenten Teile der Maske angeben, wo das maskierte Objekt sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="3c431-121">The transparent portions of the mask indicate the areas where the underlying image is hidden, whereas the opaque portions of the mask indicate where the masked object is visible.</span></span>

<span data-ttu-id="3c431-122">Es gibt mehrere Möglichkeiten, eine Deck Kraft Maske anzuwenden:</span><span class="sxs-lookup"><span data-stu-id="3c431-122">There are several ways to apply an opacity mask:</span></span>

-   <span data-ttu-id="3c431-123">Verwenden Sie die [**ID2D1RenderTarget:: fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3c431-123">Use the [**ID2D1RenderTarget::FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method.</span></span> <span data-ttu-id="3c431-124">Die **fillopacitymask** -Methode zeichnet einen rechteckigen Bereich eines Renderziels und wendet dann eine Deck Kraft Maske an, die durch eine Bitmap definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-124">The **FillOpacityMask** method paints a rectangular region of a render target and then applies an opacity mask, defined by a bitmap.</span></span> <span data-ttu-id="3c431-125">Verwenden Sie diese Methode, wenn die Deck Kraft Maske eine Bitmap ist und Sie einen rechteckigen Bereich auffüllen möchten.</span><span class="sxs-lookup"><span data-stu-id="3c431-125">Use this method when your opacity mask is a bitmap and you want to fill a rectangular region.</span></span>
-   <span data-ttu-id="3c431-126">Verwenden Sie die [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3c431-126">Use the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="3c431-127">Die **fillgeometry** -Methode zeichnet das Innere der Geometrie mit dem angegebenen [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)und wendet dann eine Deckkraft Maske an, die durch einen Pinsel definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-127">The **FillGeometry** method paints the interior of geometry with the specified [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), then applies an opacity mask, defined by a brush.</span></span> <span data-ttu-id="3c431-128">Verwenden Sie diese Methode, wenn Sie eine Deck Kraft Maske auf eine Geometrie anwenden möchten oder wenn Sie einen Pinsel als Deck Kraft Maske verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3c431-128">Use this method when you want to apply an opacity mask to a geometry or you want to use a brush as an opacity mask.</span></span>
-   <span data-ttu-id="3c431-129">Verwenden Sie eine [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) , um eine Deckkraft Maske anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="3c431-129">Use an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) to apply an opacity mask.</span></span> <span data-ttu-id="3c431-130">Verwenden Sie diesen Ansatz, wenn Sie eine Deck Kraft Maske auf eine Gruppe von Zeichnungs Inhalten anwenden möchten, nicht nur auf eine einzelne Form oder ein Bild.</span><span class="sxs-lookup"><span data-stu-id="3c431-130">Use this approach when you want to apply an opacity mask to a group of drawing content, not just a single shape or image.</span></span> <span data-ttu-id="3c431-131">Weitere Informationen finden Sie in der [Übersicht über Ebenen](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3c431-131">For details, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="use-a-bitmap-as-an-opacity-mask-with-the-fillopacitymask-method"></a><span data-ttu-id="3c431-132">Verwenden einer Bitmap als Deck Kraft Maske mit der fillopacitymask-Methode</span><span class="sxs-lookup"><span data-stu-id="3c431-132">Use a Bitmap as an Opacity Mask with the FillOpacityMask Method</span></span>

<span data-ttu-id="3c431-133">Die [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode zeichnet einen rechteckigen Bereich eines Renderziels und wendet dann eine Deck Kraft Maske an, die durch ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap)definiert wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-133">The [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method paints a rectangular region of a render target and then applies an opacity mask, defined by an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap).</span></span> <span data-ttu-id="3c431-134">Verwenden Sie diese Methode, wenn Sie über eine Bitmap verfügen, die Sie als Deck Kraft Maske für einen rechteckigen Bereich verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="3c431-134">Use this method when you have a bitmap that you want to use as an opacity mask for a rectangular region.</span></span>

<span data-ttu-id="3c431-135">Das folgende Diagramm zeigt die Auswirkung der Anwendung der Deck Kraft Maske (ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) mit einem Bild einer Blume) auf eine [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) mit einem Bild einer fern-Anlage.</span><span class="sxs-lookup"><span data-stu-id="3c431-135">The following diagram shows an effect of applying the opacity mask (an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) with an image of a flower) to an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) with an image of a fern plant.</span></span> <span data-ttu-id="3c431-136">Das resultierende Bild ist eine Bitmap einer Anlage, die auf die Blumenform zugeschnitten ist.</span><span class="sxs-lookup"><span data-stu-id="3c431-136">The resulting image is a bitmap of a plant clipped to the flower shape.</span></span>

![Diagramm einer Blumen Bitmap, die als Deck Kraft Maske für ein Bild einer fardrource verwendet wird](images/brushes-ovw-bitmapopacity.png)

<span data-ttu-id="3c431-138">Die folgenden Codebeispiele zeigen, wie dies erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-138">The following code examples shows how this is accomplished.</span></span>

<span data-ttu-id="3c431-139">Im ersten Beispiel wird die folgende Bitmap ( *m \_ pbitmapmask*) für die Verwendung als Bitmap-Maske geladen.</span><span class="sxs-lookup"><span data-stu-id="3c431-139">The first example loads the following bitmap, *m\_pBitmapMask*, for use as a bitmap mask.</span></span> <span data-ttu-id="3c431-140">Die folgende Abbildung zeigt die Ausgabe, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-140">The following illustration shows the output that is produced.</span></span> <span data-ttu-id="3c431-141">Beachten Sie Folgendes: Obwohl der nicht transparente Teil der Bitmap schwarz erscheint, haben die Farbinformationen in der Bitmap keine Auswirkung auf die Deck Kraft Maske. nur die Deckkraft Informationen der einzelnen Pixel in der Bitmap werden verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c431-141">Note that, although the opaque portion of the bitmap appears black, the color information in the bitmap has no effect on the opacity mask; only the opacity information of each pixel in the bitmap is used.</span></span> <span data-ttu-id="3c431-142">Die vollständig transparenten Pixel in dieser Bitmap sind nur zu Illustrations Zwecken schwarz gefärbt.</span><span class="sxs-lookup"><span data-stu-id="3c431-142">The fully opaque pixels in this bitmap have been colored black for illustrative purposes only.</span></span>

![Abbildung der Blumen Bitmap-Maske](images/bitmapmask.png)

<span data-ttu-id="3c431-144">In diesem Beispiel wird das [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) -Hilfsprogramm von einer Hilfsmethode geladen, die an anderer Stelle im Beispiel als loadresourcebitmap definiert ist.</span><span class="sxs-lookup"><span data-stu-id="3c431-144">In this example, the [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) is loaded by a helper method, LoadResourceBitmap, defined elsewhere in the sample.</span></span>


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



<span data-ttu-id="3c431-145">Im nächsten Beispiel wird der Pinsel " *m \_ pfern bitmapbrush*" definiert, auf den die Deck Kraft Maske angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-145">The next example defines the brush, *m\_pFernBitmapBrush*, to which the opacity mask is applied.</span></span> <span data-ttu-id="3c431-146">In diesem Beispiel wird ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) verwendet, das ein Bild eines fards enthält, aber Sie können stattdessen eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush)oder [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c431-146">This example uses an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that contains an image of a fern, but you could use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) instead.</span></span> <span data-ttu-id="3c431-147">Die folgende Abbildung zeigt die Ausgabe, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-147">The following illustration shows the output that is produced.</span></span>

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





<span data-ttu-id="3c431-149">Nachdem Sie nun die Deck Kraft Maske und den Pinsel definiert haben, können Sie die [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode in der Rendering-Methode Ihrer Anwendung verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c431-149">Now that opacity mask and the brush are defined, you can use the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method in your application's rendering method.</span></span> <span data-ttu-id="3c431-150">Wenn Sie die **fillopacitymask** -Methode aufzurufen, müssen Sie den Typ der von Ihnen verwendeten Deck Kraft Maske angeben: **\_ \_ \_ Inhalts \_ Grafiken der D2D1 Deck Kraft Mask**, **D2D1 \_ Deck Kraft \_ mask \_ Content \_ Text \_ Natural** und **D2D1 \_ Deck Kraft \_ mask \_ Content \_ Text \_ GDI \_ Compatible**.</span><span class="sxs-lookup"><span data-stu-id="3c431-150">When you call the **FillOpacityMask** method, you must specify the type of opacity mask you are using: **D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**, **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_NATURAL**, and **D2D1\_OPACITY\_MASK\_CONTENT\_TEXT\_GDI\_COMPATIBLE**.</span></span> <span data-ttu-id="3c431-151">Die Bedeutung dieser drei Typen finden Sie unter [**D2D1 \_ Opacity \_ mask \_ Content**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span><span class="sxs-lookup"><span data-stu-id="3c431-151">For the meanings of these three types, see [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content).</span></span>

> [!Note]  
> <span data-ttu-id="3c431-152">Ab Windows 8 ist der [**Inhalt der D2D1 \_ Opacity \_ mask \_**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3c431-152">Starting with Windows 8, the [**D2D1\_OPACITY\_MASK\_CONTENT**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content) is not required.</span></span> <span data-ttu-id="3c431-153">Weitere Informationen finden Sie unter der [**ID2D1DeviceContext:: fillopacitymask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) -Methode, die über keinen Content-Parameter der **D2D1 \_ Opacity \_ mask \_** verfügt.</span><span class="sxs-lookup"><span data-stu-id="3c431-153">See the [**ID2D1DeviceContext::FillOpacityMask**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-fillopacitymask(id2d1bitmap_id2d1brush_constd2d1_rect_f_constd2d1_rect_f)) method, which has no **D2D1\_OPACITY\_MASK\_CONTENT** parameter.</span></span>

 

<span data-ttu-id="3c431-154">Im nächsten Beispiel wird der Antialiasing Modus des Renderziels auf [**D2D1 \_ Antialias \_ Mode \_ Aliasing**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) festgelegt, sodass die Deck Kraft Maske ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3c431-154">The next example sets the render target's antialiasing mode to [**D2D1\_ANTIALIAS\_MODE\_ALIASED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_antialias_mode) so that the opacity mask will work properly.</span></span> <span data-ttu-id="3c431-155">Anschließend ruft er die [**fillopacitymask**](id2d1rendertarget-fillopacitymask.md) -Methode auf und übergibt ihm die Deck Kraft Maske (*m \_ pbitmapmask*), den Pinsel, auf den die Deck Kraft Maske angewendet wird (*m \_ pfern bitmapbrush*), den Inhaltstyp in der Deck Kraft Maske ([**D2D1 \_ Deck Kraft \_ mask \_ Content \_ graphics**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)) und den Bereich, der gezeichnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c431-155">It then calls the [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) method and passes it the opacity mask (*m\_pBitmapMask*), the brush to which the opacity mask is applied (*m\_pFernBitmapBrush*), the type of content inside the opacity mask ([**D2D1\_OPACITY\_MASK\_CONTENT\_GRAPHICS**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_opacity_mask_content)), and the area to paint.</span></span> <span data-ttu-id="3c431-156">Die folgende Abbildung zeigt die Ausgabe, die erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-156">The following illustration shows the output that is produced.</span></span>

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





<span data-ttu-id="3c431-158">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="3c431-158">Code has been omitted from this example.</span></span>

## <a name="use-a-brush-as-an-opacity-mask-with-the-fillgeometry-method"></a><span data-ttu-id="3c431-159">Verwenden eines Pinsels als Deck Kraft Maske mit der fillgeometry-Methode</span><span class="sxs-lookup"><span data-stu-id="3c431-159">Use a Brush as an Opacity Mask with the FillGeometry Method</span></span>

<span data-ttu-id="3c431-160">Im vorherigen Abschnitt wurde beschrieben, wie ein [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) als Deck Kraft Maske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-160">The preceding section described how to use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) as an opacity mask.</span></span> <span data-ttu-id="3c431-161">Direct2D bietet außerdem die [**ID2D1RenderTarget:: fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode, die es Ihnen ermöglicht, beim Ausfüllen eines [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)optional Pinsel als Deck Kraft Maske anzugeben.</span><span class="sxs-lookup"><span data-stu-id="3c431-161">Direct2D also provides the [**ID2D1RenderTarget::FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, which enables you to optionally specify brush as an opacity mask when you fill an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry).</span></span> <span data-ttu-id="3c431-162">Dies ermöglicht es Ihnen, Deck Kraft Masken aus Farbverläufen (mit [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) oder [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) und Bitmaps (mithilfe von **ID2D1Bitmap**) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3c431-162">This enables you to create opacity masks from gradients (using [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) or [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)) and bitmaps (using **ID2D1Bitmap**).</span></span>

<span data-ttu-id="3c431-163">Die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode nimmt drei Parameter an:</span><span class="sxs-lookup"><span data-stu-id="3c431-163">The [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method takes three parameters:</span></span>

-   <span data-ttu-id="3c431-164">Der erste Parameter, ein [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), definiert die zu zeichnende Form.</span><span class="sxs-lookup"><span data-stu-id="3c431-164">The first parameter, an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry), defines the shape to paint.</span></span>
-   <span data-ttu-id="3c431-165">Der zweite Parameter, ein [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), gibt den Pinsel an, der zum Zeichnen der Geometrie verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-165">The second parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies the brush used to paint the geometry.</span></span> <span data-ttu-id="3c431-166">Dieser Parameter muss ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) sein, dessen x-und y-Erweiterungs Modi auf die [**D2D1 Erweiterungs \_ Modus \_ - \_ Klammer**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="3c431-166">This parameter must be an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) that has its x- and y-extend modes set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>
-   <span data-ttu-id="3c431-167">Der dritte Parameter, ein [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), gibt einen Pinsel an, der als Deck Kraft Maske verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c431-167">The third parameter, an [**ID2D1Brush**](/windows/win32/api/d2d1/nn-d2d1-id2d1brush), specifies a brush to use as the opacity mask.</span></span> <span data-ttu-id="3c431-168">Dieser Pinsel kann ein [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush)oder ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush)sein.</span><span class="sxs-lookup"><span data-stu-id="3c431-168">This brush may be an [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush), [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush), or an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush).</span></span> <span data-ttu-id="3c431-169">(Technisch gesehen können Sie eine [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)verwenden, aber die Verwendung eines voll Tonfarbe-Pinsels als Deck Kraft Maske erzeugt keine interessanten Ergebnisse.)</span><span class="sxs-lookup"><span data-stu-id="3c431-169">(Technically, you may use an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush), but using a solid color brush as an opacity mask doesn't produce interesting results.)</span></span>

<span data-ttu-id="3c431-170">In den folgenden Abschnitten wird beschrieben, wie [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) -und [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) -Objekte als Deck Kraft Masken verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3c431-170">The following sections describe how to use [**ID2D1LinearGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1lineargradientbrush) and [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) objects as opacity masks.</span></span>

### <a name="use-an-linear-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="3c431-171">Verwenden eines linearen Farbverlaufs Pinsels als Deck Kraft Maske</span><span class="sxs-lookup"><span data-stu-id="3c431-171">Use an Linear Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="3c431-172">Das folgende Diagramm zeigt die Auswirkung der Anwendung eines linearen Farbverlaufs Pinsels auf ein Rechteck, das mit einer Bitmap von Blumen gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="3c431-172">The following diagram shows the effect of applying a linear gradient brush to a rectangle that is filled with a bitmap of flowers.</span></span>

![Diagramm einer Blumen Bitmap, auf die ein linearer Farbverlaufs Pinsel angewendet wird](images/brushes-ovw-lineargradient-opacitymask.png)

<span data-ttu-id="3c431-174">In den folgenden Schritten wird beschrieben, wie dieser Effekt neu erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-174">The steps that follow describe how to re-create this effect.</span></span>

1.  <span data-ttu-id="3c431-175">Definieren Sie den Inhalt, der maskiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3c431-175">Define the content to be masked.</span></span> <span data-ttu-id="3c431-176">Im folgenden Beispiel wird ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ plinearfadeflowersbitmap*, erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c431-176">The following example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pLinearFadeFlowersBitmap*.</span></span> <span data-ttu-id="3c431-177">Der Erweiterungs Modus x-und y-für *m \_ plinearfadeflowersbitmap* ist auf [**D2D1 \_ Extend \_ Mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) festgelegt, sodass er mit einer Deckkraft Maske von der [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3c431-177">The extend mode x- and y- for *m\_pLinearFadeFlowersBitmap* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode) so that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span>

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
    <th><span data-ttu-id="3c431-178">C++</span><span class="sxs-lookup"><span data-stu-id="3c431-178">C++</span></span></th>
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
    <th><span data-ttu-id="3c431-179">C++</span><span class="sxs-lookup"><span data-stu-id="3c431-179">C++</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><pre><code>            }</code></pre></td>
    </tr>
    </tbody>
    </table>

    

2.  <span data-ttu-id="3c431-180">Definieren Sie die Deckkraft Maske.</span><span class="sxs-lookup"><span data-stu-id="3c431-180">Define the opacity mask.</span></span> <span data-ttu-id="3c431-181">Im nächsten Codebeispiel wird ein diagonaler linearer Farbverlaufs Pinsel (*m \_ plineargradientbrush*) erstellt, der von vollständig undurchsichtigem schwarz an Position 0 bis vollständig transparent weiß an Position 1 verschwindet.</span><span class="sxs-lookup"><span data-stu-id="3c431-181">The next code example creates a diagonal linear gradient brush (*m\_pLinearGradientBrush*) that fades from fully opaque black at position 0 to completely transparent white at position 1.</span></span>
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



    

3.  <span data-ttu-id="3c431-182">Verwenden Sie die [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3c431-182">Use the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method.</span></span> <span data-ttu-id="3c431-183">Im letzten Beispiel wird die **fillgeometry** -Methode für den Content-Pinsel verwendet, um ein [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ prectgeography*) mit einem [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ plinearfadeflowersbitmap*) zu füllen und eine Deck Kraft Maske (*m \_ plineargradientbrush*) anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="3c431-183">The final example uses the **FillGeometry** method to the content brush to fill a [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*) with an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pLinearFadeFlowersBitmap*) and applies an opacity mask (*m\_pLinearGradientBrush*).</span></span>
```C++
            m_pRenderTarget->FillGeometry(
                m_pRectGeo, 
                m_pLinearFadeFlowersBitmapBrush, 
                m_pLinearGradientBrush
                );
```

    

<span data-ttu-id="3c431-184">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="3c431-184">Code has been omitted from this example.</span></span>

### <a name="use-a-radial-gradient-brush-as-an-opacity-mask"></a><span data-ttu-id="3c431-185">Verwenden eines radialen Farbverlaufs Pinsels als Deck Kraft Maske</span><span class="sxs-lookup"><span data-stu-id="3c431-185">Use a Radial Gradient Brush as an Opacity Mask</span></span>

<span data-ttu-id="3c431-186">Das folgende Diagramm zeigt den visuellen Effekt der Anwendung eines radialen Farbverlaufs Pinsels auf ein Rechteck, das mit einer Bitmap mit einem Laub gefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="3c431-186">The following diagram shows the visual effect of applying a radial gradient brush to a rectangle that is filled with a bitmap of foliage.</span></span>

![Diagramm einer laubbitmap mit angewendetem radialen Farbverlaufs Pinsel](images/brushes-ovw-radialgradient-opacitymask.png)

<span data-ttu-id="3c431-188">Im ersten Beispiel wird ein [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m \_ pradialfadeflowersbitmapbrush*, erstellt.</span><span class="sxs-lookup"><span data-stu-id="3c431-188">The first example creates an [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush), *m\_pRadialFadeFlowersBitmapBrush*.</span></span> <span data-ttu-id="3c431-189">Damit Sie mit einer Deck Kraft Maske von der [**fillgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) -Methode verwendet werden kann, wird der Erweiterungs Modus x-und y-für *m \_ pradialfadeflowersbitmapbrush* auf [**D2D1 \_ Extend \_ Mode \_ Clamp**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode)festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3c431-189">So that it can be used with an opacity mask by the [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) method, the extend mode x- and y- for *m\_pRadialFadeFlowersBitmapBrush* are set to [**D2D1\_EXTEND\_MODE\_CLAMP**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_extend_mode).</span></span>


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
<th><span data-ttu-id="3c431-190">C++</span><span class="sxs-lookup"><span data-stu-id="3c431-190">C++</span></span></th>
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
<th><span data-ttu-id="3c431-191">C++</span><span class="sxs-lookup"><span data-stu-id="3c431-191">C++</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>            }</code></pre></td>
</tr>
</tbody>
</table>



<span data-ttu-id="3c431-192">Im nächsten Beispiel wird der radiale Farbverlaufs Pinsel definiert, der als Deck Kraft Maske verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3c431-192">The next example defines the radial gradient brush that will be used as the opacity mask.</span></span>


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





<span data-ttu-id="3c431-193">Im letzten Codebeispiel wird das [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m \_ pradialfadeflowersbitmapbrush*) und die Deck Kraft Maske (*m \_ pradialgradientbrush*) zum Ausfüllen eines [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m \_ prectbrush*) verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c431-193">The final code example uses the [**ID2D1BitmapBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmapbrush) (*m\_pRadialFadeFlowersBitmapBrush*) and the opacity mask (*m\_pRadialGradientBrush*) to fill an [**ID2D1RectangleGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1rectanglegeometry) (*m\_pRectGeo*).</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            m_pRectGeo,
            m_pRadialFadeFlowersBitmapBrush, 
            m_pRadialGradientBrush
            );
```



<span data-ttu-id="3c431-194">Code wurde in diesem Beispiel ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="3c431-194">Code has been omitted from this example.</span></span>

## <a name="apply-an-opacity-mask-to-a-layer"></a><span data-ttu-id="3c431-195">Anwenden einer Deck Kraft Maske auf eine Ebene</span><span class="sxs-lookup"><span data-stu-id="3c431-195">Apply an Opacity Mask to a Layer</span></span>

<span data-ttu-id="3c431-196">Wenn Sie [**pushlayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) aufzurufen, um ein [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) -Element auf ein Renderziel zu übertragen, können Sie die [**D2D1 \_ Layer \_ Parameters**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) -Struktur verwenden, um einen Pinsel als Deck Kraft Maske zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3c431-196">When you call [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer)) to push an [**ID2D1Layer**](/windows/win32/api/d2d1/nn-d2d1-id2d1layer) onto an render target, you can use the [**D2D1\_LAYER\_PARAMETERS**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_layer_parameters) structure to apply a brush as an opacity mask.</span></span> <span data-ttu-id="3c431-197">Im folgenden Codebeispiel wird ein [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) als Deck Kraft Maske verwendet.</span><span class="sxs-lookup"><span data-stu-id="3c431-197">The following code example uses an [**ID2D1RadialGradientBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1radialgradientbrush) as an opacity mask.</span></span>


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



<span data-ttu-id="3c431-198">Weitere Informationen zum Verwenden von Ebenen finden Sie unter [Übersicht über Ebenen](direct2d-layers-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3c431-198">For more information about using layers, see the [Layers Overview](direct2d-layers-overview.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c431-199">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="3c431-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c431-200">Übersicht über Pinsel</span><span class="sxs-lookup"><span data-stu-id="3c431-200">Brushes Overview</span></span>](direct2d-brushes-overview.md)
</dt> <dt>

[<span data-ttu-id="3c431-201">Übersicht über Schichten</span><span class="sxs-lookup"><span data-stu-id="3c431-201">Layers Overview</span></span>](direct2d-layers-overview.md)
</dt> </dl>

 

 