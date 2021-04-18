---
title: RGB-zu-Hue-Effekt
description: Konvertiert ein RGB-Bild in die Farbbereiche HSL (Hue, Sättigung, Helligkeit) oder HSV (Farbton, Sättigung, Wert).
ms.assetid: 1def972d-8172-9217-8ce7-abce4a93f6e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ccb4d3f67d116426d7a3497c04c4e8fb115b74
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391828"
---
# <a name="rgb-to-hue-effect"></a>RGB-zu-Hue-Effekt

Konvertiert ein RGB-Bild in die Farbbereiche HSL (Hue, Sättigung, Helligkeit) oder HSV (Farbton, Sättigung, Wert).

HSL und HSV sind zwei verschiedene Modelle für die Darstellung einer RGB-Farbe in einem zylindrischen Farbraum. Sie sind nützlich, da Sie eine Farbe mit intuitiveren Konzepten wie Hue und Intensität und Kombinieren von roten, grünen und blauen Werten haben können.

Dieser Effekt normalisiert die Ausgabedaten (Hue, Sättigungswert für HSV, Hue, Sättigung, Helligkeit für HSL) in den Bereich \[ 0, 1 \] .

Die CLSID für diesen Effekt ist CLSID \_ D2D1RgbToHue.

Um das Verhalten dieses Effekts umzukehren, verwenden Sie den [Effekt Hue in RGB](hue-to-rgb-effect.md).

-   [Beispielcode](#sample-code)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
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



## <a name="effect-properties"></a>Effekt Eigenschaften

Die Eigenschaften für den Kontrast Effekt werden durch die [**D2D1 \_ rgbflhue \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_rgbtohue_prop) -Enumeration definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |


## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
