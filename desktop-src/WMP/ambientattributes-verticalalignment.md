---
title: AmbientAttributes.verticalAlignment
description: Das verticalAlignment-Attribut gibt einen Wert an, der die vertikale Platzierung des Steuerelements angibt, wenn view oder die übergeordnete UNTERANSICHT gestreckt wird, oder ruft einen Wert ab.
ms.assetid: 08ef483a-58ee-4a35-9973-2567076d07f7
keywords:
- AmbientAttributes.verticalAlignment Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.verticalAlignment
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a116a8883fe1d591f5c68050e4a5ab738a3cf913322ae7c671c71a507f2c924d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956390"
---
# <a name="ambientattributesverticalalignment"></a>AmbientAttributes.verticalAlignment

Das **verticalAlignment-Attribut** gibt einen Wert an, der die vertikale Platzierung des Steuerelements angibt, wenn **view** oder die übergeordnete **UNTERANSICHT** gestreckt wird, oder ruft einen Wert ab.

``` syntax
        elementID.verticalAlignment
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**



| Wert   | Beschreibung                                                                                                                                                                                                                                                                                                                                     |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| top     | Standard. Behält die Platzierung des Steuerelements relativ zum oberen Teil der **ANSICHT** oder übergeordneten **UNTERANSICHT** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                             |
| bottom  | Behält die Platzierung des Steuerelements relativ zum unteren Rand der **VIEW-** oder übergeordneten **UNTERANSICHT** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                                   |
| Zentrum  | Behält die Platzierung des Steuerelements relativ zur vertikalen Mitte der **VIEW-** oder übergeordneten **UNTERANSICHT** bei, wenn die Größe der Ansicht geändert wird.                                                                                                                                                                                                          |
| strecken | Behält die Platzierung des Steuerelements relativ zum oberen und unteren Rand der Ansicht bei, wenn die Größe geändert wird. Das Steuerelement wird gestreckt, damit es passt, **wenn die VIEW-** oder **übergeordnete UNTERANSICHT** gestreckt wird. Das tatsächliche Bild wird nur dann größer oder verkleinert, wenn es in der Größe geändert werden kann, aber der klickbare Bereich wächst oder verkleinert sich, wenn er nicht durch ein **clippingImage-Objekt gebunden ist.** |



 

## <a name="remarks"></a>Hinweise

Sofern **verticalAlignment** nicht auf "center" festgelegt ist, behält das Steuerelement seinen ursprünglichen Abstand vom angegebenen Rand oder von beiden Kanten bei, wenn "stretch" angegeben ist und die Größe des Steuerelements geändert werden kann. Wenn die Größe des Steuerelements nicht geändert werden kann und "stretch" angegeben ist, wird stattdessen der klickbare Bereich gestreckt.

Sie können eine beliebige Kombination der **Attribute horizontalAlignment** und **verticalAlignment** festlegen. Wenn Sie beispielsweise möchten, dass ein Steuerelement sowohl horizontal als auch vertikal zentriert wird, legen Sie **horizontalAlignment** auf "center" und **verticalAlignment** auf "center" fest.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> <dt>

[**AmbientAttributes.horizontalAlignment**](ambientattributes-horizontalalignment.md)
</dt> </dl>

 

 





