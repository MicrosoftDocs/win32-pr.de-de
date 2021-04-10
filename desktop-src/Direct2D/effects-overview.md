---
title: Effekte (Direct2D)
description: Eine Übersicht über Direct2D-Effekte.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0dd29a4b2968e91bd0d516a74ec01538f69821bb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039357"
---
# <a name="effects"></a><span data-ttu-id="02466-103">Effekte</span><span class="sxs-lookup"><span data-stu-id="02466-103">Effects</span></span>

## <a name="what-are-direct2d-effects"></a><span data-ttu-id="02466-104">Was sind Direct2D-Effekte?</span><span class="sxs-lookup"><span data-stu-id="02466-104">What are Direct2D effects?</span></span>

<span data-ttu-id="02466-105">Mit Direct2D können Sie eine oder mehrere hochwertige Effekte auf ein Bild oder einen Satz von Bildern anwenden.</span><span class="sxs-lookup"><span data-stu-id="02466-105">You can use Direct2D to apply one or more high quality effects to an image or a set of images.</span></span> <span data-ttu-id="02466-106">Die Effekte-APIs basieren auf [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) und nutzen GPU-Features für die Bildverarbeitung.</span><span class="sxs-lookup"><span data-stu-id="02466-106">The effects APIs are built on [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) and take advantage of GPU features for image processing.</span></span> <span data-ttu-id="02466-107">Sie können Effekte in einem Effekt Diagramm verketten und die Ausgabe von Effekten verfassen oder mischen.</span><span class="sxs-lookup"><span data-stu-id="02466-107">You can chain effects in an effect graph and compose or blend the output of effects.</span></span>

<span data-ttu-id="02466-108">Ein Direct2D-Effekt führt einen Abbild Erstellungs Task aus, wie z. b. das Ändern der Helligkeit, das desätalisieren eines Bilds oder das Erstellen eines</span><span class="sxs-lookup"><span data-stu-id="02466-108">A Direct2D effect performs an imaging task, like changing brightness, de-saturating an image, or creating a drop shadow.</span></span> <span data-ttu-id="02466-109">Effekte können NULL oder mehr Eingabe Bilder akzeptieren, mehrere Eigenschaften verfügbar machen, die ihren Vorgang steuern, und ein einzelnes Ausgabe Bild generieren.</span><span class="sxs-lookup"><span data-stu-id="02466-109">Effects can accept zero or more input images, expose multiple properties that control their operation, and generate a single output image.</span></span>

<span data-ttu-id="02466-110">Jeder Effekt erstellt ein internes Transformations Diagramm, das aus einzelnen Transformationen besteht.</span><span class="sxs-lookup"><span data-stu-id="02466-110">Each effect creates an internal transform graph made up of individual transforms.</span></span> <span data-ttu-id="02466-111">Jede Transformation stellt einen einzelnen Bild Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="02466-111">Each transform represents a single image operation.</span></span> <span data-ttu-id="02466-112">Der Hauptzweck einer Transformation besteht darin, die Shader zu beherbergen, die für jedes Ausgabe Pixel ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="02466-112">The main purpose of a transform is to house the shaders that are executed for each output pixel.</span></span> <span data-ttu-id="02466-113">Diese Shader können Pixel-Shader, Vertex-Shader, die Blend-Phase einer GPU und Compute-Shader enthalten.</span><span class="sxs-lookup"><span data-stu-id="02466-113">These shaders can include pixel shaders, vertex shaders, the blend stage of a GPU, and compute shaders.</span></span>

<span data-ttu-id="02466-114">Die [integrierten Effekte](built-in-effects.md) von [Direct2D](./direct2d-portal.md) und benutzerdefinierte Effekte, die Sie mithilfe der [API für benutzerdefinierte Effekte](custom-effects.md) treffen können, funktionieren auf diese Weise.</span><span class="sxs-lookup"><span data-stu-id="02466-114">Both the [Direct2D](./direct2d-portal.md) [built-in effects](built-in-effects.md) and custom effects you can make using the [custom effects API](custom-effects.md) work this way.</span></span>

<span data-ttu-id="02466-115">Es gibt eine Reihe [integrierter Effekte](built-in-effects.md) aus Kategorien, wie hier beschrieben.</span><span class="sxs-lookup"><span data-stu-id="02466-115">There are a range of [built-in effects](built-in-effects.md) from categories like the ones here.</span></span> <span data-ttu-id="02466-116">Eine vollständige Liste finden Sie im Abschnitt [integrierte Effekte](built-in-effects.md) .</span><span class="sxs-lookup"><span data-stu-id="02466-116">See the [Built-in Effects](built-in-effects.md) section for a full list.</span></span>

