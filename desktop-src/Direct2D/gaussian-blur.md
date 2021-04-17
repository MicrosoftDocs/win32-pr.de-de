---
title: Gauscher Weichzeichnereffekt
description: Verwenden Sie den gauischen Weichzeichnereffekt, um auf der Grundlage der gauschen Funktion für das gesamte Eingabebild einen weich Zeiger zu erstellen.
ms.assetid: 6B8C9A0A-81D6-4CC2-B30B-995D4C2E59FC
keywords:
- Gauscher Weichzeichner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfbe8b309a498315e389be45d382eca3ee1b98ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104558451"
---
# <a name="gaussian-blur-effect"></a>Gauscher Weichzeichnereffekt

Verwenden Sie den gauischen Weichzeichnereffekt, um auf der Grundlage der gauschen Funktion für das gesamte Eingabebild einen weich Zeiger zu erstellen.

Mithilfe dieses Effekts können Sie Leuchten-und Schlag Schatten erstellen und mithilfe des zusammen [gesetzten](composite.md) Effekts das Ergebnis auf das ursprüngliche Bild anwenden. Es ist nützlich bei der Foto Verarbeitung für Filter wie Highlights und Shadows. Sie können die Ausgabe dieses Effekts für die Eingabe in Beleuchtungseffekte verwenden, wie z. b. die Glanz [Beleuchtung](specular-lighting.md) oder [diffuse Beleuchtungs](diffuse-lighting.md) Effekte, da der Alphakanal verschwommen ist, und die Beleuchtungseffekte verwenden den Alphakanal, um die Oberflächengeometrie als Höhen Zuordnung zu bestimmen.

Dieser Effekt wird vom integrierten [Schatten](drop-shadow.md) Effekt verwendet.

Die CLSID für diesen Effekt ist CLSID \_ D2D1GaussianBlur.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Optimierungs Modi](#optimization-modes)
-   [Rahmen Modi](#border-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| Nach                                                        |
| ![das Bild nach der Transformation.](images/1-gaussianblur.png) |



 


```C++
ComPtr<ID2D1Effect> gaussianBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1GaussianBlur, &gaussianBlurEffect);

gaussianBlurEffect->SetInput(0, bitmap);
gaussianBlurEffect->SetValue(D2D1_GAUSSIANBLUR_PROP_STANDARD_DEVIATION, 3.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(gaussianBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                    | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                         |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation (Standardabweichung)<br/> D2D1 \_ gausianweichungs- \_ \_ Standard \_ Abweichung<br/> | Die auf das Bild anzuwendende Menge an weich. Sie können den weichungs Radius des Kernels berechnen, indem Sie die Standardabweichung um 3 multiplizieren. Die Einheiten der Standardabweichung und des weichungs RADIUS sind Dips. Mit einem Wert von NULL Dips wird dieser effektvoll ständig deaktiviert. Der Typ ist "float".<br/> Der Standardwert ist 3.0 f.<br/> |
| Optimization<br/> D2D1 \_ gausianweich- \_ Prop- \_ Optimierung<br/>             | Der Optimierungs Modus. Weitere Informationen finden Sie unter [Optimierungs Modi](#optimization-modes) . Der Typ ist "D2D1 \_ gauanweich- \_ Optimierung".<br/> Der Standardwert ist "D2D1 \_ gauanweich- \_ Optimierung" \_ .<br/>                                                                                                            |
| Bordermode<br/> D2D1 \_ gausianweich-Prop-Rahmen \_ \_ \_ Modus<br/>               | Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart. Weitere Informationen finden Sie unter [Border Modes](#border-modes) . <br/> Der Typ ist der D2D1 \_ gausid- \_ Rahmen \_ Modus.<br/> Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.<br/>                                                                                   |



 

## <a name="optimization-modes"></a>Optimierungs Modi



| Name                                          | BESCHREIBUNG                                                                                                                           |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| D2D1- \_ \_ Optimierungs Geschwindigkeit für directionalblur \_    | Wendet interne Optimierungen an, wie z. b. die vorab Skalierung bei relativ kleinen Radii. Verwendet lineare Filterung.                                  |
| D2D1 \_ directionalblur- \_ Optimierung \_ ausgeglichen | Verwendet die gleichen Optimierungs Schwellenwerte wie der Geschwindigkeits Modus, verwendet jedoch die drei lineare Filterung.                                                    |
| D2D1 \_ directionalblur- \_ Optimierungs \_ Qualität  | Verwendet nur interne Optimierungen mit großen weichungs Radien, bei denen es weniger wahrscheinlich ist, dass Näherungen sichtbar sind. Verwendet die drei lineare Filterung. |



 

## <a name="border-modes"></a>Rahmen Modi



| Name                     | BESCHREIBUNG                                                                                                                                                                                                              |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| D2D1 \_ Border \_ Mode \_ Soft | Der Effekt füllt das Bild mit transparenten schwarzen Pixeln auf, da es den Weichzeichnerkernel anwendet, was zu einem weichen Rand führt. <br/>                                                                                             |
| D2D1 \_ Rahmen \_ Modus \_ hart | Der Effekt bindet die Ausgabe an die Größe des Eingabe Bilds. Wenn der Effekt den Weichzeichnerkernel anwendet, erweitert er das Eingabebild mit einer Rahmen Transformation für einen Spiegelungs Typ für Beispiele außerhalb der Eingabe Begrenzungen.<br/> |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Ausgabe dieses Effekts kann größer als die Eingabe Bitmap sein, die auf dem weichzeichenradius und dem Rahmen Modus basiert. Wenn der Border-Modus auf D2D1 \_ Border Mode Soft festgelegt ist \_ , wird \_ die s imale der Ausgabe Bitmap um die Größe des Weichzeichnerkernels vergrößert, dargestellt in Pixel. Diese Tabelle stellt eine Gleichung bereit, mit der Sie die Ausgabe Bitmap berechnen können.

`Output bitmap growth (X and Y) = StandardDeviation  (DIPs)*6*((User DPI)/96)`

Wenn also die Bildgröße um 10 Pixel in jeder Richtung zunimmt, befindet sich die obere linke Ecke des Bilds bei (-5,-5), während die untere Rechte bei (105, 105) liegt.

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

 

