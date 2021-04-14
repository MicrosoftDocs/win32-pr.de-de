---
title: Anwenden von Effekten auf primitive
description: In diesem Thema wird gezeigt, wie Sie eine Reihe von Effekten auf Direct2D und DirectWrite-primitive anwenden.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aafb171c20c567d1fbd6385d23cc3b2925efc154
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390736"
---
# <a name="how-to-apply-effects-to-primitives"></a><span data-ttu-id="b1b50-103">Anwenden von Effekten auf primitive</span><span class="sxs-lookup"><span data-stu-id="b1b50-103">How to Apply Effects to Primitives</span></span>

<span data-ttu-id="b1b50-104">In diesem Thema wird gezeigt, wie Sie eine Reihe von Effekten auf [Direct2D](./direct2d-portal.md) und [DirectWrite](direct2d-and-directwrite.md) -primitive anwenden.</span><span class="sxs-lookup"><span data-stu-id="b1b50-104">This topic shows how to apply a series of effect to [Direct2D](./direct2d-portal.md) and [DirectWrite](direct2d-and-directwrite.md) primitives.</span></span>

<span data-ttu-id="b1b50-105">Mit der [Direct2D Effects-API](effects-overview.md) können Sie Effekt Diagramme auf primitive anwenden, die von [Direct2D](./direct2d-portal.md) auf ein Bild gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="b1b50-105">You can use the [Direct2D effects API](effects-overview.md) to apply effect graphs to primitives rendered by [Direct2D](./direct2d-portal.md) to an image.</span></span> <span data-ttu-id="b1b50-106">Das Beispiel enthält zwei abgerundete Rechtecke und den Text "Direct2D".</span><span class="sxs-lookup"><span data-stu-id="b1b50-106">The example here has two rounded rectangles and the text "Direct2D".</span></span> <span data-ttu-id="b1b50-107">Verwenden Sie Direct2D, um die Rechtecke und [DirectWrite](direct2d-and-directwrite.md) zum Zeichnen des Texts zu zeichnen.</span><span class="sxs-lookup"><span data-stu-id="b1b50-107">Use Direct2D to draw the rectangles and [DirectWrite](direct2d-and-directwrite.md) to draw the text.</span></span>

![Rechtecke mit dem Text "Direct2D" in.](images/direct2d-rounded.png)

<span data-ttu-id="b1b50-109">Durch die Verwendung von [Direct2D-Effekten](effects-overview.md)können Sie dieses Bild wie das nächste Bild aussehen lassen.</span><span class="sxs-lookup"><span data-stu-id="b1b50-109">Using [Direct2D effects](effects-overview.md), you can make this image look like the next image.</span></span> <span data-ttu-id="b1b50-110">Wenden Sie die [Gaußscher Weichzeichner](gaussian-blur.md), [Punkt Glanz Beleuchtung](specular-lighting.md), [arithmetische zusammengesetzte](arithmetic-composite.md)und zusammen [gesetzte](composite.md) Effekte auf die 2D-primitiven an, um das Bild hier zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1b50-110">Apply the [Gaussian Blur](gaussian-blur.md), [Point Specular Lighting](specular-lighting.md), [Arithmetic Composite](arithmetic-composite.md), and [Composite](composite.md) effects to the 2D primitives to create the image here.</span></span>

![Rechtecke mit dem Text "Direct2D" in, nachdem mehrere Effekte angewendet wurden.](images/direct2d-svg.png)

