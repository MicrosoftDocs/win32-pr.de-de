---
title: SLIDER.foregroundImage
description: Das foregroundImage-Attribut gibt das Vordergrundbild des Schiebereglers an oder ruft es ab.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- SLIDER.foregroundImage-Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2f7fad50a6e33ca4de5890dfca340e36aa2fdc0af0c0b938793eac4edc1dfb71
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119735710"
---
# <a name="sliderforegroundimage"></a>SLIDER.foregroundImage

Das **foregroundImage-Attribut** gibt das Vordergrundbild des Schiebereglers an oder ruft es ab.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Dieses Attribut ist optional. Wenn Sie Bilder zum Erstellen eines Schieberegler-Steuerelements verwenden, wird **backgroundImage** für das Hauptschiebereglerbild verwendet. ThumbImage **stellt** den eigentlichen Schieberegler dar und kann mit der Maus verschoben werden. Auf  dem ThumbImage-Schieberegler befindet sich eine unsichtbare Linie, in der das Hintergrundbild auf einer Seite der Linie und das Vordergrundbild auf der anderen Seite angezeigt wird.

Wenn der **ThumbImage-Schieberegler** mit  der Maus bewegt wird und die Folie auf TRUE festgelegt ist, wird das Vordergrundbild wie durch den Schieberegler gezogen, um das Hintergrundbild zu bedecken. Wenn **die** Folie auf FALSE festgelegt ist, wird das Vordergrundbild nicht bewegt, sondern an Ort und Stelle angezeigt, als würde der Schieberegler das Hintergrundbild vom Vordergrundbild verschieben.

Wenn das **gekachelte** Attribut auf TRUE festgelegt ist und das Vordergrundbild kleiner als der Vordergrundbereich des Schieberegler-Steuerelements ist, wird das Bild je nach Richtungsattribut horizontal oder vertikal angeordnet, um den verfügbaren Platz zu füllen. 

Die unterstützten Formate sind BMP, JPG, PNG und GIF (ohne animierte GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.slide**](slider-slide.md)
</dt> <dt>

[**SLIDER.thumbImage**](slider-thumbimage.md)
</dt> <dt>

[**SLIDER.value**](slider-value.md)
</dt> </dl>

 

 





