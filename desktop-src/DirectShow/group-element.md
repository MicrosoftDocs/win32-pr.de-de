---
description: Das Group-Element definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: group-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31502cef89c8383e935f409d76b9e31ca53a2da1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909248"
---
# <a name="group-element"></a>group-Element

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]

 

Das **Group-Element** definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.

## <a name="attributes"></a>Attributes

[**bitdepth**](bitdepth-attribute.md), [**buffering**](buffering-attribute.md), [**framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**name**](name-attribute.md), [**previewmode**](previewmode-attribute.md), [**samplingrate**](samplingrate-attribute.md), [**type**](type-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md), [**width**](width-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**Zeitachse**](timeline-element.md)                                                                     |
| Children | [**composite**](composite-element.md), [**effect**](effect-element.md), [**track**](track-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Innerhalb eines Elements wird die Priorität geschachtelter Ebenen implizit durch die Reihenfolge `group` bestimmt, in der sie im Element angezeigt werden. Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.

## <a name="examples"></a>Beispiele


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