<span data-ttu-id="b1b50-112">Nachdem Sie die Rechtecke und den Text auf einer zwischen Oberfläche rendert haben, können Sie diese als Eingabe für [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Objekte im Bild Diagramm verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1b50-112">After you render the rectangles and text to a intermediate surface, you can use this as input for [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects in the image graph.</span></span>

<span data-ttu-id="b1b50-113">Legen Sie in diesem Beispiel das ursprüngliche Bild als Eingabe für den [Gaußscher Weichzeichner Effekt](gaussian-blur.md) fest, und legen Sie dann die Ausgabe des weichpunkts als Eingabe für den Glanz der [Punktbeleuchtung](specular-lighting.md)fest.</span><span class="sxs-lookup"><span data-stu-id="b1b50-113">In this example, set the original image as the input to the [Gaussian Blur effect](gaussian-blur.md) and then set the output of the blur as the input for the [Point Specular Lighting effect](specular-lighting.md).</span></span> <span data-ttu-id="b1b50-114">Das Ergebnis dieses Effekts wird dann zweimal mit dem ursprünglichen Bild zusammengesetzt, um das endgültige Bild zu erhalten, das im Fenster gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b1b50-114">The result of this effect is then composited with the original image twice to get the final image that is rendered to the window.</span></span>

<span data-ttu-id="b1b50-115">Im folgenden finden Sie ein Diagramm des Bild Diagramms.</span><span class="sxs-lookup"><span data-stu-id="b1b50-115">Here is a diagram of the image graph.</span></span>

![Diagramm des Wirkungs Diagramms.](images/effect-graph.png)

<span data-ttu-id="b1b50-117">Dieses Effekt Diagramm besteht aus vier [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Objekten, die jeweils einen anderen integrierten Effekt darstellen.</span><span class="sxs-lookup"><span data-stu-id="b1b50-117">This effect graph consists of four [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) objects, each representing a different built-in effect.</span></span> <span data-ttu-id="b1b50-118">Sie können benutzerdefinierte Effekte auf die gleiche Weise erstellen und verbinden, nachdem Sie Sie mit [**ID1D1Factory1:: registereffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring)registriert haben.</span><span class="sxs-lookup"><span data-stu-id="b1b50-118">You can create and connect custom effects in the same way, after you register them using [**ID1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring).</span></span> <span data-ttu-id="b1b50-119">Der Code hier erstellt die Effekte, legt die Eigenschaften fest und verbindet das zuvor gezeigte Effekt Diagramm.</span><span class="sxs-lookup"><span data-stu-id="b1b50-119">The code here creates the effects, sets the properties, and connects the effect graph shown earlier.</span></span>

1.  <span data-ttu-id="b1b50-120">Erstellen Sie den [gauischen](gaussian-blur.md) Weichzeichnereffekt mithilfe der [**ID2D1DeviceContext:: kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) -Methode, und geben Sie die richtige CLSID an.</span><span class="sxs-lookup"><span data-stu-id="b1b50-120">Create the [Gaussian blur](gaussian-blur.md) effect using the [**ID2D1DeviceContext::CreateEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) method and specifying the proper CLSID.</span></span> <span data-ttu-id="b1b50-121">Die CLSIDs für die integrierten Effekte werden in d2d1effects. h definiert.</span><span class="sxs-lookup"><span data-stu-id="b1b50-121">The CLSIDs for the built-in effects are defined in d2d1effects.h.</span></span> <span data-ttu-id="b1b50-122">Anschließend legen Sie die Standardabweichung des weichungs Werts mithilfe der [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode fest.</span><span class="sxs-lookup"><span data-stu-id="b1b50-122">You then set the standard deviation of the blur using the [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Gaussian Blur Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect)
        );

    // Set the blur amount
    DX::ThrowIfFailed(
        gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, sc_gaussianBlurStDev)
        );
    ```

    

    <span data-ttu-id="b1b50-123">Mit dem [gauischen](gaussian-blur.md) Weichzeichnereffekt werden alle Kanäle des Bilds, einschließlich des Alphakanals, verwischt.</span><span class="sxs-lookup"><span data-stu-id="b1b50-123">The [Gaussian blur](gaussian-blur.md) effect blurs all of the channels of the image, including the alpha channel.</span></span>

2.  <span data-ttu-id="b1b50-124">Erstellen Sie den Glanzeffekt, und legen [Sie die Eigenschaften](point-specular.md) fest.</span><span class="sxs-lookup"><span data-stu-id="b1b50-124">Create the [specular lighting](point-specular.md) effect and set the properties.</span></span> <span data-ttu-id="b1b50-125">Die Position des Lichts ist ein Vektor von drei Gleit Komma Werten, sodass Sie ihn als separate Variable deklarieren und an die [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode übergeben müssen.</span><span class="sxs-lookup"><span data-stu-id="b1b50-125">The position of the light is a vector of 3 floating point values, so you must declare it as a separate variable and pass it to the [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) method.</span></span>

    ```C++
    // Create the Specular Lighting Effect
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1PointSpecular, &specularLightingEffect)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_LIGHT_POSITION, sc_specularLightPosition)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_EXPONENT, sc_specularExponent)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SURFACE_SCALE, sc_specularSurfaceScale)
        );

    DX::ThrowIfFailed(
        specularLightingEffect->SetValue(D2D1_POINTSPECULAR_PROP_SPECULAR_CONSTANT, sc_specularConstant)
        );
    ```

    

    <span data-ttu-id="b1b50-126">Der Glanz [Licht](point-specular.md) Effekt verwendet den Alphakanal der Eingabe, um eine Höhen Zuordnung für die Beleuchtung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b1b50-126">The [specular lighting](point-specular.md) effect uses the alpha channel of the input to create a height map for the lighting.</span></span>

3.  <span data-ttu-id="b1b50-127">Es gibt zwei verschiedene [zusammengesetzte Effekte](composite.md) , die Sie zusammen mit dem zusammengesetzten Effekt und der [arithmetischen](arithmetic-composite.md)Zusammensetzung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="b1b50-127">There are two different composite effects that you can use the [composite](composite.md) effect and the [arithmetic composite](arithmetic-composite.md).</span></span> <span data-ttu-id="b1b50-128">Dieses Effekt Diagramm verwendet beide.</span><span class="sxs-lookup"><span data-stu-id="b1b50-128">This effect graph uses both.</span></span>

    <span data-ttu-id="b1b50-129">Erstellen Sie den zusammen [gesetzten](composite.md) Effekt, und legen Sie den Modus auf D2D1 \_ Composite \_ Mode \_ Source \_ in fest, der die Schnittmenge der Quell-und Ziel Images ausgibt.</span><span class="sxs-lookup"><span data-stu-id="b1b50-129">Create the [composite](composite.md) effect and set the mode to D2D1\_COMPOSITE\_MODE\_SOURCE\_IN, which outputs the intersection of the source and destination images.</span></span>

    <span data-ttu-id="b1b50-130">Durch den [arithmetischen zusammengesetzten](arithmetic-composite.md) Effekt werden die beiden Eingabe Bilder auf der Grundlage einer Formel verfasst, die durch den World Wide Web Consortium (W3C) für den SVG (Scalable Vector Graphics)-Standard definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b1b50-130">The [arithmetic composite](arithmetic-composite.md) effect composes the two input images based on a formula defined by the World Wide Web Consortium (W3C) for the Scalable Vector Graphics (SVG) standard.</span></span> <span data-ttu-id="b1b50-131">Erstellen Sie eine arithmetische zusammengesetzte, und legen Sie die Koeffizienten für die Formel fest.</span><span class="sxs-lookup"><span data-stu-id="b1b50-131">Create arithmetic composite and set the coefficients for the formula.</span></span>

    ```C++
    // Create the Composite Effects
    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect)
        );

    DX::ThrowIfFailed(
        compositeEffect->SetValue(D2D1_COMPOSITE_PROP_MODE, D2D1_COMPOSITE_MODE_SOURCE_IN)
        );

    DX::ThrowIfFailed(
        m_d2dContext->CreateEffect(CLSID_D2D1ArithmeticComposite, &m_arithmeticCompositeEffect)
        );

    DX::ThrowIfFailed(
        m_arithmeticCompositeEffect->SetValue(D2D1_ARITHMETICCOMPOSITE_PROP_COEFFICIENTS, sc_arithmeticCoefficients)
        );
    ```

    

    <span data-ttu-id="b1b50-132">Die Koeffizienten für den [arithmetischen zusammengesetzten](arithmetic-composite.md) Effekt werden hier dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b1b50-132">The coefficients for the [arithmetic composite](arithmetic-composite.md) effect are shown here.</span></span>

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    <span data-ttu-id="b1b50-133">In diesem Effekt Diagramm führen beide zusammengesetzten Effekte die Ausgabe der anderen Effekte und die zwischen Oberfläche als Eingaben aus und führen Sie zusammen.</span><span class="sxs-lookup"><span data-stu-id="b1b50-133">In this effect graph, both of the composite effects take the output of the other effects and the intermediate surface as inputs and composites them.</span></span>

4.  <span data-ttu-id="b1b50-134">Schließlich verbinden Sie die Effekte, um das Diagramm zu bilden, indem Sie die Eingaben auf die richtigen Bilder und Bitmaps festlegen.</span><span class="sxs-lookup"><span data-stu-id="b1b50-134">Finally, you connect the effects to form the graph by setting the inputs to the proper images and bitmaps.</span></span>

    <span data-ttu-id="b1b50-135">Der erste Effekt, [gauweich](gaussian-blur.md)weich, empfängt seine Eingabe von der zwischen Oberfläche, in der Sie die primitiven gerendert haben.</span><span class="sxs-lookup"><span data-stu-id="b1b50-135">The first effect, [Gaussian blur](gaussian-blur.md), receives its input from the intermediate surface that you rendered the primitives to.</span></span> <span data-ttu-id="b1b50-136">Sie legen die Eingabe mithilfe der [**ID2D1Effect:: SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) -Methode und angeben des Indexes eines [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) -Objekts fest.</span><span class="sxs-lookup"><span data-stu-id="b1b50-136">You set the input using the [**ID2D1Effect::SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) method and specifying the index of an [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) object.</span></span> <span data-ttu-id="b1b50-137">Die Gauß-und Glanz [Lichter](point-specular.md) wirken sich nur auf eine einzelne Eingabe aus.</span><span class="sxs-lookup"><span data-stu-id="b1b50-137">The Gaussian blur and [specular lighting](point-specular.md) effects have only a single input.</span></span> <span data-ttu-id="b1b50-138">Der Glanzlicht Effekt verwendet den unscharfen Alphakanal des Gauß</span><span class="sxs-lookup"><span data-stu-id="b1b50-138">The specular lighting effect uses the blurred alpha channel of the Gaussian blur</span></span>

    <span data-ttu-id="b1b50-139">Die [zusammengesetzten und](composite.md) [arithmetischen zusammengesetzten](arithmetic-composite.md) Effekte haben mehrere Eingaben.</span><span class="sxs-lookup"><span data-stu-id="b1b50-139">The [composite](composite.md) and [arithmetic composite](arithmetic-composite.md) effects have multiple inputs.</span></span> <span data-ttu-id="b1b50-140">Um sicherzustellen, dass die Bilder in der richtigen Reihenfolge angeordnet werden, müssen Sie den korrekten Index für jedes Eingabe Abbild angeben.</span><span class="sxs-lookup"><span data-stu-id="b1b50-140">To make sure the images are put together in the right order, you must specify the correct index for each input image.</span></span>

    ```C++
    // Connect the graph.
    // Apply a blur effect to the original image.
    gaussianBlurEffect->SetInput(0, m_inputImage.Get());

    // Apply a specular lighting effect to the result.
    specularLightingEffect->SetInputEffect(0, gaussianBlurEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    compositeEffect->SetInput(0, m_inputImage.Get());
    compositeEffect->SetInputEffect(1, specularLightingEffect.Get());

    // Compose the original bitmap under the output from lighting and blur.
    m_arithmeticCompositeEffect->SetInput(0, m_inputImage.Get());
    m_arithmeticCompositeEffect->SetInputEffect(1, compositeEffect.Get());
    ```

    

5.  <span data-ttu-id="b1b50-141">Übergeben Sie das [arithmetische zusammengesetzte](arithmetic-composite.md) Effekt Objekt an die [**ID2DDeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) -Methode, und die Ausgabe des Diagramms wird verarbeitet und gezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b1b50-141">Pass the [arithmetic composite](arithmetic-composite.md) effect object into the [**ID2DDeviceContext::DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) method and it processes and draws the output of the graph.</span></span>

    ```C++
        // Draw the output of the effects graph.
        m_d2dContext->DrawImage(
            m_arithmeticCompositeEffect.Get(),
            D2D1::Point2F(
                (size.width - sc_inputBitmapSize.width) / 2,
                (size.height - sc_inputBitmapSize.height) / 2 + sc_offset
                )
            );
    ```

    

 

 