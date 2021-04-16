---
title: Highlights und Schatteneffekte
description: Passt die Highlights und Schatten des Bilds an.
ms.assetid: ebbb7d99-9144-ffff-af73-d89e7d269924
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d595a5b82a2df0b0b0bab14c03e6a807511ed61
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104562388"
---
# <a name="highlights-and-shadows-effect"></a>Highlights und Schatteneffekte

Passt die Highlights und Schatten des Bilds an.

Die CLSID für diesen Effekt ist CLSID \_ D2D1HighlightsShadows.

-   [Beispielbild](#example-image)
-   [Beispielcode](#sample-code)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für Effekte Ausgabe](images/highlights-and-shadows-effect.png)

## <a name="sample-code"></a>Beispielcode

```cpp
ComPtr<ID2D1Effect> highlightsAndShadowsEffect;
m_d2dContext->CreateEffect(CLSID_D2D1HighlightsShadows, &highlightsAndShadowsEffect);
 
highlightsAndShadowsEffect->SetInput(0, bitmap);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_HIGHLIGHTS, 0.0f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_SHADOWS, 0.5f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_CLARITY, 0.2f);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_INPUT_GAMMA, D2D1_HIGHLIGHTSANDSHADOWS_INPUT_GAMMA_LINEAR);
highlightsAndShadowsEffect->SetValue(D2D1_HIGHLIGHTSANDSHADOWS_PROP_MASK_BLUR_RADIUS, 1.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(hueToRgbEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Effekt Eigenschaften

Die Eigenschaften für den Hervorhebungen und den Schatteneffekt werden von der [**D2D1 \_ highlighnerandshadows- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_highlightsandshadows_prop) -Enumeration definiert.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
