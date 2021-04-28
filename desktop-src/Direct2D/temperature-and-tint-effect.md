---
title: Temperature and Tönungseffekt
description: Temperatur- und Tönungseffekt
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc2c3628e1fdcb1c72a84a9e08736e4215d55514
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096638"
---
# <a name="temperature-and-tint-effect"></a>Temperatur- und Tönungseffekt

Die CLSID für diesen Effekt ist CLSID \_ D2D1TemperatureTint.

## <a name="sample-code"></a>Beispielcode

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Effect-Eigenschaften

Die Eigenschaften für den Temperatur- und Tönungseffekt werden durch die [**D2D1 \_ TEMPERATUREANDTINT \_ PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderungen | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 desktop \[ apps \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 desktop \[ apps \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |



 

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
