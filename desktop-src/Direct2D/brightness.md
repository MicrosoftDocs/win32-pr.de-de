---
title: Helligkeitseffekt
description: Verwenden Sie den Helligkeitseffekt, um die Helligkeit des Bilds zu steuern.
ms.assetid: 5088D4D4-DFC8-45D3-B1C3-D576742D931C
keywords:
- Helligkeitseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f88b67615948cbea74333605e900de194c0eeeb3d747d83af5eae8a750e6f135
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119215401"
---
# <a name="brightness-effect"></a>Helligkeitseffekt

Verwenden Sie den Helligkeitseffekt, um die Helligkeit des Bilds zu steuern.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Brightness.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild



| Vorher                                                      |
|-------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)  |
| Danach                                                       |
| ![das Bild nach der Transformation.](images/34-brightness.png) |



 


```C++
ComPtr<ID2D1Effect> brightnessEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Brightness, &brightnessEffect);

brightnessEffect->SetValue(D2D1_BRIGHTNESS_PROP_BLACK_POINT, D2D1::Vector2F(0.0f, 0.2f));

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(brightnessEffect.Get());
m_d2dContext->EndDraw();
```



## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename der Eigenschaft                                                 | Typ und Standardwert                              | Beschreibung                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Weißtons<br/> D2D1 \_ \_ HELLIGKEITSPROP \_ WHITE \_ POINT<br/> | D2D1 \_ VECTOR \_ 2F<br/> {1.0f, 1.0f}<br/> | Der obere Teil der Helligkeitsübertragungskurve. Der weiße Punkt passt die Darstellung der helleren Teile des Bilds an. Diese Eigenschaft gilt sowohl für den x-Wert als auch für den y-Wert in dieser Reihenfolge. Jeder Wert dieser Eigenschaft liegt zwischen 0 und 1 (einschließlich). |
| BlackPoint<br/> D2D1 \_ \_ HELLIGKEITSPROP \_ BLACK \_ POINT<br/> | D2D1 \_ VECTOR \_ 2F<br/> {0.0f, 0.0f}<br/> | Der untere Teil der Helligkeitsübertragungskurve. Der schwarze Punkt passt die Darstellung der dunkleren Teile des Bilds an. Diese Eigenschaft gilt sowohl für den x-Wert als auch für den y-Wert in dieser Reihenfolge. Jeder Wert dieser Eigenschaft liegt zwischen 0 und 1 (einschließlich).   |



 

Dieser Effekt verwendet die angegebenen weißen und schwarzen Punkte, um eine Übertragungsfunktion zu generieren, die zum Anpassen der Bitmap verwendet wird. Die nächste Gleichung beschreibt die Übertragungsfunktion. Die Eingabeintensiven werden zwischen 0 und 1 definiert.

![Helligkeitsalgorithmus](images/brightness-formula1.png)

Der Effektalgorithmus implementiert eine Gleichung, die die Übertragungsfunktion erstellt. Wir verwenden diese Funktion, um die Bildpixel anzupassen. Die x- und y-Werte des schwarzen Punkts und des weißen Punkts sind die Koordinaten in zwei Dimensionen, die verbunden sind, um die Transformation zu bilden. Jeder Teil der endgültigen Ausgabegleichung:

1.  Konvertiert die Bilddaten mithilfe dieser Gleichung aus dem linearen Raum in den nicht linearen Raum:![Hilfsfunktion 1](images/brightness-formula2.png)

2.  Passt das Bild entsprechend den folgenden Werten an:
    -   *input* sind die Pixelstärkewerte des Eingabebilds von 0 bis 1.

    -   *White Pt. (x, y) die* Position der Transformationskurve für hellere Pixelstärken.

    -   *Black Pt. (x, y)* ist die Position der Transformationskurve für abgeblendere Pixelstärken.

3.  Konvertiert die Bilddaten mithilfe dieser Gleichung wieder in linearen Raum: ![Hilfsfunktion 2](images/brightness-formula3.png)

Die endgültige Ausgabegleichung und die Komponententeile werden hier gezeigt.

![die vollständigen Berechnungen für die Helligkeitsanpassung](images/brightness-formula4.png)

## <a name="output-bitmap"></a>Ausgabebitmap

Die Größe der Ausgabebitmap ist mit der Größe der Eingabebitmap identisch.

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

 