-   [<span data-ttu-id="02466-117">Filterung</span><span class="sxs-lookup"><span data-stu-id="02466-117">Filtering</span></span>](built-in-effects.md)
-   [<span data-ttu-id="02466-118">Komposition und Vermischung</span><span class="sxs-lookup"><span data-stu-id="02466-118">Composition and Blending</span></span>](built-in-effects.md)
-   [<span data-ttu-id="02466-119">Transparenz</span><span class="sxs-lookup"><span data-stu-id="02466-119">Transparency</span></span>](built-in-effects.md)
-   [<span data-ttu-id="02466-120">Farbe</span><span class="sxs-lookup"><span data-stu-id="02466-120">Color</span></span>](built-in-effects.md)
-   [<span data-ttu-id="02466-121">Beleuchtung und stilialisierung</span><span class="sxs-lookup"><span data-stu-id="02466-121">Lighting and Stylizing</span></span>](built-in-effects.md)
-   [<span data-ttu-id="02466-122">Transformieren und Skalieren</span><span class="sxs-lookup"><span data-stu-id="02466-122">Transforming and Scaling</span></span>](built-in-effects.md)
-   [<span data-ttu-id="02466-123">Sources</span><span class="sxs-lookup"><span data-stu-id="02466-123">Sources</span></span>](built-in-effects.md)

<span data-ttu-id="02466-124">Sie können Effekte auf jede beliebige Bitmap anwenden, einschließlich der von der [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api)geladenen Bilder, primitiver Zeichen, die von [Direct2D](./direct2d-portal.md)gezeichnet werden, von Text aus [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)oder von [Direct3D](/windows/desktop/direct3d10/d3d10-graphics)gerenderten Szenen.</span><span class="sxs-lookup"><span data-stu-id="02466-124">You can apply effects to any bitmap, including: images loaded by the [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api), primitives drawn by [Direct2D](./direct2d-portal.md), text from [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal), or scenes rendered by [Direct3D](/windows/desktop/direct3d10/d3d10-graphics).</span></span>

<span data-ttu-id="02466-125">Mit Direct2D-Effekten können Sie eigene Effekte schreiben, die Sie für Ihre Anwendungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="02466-125">With Direct2D effects you can write your own effects that you can use for your applications.</span></span> <span data-ttu-id="02466-126">Mithilfe eines benutzerdefinierten Effekts-Frameworks können Sie GPU-Funktionen wie Pixel-Shader, Vertex-Shader und die Mischungs Einheit verwenden.</span><span class="sxs-lookup"><span data-stu-id="02466-126">A custom effect framework allows you to use GPU features such as pixel shaders, vertex shaders, and the blending unit.</span></span> <span data-ttu-id="02466-127">Sie können auch andere integrierte oder benutzerdefinierte Effekte in Ihren benutzerdefinierten Effekt einschließen.</span><span class="sxs-lookup"><span data-stu-id="02466-127">You can also include other built-in or custom effects in your custom effect.</span></span> <span data-ttu-id="02466-128">Das Framework zum Erstellen von benutzerdefinierten Effekten ist das gleiche, das verwendet wurde, um die integrierten Effekte von [Direct2D](./direct2d-portal.md)zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02466-128">The framework for building custom effects is the same one that was used to create the built-in effects of [Direct2D](./direct2d-portal.md).</span></span> <span data-ttu-id="02466-129">Die [Direct2D Effect Author-API](custom-effects.md) stellt eine Reihe von Schnittstellen zum Erstellen und Registrieren von Effekten bereit.</span><span class="sxs-lookup"><span data-stu-id="02466-129">The [Direct2D effect author API](custom-effects.md) provides a set of interfaces to create and register effects.</span></span>

### <a name="more-effects-topics"></a><span data-ttu-id="02466-130">Themen zu weiteren Effekten</span><span class="sxs-lookup"><span data-stu-id="02466-130">More effects topics</span></span>

<span data-ttu-id="02466-131">Im weiteren Verlauf dieses Themas werden die Grundlagen von Direct2D Effekten erläutert, wie z. b. das Anwenden eines Effekts auf ein Bild.</span><span class="sxs-lookup"><span data-stu-id="02466-131">The rest of this topic explains the basics of Direct2D effects, like applying an effect to an image.</span></span> <span data-ttu-id="02466-132">Die Tabelle enthält Links zu weiteren Themen zu den Auswirkungen.</span><span class="sxs-lookup"><span data-stu-id="02466-132">The table here has links to additional topics about effects.</span></span>

