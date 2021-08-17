---
title: EQUALIZERSETTINGS.gainLevel10
description: Das gainLevel10-Attribut gibt die Verstärkungsstufe von Band 10 an oder ruft sie ab.
ms.assetid: 0d645719-86aa-4475-8e87-ea6c20e4fed7
keywords:
- EQUALIZERSETTINGS.gainLevel10 Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevel10
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e80e05686d06871aa40e8a649a119a41fb1a7a59bbb60a77b56497561ae9f27
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117748817"
---
# <a name="equalizersettingsgainlevel10"></a>EQUALIZERSETTINGS.gainLevel10

Das **gainLevel10-Attribut** gibt die Verstärkungsstufe von Band 10 an oder ruft sie ab.

``` syntax
        elementID.gainLevel10
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/Schreibnummer (**float**), deren Wert normalerweise zwischen 20 und +20 liegt.  Der Standardwert ist 0 (null).

## <a name="remarks"></a>Hinweise

Dieses Attribut passt den Teil des Audiofrequenzspektrums an, der auf 16kHz zentriert ist.

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

 

 





