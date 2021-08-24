---
title: Effekte (Direct2D)
description: Eine Übersicht über Direct2D-Effekte.
ms.assetid: 1446BDA9-AD4C-472C-8F1D-82ABC1880E13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe0a88ff64721fc32955416dcfe108b1c9e87f7565a67fc2e1d8192a1eaf369d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119317988"
---
# <a name="effects"></a>Effekte

## <a name="what-are-direct2d-effects"></a>Was sind Direct2D-Effekte?

Sie können Direct2D verwenden, um einen oder mehrere qualitativ hochwertige Effekte auf ein Bild oder eine Gruppe von Bildern anzuwenden. Die Effekt-APIs bauen auf [Direct3D 11](/windows/desktop/direct3d11/direct3d-11-features) auf und nutzen GPU-Features für die Bildverarbeitung. Sie können Effekte in einem Effektdiagramm verketten und die Ausgabe von Effekten zusammenstellen oder mischen.

Ein Direct2D-Effekt führt eine Bildverarbeitungsaufgabe aus, z. B. das Ändern der Helligkeit, das Entsättigen eines Bilds oder das Erstellen eines Schlagschattens. Effekte können null oder mehr Eingabebilder akzeptieren, mehrere Eigenschaften verfügbar machen, die ihren Betrieb steuern, und ein einzelnes Ausgabebild generieren.

Jeder Effekt erstellt ein internes Transformationsdiagramm, das aus einzelnen Transformationen besteht. Jede Transformation stellt einen einzelnen Bildvorgang dar. Der Hauptzweck einer Transformation ist es, die Shader zu verwenden, die für jedes Ausgabepixel ausgeführt werden. Diese Shader können Pixel-Shader, Vertex-Shader, die Überblendungsphase einer GPU und Compute-Shader enthalten.

Sowohl die [integrierten Direct2D-Effekte](./direct2d-portal.md) [](built-in-effects.md) als auch die benutzerdefinierten Effekte, die Sie mithilfe der API [für](custom-effects.md) benutzerdefinierte Effekte erzielen können, funktionieren auf diese Weise.

Es gibt eine Reihe von [integrierten Effekten aus](built-in-effects.md) Kategorien wie hier. Eine vollständige [Liste finden Sie im](built-in-effects.md) Abschnitt Integrierte Effekte.

-   [Filterung](built-in-effects.md)
-   [Komposition und Mischung](built-in-effects.md)
-   [Transparenz](built-in-effects.md)
-   [Farbe](built-in-effects.md)
-   [Beleuchtung und Stilisierung](built-in-effects.md)
-   [Transformieren und Skalieren](built-in-effects.md)
-   [Sources](built-in-effects.md)

Sie können Effekte auf beliebige Bitmaps anwenden, z. B.: bilder, die von der [Windows Imaging Component (WIC)](/windows/desktop/wic/-wic-api)geladen werden, primitive, von [Direct2D](./direct2d-portal.md)gezeichnete Primitive, Text aus [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)oder Szenen, die von [Direct3D](/windows/desktop/direct3d10/d3d10-graphics)gerendert werden.

Mit Direct2D-Effekten können Sie Ihre eigenen Effekte schreiben, die Sie für Ihre Anwendungen verwenden können. Mit einem benutzerdefinierten Effektframework können Sie GPU-Features wie Pixel-Shader, Vertex-Shader und die Mischungseinheit verwenden. Sie können auch andere integrierte oder benutzerdefinierte Effekte in Ihren benutzerdefinierten Effekt einverfolgen. Das Framework zum Erstellen benutzerdefinierter Effekte ist das gleiche, das zum Erstellen der integrierten Effekte von [Direct2D verwendet wurde.](./direct2d-portal.md) Die [Direct2D Effect Author-API](custom-effects.md) stellt eine Reihe von Schnittstellen zum Erstellen und Registrieren von Effekten bereit.

### <a name="more-effects-topics"></a>Weitere Effekte – Themen

Im restlichen Teil dieses Themas werden die Grundlagen von Direct2D-Effekten erläutert, z. B. das Anwenden eines Effekts auf ein Bild. Die Tabelle enthält Links zu weiteren Themen zu Effekten.

