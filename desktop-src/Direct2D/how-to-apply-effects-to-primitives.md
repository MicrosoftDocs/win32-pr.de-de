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
# <a name="how-to-apply-effects-to-primitives"></a>Anwenden von Effekten auf primitive

In diesem Thema wird gezeigt, wie Sie eine Reihe von Effekten auf [Direct2D](./direct2d-portal.md) und [DirectWrite](direct2d-and-directwrite.md) -primitive anwenden.

Mit der [Direct2D Effects-API](effects-overview.md) können Sie Effekt Diagramme auf primitive anwenden, die von [Direct2D](./direct2d-portal.md) auf ein Bild gerendert werden. Das Beispiel enthält zwei abgerundete Rechtecke und den Text "Direct2D". Verwenden Sie Direct2D, um die Rechtecke und [DirectWrite](direct2d-and-directwrite.md) zum Zeichnen des Texts zu zeichnen.

![Rechtecke mit dem Text "Direct2D" in.](images/direct2d-rounded.png)

Durch die Verwendung von [Direct2D-Effekten](effects-overview.md)können Sie dieses Bild wie das nächste Bild aussehen lassen. Wenden Sie die [Gaußscher Weichzeichner](gaussian-blur.md), [Punkt Glanz Beleuchtung](specular-lighting.md), [arithmetische zusammengesetzte](arithmetic-composite.md)und zusammen [gesetzte](composite.md) Effekte auf die 2D-primitiven an, um das Bild hier zu erstellen.

![Rechtecke mit dem Text "Direct2D" in, nachdem mehrere Effekte angewendet wurden.](images/direct2d-svg.png)

Nachdem Sie die Rechtecke und den Text auf einer zwischen Oberfläche rendert haben, können Sie diese als Eingabe für [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Objekte im Bild Diagramm verwenden.

Legen Sie in diesem Beispiel das ursprüngliche Bild als Eingabe für den [Gaußscher Weichzeichner Effekt](gaussian-blur.md) fest, und legen Sie dann die Ausgabe des weichpunkts als Eingabe für den Glanz der [Punktbeleuchtung](specular-lighting.md)fest. Das Ergebnis dieses Effekts wird dann zweimal mit dem ursprünglichen Bild zusammengesetzt, um das endgültige Bild zu erhalten, das im Fenster gerendert wird.

Im folgenden finden Sie ein Diagramm des Bild Diagramms.

![Diagramm des Wirkungs Diagramms.](images/effect-graph.png)

Dieses Effekt Diagramm besteht aus vier [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Objekten, die jeweils einen anderen integrierten Effekt darstellen. Sie können benutzerdefinierte Effekte auf die gleiche Weise erstellen und verbinden, nachdem Sie Sie mit [**ID1D1Factory1:: registereffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1factory1-registereffectfromstring)registriert haben. Der Code hier erstellt die Effekte, legt die Eigenschaften fest und verbindet das zuvor gezeigte Effekt Diagramm.

1.  Erstellen Sie den [gauischen](gaussian-blur.md) Weichzeichnereffekt mithilfe der [**ID2D1DeviceContext:: kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) -Methode, und geben Sie die richtige CLSID an. Die CLSIDs für die integrierten Effekte werden in d2d1effects. h definiert. Anschließend legen Sie die Standardabweichung des weichungs Werts mithilfe der [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode fest.

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

    

    Mit dem [gauischen](gaussian-blur.md) Weichzeichnereffekt werden alle Kanäle des Bilds, einschließlich des Alphakanals, verwischt.

2.  Erstellen Sie den Glanzeffekt, und legen [Sie die Eigenschaften](point-specular.md) fest. Die Position des Lichts ist ein Vektor von drei Gleit Komma Werten, sodass Sie ihn als separate Variable deklarieren und an die [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode übergeben müssen.

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

    

    Der Glanz [Licht](point-specular.md) Effekt verwendet den Alphakanal der Eingabe, um eine Höhen Zuordnung für die Beleuchtung zu erstellen.

3.  Es gibt zwei verschiedene [zusammengesetzte Effekte](composite.md) , die Sie zusammen mit dem zusammengesetzten Effekt und der [arithmetischen](arithmetic-composite.md)Zusammensetzung verwenden können. Dieses Effekt Diagramm verwendet beide.

    Erstellen Sie den zusammen [gesetzten](composite.md) Effekt, und legen Sie den Modus auf D2D1 \_ Composite \_ Mode \_ Source \_ in fest, der die Schnittmenge der Quell-und Ziel Images ausgibt.

    Durch den [arithmetischen zusammengesetzten](arithmetic-composite.md) Effekt werden die beiden Eingabe Bilder auf der Grundlage einer Formel verfasst, die durch den World Wide Web Consortium (W3C) für den SVG (Scalable Vector Graphics)-Standard definiert ist. Erstellen Sie eine arithmetische zusammengesetzte, und legen Sie die Koeffizienten für die Formel fest.

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

    

    Die Koeffizienten für den [arithmetischen zusammengesetzten](arithmetic-composite.md) Effekt werden hier dargestellt.

    ```C++
    D2D1_VECTOR_4F sc_arithmeticCoefficients   = D2D1::Vector4F(0.0f, 1.0f, 1.0f, 0.0f);
    ```

    

    In diesem Effekt Diagramm führen beide zusammengesetzten Effekte die Ausgabe der anderen Effekte und die zwischen Oberfläche als Eingaben aus und führen Sie zusammen.

4.  Schließlich verbinden Sie die Effekte, um das Diagramm zu bilden, indem Sie die Eingaben auf die richtigen Bilder und Bitmaps festlegen.

    Der erste Effekt, [gauweich](gaussian-blur.md)weich, empfängt seine Eingabe von der zwischen Oberfläche, in der Sie die primitiven gerendert haben. Sie legen die Eingabe mithilfe der [**ID2D1Effect:: SetInput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-setinput) -Methode und angeben des Indexes eines [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) -Objekts fest. Die Gauß-und Glanz [Lichter](point-specular.md) wirken sich nur auf eine einzelne Eingabe aus. Der Glanzlicht Effekt verwendet den unscharfen Alphakanal des Gauß

    Die [zusammengesetzten und](composite.md) [arithmetischen zusammengesetzten](arithmetic-composite.md) Effekte haben mehrere Eingaben. Um sicherzustellen, dass die Bilder in der richtigen Reihenfolge angeordnet werden, müssen Sie den korrekten Index für jedes Eingabe Abbild angeben.

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

    

5.  Übergeben Sie das [arithmetische zusammengesetzte](arithmetic-composite.md) Effekt Objekt an die [**ID2DDeviceContext::D rawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) -Methode, und die Ausgabe des Diagramms wird verarbeitet und gezeichnet.

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

    

 

 