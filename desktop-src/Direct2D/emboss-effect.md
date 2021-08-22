---
title: Emboss-Effekt
description: Erstellt eine Graustufenversion des Bilds, das so aussieht, als wäre es in Papierform gestempelt worden.
ms.assetid: 74f63875-35cd-f335-62cd-410a953e53ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d0fe9b779cbad2b73b877338871f7adff3a36fb4bfb1c291be6de94f736088f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586964"
---
# <a name="emboss-effect"></a>Emboss-Effekt

Erstellt eine Graustufenversion des Bilds, das so aussieht, als wäre es in Papierform gestempelt worden.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Ezöss.

-   [Beispielbild](#example-image)
-   [Beispielcode](#sample-code)
-   [Effekteigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für die Effektausgabe](images/emboss-effect.png)

## <a name="sample-code"></a>Beispielcode

```cpp
ComPtr<ID2D1Effect> embossEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Emboss, &embossEffect);
 
embossEffect->SetInput(0, bitmap);
embossEffect->SetValue(D2D1_EMBOSS_PROP_HEIGHT, 1.0f);
embossEffect->SetValue(D2D1_EMBOSS_PROP_DIRECTION, 0.0f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(embossEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Effect-Eigenschaften

Die Eigenschaften für den Emboss-Effekt werden durch die [**D2D1 \_ EMBOSS \_ PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_emboss_prop) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
