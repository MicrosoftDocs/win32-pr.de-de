---
description: Das zusammengesetzte Element definiert eine Komposition, ein Containerobjekt für Spuren und andere geschachtelte Kompositionen.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: composite-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec9ce7c889829ee227ce31df25d5d17985e877ed107870170f6939aebf14fd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084310"
---
# <a name="composite-element"></a>composite-Element

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das `composite` -Element definiert eine Komposition, ein Containerobjekt für Spuren und andere geschachtelte Kompositionen.

## <a name="attributes"></a>Attribute

[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **Gruppe**](group-element.md)                                                                             |
| Children | `composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md) |



 

## <a name="remarks"></a>Hinweise

Innerhalb eines Elements wird die Priorität geschachtelter Ebenen implizit durch die Reihenfolge bestimmt, in der `composite` sie innerhalb des Elements angezeigt werden. Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.

## <a name="examples"></a>Beispiele


```XML
<composite> </composite>
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



