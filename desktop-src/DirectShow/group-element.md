---
description: Das Group-Element definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.
ms.assetid: db2f1fdd-bcb1-4401-91f4-5e167e4da215
title: Group-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0b8146586d93a53093a68bb1abc08e85c52f14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103958068"
---
# <a name="group-element"></a>Group-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das **Group** -Element definiert eine Gruppe, das Objekt der obersten Ebene in einer Zeitachse.

## <a name="attributes"></a>Attribute

[**Bittiefe**](bitdepth-attribute.md), [**Pufferung**](buffering-attribute.md), [**Framerate**](framerate-attribute.md), [**height**](height-attribute.md), [**Lock**](lock-attribute.md), [**stumm**](mute-attribute.md), [**Name**](name-attribute.md), [**PreviewMode**](previewmode-attribute.md), [**Samplingrate**](samplingrate-attribute.md), [**Type**](type-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md), [**Width**](width-attribute.md)

## <a name="parentchild-information"></a>Über-/unterordnungsinformationen



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**Zeitplan**](timeline-element.md)                                                                     |
| Children | zusammen [**gesetzte**](composite-element.md), [**Effekte**](effect-element.md), nach [**Verfolgung**](track-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Innerhalb eines- `group` Elements wird die Priorität von geschachtelten Ebenen implizit durch die Reihenfolge bestimmt, in der Sie im-Element angezeigt werden. Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.

## <a name="examples"></a>Beispiele


```XML
<group type="video" width="640" height="480" framerate="30"> </group>
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



