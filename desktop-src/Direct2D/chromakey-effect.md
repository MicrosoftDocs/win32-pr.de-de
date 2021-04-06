---
title: Chroma-Schlüssel Effekt
description: Konvertiert eine angegebene Farbe plus oder minus eine Toleranz in alpha. Beispielsweise kann Chroma-Key den Hintergrund eines Bilds für einen Überlagerungs Effekt mit grünes Bildschirm entfernen.
ms.assetid: f7bb5c65-f406-f947-c05d-2756cff99d21
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a13d5558d103d6f937ed6638d0debbeddaf71dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858812"
---
# <a name="chroma-key-effect"></a>Chroma-Schlüssel Effekt

Konvertiert eine angegebene Farbe plus oder minus eine Toleranz in alpha. Beispielsweise kann Chroma-Key den Hintergrund eines Bilds für einen Überlagerungs Effekt mit grünes Bildschirm entfernen.

Die CLSID für diesen Effekt ist CLSID \_ D2D1ChromaKey.

-   [Beispielbild](#example-image)
-   [Beispielcode](#sample-code)
-   [Effekt Eigenschaften](#effect-properties)
-   [Anforderungen](#requirements)
-   [Zugehörige Themen](#related-topics)

## <a name="example-image"></a>Beispielbild

![Beispiel für Effekte Ausgabe](images/chromakey-effect.png)

> [!Note]  
> In diesem Beispiel ist die Ausgabe des Chroma-Key-Effekts das zweite Bild mit dem transparenten Hintergrund des checkboards. Das dritte Bild kombiniert dies mit einem Hintergrundbild für den abschließenden grünen Bildschirm.

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

## <a name="effect-properties"></a>Effekt Eigenschaften

Die Eigenschaften des Chroma-Key-Effekts werden von der [**D2D1 \_ Chromakey- \_ Prop**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_chromakey_prop) -Enumeration definiert.

## <a name="requirements"></a>Anforderungen

| Anforderung | Wert |
|--------------------------|---------------------------------------------------|
| Unterstützte Mindestversion (Client) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Unterstützte Mindestversion (Server) | Windows 10 \[ Desktop Apps- \| Windows Store-Apps\] |
| Header                   | d2d1effects \_ 2. h                                  |
| Bibliothek                  | d2d1. lib, dxguid. lib                              |

## <a name="related-topics"></a>Zugehörige Themen

* [ID2D1Effect-Schnittstelle](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