| Thema                                                                                                                    | Beschreibung                                                                                                                                                                                   |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Effektshader-Verknüpfung](effect-shader-linking.md)<br/>                                                            | Direct2D verwendet eine Optimierung namens Effekt-Shaderverknüpfung, bei der das Rendern mehrerer Effektdiagramme in einem einzelnen Durchgang kombiniert wird.<br/>                                               |
| [Benutzerdefinierte Effekte](custom-effects.md)<br/>                                                                          | Zeigt Ihnen, wie Sie eigene benutzerdefinierte Effekte mit hlsl-Standardeffekten schreiben.<br/>                                                                                                                |
| [Laden eines Bilds in Direct2D-Effekte mit filepicker](load-a-id2d1image-using-the-filepicker.md)<br/> | Zeigt, wie sie [**Windows::Storage::P ickers::FileOpenPicker**](/uwp/api/Windows.Storage.Pickers.FileOpenPicker) verwenden, um ein Bild in Direct2D-Effekte zu laden.<br/>                                      |
| [Speichern von Direct2D-Inhalten in einer Bilddatei](save-direct2d-content-to-an-image-file.md)<br/>                   | In diesem Thema wird gezeigt, wie Sie MITHILFE von [**IWICImageEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicimageencoder) Inhalte in Form eines [**ID2D1Image**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) in einer codierten Bilddatei wie JPEG speichern.<br/> |
| [Anwenden von Effekten auf Primitive](how-to-apply-effects-to-primitives.md)<br/>                                  | In diesem Thema wird gezeigt, wie Sie eine Reihe von Effekten auf [Direct2D](./direct2d-portal.md) und [DirectWrite](direct2d-and-directwrite.md) anwenden.<br/>                           |
| [Steuern der Genauigkeit und numerischen Beschneidung in Effektdiagrammen](precision-and-clipping-in-effect-graphs.md)<br/>  | Anwendungen, die Effekte mit Direct2D rendern, müssen darauf achten, das gewünschte Maß an Qualität und Vorhersagbarkeit in Bezug auf die numerische Genauigkeit zu erreichen. <br/>                    |

## <a name="applying-an-effect-to-an-image"></a>Anwenden eines Effekts auf ein Bild

Sie können die Direct2D-Effekt-API verwenden, um Transformationen auf Bilder anzuwenden.

> [!Note]  
> In diesem Beispiel wird davon ausgegangen, dass Bereits [**ID2D1DeviceContext-**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1devicecontext) und [IWICBitmapSource-Objekte erstellt](/windows/desktop/wic/-wic-imp-iwicbitmapsource) wurden. Weitere Informationen zum Erstellen dieser Objekte finden Sie unter Laden eines Bilds in [Direct2D-Effekte](load-a-id2d1image-using-the-filepicker.md) mithilfe von FilePicker und [Geräte und Gerätekontexte.](devices-and-device-contexts.md)

 

1.  Deklarieren Sie [**eine ID2D1Effect-Variable,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) und erstellen Sie dann mithilfe der [**ID2DDeviceContext::CreateEffect-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-createeffect) einen Bitmapquelleneffekt. [](bitmap-source.md)

    ```C++
        ComPtr<ID2D1Effect> bitmapSourceEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1BitmapSource, &bitmapSourceEffect));
    ```

    

2.  Legen Sie die BitmapSource-Eigenschaft mithilfe von [**ID2D1Effect::SetValue**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32))auf die WIC-Bitmapquelle fest.

    ```C++
            DX::ThrowIfFailed(m_bitmapSourceEffect->SetValue(D2D1_BITMAPSOURCE_PROP_WIC_BITMAP_SOURCE, m_wicBitmapSource.Get()));
    ```

    

3.  Deklarieren [**Sie eine ID2D1Effect-Variable,**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) und erstellen Sie dann [den Gauß-Weichdeeffekt.](gaussian-blur.md)

    ```C++
        ComPtr<ID2D1Effect> gaussianBlurEffect;

        DX::ThrowIfFailed(m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect));
    ```

    

4.  Legen Sie die Eingabe fest, um das Bild vom Bitmapquelleneffekt zu empfangen. Legen Sie den Weichdewert für die [**SetValue-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1properties-setvalue(uint32_constbyte_uint32)) und die Standardabweichungseigenschaft fest.

    ```C++
        gaussianBlurEffect->SetInputEffect(0, bitmapSourceEffect.Get());

        DX::ThrowIfFailed(gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 6.0f));
    ```

    

5.  Verwenden Sie den Gerätekontext, um die resultierende Bildausgabe zu zeichnen.

    ```C++
        m_d2dContext->BeginDraw();

        m_d2dContext->Clear(D2D1::ColorF(D2D1::ColorF::CornflowerBlue));

        // Draw the blurred image.
        m_d2dContext->DrawImage(gaussianBlurEffect.Get());

        HRESULT hr = m_d2dContext->EndDraw();
    ```

    

    Die [**DrawImage-Methode**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1devicecontext-drawimage(id2d1image_constd2d1_point_2f_constd2d1_rect_f_d2d1_interpolation_mode_d2d1_composite_mode)) muss wie bei anderen Direct2D-Rendervorgängen zwischen den [**Aufrufen ID2DDeviceContext::BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) und [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) aufgerufen werden. **DrawImage** kann ein Bild oder die Ausgabe eines Effekts auf der Zieloberfläche rendern.

