---
title: EQUALIZERSETTINGS.gainLevel4
description: Das gainLevel4-Attribut gibt die Verstärkungsstufe von Band 4 an oder ruft sie ab.
ms.assetid: 01383171-f991-4d09-858a-ce21ce93e14e
keywords:
- EQUALIZERSETTINGS.gainLevel4 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel4
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f7b1479d1be95895f124c5150d17a281fec5fc95fcbbedd65ca2ce9887678fae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118578167"
---
# <a name="equalizersettingsgainlevel4"></a>EQUALIZERSETTINGS.gainLevel4

Das **gainLevel4-Attribut** gibt die Verstärkungsstufe von Band 4 an oder ruft sie ab.

``` syntax
        elementID.gainLevel4
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/Schreibnummer (**float**), deren Wert normalerweise zwischen 20 und +20 liegt.  Sie hat den Standardwert 0 (null).

## <a name="remarks"></a>Hinweise

Dieses Attribut passt den Teil des Audiofrequenzspektrums an, der auf 250Hz zentriert ist.

Wenn dieses Attribut nicht angegeben wird, wird der vorherige Wert beibehalten.

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

 

 





