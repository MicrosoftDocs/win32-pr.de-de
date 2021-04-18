---
title: Schaltfläche. nach unten
description: Mit dem Attribut "Down" wird ein Wert angegeben oder abgerufen, der angibt, ob sich die Schaltfläche an der nach-oben-oder der
ms.assetid: 75398e8c-b13e-4836-b487-ed880da753ea
keywords:
- Button. Windows-Media Player nach unten
topic_type:
- apiref
api_name:
- BUTTON.down
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a0e2c7f97f782b51c145f3974f1490d0286fbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372096"
---
# <a name="buttondown"></a>Schaltfläche. nach unten

Mit dem Attribut " **down** " wird ein Wert angegeben oder abgerufen, der angibt, ob sich die **Schaltfläche** an der nach-oben-oder der

``` syntax
        elementID.down
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                   |
|-------|---------------------------------------------------------------|
| true  | Gibt an, dass sich die **Schaltfläche** an der Position nach unten befindet.        |
| false | Standard. Gibt an, dass sich die **Schaltfläche** in der up-Position befindet. |



 

## <a name="remarks"></a>Bemerkungen

Damit eine **Schaltfläche** an der nach-unten-Position verbleibt **, muss die** Kurznotiz auf true festgelegt werden. Standardmäßig ist die Kurznotiz false, und jeder **Versuch, auf true fest** **zulegen, wird** ignoriert.

Wenn ein ungültiger Wert angegeben wird, wird der vorherige Zustand beibehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> <dt>

[**Button. downImage**](button-downimage.md)
</dt> <dt>

[**Button. downtooltip**](button-downtooltip.md)
</dt> </dl>

 

 