| <span data-ttu-id="02466-133">Thema</span><span class="sxs-lookup"><span data-stu-id="02466-133">Topic</span></span>                                                                                                                    | <span data-ttu-id="02466-134">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="02466-134">Description</span></span>                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="02466-135">Effektshader-Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="02466-135">Effect Shader Linking</span></span>](effect-shader-linking.md)<br/>                                                            | <span data-ttu-id="02466-136">Direct2D verwendet eine Optimierung namens "Effect Shader Linking", die das Rendering mehrerer Effekte Diagramm Rendering in einem einzigen Durchlauf kombiniert.</span><span class="sxs-lookup"><span data-stu-id="02466-136">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span><br/>                                               |
| [<span data-ttu-id="02466-137">Benutzerdefinierte Effekte</span><span class="sxs-lookup"><span data-stu-id="02466-137">Custom effects</span></span>](custom-effects.md)<br/>                                                                          | <span data-ttu-id="02466-138">Zeigt, wie Sie Ihre eigenen benutzerdefinierten Effekte mit dem Standard-HLSL schreiben.</span><span class="sxs-lookup"><span data-stu-id="02466-138">Shows you how to write your own custom effects using standard HLSL.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="02466-139">Laden eines Bilds in Direct2D Effekte mithilfe der Dateiauswahl</span><span class="sxs-lookup"><span data-stu-id="02466-139">How to load an image into Direct2D Effects using the FilePicker</span></span>](load-a-id2d1image-using-the-filepicker.md)<br/> | <span data-ttu-id="02466-140">Veranschaulicht die Verwendung von [**Windows:: Storage::P icker:: fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) zum Laden eines Bilds in Direct2D-Effekte.</span><span class="sxs-lookup"><span data-stu-id="02466-140">Shows how to use the [**Windows::Storage::Pickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) to load an image into Direct2D effects.</span></span><br/>                                      |
| [<span data-ttu-id="02466-141">Speichern von Direct2D-Inhalten in einer Bilddatei</span><span class="sxs-lookup"><span data-stu-id="02466-141">How to save Direct2D content to an image file</span></span>](save-direct2d-content-to-an-image-file.md)<br/>                   | <span data-ttu-id="02466-142">In diesem Thema wird gezeigt, wie [**iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) verwendet wird, um Inhalt in Form einer [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in einer codierten Bilddatei (z. b. JPEG) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="02466-142">This topic shows how to use [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) to save content in the form of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) to an encoded image file such as JPEG.</span></span><br/> |
| [<span data-ttu-id="02466-143">Anwenden von Effekten auf primitive</span><span class="sxs-lookup"><span data-stu-id="02466-143">How to Apply Effects to Primitives</span></span>](how-to-apply-effects-to-primitives.md)<br/>                                  | <span data-ttu-id="02466-144">In diesem Thema wird gezeigt, wie Sie eine Reihe von Effekten auf [Direct2D](./direct2d-portal.md) und [DirectWrite](direct2d-and-directwrite.md) -primitive anwenden.</span><span class="sxs-lookup"><span data-stu-id="02466-144">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span><br/>                           |
| [<span data-ttu-id="02466-145">Steuern der Genauigkeit und des numerischen Clipping in Effekt Diagrammen</span><span class="sxs-lookup"><span data-stu-id="02466-145">Controlling Precision and Numerical Clipping in Effect Graphs</span></span>](precision-and-clipping-in-effect-graphs.md)<br/>  | <span data-ttu-id="02466-146">Anwendungen, die Effekte mithilfe von Direct2D renderingeffekte darstellen, müssen darauf achten, dass die gewünschte Qualität und Vorhersagbarkeit hinsichtlich der numerischen Genauigkeit erreicht wird.</span><span class="sxs-lookup"><span data-stu-id="02466-146">Applications that render effects using Direct2D must take care to achieve the desired level of quality and predictability with respect to numerical precision.</span></span> <br/>                    |

## <a name="applying-an-effect-to-an-image"></a><span data-ttu-id="02466-147">Anwenden eines Effekts auf ein Bild</span><span class="sxs-lookup"><span data-stu-id="02466-147">Applying an effect to an image</span></span>

