---
title: EQUALIZERSETTINGS.gainLevel2
description: Das gainLevel2-Attribut gibt die Verstärkungsstufe von Band 2 an oder ruft sie ab.
ms.assetid: e602d9cc-42b3-402e-9df5-8b970d878904
keywords:
- EQUALIZERSETTINGS.gainLevel2 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel2
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe4979cb44fbd39b37acd29fe8e3303c879c45b40dfafc554180dad5301f0b0c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339830"
---
# <a name="equalizersettingsgainlevel2"></a>EQUALIZERSETTINGS.gainLevel2

Das **gainLevel2-Attribut** gibt die Verstärkungsstufe von Band 2 an oder ruft sie ab.

``` syntax
        elementID.gainLevel2
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/Schreibnummer (**float**), deren Wert normalerweise zwischen 20 und +20 liegt.  Der Standardwert ist 0 (null).

## <a name="remarks"></a>Hinweise

Dieses Attribut passt den Teil des Audiofrequenzspektrums an, der auf 62Hz zentriert ist.

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

 

 





