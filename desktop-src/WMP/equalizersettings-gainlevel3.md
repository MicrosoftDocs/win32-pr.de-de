---
title: EQUALIZERSETTINGS.gainLevel3
description: Das gainLevel3-Attribut gibt die Verstärkungsebene von Band 3 an oder ruft sie ab.
ms.assetid: 508d00c6-2429-4f35-b7ab-bf30f774e614
keywords:
- EQUALIZERSETTINGS.gainLevel3 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel3
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b8e719cd59a253ded35ad10e067f537d6f7d3a68d0d0b05a4cf79d0cd976f5e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123650"
---
# <a name="equalizersettingsgainlevel3"></a>EQUALIZERSETTINGS.gainLevel3

Das **gainLevel3-Attribut** gibt die Verstärkungsebene von Band 3 an oder ruft sie ab.

``` syntax
        elementID.gainLevel3
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Lese-/Schreibnummer **(float)** mit einem Wert, der normalerweise zwischen 20 und +20 liegt. Der Standardwert ist 0 (null).

## <a name="remarks"></a>Hinweise

Dieses Attribut passt den Teil des Audiofrequenzspektrums an, der auf 125Hz zentriert ist.

Wenn dieses Attribut nicht angegeben ist, wird der vorherige Wert beibehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EQUALIZERSETTINGS-Element**](equalizersettings-element.md)
</dt> <dt>

[**EQUALIZERSETTINGS. gainLevels**](equalizersettings-gainlevels.md)
</dt> </dl>

 

 





