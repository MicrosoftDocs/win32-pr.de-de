---
description: Der Clip gibt eine Medienquelle an.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: Clip-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe975113f370b13e50ba695d6fb3388a43c3a74
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104480995"
---
# <a name="clip-element"></a>Clip-Element

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Der ermittelt `clip` eine Medienquelle.

## <a name="attributes"></a>Attribute

[**CLSID**](clsid-attribute.md), [**Framerate**](framerate-attribute.md), [**Lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstopps**](mstop-attribute.md), [**stumm**](mute-attribute.md), [**src**](src-attribute.md), [**Start**](start-attribute.md), [](stop-attribute.md)Start, [**Stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Über-/unterordnungsinformationen



|          |                                  |
|----------|----------------------------------|
| Parent   | [**track**](track-element.md)   |
| Children | [**entsprechende**](effect-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Das **CLSID** -Attribut gibt die CLSID eines Quell Filters an, der als Quelle verwendet werden soll. Geben Sie die Attribute **src** und **CLSID** nicht innerhalb desselben `clip` Elements an.

Geben Sie mindestens ein Start Zeit Attribut ("**Start** " oder " **mstart**") und ein Attribut für die Beendigung an ("**Ende** " oder " **mstoppzeit**"). Wenn eines der Start Zeit Attribute nicht angegeben ist, wird es standardmäßig auf 0 (den Anfang der Zeitachse für **Start** oder den Anfang des Clips für **mstart**) festgelegt. Wenn eines der Attribute für die Endzeit nicht angegeben ist, nimmt des eine normale Wiedergabe Rate an und berechnet die nicht angegebene Endzeit entsprechend. Wenn beide Endzeiten angegeben sind, ist die Wiedergabe bei Bedarf schneller oder langsamer als normal.

Im folgenden Beispiel beträgt die Zeitachsen Dauer sieben Sekunden (**Ende** minus **Start**). Es wird davon ausgegangen, dass die Standard Wiedergabe Rate standardmäßig 10 Sekunden beträgt (die Dauer Plus **mstart**).


```
<clip start="2" stop="9" mstart="3" />
```



Im nächsten Beispiel wird die Start Zeit der Medien standardmäßig auf 0 (null) eingestellt und die Dauer des Mediums auf 10 Sekunden erzwungen. Die Zeitachsen Dauer beträgt fünf Sekunden, sodass der Clip mit der doppelten Geschwindigkeit wiedergegeben wird.


```
<clip start="5" stop="10" mstop="10" />  
```



Wenn das **src** -Attribut ein immer noch Bild angibt, versucht des, eine Reihe von Bildern zu laden, um eine Animation zu erstellen. Wenn das **src** -Attribut z. b. IMAGE001.BMP ist, sucht des nach IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP usw. Wenn Sie vorhanden sind, werden Sie in sequenzieller numerischer Reihenfolge mit dem vom **Framerate** -Attribut angegebenen Satz angezeigt.

## <a name="examples"></a>Beispiele


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



