---
title: Slider. ForegroundColor
description: Das ForegroundColor-Attribut gibt die Vordergrundfarbe des Schieberegler-Steuer Elements an oder ruft diese ab.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- Schieberegler. ForegroundColor-Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d334dff4d9b7d90582e44018bf8f56c04fa784a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365633"
---
# <a name="sliderforegroundcolor"></a>Slider. ForegroundColor

Das **ForegroundColor** -Attribut gibt die Vordergrundfarbe des Schieberegler-Steuer Elements an oder ruft diese ab.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** mit einem beliebigen Microsoft Internet Explorer-Farbwert. Der Standardwert ist "White".

## <a name="remarks"></a>Bemerkungen

Ein grundlegendes Schieberegler-Steuerelement kann erstellt werden, indem eines von zwei Attributen von Attributen angegeben wird: **Background Color** und **ForegroundColor** oder **BackgroundImage** und **foregroundimage**.

Wenn Sie mithilfe der Color-Attribute ein Schieberegler-Steuerelement erstellen, definieren die Abmessungen des Schieberegler-Steuer Elements den Bereich, der von der Hintergrundfarbe ausgefüllt wird. Die Vordergrundfarbe deckt die Hintergrundfarbe ab, wenn die Schiebereglerposition zunimmt.

Geben Sie die Attribute **backgroundendcolor** oder **foregroundendcolor** an, um eine Verlaufs Füllung in dem Bereich zu erstellen, der durch die Hintergrund-oder Vordergrundfarbe belegt ist.

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

[**Slider. BackgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**Slider. backgroundendcolor**](slider-backgroundendcolor.md)
</dt> <dt>

[**Slider. foregroundendcolor**](slider-foregroundendcolor.md)
</dt> <dt>

[**Slider. foregroundimage**](slider-foregroundimage.md)
</dt> </dl>

 

 





