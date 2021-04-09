---
title: Vigffekt
description: Blendet das Eingabebild an den Rändern in eine Benutzer Satz Farbe aus.
ms.assetid: 34da221f-44a2-1d01-d88d-d7846b9770b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3fe9302a86a49b060aa05ecb856ce43122d946d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104936"
---
# <a name="vignette-effect"></a>Vigffekt

Blendet das Eingabebild an den Rändern in eine Benutzer Satz Farbe aus.

Die CLSID für diesen Effekt ist CLSID \_ D2D1Vignette.

-   [Beispielbild](#example-image)
-   [Beispielcode](#sample-code)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für Effekte Ausgabe](images/vignette-effect.png)

## <a name="sample-code"></a>Beispielcode

```cpp
ComPtr<ID2D1Effect> vignetteEffect;
m_d2dContext->CreateEffect(CLSID_D2D1Vignette, &vignetteEffect);
 
vignetteEffect->SetInput(0, bitmap);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_COLOR, );
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_TRANSITION_SIZE, 0.1f);
vignetteEffect->SetValue(D2D1_VIGNETTE_PROP_STRENGTH, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(vignetteEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a>Effekt Eigenschaften

Die Eigenschaften für den vigaseeffekt werden durch die [**D2D1- \_ Vignette- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_vignette_prop) -Enumeration definiert.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
