---
title: Kontrast Effekt
description: Erhöht oder verringert den Kontrast eines Bilds.
ms.assetid: c0cc0f86-f6d4-e951-0cdd-dbad488e0793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6f287b1309aceadc4709bae3b1c2101a06df32d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040716"
---
# <a name="contrast-effect"></a>Kontrast Effekt

Erhöht oder verringert den Kontrast eines Bilds.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Contrast.

Die Funktion "Kontrast" ändert jeden farbchannelwert mithilfe von zwei, schrittweisen, quadratischen Polynomen, die mit der Neigungs Kontinuität am Punkt (0,5, 0,5) übereinstimmen.

![schrittweise quadratische Polynomen, die mit der Neigungs Kontinuität an der Stelle (0,5, 0,5) erfüllen](images/contrast-effect-slope.png)

-   [Beispiel Bilder](#example-images)
-   [Beispielcode](#sample-code)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-images"></a>Beispiel Bilder

Dieses Beispiel zeigt die Ausgabe des Effekts mit angewendetem maximalem Kontrast (Kontrast = 1,0).

Vorher

![Bild vor Auswirkung wird angewendet](images/contrast-effect-before.png)

Nach

![Bild nach dem Anwenden der Auswirkung](images/contrast-effect-after.png)

## <a name="sample-code"></a>Beispielcode

```cpp
ComPtr<ID2D1Effect> contrastEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Contrast, &contrastEffect);
 
contrastEffect->SetInput(0, bitmap);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CONTRAST, 0.5f);
contrastEffect->SetValue(D2D1_CONTRAST_PROP_CLAMP_INPUT, TRUE);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(contrastEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Effekt Eigenschaften

Die Eigenschaften für den Kontrast Effekt werden durch die [**\_ \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_contrast_prop) -Enumeration D2D1 Kontraste definiert.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
