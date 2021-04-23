---
description: Das at-Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909828"
---
# <a name="at-element"></a>at-Element

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]

 

Das `at` -Element definiert den Wert eines [**param-Elements**](param-element.md) zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält. Das -Element bewirkt, dass der -Parameter zum angegebenen Zeitpunkt plötzlich zum `at` neuen Wert springt. Verwenden Sie das lineare Element, um einen reibungslosen Verlauf zu einem [**neuen Wert**](linear-element.md) zu erhalten.

## <a name="attributes"></a>Attributes

[**time,**](time-attribute.md) [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|--------------------------------|
| Parent   | [**Parameter**](param-element.md) |
| Children | Keine                           |



 

## <a name="examples"></a>Beispiele


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



