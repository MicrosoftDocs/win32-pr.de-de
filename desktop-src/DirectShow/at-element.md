---
description: Das at-Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: at-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d67a5e3c3ca2bd47381084ad0e0090d7aa208db87f35e5efe3a7d805a73d097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824390"
---
# <a name="at-element"></a>at-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das `at` -Element definiert den Wert eines [**Param-Elements**](param-element.md) zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der den Parameter enthält. Das `at` -Element bewirkt, dass der Parameter zum angegebenen Zeitpunkt plötzlich zum neuen Wert springt. Verwenden Sie das lineare Element, um einen [**reibungslosen**](linear-element.md) Übergang zu einem neuen Wert zu haben.

## <a name="attributes"></a>Attribute

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
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

 

 



