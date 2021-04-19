---
title: Slider. BorderSize
description: Das BorderSize-Attribut gibt die Rahmenbreite in Pixel an oder ruft Sie ab.
ms.assetid: ca766b45-1be3-4207-8cd0-ad50c33d52be
keywords:
- Schieberegler. BorderSize-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.borderSize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c3ebc95e3ecf04ae78fa78c4b46f38fdd910004
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372598"
---
# <a name="sliderbordersize"></a>Slider. BorderSize

Das **BorderSize** -Attribut gibt die Rahmenbreite in Pixel an oder ruft Sie ab.

``` syntax
        elementID.borderSize
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibzahl (**Long**), die die Breite des Rahmens in Pixel darstellt.  Der Standardwert ist 0 (null).

## <a name="remarks"></a>Bemerkungen

Dieses Attribut definiert einen Offset vom Anfang und Ende des Schieberegler-Steuer Elements, von links nach rechts, wenn das **Direction** -Attribut auf "horizontal" festgelegt ist, und von oben nach unten, wenn es auf "vertikal" festgelegt ist. Diese Offset Positionen legen die minimalen und maximalen Positionen des Schieberegler-Zieh Punkts fest, über den die Vordergrundfarbe oder das Bild nicht angewendet wird.

Wenn ein Hintergrundbild mit dem auf true festgelegten **Kachel** Attribut verwendet wird, wird der Offset auf das Bild angewendet, wobei die Größe des Bilds (entweder von links nach rechts oder von oben nach unten) für den Anfangs-und Endrahmen des Schieberegler-Steuer Elements festgelegt wird, wobei der zentrale Teil des Bilds im gesamten Rest gekachelt wird. Auf diese Weise kann ein kleines Hintergrundbild verwendet werden, um die vollständige Länge eines größeren Schieberegler-Steuer Elements abzudecken.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Slider. ForegroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**Slider. foregroundimage**](slider-foregroundimage.md)
</dt> <dt>

[**Slider. thumbimage**](slider-thumbimage.md)
</dt> <dt>

[**Schieberegler. Kachel**](slider-tiled.md)
</dt> </dl>

 

 





