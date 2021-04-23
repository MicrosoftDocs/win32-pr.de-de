---
description: Der Clip gibt eine Medienquelle an.
ms.assetid: 40323e64-ad5f-4646-bad7-2a4e7d0ddcf6
title: clip-Element
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6d937f942ba7b564e65b0e37d9c11929805287da
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908668"
---
# <a name="clip-element"></a>clip-Element

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]

 

Gibt `clip` eine Medienquelle an.

## <a name="attributes"></a>Attributes

[**clsid**](clsid-attribute.md), [**framerate**](framerate-attribute.md), [**lock**](lock-attribute.md), [**mlength**](mlength-attribute.md), [**mstart**](mstart-attribute.md), [**mstop**](mstop-attribute.md), [**mute**](mute-attribute.md), [**src**](src-attribute.md), [**start**](start-attribute.md), [**stop**](stop-attribute.md), [**stream**](stream-attribute.md), [**stretchmode**](stretchmode-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informationen zu über- und untergeordneten Daten



| Bezeichnung | Wert |
|----------|----------------------------------|
| Parent   | [**track**](track-element.md)   |
| Children | [**Wirkung**](effect-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Das **clsid-Attribut** gibt die CLSID eines Quellfilters an, der als Quelle verwendet werden soll. Geben Sie die **Attribute src** und **clsid nicht** innerhalb desselben Elements `clip` an.

Geben Sie mindestens ein Startzeitattribut (**start** oder **mstart**) und ein Stoppzeitattribut (**stop** oder mstop ) **an.** Wenn eines der Startzeitattribute nicht angegeben ist, wird standardmäßig 0 (der Anfang der Zeitachse für **start** oder der Anfang des Clips für **mstart ) verwendet.** Wenn eines der Stoppzeitattribute nicht angegeben ist, geht DES von einer normalen Wiedergaberate aus und berechnet die nicht angegebene Stoppzeit entsprechend. Wenn beide Stoppzeiten angegeben sind, ist die Wiedergabe bei Bedarf schneller oder langsamer als normal.

Im folgenden Beispiel beträgt die Zeitachse sieben Sekunden (**Stop** minus **Start**). Es wird eine normale Wiedergaberate angenommen, sodass die Medienstoppzeit standardmäßig 10 Sekunden beträgt (Dauer plus **mstart).**


```
<clip start="2" stop="9" mstart="3" />
```



Im nächsten Beispiel wird die Medienstartzeit standardmäßig auf 0 festgelegt, sodass die Mediendauer 10 Sekunden beträgt. Die Dauer der Zeitachse beträgt fünf Sekunden, sodass der Clip doppelt so schnell wie gewohnt abspielt.


```
<clip start="5" stop="10" mstop="10" />  
```



Wenn das **src-Attribut** ein Stillbild angibt, versucht DES, eine Reihe von Still-Bildern zu laden, um eine Animation zu erstellen. Wenn das **src-Attribut** beispielsweise IMAGE001.BMP ist, sucht DES nach IMAGE002.BMP, IMAGE003.BMP, IMAGE004.BMP usw. Wenn sie vorhanden sind, werden sie in sequenzieller numerischer Reihenfolge mit der vom **Framerate-Attribut** angegebenen Rate angezeigt.

## <a name="examples"></a>Beispiele


```XML
<clip src="sample.avi" start="1:05" stop="1:42.5" mstart="30" />
```



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[XTL-Elemente](xtl-elements.md)
</dt> </dl>

 

 



