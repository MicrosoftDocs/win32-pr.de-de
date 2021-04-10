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
# <a name="effects"></a>Effekte

## <a name="what-are-direct2d-effects"></a>Was sind Direct2D-Effekte?

Mit Direct2D können Sie eine oder mehrere hochwertige Effekte auf ein Bild oder einen Satz von Bildern anwenden. Die Effekte-APIs basieren auf [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) und nutzen GPU-Features für die Bildverarbeitung. Sie können Effekte in einem Effekt Diagramm verketten und die Ausgabe von Effekten verfassen oder mischen.

Ein Direct2D-Effekt führt einen Abbild Erstellungs Task aus, wie z. b. das Ändern der Helligkeit, das desätalisieren eines Bilds oder das Erstellen eines Effekte können NULL oder mehr Eingabe Bilder akzeptieren, mehrere Eigenschaften verfügbar machen, die ihren Vorgang steuern, und ein einzelnes Ausgabe Bild generieren.

Jeder Effekt erstellt ein internes Transformations Diagramm, das aus einzelnen Transformationen besteht. Jede Transformation stellt einen einzelnen Bild Vorgang dar. Der Hauptzweck einer Transformation besteht darin, die Shader zu beherbergen, die für jedes Ausgabe Pixel ausgeführt werden. Diese Shader können Pixel-Shader, Vertex-Shader, die Blend-Phase einer GPU und Compute-Shader enthalten.

Die [integrierten Effekte](built-in-effects.md) von [Direct2D](./direct2d-portal.md) und benutzerdefinierte Effekte, die Sie mithilfe der [API für benutzerdefinierte Effekte](custom-effects.md) treffen können, funktionieren auf diese Weise.

Es gibt eine Reihe [integrierter Effekte](built-in-effects.md) aus Kategorien, wie hier beschrieben. Eine vollständige Liste finden Sie im Abschnitt [integrierte Effekte](built-in-effects.md) .

-   [Filterung](built-in-effects.md)
-   [Komposition und Vermischung](built-in-effects.md)
-   [Transparenz](built-in-effects.md)
-   [Farbe](built-in-effects.md)
-   [Beleuchtung und stilialisierung](built-in-effects.md)
-   [Transformieren und Skalieren](built-in-effects.md)
-   [Sources](built-in-effects.md)

Sie können Effekte auf jede beliebige Bitmap anwenden, einschließlich der von der [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api)geladenen Bilder, primitiver Zeichen, die von [Direct2D](./direct2d-portal.md)gezeichnet werden, von Text aus [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)oder von [Direct3D](/windows/desktop/direct3d10/d3d10-graphics)gerenderten Szenen.

Mit Direct2D-Effekten können Sie eigene Effekte schreiben, die Sie für Ihre Anwendungen verwenden können. Mithilfe eines benutzerdefinierten Effekts-Frameworks können Sie GPU-Funktionen wie Pixel-Shader, Vertex-Shader und die Mischungs Einheit verwenden. Sie können auch andere integrierte oder benutzerdefinierte Effekte in Ihren benutzerdefinierten Effekt einschließen. Das Framework zum Erstellen von benutzerdefinierten Effekten ist das gleiche, das verwendet wurde, um die integrierten Effekte von [Direct2D](./direct2d-portal.md)zu erstellen. Die [Direct2D Effect Author-API](custom-effects.md) stellt eine Reihe von Schnittstellen zum Erstellen und Registrieren von Effekten bereit.

### <a name="more-effects-topics"></a>Themen zu weiteren Effekten

Im weiteren Verlauf dieses Themas werden die Grundlagen von Direct2D Effekten erläutert, wie z. b. das Anwenden eines Effekts auf ein Bild. Die Tabelle enthält Links zu weiteren Themen zu den Auswirkungen.

