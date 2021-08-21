---
title: VIDEO.backgroundColor
description: Das backgroundColor-Attribut gibt die Hintergrundfarbe des Video-Steuerelements an oder ruft sie ab.
ms.assetid: 7acf7dc8-80c3-4620-ad89-4c8de20d17ee
keywords:
- VIDEO.backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- VIDEO.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41b5e4f637aa4d15aa9496eb85ee0b60a103ed4db33185e8434b8409173da298
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118830259"
---
# <a name="videobackgroundcolor"></a>VIDEO.backgroundColor

Das **backgroundColor-Attribut** gibt die Hintergrundfarbe des Video-Steuerelements an oder ruft sie ab.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die einen beliebigen Microsoft Internet Explorer Farbwert oder den Wert "none" enthält. Er hat den Standardwert "none", d.h., wenn dem Videosteuerelement kein Video zugeordnet ist, ist das Video-Steuerelement transparent, und der Hintergrund wird angezeigt.

## <a name="remarks"></a>Hinweise

Wenn das Video kleiner als das Fenster ist und **stretchToFit** false ist, wird die Hintergrundfarbe um das Video herum angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Farbreferenz**](color-reference.md)
</dt> <dt>

[**VIDEO-Element**](video-element.md)
</dt> <dt>

[**VIDEO.stretchToFit**](video-stretchtofit.md)
</dt> </dl>

 

 





