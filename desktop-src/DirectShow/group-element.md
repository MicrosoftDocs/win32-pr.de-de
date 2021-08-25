---
description: Das Group-Element definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: group-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eda120363540eaf467ebb9beaea4705c4b430077c55b5b05c46197d90920b40a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119997830"
---
# <a name="group-element"></a>group-Element

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Das **Group-Element** definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.

## <a name="attributes"></a>Attribute

[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**Zeitachse**](timeline-element.md)                                                                     |
| Children | [**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md) |



 

## <a name="remarks"></a>Hinweise

Innerhalb eines Elements wird die Priorität geschachtelter Ebenen implizit durch die Reihenfolge `group` bestimmt, in der sie im Element angezeigt werden. Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.

## <a name="examples"></a>Beispiele


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