| Thema                                                                                                                    | BESCHREIBUNG                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Effektshader-Verknüpfung](effect-shader-linking.md)<br/>                                                            | Direct2D verwendet eine Optimierung namens "Effect Shader Linking", die das Rendering mehrerer Effekte Diagramm Rendering in einem einzigen Durchlauf kombiniert.<br/>                                               |
| [Benutzerdefinierte Effekte](custom-effects.md)<br/>                                                                          | Zeigt, wie Sie Ihre eigenen benutzerdefinierten Effekte mit dem Standard-HLSL schreiben.<br/>                                                                                                                |
| [Laden eines Bilds in Direct2D Effekte mithilfe der Dateiauswahl](load-a-id2d1image-using-the-filepicker.md)<br/> | Veranschaulicht die Verwendung von [**Windows:: Storage::P icker:: fileopenpicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) zum Laden eines Bilds in Direct2D-Effekte.<br/>                                      |
| [Speichern von Direct2D-Inhalten in einer Bilddatei](save-direct2d-content-to-an-image-file.md)<br/>                   | In diesem Thema wird gezeigt, wie [**iwicimageencoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) verwendet wird, um Inhalt in Form einer [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in einer codierten Bilddatei (z. b. JPEG) zu speichern.<br/> |
| [Anwenden von Effekten auf primitive](how-to-apply-effects-to-primitives.md)<br/>                                  | In diesem Thema wird gezeigt, wie Sie eine Reihe von Effekten auf [Direct2D](./direct2d-portal.md) und [DirectWrite](direct2d-and-directwrite.md) -primitive anwenden.<br/>                           |
| [Steuern der Genauigkeit und des numerischen Clipping in Effekt Diagrammen](precision-and-clipping-in-effect-graphs.md)<br/>  | Anwendungen, die Effekte mithilfe von Direct2D renderingeffekte darstellen, müssen darauf achten, dass die gewünschte Qualität und Vorhersagbarkeit hinsichtlich der numerischen Genauigkeit erreicht wird. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Anwenden eines Effekts auf ein Bild

Mit der Direct2D Effects-API können Sie Transformationen auf Bilder anwenden.

> [!Note]  
> In diesem Beispiel wird davon ausgegangen, dass Sie bereits [**ID2D1DeviceContext**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) -und [IWICBitmapSource](/windows/desktop/wic/-wic-imp-iwicbitmapsource) -Objekte erstellt haben. Weitere Informationen zum Erstellen dieser Objekte finden Sie unter Gewusst [wie: Laden eines Bilds in Direct2D Effekte mithilfe der Datei](load-a-id2d1image-using-the-filepicker.md) Auswahl und [Geräte und Geräte Kontexte](devices-and-device-contexts.md).

 

1.  Deklarieren Sie eine [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Variable, und erstellen Sie dann mithilfe der [**ID2DDeviceContext:: kreateeffect**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) -Methode einen [Bitmap-Quell](bitmap-source.md) Effekt.

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  Legen Sie die Eigenschaft BitmapSource mithilfe von [**ID2D1Effect:: SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))auf die WIC-Bitmapquelle fest.

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Deklarieren Sie eine [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Variable, und erstellen Sie dann den [Gaußschen](gaussian-blur.md) weich Effekt.

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  Legen Sie die Eingabe fest, um das Bild aus dem Bitmap-Quell Effekt zu empfangen. Legen Sie den weichungs Betrag der [**SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) -Methode und der Standardabweichung-Eigenschaft fest.

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  Verwenden Sie den Gerätekontext, um die resultierende Bild Ausgabe zu zeichnen.

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    Die [**DrawImage**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) -Methode muss zwischen den [**ID2DDeviceContext:: beginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) -und [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) -aufrufen wie andere Direct2D-Rendering-Vorgänge aufgerufen werden. **DrawImage** kann ein Bild oder die Ausgabe eines Effekts annehmen und es auf der Ziel Oberfläche Rendering.

## <a name="spatial-transforms"></a>Räumliche Transformationen

Direct2D bietet integrierte Effekte, die Bilder im 2D-und 3D-Raum sowie die Skalierung transformieren können. Die Auswirkungen auf die Skalierung und Transformation bieten verschiedene Qualitätsstufen, wie z. b. die nächstgelegene Nachbar-, lineare, kubische, Multisample-linear, Anisotropic und High Quality-kubische

> [!Note]  
> Der anisotrope Modus generiert bei der Skalierung Mipmaps. Wenn Sie jedoch die **zwischengespeicherte** Eigenschaft für die Effekte, die für die Transformation eingegeben werden, auf true festlegen, werden die Mipmaps bei ausreichend kleinen Bildern nicht jedes Mal generiert.

 


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



Durch diese Verwendung des 2D-affinen Transformations Effekts wird die Bitmap leicht gegen den Uhrzeigersinn gedreht.



| Vorher                                                            |
|-------------------------------------------------------------------|
| ![2D-Affinität vor dem Bild.](images/default-before.jpg)      |
| Nach                                                             |
| ![2D-Affinität nach dem Bild.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Zusammengesetzte Images

Bei einigen Effekten werden mehrere Eingaben akzeptiert und in einem resultierenden Bild zusammengeführt.

Die integrierten zusammengesetzten und arithmetischen zusammengesetzten Effekte bieten verschiedene Modi. Weitere Informationen finden Sie im zusammen [gesetzten](composite.md) Thema. Der [Blend](blend.md) -Effekt bietet eine Vielzahl von verfügbaren GPU-Modi.


```C++
ComPtr<ID2D1Effect> compositeEffect;
DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect));

compositeEffect->SetInput(0, bitmap.Get());
compositeEffect->SetInput(1, bitmapTwo.Get());

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



Der zusammengesetzte Effekt kombiniert Bilder auf verschiedene Weise entsprechend dem von Ihnen angegebenen Modus.

## <a name="pixel-adjustments"></a>Pixel Anpassungen

Es gibt einige integrierte Direct2D Effekte, mit denen Sie die Pixeldaten ändern können. Beispielsweise kann der Farbmatrix Effekt verwendet werden, um die Farbe eines Bilds zu ändern.


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



Dieser Code nimmt das Bild an und ändert die Farbe, wie in den Beispielbildern hier gezeigt.



| Vorher                                                          |
|-----------------------------------------------------------------|
| ![der Farbmatrix Effekt vor dem Bild.](images/default-before.jpg) |
| Nach                                                           |
| ![Farbmatrix Effekt nach Bild.](images/15-colormatrix.png)  |



 

Weitere Informationen finden Sie im Abschnitt [Color-integrierte Effekte](how-to-create-a-solid-color-brush.md) .

## <a name="building-effect-graphs"></a>Gebäude Effekt Diagramme

Sie können Effekte verketten, um Bilder umzuwandeln. Beispielsweise wendet der Code hier einen Schatten und eine 2D-Transformation an und führt dann die Ergebnisse aus.


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



Im Folgenden wird das Ergebnis aufgeführt:

![Ausgabe des Schatten Effekts.](images/effect-overview-shadow.png)

Effekte akzeptieren [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) -Objekte als Eingabe. Sie können eine [**ID2D1Bitmap**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) verwenden, da die Schnittstelle von **ID2D1Image** abgeleitet ist. Sie können auch " [**ID2D1Effect:: GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) " verwenden, um die Ausgabe eines [**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) -Objekts als **ID2D1Image** zu erhalten, oder die **setinputeffect** -Methode verwenden, die die Ausgabe für Sie konvertiert. In den meisten Fällen besteht ein Wirkungs Diagramm aus **ID2D1Effect** -Objekten, die direkt verkettet sind, sodass es einfach ist, mehrere Effekte auf ein Bild anzuwenden, um überzeugende Visualisierungen zu erstellen.

Weitere Informationen finden [Sie unter How to Apply effects to Primitives](how-to-apply-effects-to-primitives.md) .

## <a name="related-topics"></a>Zugehörige Themen

[Beispiel für Direct2D grundlegende Bildeffekte](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Integrierte Effekte](built-in-effects.md)