---
title: Hue-to-RGB-Effekt
description: Konvertiert ein HSL-Bild (Hue, Sättigung, Helligkeit) oder HSV-Bild (Hue, Sättigung, Wert) in den RGB-Farbraum.
ms.assetid: 18e92535-9e89-bf8d-b8c3-a49b645fc417
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3abc45ec09cc77935c332a702648472e6be7edeb06bdf9237e4232f467b1e073
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118003131"
---
# <a name="hue-to-rgb-effect"></a>Hue-to-RGB-Effekt

Konvertiert ein HSL-Bild (Hue, Sättigung, Helligkeit) oder HSV-Bild (Hue, Sättigung, Wert) in den RGB-Farbraum.

HSL und HSV sind zwei verschiedene Modelle für die Darstellung einer RGB-Farbe in einem farbigen Farbraum. Sie sind nützlich, da Sie mit intuitiveren Konzepten wie Farbton und Intensität über eine Farbe nachdenken können, anstatt rote, grüne und blaue Werte zu kombinieren.

Dieser Effekt durchläuft alle Alpha-Eingabewerte.

Die CLSID für diesen Effekt ist CLSID \_ D2D1HueToRgb.

Um das Verhalten dieses Effekts umzukehren, verwenden Sie den [RGB-Zu-Hue-Effekt](rgb-to-hue-effect.md).

-   [Beispielcode](#sample-code)
-   [Effekteigenschaften](#effect-properties)
-   [Requirements](#requirements)
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

## <a name="effect-properties"></a>Effect-Eigenschaften

Die Eigenschaften für den Kontrasteffekt werden durch die [**D2D1 \_ HUETORGB \_ PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_huetorgb_prop) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |



## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
