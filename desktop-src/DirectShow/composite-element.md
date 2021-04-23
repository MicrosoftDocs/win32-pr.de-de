---
description: Das zusammengesetzte Element definiert eine Komposition, ein Containerobjekt für Spuren und andere geschachtelte Kompositionen.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: composite-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908838"
---
# <a name="composite-element"></a>composite-Element

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]

 

Das `composite` -Element definiert eine Komposition, ein Containerobjekt für Spuren und andere geschachtelte Kompositionen.

## <a name="attributes"></a>Attributes

[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **Gruppe**](group-element.md)                                                                             |
| Children | `composite`, [**effect**](effect-element.md), [**track**](track-element.md), [**transition**](transition-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Innerhalb eines Elements wird die Priorität geschachtelter Ebenen implizit durch die Reihenfolge bestimmt, in der `composite` sie innerhalb des Elements angezeigt werden. Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.

## <a name="examples"></a>Beispiele


```XML
<composite> </composite>
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



