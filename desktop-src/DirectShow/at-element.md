---
description: Das at-Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8cb539331519fb23b6b8aa45b374457229f807a5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747264"
---
# <a name="at-element"></a>at-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `at` Element definiert den Wert eines [**param**](param-element.md) -Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält. Das- `at` Element bewirkt, dass der-Parameter zum angegebenen Zeitpunkt abrupt zum neuen Wert springt. Verwenden Sie das [**lineare**](linear-element.md) -Element, um einen reibungslosen Übergang zu einem neuen Wert zu erhalten.

## <a name="attributes"></a>Attribute

[**Uhrzeit**](time-attribute.md), [ **Wert**](value-attribute.md)

## <a name="parentchild-information"></a>Über-/unterordnungsinformationen



|          |                                |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Children | Keine                           |



 

## <a name="examples"></a>Beispiele


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



