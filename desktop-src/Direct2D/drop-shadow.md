---
title: Schatteneffekt
description: Verwenden Sie den Schatteneffekt, um einen Schatten aus dem Alphakanal eines Bilds zu generieren.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- Schatteneffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c42fd8755078dd79f2b01b623b1839785beb3c3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340408"
---
# <a name="shadow-effect"></a>Schatteneffekt

Verwenden Sie den Schatteneffekt, um einen Schatten aus dem Alphakanal eines Bilds zu generieren. Der Schatten ist für höhere Alpha Werte transparenter und transparenter für niedrigere Alpha Werte. Sie können den Grad der weich Zeichnung und die Farbe des Schattens festlegen.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Optimierungs Modi](#optimization-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

Die CLSID für diesen Effekt ist CLSID \_ D2D1Shadow.

## <a name="example-image"></a>Beispielbild

Das Beispiel hier zeigt die Ausgabe des Schatten Effekts übersetzt und rechts mit dem Quell Bild am ursprünglichen Speicherort. Der Schatteneffekt gibt nur den Schatten aus.



| Vorher                                                  |
|---------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/8-crop.png)      |
| Nach                                                   |
| ![das Bild nach der Transformation.](images/25-shadow.png) |



 


```C++
ComPtr<ID2D1Effect> shadowEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Shadow, &shadowEffect);

shadowEffect->SetInput(0, bitmap);

// Shadow is composited on top of a white surface to show opacity.
ComPtr<ID2D1Effect> floodEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Flood, &floodEffect);

floodEffect->SetValue(D2D1_FLOOD_PROP_COLOR, D2D1::Vector4F(1.0f, 1.0f, 1.0f, 1.0f));

ComPtr<ID2D1Effect> affineTransformEffect;
m_d2dContext->CreateEffect(CLSID_D2D12DAffineTransform, &affineTransformEffect);

affineTransformEffect->SetInputEffect(0, shadowEffect.Get());

D2D1_MATRIX_3X2_F matrix = D2D1::Matrix3x2F::Translation(20, 20));

affineTransformEffect->SetValue(D2D1_2DAFFINETRANSFORM_PROP_TRANSFORM_MATRIX, matrix);

ComPtr<ID2D1Effect> compositeEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Composite, &compositeEffect);

compositeEffect->SetInputEffect(0, floodEffect.Get());
compositeEffect->SetInputEffect(1, affineTransformEffect.Get());
compositeEffect->SetInput(2, bitmap);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(compositeEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blurstandardabweichung<br/> D2D1 \_ Shadow \_ Prop \_ - \_ Standard \_ Abweichung<br/> | Der auf den Alpha-Kanal des Bilds anzuwendende Wert. Sie können den weichungs Radius des Kernels berechnen, indem Sie die Standardabweichung um 3 multiplizieren. Die Einheiten der Standardabweichung und des weichungs RADIUS sind Dips.<br/> Diese Eigenschaft ist identisch mit der [Gaußscher Weichzeichner](gaussian-blur.md) Eigenschaft Standardabweichung. <br/> Der Typ ist "float".<br/> Der Standardwert ist 3.0 f.<br/> |
| Color<br/> D2D1 \_ Schatten- \_ Prop- \_ Farbe<br/>                                     | Die Farbe des Schlagschattens. Diese Eigenschaft ist ein D2D1 \_ Vector \_ 4f, definiert als: (R, G, B, a). Sie müssen diese Farbe in der geraden Alpha Angabe angeben.<br/> Der Typ ist "D2D1 \_ Vector \_ 4f".<br/> Der Standardwert ist {0,0 f, 0,0 f, 0,0 f, 1.0 f}.<br/>                                                                                                                                                                     |
| Optimization<br/> D2D1- \_ Schatten- \_ Prop- \_ Optimierung<br/>                       | Die Ebene der Leistungsoptimierung.<br/> Der Typ ist die D2D1- \_ Schatten \_ Optimierung.<br/> Der Standardwert ist D2D1 \_ Schatten \_ Optimierung \_ ausgeglichen.<br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a>Optimierungs Modi



| Name                                          | BESCHREIBUNG                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1- \_ \_ Optimierungs Geschwindigkeit für directionalblur \_    | Wendet interne Optimierungen an, wie z. b. die vorab Skalierung bei relativ kleinen Radii. Verwendet lineare Filterung.                                  |
| D2D1 \_ directionalblur- \_ Optimierung \_ ausgeglichen | Verwendet die gleichen Optimierungs Schwellenwerte wie der Geschwindigkeits Modus, verwendet jedoch die drei lineare Filterung.                                                    |
| D2D1 \_ directionalblur- \_ Optimierungs \_ Qualität  | Verwendet nur interne Optimierungen mit großen weichungs Radien, bei denen es weniger wahrscheinlich ist, dass Näherungen sichtbar sind. Verwendet die drei lineare Filterung. |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe Bitmap entspricht der Größe der weichzeichnerausgabe. Der Betrag, um den die Ausgabe Bitmap relativ zur ursprünglichen Bitmap vergrößert werden kann, kann mit der folgenden Formel berechnet werden:

Vergrößerung der Bitmap (X und Y) = blurstandardabweichung (geräteunabhängige Pixel (Dips)) \* 6 \* (Benutzer dpi)/96

Die Ausgabe erhöht sich gleichmäßig in alle Richtungen. wenn die Größe beispielsweise um 10 Pixel in jeder Richtung zunimmt, befindet sich die obere linke Ecke der Bitmap bei (-5,-5), und die untere rechte wird um (105, 105), wie im Diagramm dargestellt.

![Diagramm der Größe der Ausgabegröße der Schatteneffekte.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Platt Form Update für Windows 7 \[ -Desktop-Apps für \| Windows Store-Apps\] |
| Header                   | d2d1effects. h                                                                      |
| Bibliothek                  | d2d1. lib, dxguid. lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

