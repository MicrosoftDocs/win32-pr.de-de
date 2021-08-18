---
title: TEXT.scrollingAmount
description: Das scrollingAmount-Attribut gibt die Anzahl der Pixel an, die der Text während jeder Bildlaufbewegung verschiebt, oder ruft sie ab.
ms.assetid: 46f74531-69dd-4505-8937-5b48b6e9be7b
keywords:
- TEXT.scrollingAmount Windows Media Player
topic_type:
- apiref
api_name:
- TEXT.scrollingAmount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a8d5b703c02c2d3049f98a934980f1dbf8b1c5beceaca4d97158ea68c13db9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119466960"
---
# <a name="textscrollingamount"></a>TEXT.scrollingAmount

Das **scrollingAmount-Attribut** gibt die Anzahl der Pixel an, die der Text während jeder Bildlaufbewegung verschiebt, oder ruft sie ab.

``` syntax
        elementID.scrollingAmount
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  positive Lese-/Schreibnummer **(int)** mit dem Standardwert 6.

## <a name="remarks"></a>Hinweise

Für einen reibungslosen Bildlauf sollte **scrollingAmount** klein sein. Für schnelles Zeichnen mit großen Lücken sollte **scrollingAmount** größer sein. Beim **Scrollen** von ="false" wird **scrollingAmount** ignoriert.

Ein Beispiel, das veranschaulicht, wie die Attribute des **TEXT-Elements** verwendet werden, finden Sie im [Value-Attribut.](text-value.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**TEXT-Element**](text-element.md)
</dt> <dt>

[**TEXT.scrolling**](text-scrolling.md)
</dt> </dl>

 

 





