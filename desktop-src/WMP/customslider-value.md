---
title: Customslider. Value
description: Das value-Attribut gibt die aktuelle Position des Schiebereglers an oder ruft diese ab. | Customslider. Value
ms.assetid: 29e17f48-1848-458d-9da4-316013b21980
keywords:
- Customslider. Value-Fenster Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 89be4edd43fc79c8a8938a3861c982068760bcf3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367761"
---
# <a name="customslidervalue"></a>Customslider. Value

Das **value** -Attribut gibt die aktuelle Position des Schiebereglers an oder ruft diese ab.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibnummer (**float**) mit einem Standardwert, **der dem** Minimum-Attribut entspricht. 

## <a name="remarks"></a>Bemerkungen

Der **Wert** muss größer als oder gleich **Min** und kleiner als oder gleich dem **maximalen** Wert sein. Wenn der Wert außerhalb des Bereichs liegt, wird eine Warnung ausgegeben, und der Wert ändert sich nicht.

## <a name="examples"></a>Beispiele

Unter dem [positionImage](customslider-positionimage.md) -Attribut finden Sie ein Beispiel, das veranschaulicht, wie die Attribute des **customslider** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Customslider-Element**](customslider-element.md)
</dt> </dl>

 

 





