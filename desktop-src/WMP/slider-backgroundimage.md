---
title: Slider. BackgroundImage
description: Das BackgroundImage-Attribut gibt das Hintergrundbild des Schiebereglers an oder ruft es ab.
ms.assetid: 73757635-4d1c-4ed0-8721-0608cd85859c
keywords:
- Slider. BackgroundImage-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1188756c16b13bef69dfd0bcd9a5b66560856f99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358252"
---
# <a name="sliderbackgroundimage"></a>Slider. BackgroundImage

Das **BackgroundImage** -Attribut gibt das Hintergrundbild des Schiebereglers an oder ruft es ab.

``` syntax
        elementID.backgroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional. Wenn Sie Bilder zum Erstellen eines Schiebereglers verwenden, wird **BackgroundImage** für den hauptschiebe Regler verwendet. " **Thumbimage** " stellt den tatsächlichen Schieberegler dar und kann mit der Maus verschoben werden. Im Schieberegler " **thumbimage** " gibt es eine unsichtbare Zeile, in der das Hintergrundbild auf einer Seite der Zeile angezeigt wird, und das Vordergrundbild wird auf der anderen Seite angezeigt.

Wenn der Schieberegler " **thumbimage** " mit der Maus bewegt wird und " **Folie** " auf "true" festgelegt ist, wird das Vordergrundbild so bewegt, als ob es vom Schieberegler abgerufen wird, um das Hintergrundbild abzudecken. Wenn **Folie** auf false festgelegt ist, wird das Vordergrundbild nicht verschoben, sondern direkt angezeigt, als ob der Schieberegler das Hintergrundbild aus dem Vordergrundbild verschiebt.

Wenn das **Kachel** Attribut auf "true" festgelegt ist und das Hintergrundbild kleiner als das Schieberegler-Steuerelement ist, wird das Bild abhängig vom **Direction** -Attribut entweder horizontal oder vertikal gekachelt. Wenn das **BorderSize** -Attribut auf einen Wert größer als 0 (null) festgelegt ist, ist die angegebene Zahl die Anzahl der Pixel von links nach rechts oder oben und unten im Bild (abhängig vom **Direction** -Attribut), die für die Rahmen des Schieberegler-Steuer Elements reserviert werden. In diesem Fall wird nur der zentrale Teil des Bilds zum Durchsuchen des restlichen Steuer Elements verwendet.

Die unterstützten Formate sind BMP, JPG, PNG und GIF (keine animierten GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Slider. foregroundimage**](slider-foregroundimage.md)
</dt> <dt>

[**Schieberegler. Folie**](slider-slide.md)
</dt> <dt>

[**Slider. thumbimage**](slider-thumbimage.md)
</dt> </dl>

 

 





