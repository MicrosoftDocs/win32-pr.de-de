---
description: Das param-Element gibt den Wert einer Eigenschaft eines Übergangs, eines Effekts oder eines anderen unter Objekts an.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: param-Element (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb1d007a7f3e2dcffaa7b9163c76be604fed7a9a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860387"
---
# <a name="param-element"></a>param-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Das- `param` Element gibt den Wert einer Eigenschaft eines Übergangs, eines Effekts oder eines anderen unter Objekts an.

## <a name="attributes"></a>Attribute

[**Name**](name-attribute.md), [ **Wert**](value-attribute.md)

## <a name="parentchild-information"></a>Über-/unterordnungsinformationen



|          |                                                                                                          |
|----------|----------------------------------------------------------------------------------------------------------|
| Parent   | [**Clip**](clip-element.md), [**Effekt**](effect-element.md), [**Übergang**](transition-element.md) |
| Children | [**bei**](at-element.md), [ **linear**](linear-element.md)                                               |



 

## <a name="remarks"></a>Bemerkungen

Das **value** -Attribut gibt den Wert der-Eigenschaft am Anfang des Übergangs oder Effekts an. Verwenden Sie das **at** -oder **lineare** -Element, um veränderliche Werte anzugeben. Wenn das **param** -Element keine oder **lineare** Elemente enthält, bleibt der Wert während der Dauer des **Effekts oder Übergangs** konstant.

> [!Note]  
> Ein **param** -Element innerhalb eines **Clip** -Elements darf **keine oder** **lineare** Elemente enthalten.

 

Viele Übergänge unterstützen eine **Standardstatus** Eigenschaft, die zwischen 0 und 1,0 liegt und angibt, welcher Prozentsatz des Übergangs in der Ausgabe reflektiert wird. Bei **Progress** = 0,0 erfolgt der Übergang am Anfang seiner Sequenz (vollständig das erste Video Bild). Bei **Progress** = 0,5 ist der Übergang halb abgeschlossen. (Beispielsweise wird bei einer Löschung, bei **Progress** = 0,5, die Übergangsgrenze in der Mitte des Bilds angezeigt.) Bei **Progress** = 1,0 ist der Übergang abgeschlossen (vollständig das zweite Bild). Standardmäßig gehen Übergänge von **Progress** = 0,0 zu Beginn des Übergangs in **Progress** = 1,0 am Ende über.

Andere Eigenschaften sind normalerweise spezifisch für einen bestimmten Übergang oder einen bestimmten Effekt. Beispielsweise unterstützt der Übergangs Übergang eine **gradientsize** -Eigenschaft, die die Breite des Übergangsbereichs steuert.

Legen Sie zum Ausführen eines Übergangs rückwärts die Status **-Eigenschaft am** Anfang des Übergangs auf 1,0 fest, und verwenden Sie das **lineare** -Element, um den Wert in 0,0 zu ändern, wie im folgenden Beispiel gezeigt:


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

 

 



