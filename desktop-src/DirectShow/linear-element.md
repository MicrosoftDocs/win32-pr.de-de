---
description: Das lineare Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der das param-Element enthält.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: lineares Element (Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4e722dcbc68d24d76f34c80bdd17a91ad44423aa
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910088"
---
# <a name="linear-element"></a>lineares Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das lineare Element definiert den Wert eines [**Param-Elements**](param-element.md) zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der das **param-Element** enthält. Das `linear` -Element bewirkt, dass der -Parameter einen reibungslosen Übergang von seinem vorherigen Wert zum neuen Wert bewirkt. Verwenden Sie das at-Element, um [](at-element.md) sofort zu einem neuen Wert zu springen.

## <a name="attributes"></a>Attributes

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|--------------------------------|
| Parent   | [**Parameter**](param-element.md) |
| Children | Keine                           |



 

## <a name="examples"></a>Beispiele


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Camerauicontrol.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 




