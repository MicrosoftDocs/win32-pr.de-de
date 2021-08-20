---
title: Sepia-Effekt
description: Konvertiert ein Bild in Sepiatöne.
ms.assetid: fe321be9-6ade-bd0c-1c66-cc8042e5a5e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c30b2fcd49b30306b055f60bb3e4262a22740d8efa168ade428698c7b23ce10d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118664982"
---
# <a name="sepia-effect"></a>Sepia-Effekt

Konvertiert ein Bild in Sepiatöne.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Sepia.

-   [Beispielbild](#example-image)
-   [Beispielcode](#sample-code)
-   [Effekteigenschaften](#effect-properties)
-   [Requirements](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für die Effektausgabe](images/sepia-effect.png)

## <a name="sample-code"></a>Beispielcode


```C++
ComPtr<ID2D1Effect> sepiaEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Sepia, &sepiaEffect);
 
sepiaEffect->SetInput(0, bitmap);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_INTENSITY, 0.75f);
sepiaEffect->SetValue(D2D1_SEPIA_PROP_ALPHA_MODE, D2D1_ALPHA_MODE_PREMULTIPLIED);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(sepiaEffect.Get());
m_d2dContext->EndDraw();


```



## <a name="effect-properties"></a>Effect-Eigenschaften

Die Eigenschaften für den Sepia-Effekt werden durch die [**D2D1 \_ SEPIA \_ PROP-Enumeration**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_sepia_prop) definiert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Unterstützte Mindestversion (Server) | \[Windows 10 Desktop-Apps \| Windows Store Apps\] |
| Header                   | d2d1effects \_ 2.h                                  |
| Bibliothek                  | d2d1.lib, dxguid.lib                              |


## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)