<span data-ttu-id="02466-148">Mit der Direct2D Effects-API können Sie Transformationen auf Bilder anwenden.</span><span class="sxs-lookup"><span data-stu-id="02466-148">You can use the Direct2D effects API to apply transforms to images.</span></span>

> [!Note]  
> <span data-ttu-id="02466-149">In diesem Beispiel wird davon ausgegangen, dass Sie bereits [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -und [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) -Objekte erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="02466-149">This example assumes that you already have [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) and [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) objects created.</span></span> <span data-ttu-id="02466-150">Weitere Informationen zum Erstellen dieser Objekte finden Sie unter Gewusst [wie: Laden eines Bilds in Direct2D Effekte mithilfe der Datei](load-a-id2d1image-using-the-filepicker.md) Auswahl und [Geräte und Geräte Kontexte](devices-and-device-contexts.md).</span><span class="sxs-lookup"><span data-stu-id="02466-150">For more information on creating these objects see [How to load an image into Direct2D effects using the FilePicker](load-a-id2d1image-using-the-filepicker.md) and [Devices and Device Contexts](devices-and-device-contexts.md).</span></span>

 

1.  <span data-ttu-id="02466-151">Deklarieren Sie eine [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Variable, und erstellen Sie dann mithilfe der [**ID2DDeviceContext:: kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) -Methode einen [Bitmap-Quell](bitmap-source.md) Effekt.</span><span class="sxs-lookup"><span data-stu-id="02466-151">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create a [bitmap source](bitmap-source.md) effect using the [**ID2DDeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method.</span></span>

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  <span data-ttu-id="02466-152">Legen Sie die Eigenschaft BitmapSource mithilfe von [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))auf die WIC-Bitmapquelle fest.</span><span class="sxs-lookup"><span data-stu-id="02466-152">Set the BitmapSource property to the WIC bitmap source using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)).</span></span>

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  <span data-ttu-id="02466-153">Deklarieren Sie eine [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Variable, und erstellen Sie dann den [Gaußschen](gaussian-blur.md) weich Effekt.</span><span class="sxs-lookup"><span data-stu-id="02466-153">Declare an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) variable and then create the [gaussian blur](gaussian-blur.md) effect.</span></span>

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  <span data-ttu-id="02466-154">Legen Sie die Eingabe fest, um das Bild aus dem Bitmap-Quell Effekt zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="02466-154">Set the input to receive the image from the bitmap source effect.</span></span> <span data-ttu-id="02466-155">Legen Sie den weichungs Betrag der [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode und der Standardabweichung-Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="02466-155">Set the blur amount the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method and the standard deviation property.</span></span>

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  <span data-ttu-id="02466-156">Verwenden Sie den Gerätekontext, um die resultierende Bild Ausgabe zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="02466-156">Use the device context to draw the resulting image output.</span></span>

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    <span data-ttu-id="02466-157">Die [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) -Methode muss zwischen den [**ID2DDeviceContext:: beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -und [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -aufrufen wie andere Direct2D-Rendering-Vorgänge aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="02466-157">The [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method must be called between the [**ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) and [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) calls like other Direct2D render operations.</span></span> <span data-ttu-id="02466-158">**DrawImage** kann ein Bild oder die Ausgabe eines Effekts annehmen und es auf der Ziel Oberfläche Rendering.</span><span class="sxs-lookup"><span data-stu-id="02466-158">**DrawImage** can take an image or the output of an effect and render it to the target surface.</span></span>

## <a name="spatial-transforms"></a><span data-ttu-id="02466-159">Räumliche Transformationen</span><span class="sxs-lookup"><span data-stu-id="02466-159">Spatial Transforms</span></span>

<span data-ttu-id="02466-160">Direct2D bietet integrierte Effekte, die Bilder im 2D-und 3D-Raum sowie die Skalierung transformieren können.</span><span class="sxs-lookup"><span data-stu-id="02466-160">Direct2D provides built-in effects that can transform images in 2D and 3D space, as well as scaling.</span></span> <span data-ttu-id="02466-161">Die Auswirkungen auf die Skalierung und Transformation bieten verschiedene Qualitätsstufen, wie z. b. die nächstgelegene Nachbar-, lineare, kubische, Multisample-linear, Anisotropic und High Quality-kubische</span><span class="sxs-lookup"><span data-stu-id="02466-161">The scale and transform effects offer various quality levels like: nearest neighbor, linear, cubic, multi-sample linear, anisotropic, and high quality cubic.</span></span>

> [!Note]  
> <span data-ttu-id="02466-162">Der anisotrope Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für die Transformation eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.</span><span class="sxs-lookup"><span data-stu-id="02466-162">Anisotropic mode generates mipmaps when scaling, however, if you set the **Cached** property to true on the effects that are input to the transform the mipmaps won't be generated every time for sufficiently small images.</span></span>

 


```C++
ComPtr<ID2D1Effect> affineTransformEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));

affineTransformEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F(0.9f, -0.1f,  0.1f, 0.9f, 8.0f, 45.0f);
DX::ThrowIfFailed(affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(affineTransformEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="02466-163">Durch diese Verwendung des 2D-affinen Transformations Effekts wird die Bitmap leicht gegen den Uhrzeigersinn gedreht.</span><span class="sxs-lookup"><span data-stu-id="02466-163">This use of the 2D affine transform effect rotates the bitmap counterclockwise slightly.</span></span>



| <span data-ttu-id="02466-164">Vorher</span><span class="sxs-lookup"><span data-stu-id="02466-164">Before</span></span>                                                            |
|-------------------------------------------------------------------|
| ![2D-Affinität vor dem Bild.](images/default-before.jpg)      |
| <span data-ttu-id="02466-166">Nach</span><span class="sxs-lookup"><span data-stu-id="02466-166">After</span></span>                                                             |
| ![2D-Affinität nach dem Bild.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a><span data-ttu-id="02466-168">Zusammengesetzte Images</span><span class="sxs-lookup"><span data-stu-id="02466-168">Compositing images</span></span>

<span data-ttu-id="02466-169">Bei einigen Effekten werden mehrere Eingaben akzeptiert und in einem resultierenden Bild zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="02466-169">Some effects accept multiple inputs and composite them into one resulting image.</span></span>

<span data-ttu-id="02466-170">Die integrierten zusammengesetzten und arithmetischen zusammengesetzten Effekte bieten verschiedene Modi. Weitere Informationen finden Sie im zusammen [gesetzten](composite.md) Thema.</span><span class="sxs-lookup"><span data-stu-id="02466-170">The built-in composite and arithmetic composite effects provide various modes, for more info see the [composite](composite.md) topic.</span></span> <span data-ttu-id="02466-171">Der [Blend](blend.md) -Effekt bietet eine Vielzahl von verfügbaren GPU-Modi.</span><span class="sxs-lookup"><span data-stu-id="02466-171">The [blend](blend.md) effect has a variety of GPU accelerated modes available.</span></span>


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="02466-172">Der zusammengesetzte Effekt kombiniert Bilder auf verschiedene Weise entsprechend dem von Ihnen angegebenen Modus.</span><span class="sxs-lookup"><span data-stu-id="02466-172">The composite effect combines images in various different ways according to the mode you specify.</span></span>

## <a name="pixel-adjustments"></a><span data-ttu-id="02466-173">Pixel Anpassungen</span><span class="sxs-lookup"><span data-stu-id="02466-173">Pixel adjustments</span></span>

<span data-ttu-id="02466-174">Es gibt einige integrierte Direct2D Effekte, mit denen Sie die Pixeldaten ändern können.</span><span class="sxs-lookup"><span data-stu-id="02466-174">There are a few built-in Direct2D effects that allow you to alter the pixel data.</span></span> <span data-ttu-id="02466-175">Beispielsweise kann der Farbmatrix Effekt verwendet werden, um die Farbe eines Bilds zu ändern.</span><span class="sxs-lookup"><span data-stu-id="02466-175">For example, the color matrix effect can be used to change the color of an image.</span></span>


```C++
ComPtr<ID2D1Effect> colorMatrixEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1ColorMatrix, &colorMatrixEffect));

colorMatrixEffect->SetInput(0, bitmap.Get());

D2D1_MATRIX_5X4_F matrix = D2D1::Matrix5x4F(0, 0, 1, 0,   0, 1, 0, 0,   1, 0, 0, 0,   0, 0, 0, 1,   0, 0, 0, 0);
DX::ThrowIfFailed(colorMatrixEffect->SetValue(D2D1_COLORMATRIX_PROP_COLOR_MATRIX, matrix));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(colorMatrixEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="02466-176">Dieser Code nimmt das Bild an und ändert die Farbe, wie in den Beispielbildern hier gezeigt.</span><span class="sxs-lookup"><span data-stu-id="02466-176">This code takes the image and alters the color as shown in the example images here.</span></span>



| <span data-ttu-id="02466-177">Vorher</span><span class="sxs-lookup"><span data-stu-id="02466-177">Before</span></span>                                                          |
|-----------------------------------------------------------------|
| ![der Farbmatrix Effekt vor dem Bild.](images/default-before.jpg) |
| <span data-ttu-id="02466-179">Nach</span><span class="sxs-lookup"><span data-stu-id="02466-179">After</span></span>                                                           |
| ![Farbmatrix Effekt nach Bild.](images/15-colormatrix.png)  |



 

<span data-ttu-id="02466-181">Weitere Informationen finden Sie im Abschnitt [Color-integrierte Effekte](how-to-create-a-solid-color-brush.md) .</span><span class="sxs-lookup"><span data-stu-id="02466-181">See the [color built-in effects](how-to-create-a-solid-color-brush.md) section for more info.</span></span>

## <a name="building-effect-graphs"></a><span data-ttu-id="02466-182">Gebäude Effekt Diagramme</span><span class="sxs-lookup"><span data-stu-id="02466-182">Building effect graphs</span></span>

<span data-ttu-id="02466-183">Sie können Effekte verketten, um Bilder umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="02466-183">You can chain effects together to transform images.</span></span> <span data-ttu-id="02466-184">Beispielsweise wendet der Code hier einen Schatten und eine 2D-Transformation an und führt dann die Ergebnisse aus.</span><span class="sxs-lookup"><span data-stu-id="02466-184">For example, the code here applies a shadow and a 2D transform, then composites the results together.</span></span>


```C++
ComPtr<ID2D1Effect> shadowEffect;
ComPtr<ID2D1Effect> affineTransformEffect;
ComPtr<ID2D1Effect> compositeEffect;

DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect));
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

shadowEffect->SetInput(0, bitmap.Get());
affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

compositeEffect->SetInputEffect(0, affineTransformEffect.Get());
compositeEffect->SetInput(1, bitmap.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



<span data-ttu-id="02466-185">Im Folgenden wird das Ergebnis aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="02466-185">Here is the result.</span></span>

![Ausgabe des Schatten Effekts.](images/effect-overview-shadow.png)

<span data-ttu-id="02466-187">Effekte akzeptieren [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) -Objekte als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="02466-187">Effects take [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) objects as input.</span></span> <span data-ttu-id="02466-188">Sie können eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) verwenden, da die Schnittstelle von **ID2D1Image** abgeleitet ist.</span><span class="sxs-lookup"><span data-stu-id="02466-188">You can use an [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) because the interface is derived from **ID2D1Image**.</span></span> <span data-ttu-id="02466-189">Sie können auch " [**ID2D1Effect:: GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) " verwenden, um die Ausgabe eines [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Objekts als **ID2D1Image** zu erhalten, oder die **setinputeffect** -Methode verwenden, die die Ausgabe für Sie konvertiert.</span><span class="sxs-lookup"><span data-stu-id="02466-189">You can also use the [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) to get the output of an [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) object as an **ID2D1Image** or use the **SetInputEffect** method, which converts the output for you.</span></span> <span data-ttu-id="02466-190">In den meisten Fällen besteht ein Wirkungs Diagramm aus **ID2D1Effect** -Objekten, die direkt verkettet sind, sodass es einfach ist, mehrere Effekte auf ein Bild anzuwenden, um überzeugende Visualisierungen zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="02466-190">In most cases an effect graph consists of **ID2D1Effect** objects directly chained together, which makes it easy to apply multiple effects to an image to create compelling visuals.</span></span>

<span data-ttu-id="02466-191">Weitere Informationen finden [Sie unter How to Apply effects to Primitives](how-to-apply-effects-to-primitives.md) .</span><span class="sxs-lookup"><span data-stu-id="02466-191">See [How to apply effects to primitives](how-to-apply-effects-to-primitives.md) for more info.</span></span>

## <a name="related-topics"></a><span data-ttu-id="02466-192">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="02466-192">Related topics</span></span>

[<span data-ttu-id="02466-193">Beispiel für Direct2D grundlegende Bildeffekte</span><span class="sxs-lookup"><span data-stu-id="02466-193">Direct2D basic image effects sample</span></span>](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[<span data-ttu-id="02466-194">Integrierte Effekte</span><span class="sxs-lookup"><span data-stu-id="02466-194">Built-in Effects</span></span>](built-in-effects.md)