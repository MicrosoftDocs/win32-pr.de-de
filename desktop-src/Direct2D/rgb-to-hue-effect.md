---
title: RGB-to-Hue-Effekt
description: Konvertiert ein RGB-Bild entweder in die HSL-Farbräume (Hue, Saturation, Lightness) oder HSV (Hue, Saturation, Value).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c474705d050c2ef2eff9050a759c60c5d8f1098440e06601ec1e3981e349aaff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118160386"
---
# <a name="rgb-to-hue-effect"></a>RGB-to-Hue-Effekt

Konvertiert ein RGB-Bild entweder in die HSL-Farbräume (Hue, Saturation, Lightness) oder HSV (Hue, Saturation, Value).

HSL und HSV sind zwei verschiedene Modelle für die Darstellung einer RGB-Farbe in einem farbigen Farbraum. Sie sind nützlich, da Sie mit intuitiveren Konzepten wie Farbton und Intensität über eine Farbe nachdenken können, anstatt rote, grüne und blaue Werte zu kombinieren.

Dieser Effekt normalisiert die Ausgabedaten (Farbton, Sättigungswert für HSV oder Farbton, Sättigung, Helligkeit für HSL) in den Bereich \[ 0, \] 1.

Die CLSID für diesen Effekt ist CLSID \_ D2D1RgbToHue.

Um das Verhalten dieses Effekts umzukehren, verwenden Sie den [Hue to RGB-Effekt](hue-to-rgb-effect.md).

-   [Beispielcode](#sample-code)
-   [Effekteigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="sample-code"></a>Beispielcode


```C++
ComPtr<ID2D1Effect> rgbToHueEffect;
m_d2dContext->CreateEffect(CLSID_D2D1RgbToHue, &rgbToHueEffect);
 
rgbToHueEffect->SetInput(0, bitmap);
rgbToHueEffect->SetValue(D2D1_RGBTOHUE_PROP_OUTPUT_COLOR_SPACE, D2D1_RGBTOHUE_OUTPUT_COLOR_SPACE_HUE_SATURATION_VALUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(rgbToHueEffect.Get());
m_d2dContext->EndDraw();

```



## <a name="effect-properties"></a>Effect-Eigenschaften

Die Eigenschaften für den Kontrasteffekt werden durch die [**D2D1 \_ RGBTOHUE \_ PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
