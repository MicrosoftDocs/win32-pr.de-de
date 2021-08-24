---
title: Schatteneffekt
description: Verwenden Sie den Schatteneffekt, um einen Schatten aus dem Alphakanal eines Bilds zu generieren.
ms.assetid: 53525584-10CF-46C2-9400-C4FB225D4693
keywords:
- Schatteneffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5d88924140caac22b688a0ccb6948ee74312411c770bff99360847ef2cd1b4c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119833052"
---
# <a name="shadow-effect"></a>Schatteneffekt

Verwenden Sie den Schatteneffekt, um einen Schatten aus dem Alphakanal eines Bilds zu generieren. Der Schatten ist für höhere Alphawerte nicht transparent und für niedrigere Alphawerte transparenter. Sie können die Menge an Weichzeichnern und die Farbe des Schattens festlegen.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Optimierungsmodi](#optimization-modes)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

Die CLSID für diesen Effekt ist CLSID \_ D2D1Shadow.

## <a name="example-image"></a>Beispielbild

Das folgende Beispiel zeigt die Ausgabe des Schatteneffekts, der nach unten und rechts übersetzt wurde, wobei das Quellbild am ursprünglichen Speicherort darüber zusammengesetzt ist. Der Schatteneffekt gibt nur den Schatten aus.



| Vorher                                                  |
|---------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/8-crop.png)      |
| Danach                                                   |
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



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                                                        | Beschreibung                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| BlurStandardDeviation<br/> D2D1 \_ \_ SCHATTENPROP \_ BLUR \_ STANDARD \_ DEVIATION<br/> | Die Menge an Weichzeichnern, die auf den Alphakanal des Bilds angewendet werden soll. Sie können den Weichzeichnerradius des Kernels berechnen, indem Sie die Standardabweichung mit 3 multiplizieren. Die Einheiten der Standardabweichung und des Weichzeichnerradius sind DIPs.<br/> Diese Eigenschaft entspricht der [Gaußscher Weichzeichner](gaussian-blur.md) Standardabweichungseigenschaft. <br/> Der Typ ist FLOAT.<br/> Der Standardwert ist 3,0f.<br/> |
| Color<br/> D2D1 \_ SHADOW \_ PROP \_ COLOR<br/>                                     | Die Farbe des Schlagschattens. Diese Eigenschaft ist ein D2D1 \_ VECTOR \_ 4F, der wie folgt definiert ist: (R, G, B, A). Sie müssen diese Farbe in geradem Alpha angeben.<br/> Der Typ ist D2D1 \_ VECTOR \_ 4F.<br/> Der Standardwert ist {0.0f, 0.0f, 0.0f, 1.0f}.<br/>                                                                                                                                                                     |
| Optimization<br/> \_D2D1–SCHATTENPROP-OPTIMIERUNG \_ \_<br/>                       | Der Grad der Leistungsoptimierung.<br/> Der Typ ist D2D1 \_ SHADOW \_ OPTIMIZATION.<br/> Der Standardwert ist D2D1 \_ SHADOW \_ OPTIMIZATION \_ BALANCED.<br/>                                                                                                                                                                                                                                                   |



 

## <a name="optimization-modes"></a>Optimierungsmodi



| Name                                          | Beschreibung                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ SPEED    | Wendet interne Optimierungen wie die Vorabskalierung bei relativ kleinen Radien an. Verwendet lineare Filterung.                                  |
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ BALANCED | Verwendet die gleichen Optimierungsschwellenwerte wie der Geschwindigkeitsmodus, verwendet jedoch die trilineare Filterung.                                                    |
| D2D1 \_ DIRECTIONALBLUR \_ OPTIMIZATION \_ QUALITY  | Verwendet nur interne Optimierungen mit großen Weichzeichnerradien, bei denen Näherungen weniger wahrscheinlich sichtbar sind. Verwendet die trilineare Filterung. |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Größe der Ausgabebitmap entspricht der Größe der Weichzeichnerausgabe. Der Betrag, um den die Ausgabebitmap relativ zur ursprünglichen Bitmap wächst, kann mithilfe der folgenden Gleichung berechnet werden:

Output Bitmap Growth (X and Y) = BlurStandardDeviation (device-independent pixels (DIPs)) \* 6 \* (User DPI)/96

Die Ausgabe erhöht sich gleichmäßig in alle Richtungen. Wenn die Größe also z. B. in jeder Richtung um 10 Pixel zunimmt, befindet sich die obere linke Ecke der Bitmap bei (-5, -5), und die untere rechte Seite befindet sich bei (105, 105), wie im Diagramm hier dargestellt.

![Diagramm zur Vergrößerung der Schatteneffektausgabegröße.](images/drop-shadow-output-growth.png)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | Windows 8 und Plattformupdate für Windows 7 \[ Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects.h                                                                      |
| Bibliothek                  | d2d1.lib, dxguid.lib                                                               |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**ID2D1Effect**](/windows/win32/api/d2d1_1/nn-d2d1_1-id2d1effect)
</dt> </dl>

 

