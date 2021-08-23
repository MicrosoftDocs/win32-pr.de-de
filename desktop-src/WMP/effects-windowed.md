---
title: EFFECTS.windowed
description: Das Windowed-Attribut gibt einen Wert an, der angibt, ob die Visualisierung fensterlos oder fensterlos ist, d. h., ob das gesamte Rechteck des Steuerelements jederzeit sichtbar ist oder ob es abgeschnitten werden kann.
ms.assetid: bc535274-8bc3-43bb-aab0-11899134d71e
keywords:
- EFFECTS.windowed Windows Media Player
topic_type:
- apiref
api_name:
- EFFECTS.windowed
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32fcd144d26de8f96c039d8199af8e6e4c1c14e60b2c5e2bf0c7dcc5a7f3cbf5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651000"
---
# <a name="effectswindowed"></a>EFFECTS.windowed

Das **Windowed-Attribut** gibt einen Wert an, der angibt, ob die Visualisierung fensterlos oder fensterlos ist, d. h., ob das gesamte Rechteck des Steuerelements jederzeit sichtbar ist oder ob es abgeschnitten werden kann. Dieses Attribut kann nur zur Entwurfszeit festgelegt werden.

``` syntax
        elementID.windowed
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher Wert,** der zur Entwurfszeit angegeben und danach schreibgeschützt ist.



| Wert | BESCHREIBUNG                              |
|-------|------------------------------------------|
| true  | Das Steuerelement wird eingeblendet.            |
| false | Standard. Das Steuerelement ist fensterlos. |



 

## <a name="remarks"></a>Hinweise

Wenn ein nicht rechteckiges Visualisierungsfenster gewünscht ist oder ein Teil des Fensters durch ein Bild abgedeckt wird, muss dieses Attribut auf FALSE festgelegt werden. Dadurch wird die Leistung für die erforderlichen Ausschneidefunktionen geerkt.

Wenn **windowed** auf TRUE festgelegt ist, wird jedes Bild, das das Visualisierungsfenster abdeckt, ignoriert, und das Visualisierungsfenster weist die höchste Z-Reihenfolge auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**EFFECTS-Element**](effects-element.md)
</dt> </dl>

 

 





