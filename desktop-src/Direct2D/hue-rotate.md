---
title: Hue-Rotatationseffekt
description: Verwenden Sie den Farbtonrotationseffekt, um den Farbton eines Bilds zu ändern, indem Sie eine Farbmatrix basierend auf dem Drehwinkel anwenden.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- Farbtonrotationseffekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 531ab9b1649db96bc5ee100df98ed10b4021b506e3ad71bb426778655348b2df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119569129"
---
# <a name="hue-rotatation-effect"></a>Hue-Rotatationseffekt

Verwenden Sie den Farbtonrotationseffekt, um den Farbton eines Bilds zu ändern, indem Sie eine Farbmatrix basierend auf dem Drehwinkel anwenden.

Die CLSID für diesen Effekt ist CLSID \_ D2D1HueRotation.

-   [Beispielbild](#example-image)
-   [Effect-Eigenschaften](#effect-properties)
-   [Ausgabebitmap](#output-bitmap)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das folgende Beispiel zeigt die Ein- und Ausgabebilder des Farbtonrotationseffekts mit einem Drehwinkel von 270 Grad.



| Vorher                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| Danach                                                        |
| ![das Bild nach der Transformation.](images/17-huerotation.png) |



 


```C++
ComPtr<ID2D1Effect> hueRotationEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueRotation, &hueRotationEffect);

hueRotationEffect->SetInput(0, bitmap);
hueRotationEffect->SetValue(D2D1_HUEROTATION_PROP_ANGLE, 270.0f);

m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueRotationEffect.Get());
m_d2dContext->EndDraw();
```



Der Effekt berechnet eine Farbmatrix basierend auf dem Drehwinkel (*?*), den Sie mit der D2D1 \_ HUEROTATION \_ PROP \_ ANGLE-Eigenschaft angeben. Hier sind die Matrixgleichungen.

![Berechnungen der Farbtonrotation](images/hue-formula.png)

Die erstellte Matrix hängt nur vom Drehwinkel ab. Sie können den [Farbmatrixeffekt](color-matrix.md) verwenden, wenn Sie eine bestimmte Matrix benötigen.

## <a name="effect-properties"></a>Effect-Eigenschaften



| Anzeigename und Indexenumeration                         | Typ und Standardwert           | Beschreibung                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| Angle<br/> D2D1 \_ HUEROTATION \_ PROP \_ ANGLE<br/> | GLEITKOMMAZAHL<br/> 0.0f<br/> | Der Winkel, um den der Farbton in Grad gedreht werden soll. |



 

## <a name="output-bitmap"></a>Ausgabebitmap

Die Ausgabebitmapgröße entspricht der Größe der Eingabebitmap.

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

 

