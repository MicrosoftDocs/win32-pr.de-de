---
title: BUTTONELEMENT.down
description: Das attribut down gibt einen Wert an oder ruft einen Wert ab, der angibt, ob sich das Schaltflächenelement an der position nach oben oder unten befindet.
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- BUTTONELEMENT.down-Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff20aebda01b24dc14eb7d5298ee0d663d903bedcb7ef6ef8b05b6211af8b567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764470"
---
# <a name="buttonelementdown"></a>BUTTONELEMENT.down

Das **attribut down** gibt einen Wert an oder ruft einen Wert ab, der angibt, ob sich das Schaltflächenelement an der position nach oben oder unten befindet.

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein boolescher Wert mit **Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG                                                     |
|-------|-----------------------------------------------------------------|
| true  | Gibt **an, dass sich BUTTONELEMENT** an der nach unten zeigenden Position befindet.        |
| false | Standard. Gibt **an, dass sich BUTTONELEMENT** an der position up befindet. |



 

## <a name="remarks"></a>Hinweise

Damit ein Schaltflächenelement in der nach unten angezeigten Position verbleibt, muss **sticky** auf TRUE festgelegt werden. **"sticky" ist** standardmäßig "false",  und jeder Versuch, auf "true" festgelegt zu werden, wird ignoriert.

Wenn ein ungültiger Wert angegeben wird, wird der vorherige Zustand beibehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTONELEMENT-Element**](buttonelement-element.md)
</dt> <dt>

[**BUTTONELEMENT.downToolTip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





