---
title: Hue-zu-RGB-Effekt
description: Konvertiert ein Bild vom Typ HSL (Hue, Sättigung, Helligkeit) oder HSV (Farbton, Sättigung, Wert) in den RGB-Farbraum.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82064d01281ab0edf2327f00cf6e852a0bebae53
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949808"
---
# <a name="hue-to-rgb-effect"></a>Hue-zu-RGB-Effekt

Konvertiert ein Bild vom Typ HSL (Hue, Sättigung, Helligkeit) oder HSV (Farbton, Sättigung, Wert) in den RGB-Farbraum.

HSL und HSV sind zwei verschiedene Modelle für die Darstellung einer RGB-Farbe in einem zylindrischen Farbraum. Sie sind nützlich, da Sie eine Farbe mit intuitiveren Konzepten wie Hue und Intensität und Kombinieren von roten, grünen und blauen Werten haben können.

Dieser Effekt durchläuft alle eingegebenen Alpha Werte.

Die CLSID für diesen Effekt ist CLSID \_ D2D1HueToRgb.

Um das Verhalten dieses Effekts umzukehren, verwenden Sie den [RGB-Effekt](rgb-to-hue-effect.md).

-   [Beispielcode](#sample-code)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="sample-code"></a>Beispielcode

```cpp
ComPtr<ID2D1Effect> hueToRgbEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HueToRgb, &hueToRgbEffect);
 
hueToRgbEffect->SetInput(0, bitmap);
hueToRgbEffect->SetValue(D2D1_HUETORGB_INPUT_COLOR_SPACE, D2D1_HUETORGB_INPUT_COLOR_SPACE_HUE_SATURATION_LIGHTNESS);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Effekt Eigenschaften

Die Eigenschaften für den Kontrast Effekt werden von der [**D2D1 \_ huetorgb- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) -Enumeration definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |



## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
