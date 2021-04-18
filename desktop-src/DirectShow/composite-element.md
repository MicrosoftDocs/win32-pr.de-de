---
description: Das zusammengesetzte Element definiert eine Komposition, ein Container Objekt für Spuren und andere zusammengesetzte kombinieren.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Composite-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106345580"
---
# <a name="composite-element"></a>Composite-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das `composite` -Element definiert eine Komposition, ein Container Objekt für Spuren und andere zusammengefügte Zeichen.

## <a name="attributes"></a>Attribute

[**Lock**](lock-attribute.md), [**stumm**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Über-/unterordnungsinformationen



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **Gruppe**](group-element.md)                                                                             |
| Children | `composite`, [**Auswirkung**](effect-element.md), nach [**Verfolgung**](track-element.md), [**Übergang**](transition-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Innerhalb eines- `composite` Elements wird die Priorität von geschachtelten Ebenen implizit durch die Reihenfolge bestimmt, in der Sie innerhalb des-Elements angezeigt werden. Die erste Ebene hat Priorität 0, und nachfolgende Ebenen haben höhere Prioritätswerte.

## <a name="examples"></a>Beispiele


```XML
<composite> </composite>
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



