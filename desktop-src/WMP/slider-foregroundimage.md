---
title: Slider. foregroundimage
description: Das foregroundimage-Attribut gibt das Vordergrundbild des Schiebereglers an oder ruft es ab.
ms.assetid: f713fba8-e965-4fed-b323-8a513d1f13e6
keywords:
- Slider. foregroundimage-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a286d3b73a2647160a0bd23357703f4fcb88d267
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371510"
---
# <a name="sliderforegroundimage"></a>Slider. foregroundimage

Das **foregroundimage** -Attribut gibt das Vordergrundbild des Schiebereglers an oder ruft es ab.

``` syntax
        elementID.foregroundImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional. Wenn Sie Bilder zum Erstellen eines Schieberegler-Steuer Elements verwenden, wird **BackgroundImage** für den hauptschiebe Regler verwendet. " **Thumbimage** " stellt den tatsächlichen Schieberegler dar und kann mit der Maus verschoben werden. Im Schieberegler " **thumbimage** " gibt es eine unsichtbare Zeile, in der das Hintergrundbild auf einer Seite der Zeile angezeigt wird, und das Vordergrundbild wird auf der anderen Seite angezeigt.

Wenn der Schieberegler " **thumbimage** " mit der Maus bewegt wird und " **Folie** " auf "true" festgelegt ist, wird das Vordergrundbild so bewegt, als ob es vom Schieberegler abgerufen wird, um das Hintergrundbild abzudecken. Wenn **Folie** auf false festgelegt ist, wird das Vordergrundbild nicht verschoben, sondern direkt angezeigt, als ob der Schieberegler das Hintergrundbild aus dem Vordergrundbild verschiebt.

Wenn das **Kachel** Attribut auf "true" festgelegt ist und das Vordergrundbild kleiner als der Vordergrund Bereich des Schieberegler-Steuer Elements ist, wird das Bild entweder horizontal oder vertikal gekachelt, abhängig vom **Direction** -Attribut, um den verfügbaren Platz auszufüllen.

Die unterstützten Formate sind BMP, JPG, PNG und GIF (keine animierten GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Slider. BackgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Schieberegler. Folie**](slider-slide.md)
</dt> <dt>

[**Slider. thumbimage**](slider-thumbimage.md)
</dt> <dt>

[**Slider. Wert**](slider-value.md)
</dt> </dl>

 

 





