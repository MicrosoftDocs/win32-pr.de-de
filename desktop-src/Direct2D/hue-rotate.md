---
title: Effekt der Hue-rotatung
description: Verwenden Sie den Effekt Hue Drehung, um den Farbton eines Bilds zu ändern, indem Sie eine Farbmatrix auf Grundlage des Drehwinkels anwenden.
ms.assetid: D322DB2C-2B8B-4101-BFB2-97E49CAC7BF6
keywords:
- Effekt der Hue-rotatung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525dbe8fc94377080fbae34b80252c84c05073ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104551345"
---
# <a name="hue-rotatation-effect"></a>Effekt der Hue-rotatung

Verwenden Sie den Effekt Hue Drehung, um den Farbton eines Bilds zu ändern, indem Sie eine Farbmatrix auf Grundlage des Drehwinkels anwenden.

Die CLSID für diesen Effekt ist CLSID \_ D2D1HueRotation.

-   [Beispiel Bild](#example-image)
-   [Effekt Eigenschaften](#effect-properties)
-   [Ausgabe Bitmap](#output-bitmap)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

Das Beispiel zeigt die Eingabe-und Ausgabe Bilder des Hue-Drehungs Effekts mit einem Drehungs Winkel von 270 Grad.



| Vorher                                                       |
|--------------------------------------------------------------|
| ![das Bild vor dem Effekt.](images/default-before.jpg)   |
| Nach                                                        |
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



Der Effekt berechnet eine Farbmatrix basierend auf dem Drehungs Winkel (*?*), den Sie mit der \_ \_ Prop Angle-Eigenschaft D2D1 huerotation angeben \_ . Im folgenden finden Sie die Matrix Gleichungen.

![Hue-Rotations Berechnungen](images/hue-formula.png)

Die erstellte Matrix hängt nur vom Drehungs Winkel ab. Sie können den [Farbmatrix](color-matrix.md) Effekt verwenden, wenn Sie eine bestimmte Matrix benötigen.

## <a name="effect-properties"></a>Effekt Eigenschaften



| Anzeige Name und indexenumeration                         | Typ und Standardwert           | BESCHREIBUNG                              |
|------------------------------------------------------------|----------------------------------|------------------------------------------|
| Angle<br/> D2D1 \_ huerotations- \_ Prop- \_ Winkel<br/> | GLEITKOMMAZAHL<br/> 0,0 f<br/> | Der Winkel, um den Farbton in Grad zu drehen. |



 

## <a name="output-bitmap"></a>Ausgabe Bitmap

Die Größe der Ausgabe Bitmap entspricht der Größe der Eingabe Bitmap.

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

 

