---
title: EQUALIZERSETTINGS.gainLevel7
description: Das gainLevel7-Attribut gibt die Verstärkungsstufe von Band 7 an oder ruft sie ab.
ms.assetid: f39e1475-b0c8-4204-b2d8-943bc8b4f830
keywords:
- EQUALIZERSETTINGS.gainLevel7 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel7
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cbb18676e97bc7b850dca9683f13d8e6983a138a3b674f03392645d81ab3d8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935127"
---
# <a name="equalizersettingsgainlevel7"></a>EQUALIZERSETTINGS.gainLevel7

Das **gainLevel7-Attribut** gibt die Verstärkungsstufe von Band 7 an oder ruft sie ab.

``` syntax
        elementID.gainLevel7
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/Schreibnummer (**float**), deren Wert normalerweise zwischen 20 und +20 liegt.  Der Standardwert ist 0 (null).

## <a name="remarks"></a>Hinweise

Dieses Attribut passt den Teil des Audiofrequenzspektrums an, der auf 2kHz zentriert ist.

Wenn dieses Attribut nicht angegeben wird, wird der vorherige Wert beibehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**EQUALIZERSETTINGS-Element**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





