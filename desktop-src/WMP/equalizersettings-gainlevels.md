---
title: Equalizersettings. gainlevels
description: Das Attribut "gainlevels" gibt die Gewinn Ebene des Bands an oder ruft es ab, das dem angegebenen Index entspricht.
ms.assetid: fb70e2ef-4cee-457e-a06b-7a1ae6930986
keywords:
- Equalizersettings. gainlevels-Fenster Media Player
topic_type:
- apiref
api_name:
- EQUALIZERSETTINGS.gainLevels
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d083ac829582f2abc45837cf441b2f0a565ee03a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358304"
---
# <a name="equalizersettingsgainlevels"></a>Equalizersettings. gainlevels

Das Attribut " **gainlevels** " gibt die Gewinn Ebene des Bands an oder ruft es ab, das dem angegebenen Index entspricht.

``` syntax
        elementID.gainLevels(theBand)
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibnummer (**float**) mit einem Wert, der normalerweise zwischen 20 und + 20 liegt. 

## <a name="parameters"></a>Parameter

<dl> <dt>

<span id="theBand"></span><span id="theband"></span><span id="THEBAND"></span>*das-Band*
</dt> <dd>

**Zahl**(**Long**) zwischen 1 und 10, die den Index des Bands angibt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Dieses Attribut nimmt einen Parameter an, aber sein Wert wird in Skriptcode auf dieselbe Weise wie andere Attributwerte angegeben. Sie kann nicht im Element "equalizersettings" angegeben werden und kann nicht mit dem **wmpprop** -Attribut "lauschen" verwendet werden. Stattdessen werden die nummerierten Attribute der Gewinn Ebene für diese Situationen bereitgestellt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Equalizersettings-Element**](equalizersettings-element.md)
</dt> <dt>

[**Lauschen von Attributen**](listening-attributes.md)
</dt> </dl>

 

 





