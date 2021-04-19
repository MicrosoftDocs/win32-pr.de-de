---
title: ButtonElement. Down
description: Mit dem Attribut "Down" wird ein Wert angegeben oder abgerufen, der angibt, ob sich das Schaltflächen Element an der nach-oben-oder der
ms.assetid: 6b3633c5-84c1-48a0-bd2f-94660890d9a6
keywords:
- ButtonElement. Down-Windows-Media Player
topic_type:
- apiref
api_name:
- BUTTONELEMENT.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23f48b0e2ac0f4bf02f87d90bb0bd504478beb52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370163"
---
# <a name="buttonelementdown"></a>ButtonElement. Down

Mit dem Attribut " **down** " wird ein Wert angegeben oder abgerufen, der angibt, ob sich das Schaltflächen Element an der nach-oben-oder der

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                     |
|-------|-----------------------------------------------------------------|
| true  | Gibt an, dass sich das **ButtonElement** an der Position nach unten befindet.        |
| false | Standard. Gibt an, dass sich das **ButtonElement** in der aufwärts-Position befindet. |



 

## <a name="remarks"></a>Bemerkungen

Damit ein Button-Element an der nach-unten-Position verbleibt **, muss die** Kurznotiz auf true festgelegt werden. Standardmäßig ist die Kurznotiz false, und jeder **Versuch, auf true fest** **zulegen, wird** ignoriert.

Wenn ein ungültiger Wert angegeben wird, wird der vorherige Zustand beibehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonElement-Element**](buttonelement-element.md)
</dt> <dt>

[**ButtonElement. downtooltip**](buttonelement-downtooltip.md)
</dt> </dl>

 

 





