---
title: Text. scrollingdelay
description: Das scrollingdelay-Attribut gibt die Zeitverzögerung zwischen Scrollbewegungen an oder ruft diese ab.
ms.assetid: b965fe8f-c809-431f-b8fe-f7c3060068ac
keywords:
- Text. scrollingdelay-Fenster Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingDelay
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e81259ca84c62327bea67ae70d3f9ec3363450fb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365459"
---
# <a name="textscrollingdelay"></a>Text. scrollingdelay

Das **scrollingdelay** -Attribut gibt die Zeitverzögerung zwischen Scrollbewegungen an oder ruft diese ab.

``` syntax
        elementID.scrollingDelay
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibzahl (**int**), die die Verzögerung in Millisekunden angibt.  Er verfügt über einen Mindestwert von 30 und einen Standardwert von 85. Wenn ein Wert kleiner als der minimale Wert angegeben ist, wird der Standardwert verwendet.

## <a name="remarks"></a>Bemerkungen

Wenn **Scroll** auf false festgelegt ist, wird **scrollingdelay** ignoriert.

Im [value](text-value.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **Text** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Text-Element**](text-element.md)
</dt> <dt>

[**Text. Scroll**](text-scrolling.md)
</dt> </dl>

 

 





