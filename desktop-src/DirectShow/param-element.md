---
description: Das param-Element gibt den Wert einer Eigenschaft für einen Übergang, einen Effekt oder ein anderes Unterobjekt an.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: param-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909038"
---
# <a name="param-element"></a>param-Element

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]

 

Das `param` -Element gibt den Wert einer Eigenschaft für einen Übergang, einen Effekt oder ein anderes Unterobjekt an.

## <a name="attributes"></a>Attributes

[**name**](name-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md) |
| Children | [**bei**](at-element.md), [ **linear**](linear-element.md)                                               |



 

## <a name="remarks"></a>Bemerkungen

Das **Value-Attribut** gibt den Wert der -Eigenschaft am Anfang des Übergangs oder Effekts an. Verwenden Sie das **at-** **oder lineare** -Element, um sich ändernde Werte anzugeben. Wenn das **param-Element** keine **at-** oder **linearen** Elemente enthält, bleibt der Wert über die Dauer des Effekts oder Übergangs konstant.

> [!Note]  
> Ein **param-Element** innerhalb eines **Clipelements** darf keine **at- oder** **linearen Elemente** enthalten.

 

Viele Übergänge unterstützen eine **Status-Standardeigenschaft,** die zwischen 0 und 1,0 liegt und angibt, welcher Prozentsatz des Übergangs in der Ausgabe widergespiegelt wird. Bei **Progress** = 0,0 befindet sich der Übergang am Anfang seiner Sequenz (vollständig das erste Videobild). Bei **Progress** = 0,5 ist der Übergang halb abgeschlossen. (Beispielsweise befindet sich bei einer Zurücksetzung bei **Progress** = 0,5 die Übergangsgrenze in der Mitte des Bilds.) Bei **Progress** = 1.0 ist der Übergang abgeschlossen (vollständig das zweite Bild). Standardmäßig wechseln Übergänge von **Progress** = 0.0 am Anfang des Übergangs zu **Progress** = 1.0 am Ende.

Andere Eigenschaften sind in der Regel spezifisch für einen bestimmten Übergang oder Effekt. Beispielsweise unterstützt der Zurücksetzenübergang eine **GradientSize-Eigenschaft,** die die Breite des Übergangsbereichs steuert.

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

 

 



