---
title: Effekt "Tastenknötigung"
description: Konvertiert eine bestimmte Farbe plus oder minus einer Toleranz in Alpha. Beispielsweise kann der Hintergrund eines Bilds für einen Überlagerungseffekt mit grünem Bildschirm entfernt werden.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 485cec7842c8460169b9c335eb74e9cc6d5a13e0541a49fc99835dfaa591efc2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075588"
---
# <a name="chroma-key-effect"></a>Effekt "Tastenknötigung"

Konvertiert eine bestimmte Farbe plus oder minus einer Toleranz in Alpha. Beispielsweise kann der Hintergrund eines Bilds für einen Überlagerungseffekt mit grünem Bildschirm entfernt werden.

Die CLSID für diesen Effekt ist CLSID \_ D2D1ChromaKey.

-   [Beispielbild](#example-image)
-   [Beispielcode](#sample-code)
-   [Effect-Eigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für die Auswirkungsausgabe](images/chromakey-effect.png)

> [!Note]  
> In diesem Beispiel ist die Ausgabe des Effekts "taste-key" das zweite Bild mit dem transparenten Hintergrund des Kontrollkästchens. Das dritte Bild kombiniert dies mit einem Hintergrundbild für die endgültige Überlagerung mit grünem Bildschirm.

## <a name="sample-code"></a>Beispielcode

```cppcx
ComPtr<ID2D1Effect> chromakeyEffect;
m_d2dContext->CreateEffect(CLSID_D2D1ChromaKey, &chromakeyEffect);
 
chromakeyEffect->SetInput(0, bitmap);
chromaKeyEffect->SetValue(D2D1_CHROMAKEY_PROP_COLOR, {0.0f, 1.0f, 0.0f, 0.0f});
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_TOLERANCE, 0.2f);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_INVERT_ALPHA, false);
chromakeyEffect->SetValue(D2D1_CHROMAKEY_PROP_FEATHER, false);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(chromakeyEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Effect-Eigenschaften

Die Eigenschaften für den Effekt "key-key" werden durch die [**ENUMERATION D2D1KEY \_ \_ PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) definiert.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
