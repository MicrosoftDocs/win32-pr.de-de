---
description: Das lineare Element definiert den Wert eines Param-Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der das param-Element enthält.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Linear-Element (camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27080d08a1bbec98d5fa34b2739c63958e5d170a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370521"
---
# <a name="linear-element"></a>lineares Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das lineare Element definiert den Wert eines [**param**](param-element.md) -Elements zu einem bestimmten Zeitpunkt relativ zum Anfang des Übergangs oder Effekts, der das **param** -Element enthält. Das- `linear` Element bewirkt, dass der-Parameter einen reibungslosen Übergang vom vorherigen Wert zum neuen Wert vornimmt. Verwenden Sie das [**at**](at-element.md) -Element, um sofort zu einem neuen Wert zu springen.

## <a name="attributes"></a>Attribute

[**Uhrzeit**](time-attribute.md), [ **Wert**](value-attribute.md)

## <a name="parentchild-information"></a>Über-/unterordnungsinformationen



|          |                                |
|----------|--------------------------------|
| Parent   | [**param**](param-element.md) |
| Children | Keine                           |



 

## <a name="examples"></a>Beispiele


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|----------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 




