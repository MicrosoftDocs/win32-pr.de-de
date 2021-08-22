---
title: EQUALIZERSETTINGS.gainLevels
description: Das gainLevels-Attribut gibt die Verstärkungsebene des Bandes an, die dem angegebenen Index entspricht, oder ruft sie ab.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- EQUALIZERSETTINGS.gainLevels Windows Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb3c00725ebbe75d607636e8b143146dfce9112b4d1a9dacd430a3d61b3cce5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118838270"
---
# <a name="equalizersettingsgainlevels"></a>EQUALIZERSETTINGS.gainLevels

Das **gainLevels-Attribut** gibt die Verstärkungsebene des Bandes an, die dem angegebenen Index entspricht, oder ruft sie ab.

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/Schreibnummer (**float**), deren Wert normalerweise zwischen 20 und +20 liegt. 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*theBand*
</dt> <dd>

**Zahl**(**long**) zwischen 1 und 10, die den Index des Bandes angibt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Dieses Attribut akzeptiert einen Parameter, aber sein Wert wird im Skriptcode auf die gleiche Weise wie andere Attributwerte angegeben. Sie kann weder im EQUALIZERSETTINGS-Element angegeben noch mit dem **wmpprop-Lauschenattribut** verwendet werden. Stattdessen werden die nummerierten Gainlevelattribute für diese Situationen bereitgestellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EQUALIZERSETTINGS-Element**](equalizersettings-element.md)
</dt> <dt>

[**Lauschende Attribute**](listening-attributes.md)
</dt> </dl>

 

 





