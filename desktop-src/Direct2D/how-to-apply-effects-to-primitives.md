---
title: Anwenden von Effekten auf Primitive
description: In diesem Thema wird gezeigt, wie Sie eine Reihe von Effekten auf Direct2D und DirectWrite Primitive anwenden.
ms.assetid: 9782C22E-5D4C-494D-A0B1-19474C2CA900
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c17cbf1efe17d1c23c90382f3b95fb41e33946a93935b0be02fc5b41f314a8c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569584"
---
# <a name="how-to-apply-effects-to-primitives"></a>Anwenden von Effekten auf Primitive

In diesem Thema wird gezeigt, wie Sie eine Reihe von Effekten auf [Direct2D](./direct2d-portal.md) und [DirectWrite](direct2d-and-directwrite.md) Primitive anwenden.

Sie können die [Direct2D-Effekt-API](effects-overview.md) verwenden, um Effektdiagramme auf Primitive anzuwenden, die von [Direct2D](./direct2d-portal.md) auf ein Bild gerendert werden. Das beispiel enthält zwei abgerundete Rechtecke und den Text "Direct2D". Verwenden Sie Direct2D, um die Rechtecke zu zeichnen, und [DirectWrite,](direct2d-and-directwrite.md) um den Text zu zeichnen.

![Rechtecke mit dem Darin enthaltenen Text "direct2d".](images/direct2d-rounded.png)

Mit [Direct2D-Effekten](effects-overview.md)können Sie dieses Bild wie das nächste Bild aussehen lassen. Wenden Sie die [effekte Gaußscher Weichzeichner](gaussian-blur.md), [Point Specular Lighting](specular-lighting.md), [Arithmetic Composite](arithmetic-composite.md)und [Composite](composite.md) auf die 2D-Primitive an, um das Bild hier zu erstellen.

![Rechtecke mit dem Text "direct2d" innerhalb von , nachdem mehrere Effekte angewendet wurden.](images/direct2d-svg.png)

Nachdem Sie die Rechtecke und den Text auf einer Zwischenoberfläche gerendert haben, können Sie diese als Eingabe für [**ID2D1Effect-Objekte**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) im Bilddiagramm verwenden.

Legen Sie in diesem Beispiel das ursprüngliche Bild als Eingabe für den [effekt Gaußscher Weichzeichner](gaussian-blur.md) fest, und legen Sie dann die Ausgabe des Weichzeichners als Eingabe für den [Point Specular Lighting-Effekt](specular-lighting.md)fest. Das Ergebnis dieses Effekts wird dann zweimal mit dem ursprünglichen Bild zusammengesetzt, um das endgültige Bild abzurufen, das im Fenster gerendert wird.

Hier sehen Sie ein Diagramm des Bilddiagramms.

![Diagramm des Effektdiagramms.](images/effect-graph.png)

Dieses Effektdiagramm besteht aus vier [**ID2D1Effect-Objekten,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) die jeweils einen anderen integrierten Effekt darstellen. Sie können benutzerdefinierte Effekte auf die gleiche Weise erstellen und verbinden, nachdem Sie sie mit [**id1D1Factory1::RegisterEffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring)registriert haben. Der Code hier erstellt die Effekte, legt die Eigenschaften fest und verbindet das zuvor gezeigte Effektdiagramm.

1.  Erstellen Sie den [Blureffekt "Gaussian"](gaussian-blur.md) mithilfe der [**ID2D1DeviceContext::CreateEffect-Methode,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) und geben Sie die richtige CLSID an. Die CLSIDs für die integrierten Effekte werden in d2d1effects.h definiert. Anschließend legen Sie die Standardabweichung des Weichzeichners mithilfe der [**ID2D1Effect::SetValue-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) fest.

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

    

    Der [Weichzeichnereffekt "Gaussian"](gaussian-blur.md) verwischt alle Kanäle des Bilds, einschließlich des Alphakanals.

2.  Erstellen Sie den [Glanzlichteffekt,](point-specular.md) und legen Sie die Eigenschaften fest. Die Position des Lichts ist ein Vektor von drei Gleitkommawerten. Daher müssen Sie sie als separate Variable deklarieren und an die [**SetValue-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) übergeben.

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

    

    Der [Glanzlichteffekt](point-specular.md) verwendet den Alphakanal der Eingabe, um eine Höhenkarte für die Beleuchtung zu erstellen.

3.  Es gibt zwei verschiedene zusammengesetzte Effekte, die Sie den [zusammengesetzten](composite.md) Effekt und den [arithmetischen zusammengesetzten](arithmetic-composite.md)verwenden können. Dieses Effektdiagramm verwendet beides.

    Erstellen Sie den [zusammengesetzten](composite.md) Effekt, und legen Sie den Modus auf D2D1 \_ COMPOSITE MODE SOURCE IN \_ \_ \_ fest, der die Schnittmenge der Quell- und Zielbilder ausgibt.

    Der [arithmetische zusammengesetzte](arithmetic-composite.md) Effekt erstellt die beiden Eingabebilder basierend auf einer Formel, die vom World Wide Web Consortium (W3C) für den SVG-Standard (Scalable Vector Graphics) definiert wird. Erstellen Sie eine arithmetische Zusammengesetztkeit, und legen Sie die Koeffizienten für die Formel fest.

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

    

    Die Koeffizienten für den [arithmetischen zusammengesetzten](arithmetic-composite.md) Effekt sind hier dargestellt.

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    In diesem Effektdiagramm nehmen beide zusammengesetzten Effekte die Ausgabe der anderen Effekte und die Zwischenoberfläche als Eingaben und zusammengesetzte Effekte an.

4.  Abschließend verbinden Sie die Effekte, um das Diagramm zu bilden, indem Sie die Eingaben auf die richtigen Bilder und Bitmaps festlegen.

    Der erste Effekt, [der Gausssche Weichzeichner,](gaussian-blur.md)empfängt seine Eingabe von der Zwischenoberfläche, in der Sie die Primitiven gerendert haben. Sie legen die Eingabe mithilfe der [**ID2D1Effect::SetInput-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) fest und geben den Index eines [**ID2D1Image-Objekts**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) an. Die Weichzeichner- und [Glanzlichteffekte](point-specular.md) von Gaussian weisen nur eine einzige Eingabe auf. Für den Glanzlichteffekt wird der unscharfe Alphakanal des Gaußschen Weichzeichners verwendet.

    Die [zusammengesetzten](composite.md) und [arithmetischen Verbundeffekte](arithmetic-composite.md) weisen mehrere Eingaben auf. Um sicherzustellen, dass die Bilder in der richtigen Reihenfolge zusammengestellt werden, müssen Sie den richtigen Index für jedes Eingabebild angeben.

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

    

5.  Übergeben Sie das [arithmetische Objekt des zusammengesetzten](arithmetic-composite.md) Effekts an die [**ID2DDeviceContext::D rawImage-Methode,**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) und es verarbeitet und zeichnet die Ausgabe des Graphen.

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

    

 

 