---
title: Slider. BackgroundColor
description: Das BackgroundColor-Attribut gibt die Hintergrundfarbe des Schieberegler-Steuer Elements an oder ruft diese ab.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- Schieberegler. BackgroundColor-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06cc595af13b28541fcc570e130da4e804fdeafe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365939"
---
# <a name="sliderbackgroundcolor"></a>Slider. BackgroundColor

Das **BackgroundColor** -Attribut gibt die Hintergrundfarbe des Schieberegler-Steuer Elements an oder ruft diese ab.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einem beliebigen Microsoft Internet Explorer-Farbwert. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Bemerkungen

Ein grundlegendes Schieberegler-Steuerelement kann erstellt werden, indem **Background Color** oder **BackgroundImage** und **ForegroundColor** oder **foregroundimage** angegeben werden.

Wenn die Farben verwendet werden, definieren die Abmessungen des Schieberegler-Steuer Elements den Bereich, der von der Hintergrundfarbe ausgefüllt wird. Die Vordergrundfarbe deckt die Hintergrundfarbe ab, wenn die Schiebereglerposition zunimmt.

Geben Sie die **backgroundendcolor** -oder **foregroundendcolor** -Attribute an, um eine Verlaufs Füllung des Bereichs zu erstellen, der durch die Hintergrund-oder Vordergrundfarbe belegt ist.

Weitere Informationen finden Sie unter *customslider*. [positionImage](customslider-positionimage.md) -Attribut für ein Beispiel, das veranschaulicht, wie die Attribute des **Slider** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Farb Verweis**](color-reference.md)
</dt> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Slider. backgroundendcolor**](slider-backgroundendcolor.md)
</dt> <dt>

[**Slider. BackgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**Slider. ForegroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**Slider. foregroundendcolor**](slider-foregroundendcolor.md)
</dt> <dt>

[**Slider. foregroundimage**](slider-foregroundimage.md)
</dt> </dl>

 

 