## <a name="spatial-transforms"></a>Räumliche Transformationen

Direct2D bietet integrierte Effekte, die Bilder im 2D- und 3D-Raum transformieren sowie skalieren können. Die Skalierungs- und Transformationseffekte bieten verschiedene Qualitätsstufen wie nächster Nachbar, linear, kubisch, linear mit mehreren Stichproben, anisotrop und kubisch hoher Qualität.

> [!Note]  
> Im anisotropen Modus werden beim Skalieren jedoch Mipmaps generiert, wenn Sie die **Cached-Eigenschaft** für die Effekte, die für die Transformation eingegeben werden, auf TRUE festlegen, werden die Mipmaps nicht jedes Mal für ausreichend kleine Bilder generiert.

 


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



Durch diese Verwendung des affinen 2D-Transformationseffekts wird die Bitmap gegen den Uhrzeigersinn leicht gedreht.



| Vorher                                                            |
|-------------------------------------------------------------------|
| ![2D-affiner Effekt vor dem Bild.](images/default-before.jpg)      |
| Danach                                                             |
| ![2D-affiner Effekt nach dem Bild.](images/21-2daffinetransform.png) |



 

## <a name="compositing-images"></a>Zusammenordnen von Bildern

Einige Effekte akzeptieren mehrere Eingaben und zusammengesetzt sie zu einem resultierenden Bild.

Die integrierten zusammengesetzten und arithmetischen zusammengesetzten Effekte bieten verschiedene Modi. Weitere Informationen finden Sie im [Zusammengesetzten](composite.md) Thema. Der [Blend-Effekt](blend.md) verfügt über eine Vielzahl von GPU-beschleunigten Modi.


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

## <a name="pixel-adjustments"></a>Pixelanpassungen

Es gibt einige integrierte Direct2D-Effekte, mit denen Sie die Pixeldaten ändern können. Beispielsweise kann der Farbmatrixeffekt verwendet werden, um die Farbe eines Bilds zu ändern.


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



Dieser Code verwendet das Bild und ändert die Farbe, wie in den Beispielbildern hier gezeigt.



| Vorher                                                          |
|-----------------------------------------------------------------|
| ![Farbmatrixeffekt vor dem Bild.](images/default-before.jpg) |
| Danach                                                           |
| ![Farbmatrixeffekt nach Bild.](images/15-colormatrix.png)  |



 

Weitere Informationen finden Sie im Abschnitt [Integrierte Farbeffekte.](how-to-create-a-solid-color-brush.md)

## <a name="building-effect-graphs"></a>Erstellen von Effektdiagrammen

Sie können Effekte verketten, um Bilder zu transformieren. Der Code hier wendet z. B. einen Schatten und eine 2D-Transformation an und kombiniert dann die Ergebnisse zusammen.


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

![Schatteneffektausgabe.](images/effect-overview-shadow.png)

Effekte nehmen [**ID2D1Image-Objekte**](/windows/win32/api/d2d1/nn-d2d1-id2d1image) als Eingabe an. Sie können eine [**ID2D1Bitmap verwenden,**](/windows/win32/api/d2d1/nn-d2d1-id2d1bitmap) da die Schnittstelle von **ID2D1Image abgeleitet ist.** Sie können auch [**ID2D1Effect::GetOutput**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1effect-getoutput) verwenden, um die Ausgabe eines [**ID2D1Effect-Objekts**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect) als **ID2D1Image** zu erhalten, oder die **SetInputEffect-Methode** verwenden, die die Ausgabe für Sie konvertiert. In den meisten Fällen besteht ein Effektdiagramm aus direkt miteinander **verketteten ID2D1Effect-Objekten,** wodurch es einfach ist, mehrere Effekte auf ein Bild anzuwenden, um überzeugende Visuals zu erstellen.

Weitere [Informationen finden Sie unter Anwenden von Effekten auf](how-to-apply-effects-to-primitives.md) Primitive.

## <a name="related-topics"></a>Zugehörige Themen

[Direct2D–Beispiel für grundlegende Bildeffekte](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct2D%20basic%20image%20effects%20sample)

[Integrierte Effekte](built-in-effects.md)