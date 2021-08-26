---
description: Das param-Element gibt den Wert einer Eigenschaft für einen Übergang, effekt oder ein anderes Unterobjekt an.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: param-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35c58543c5daae7ad0a77f6380bc3f3db48cf8443461eaf919c4c727163436cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050820"
---
# <a name="param-element"></a>param-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Das `param` -Element gibt den Wert einer Eigenschaft für einen Übergang, einen Effekt oder ein anderes Unterobjekt an.

## <a name="attributes"></a>Attribute

[**name**](name-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**Clip**](clip-element.md), [**Effekt**](effect-element.md), [**Übergang**](transition-element.md) |
| Children | [**bei**](at-element.md) [ **linear**](linear-element.md)                                               |



 

## <a name="remarks"></a>Hinweise

Das **value-Attribut** gibt den Wert der -Eigenschaft am Anfang des Übergangs oder Effekts an. Verwenden Sie das **at-** oder **lineare** -Element, um sich ändernde Werte anzugeben. Wenn das **param-Element** keine **at-** oder **linearen** Elemente enthält, bleibt der Wert während der Dauer des Effekts oder Übergangs konstant.

> [!Note]  
> Ein **param-Element** innerhalb eines **Clipelements** darf keine **at-** oder **linearen** Elemente enthalten.

 

Viele Übergänge unterstützen eine Standardmäßige **Progress-Eigenschaft** zwischen 0 und 1,0, die angibt, welcher Prozentsatz des Übergangs in der Ausgabe widergespiegelt wird. Bei **Progress** = 0,0 befindet sich der Übergang am Anfang der Sequenz (vollständig das erste Videobild). Bei **Status** = 0,5 ist der Übergang halb abgeschlossen. (Bei einer Zurücksetzung befindet sich die Übergangsgrenze beispielsweise bei **Status** = 0,5 in der Mitte des Bilds.) Bei **Status** = 1,0 ist der Übergang abgeschlossen (vollständig das zweite Bild). Standardmäßig wechseln Übergänge von **Status** = 0,0 am Anfang des Übergangs zu **Status** = 1,0 am Ende.

Andere Eigenschaften sind in der Regel für einen bestimmten Übergang oder Effekt spezifisch. Beispielsweise unterstützt der Zurücksetzenübergang eine **GradientSize-Eigenschaft,** die die Breite des Übergangsbereichs steuert.

Um einen Übergang rückwärts auszuführen, legen Sie die **Progress-Eigenschaft** zu Beginn des Übergangs auf 1,0 fest, und verwenden Sie das **lineare** Element, um den Wert in 0,0 zu ändern, wie im folgenden Beispiel gezeigt:


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a>Beispiele


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



