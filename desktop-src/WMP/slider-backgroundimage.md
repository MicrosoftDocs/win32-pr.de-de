---
title: SLIDER.backgroundImage
description: Das backgroundImage-Attribut gibt das Hintergrundbild des Schiebereglers an oder ruft es ab.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- SLIDER.backgroundImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b2c4f6d31e3f870541310b23544a15c7b9af0043014a9013310cea7dd4ee072
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118832997"
---
# <a name="sliderbackgroundimage"></a>SLIDER.backgroundImage

Das **backgroundImage-Attribut** gibt das Hintergrundbild des Schiebereglers an oder ruft es ab.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Dieses Attribut ist optional. Wenn Bilder zum Erstellen eines Schiebereglers verwendet werden, wird **backgroundImage** für das Hauptbild des Schiebereglers verwendet. **ThumbImage** stellt den tatsächlichen Schieberegler dar und kann mit der Maus verschoben werden. Am **ThumbImage-Schieberegler** befindet sich eine unsichtbare Linie, in der das Hintergrundbild auf einer Seite der Zeile und das Vordergrundbild auf der anderen Seite angezeigt wird.

Wenn  der ThumbImage-Schieberegler mit der Maus bewegt wird und **der Schieberegler** auf TRUE festgelegt ist, wird das Vordergrundbild so verschoben, als würde es vom Schieberegler zum Abdecken des Hintergrundbilds gezogen. Wenn **slide** auf FALSE festgelegt ist, wird das Vordergrundbild nicht verschoben, sondern an Ort und Stelle angezeigt, als würde der Schieberegler das Hintergrundbild vom Vordergrundbild verschieben.

Wenn das **gekachelte** Attribut auf TRUE festgelegt ist und das Hintergrundbild kleiner als das Schieberegler-Steuerelement ist, wird das Bild je nach **Richtungsattribut** entweder horizontal oder vertikal gekachelt. Wenn das **borderSize-Attribut** auf einen Wert größer als 0 (null) festgelegt ist, entspricht die angegebene Anzahl der Pixel links und rechts oder oben und unten im Bild (je nach Richtungsattribut), die für die Rahmen des Schieberegler-Steuerelements reserviert werden.  In diesem Fall wird nur der zentrale Teil des Bilds zum Kacheln des Rests des Steuerelements verwendet.

Die unterstützten Formate sind BMP, JPG, PNG und GIF (ohne animierte GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> <dt>

[**SLIDER.slide**](slider-slide.md)
</dt> <dt>

[**SLIDER.thumbImage**](slider-thumbimage.md)
</dt> </dl>

 

 





