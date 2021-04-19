---
title: Effekte. Windowed
description: Das Fenster-Attribut gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob die Visualisierung Fenster Weise angezeigt wird, d. h. ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist, oder ob es abgeschnitten werden kann.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- Effekte. Fenster Media Player
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3e30ae511c3e80e5e560f864baa8d797903fe2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367198"
---
# <a name="effectswindowed"></a>Effekte. Windowed

Das **Fenster** -Attribut gibt einen Wert an oder Ruft einen Wert ab, der angibt, ob die Visualisierung Fenster Weise angezeigt wird, d. h. ob das gesamte Rechteck des Steuer Elements jederzeit sichtbar ist, oder ob es abgeschnitten werden kann. Dieses Attribut kann nur zur Entwurfszeit festgelegt werden.

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert, der zur Entwurfszeit angegeben wird, und anschließend schreibgeschützt.



| Wert | BESCHREIBUNG                              |
|-------|------------------------------------------|
| true  | Das-Steuerelement wird angezeigt.            |
| false | Standard. Das Steuerelement ist fensterloser. |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein nicht rechteckiges Visualisierungs Fenster erwünscht ist oder ein Teil des Fensters durch ein Bild abgedeckt ist, muss dieses Attribut auf "false" festgelegt werden. Dadurch wird eine gewisse Leistung erzielt, um das erforderliche Clipping durchzuführen.

Wenn **Fenster** auf true festgelegt ist, wird jedes Bild, das das Visualisierungs Fenster abdeckt, ignoriert, und das Visualisierungs Fenster hat die oberste z-Reihenfolge.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Effects-Element**](effects-element.md)
</dt> </dl>

 

 





