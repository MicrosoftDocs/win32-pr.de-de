---
title: LIDER.value
description: Das Value-Attribut gibt die aktuelle Position des Schiebereglers an oder ruft sie ab. | LIDER.value
ms.assetid: 29e17f48-1848-458d-9da4-316013b21980
keywords:
- LIDER.value-Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3a256274fe2170ad50c164f7bf6768f82e3266db7a4ea5e2c6c8e28edd083c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118579708"
---
# <a name="customslidervalue"></a>LIDER.value

Das **Value-Attribut** gibt die aktuelle Position des Schiebereglers an oder ruft sie ab.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/Schreibnummer (**float**) mit einem Standardwert, der dem **min-Attribut** entspricht. 

## <a name="remarks"></a>Hinweise

Der **Wert** muss größer oder gleich **min** und kleiner oder gleich **max sein.** Wenn der Wert außerhalb des Bereichs liegt, wird eine Warnung ausgegeben, und der Wert ändert sich nicht.

## <a name="examples"></a>Beispiele

Im Attribut [positionImage finden](customslider-positionimage.md) Sie ein Beispiel, das veranschaulicht, wie die Attribute des **ELEMENTS VERDRLIDER** verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LIDER-Element**](customslider-element.md)
</dt> </dl>

 

 





