---
title: Richtungsweisendes Effekt
description: Der direktionale Weichzeichnereffekt ähnelt dem gauischen weichungs Wert, mit der Ausnahme, dass Sie den Weichzeichner in eine bestimmte Richtung neigen können.
ms.assetid: 59328FA4-5C27-4A81-AAB2-C5B25B3615C6
keywords:
- direktionaler weich
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e1c098d17929563cf69f4e61416fa0d93a88dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739856"
---
# <a name="directional-blur-effect"></a>Richtungsweisendes Effekt

Der direktionale Weichzeichnereffekt ähnelt dem [gauischen](gaussian-blur.md)weichungs Wert, mit der Ausnahme, dass Sie den Weichzeichner in eine bestimmte Richtung neigen können. Mit diesem Effekt können Sie sehen, wie sich das Bild in Bewegung befindet oder ein animiertes Bild hervorgehoben wird.

Die CLSID für diesen Effekt ist CLSID \_ D2D1DirectionalBlur.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Optimierungs Modi](#optimization-modes)
-   [Rahmen Modi](#border-modes)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                          |
|-----------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)      |
| Nach                                                           |
| ![das Bild nach der Transformation.](images/2-directionalblur.png) |



 


```C++
ComPtr<ID2D1Effect> directionalBlurEffect;
m_d2dContext->CreateEffect(CLSID_D2D1DirectionalBlur, &directionalBlurEffect);

directionalBlurEffect->SetInput(0, bitmap);
directionalBlurEffect->SetValue(D2D1_DIRECTIONALBLUR_PROP_STANDARD_DEVIATION, 7.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(directionalBlurEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| StandardDeviation (Standardabweichung)<br/> D2D1 \_ directionalblur \_ Prop- \_ Standard \_ Abweichung<br/> | Die auf das Bild anzuwendende Menge an weich. Sie können den weichungs Radius des Kernels berechnen, indem Sie die Standardabweichung um 3 multiplizieren. Die Einheiten der Standardabweichung und des weichungs RADIUS sind Dips. Durch den Wert 0 (null) wird dieser Effekt deaktiviert. Der Typ ist "float".<br/> Der Standardwert ist 3.0 f.<br/>                                                                            |
| Angle<br/> D2D1 \_ directionalweichungs \_ \_ Winkel<br/>                           | Der Winkel des weichungs Winkels in Bezug auf die x-Achse, in Richtung gegen den Uhrzeigersinn. Die Einheiten werden in Grad angegeben.<br/> Der Weichzeichnerkernel wird zuerst mit dem gleichen Prozess wie für den [gauischen](gaussian-blur.md) Weichzeichnereffekt generiert. Die Kernel Werte werden dann entsprechend dem weichzeichnerwinkel transformiert.<br/> Der Typ ist "float".<br/> Der Standardwert ist 0,0 f.<br/> |
| Optimization<br/> D2D1 \_ directionaloptimization- \_ Prop- \_ Optimierung<br/>             | Der Optimierungs Modus. Weitere Informationen finden Sie unter [Optimierungs Modi](#optimization-modes) .<br/> Der Typ ist "D2D1 \_ directionalblur \_ Optimization".<br/> Der Standardwert ist D2D1 \_ directionaloptimization \_ Optimization Balancing \_ ausgeglichen. <br/>                                                                                                                                                         |
| Bordermode<br/> D2D1 \_ directionalblur-Prop-Rahmen \_ \_ \_ Modus<br/>               | Der Modus, der verwendet wird, um den Rahmen des Bilds zu berechnen, weich oder hart. Weitere Informationen finden Sie unter [Border Modes](#border-modes) .<br/> Der Typ ist "D2D1 \_ Border \_ Mode".<br/> Der Standardwert ist D2D1 \_ Border \_ Mode \_ Soft.<br/>                                                                                                                                                                 |



 

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

Die Größe der Ausgabe Bitmap erhöht sich basierend auf der Standardabweichung, dem Winkel des Effekts und dem Rahmen Modus. Wenn der Border-Modus auf D2D1 \_ Border Mode Soft festgelegt ist \_ , wird \_ die Größe der Ausgabe Bitmap um die Größe des Weichzeichnerkernels erhöht, dargestellt in Pixel. Diese Gleichungen können verwendet werden, um die Größe der Ausgabe Bitmap zu berechnen.



| Anforderung | Wert |
|------------------------|-------------------------------------------------------------------|
| Ergebnis der Ausgabe Bitmap X | Standardabweichung (Dips) \* 6 \* ((Benutzer dpi)/96) \* cos (Winkel)) |
| Ergebnis der Ausgabe Bitmap Y | Standardabweichung (Dips) \* 6 \* ((Benutzer dpi)/96) \* Sin (Winkel)) |



 

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

 

