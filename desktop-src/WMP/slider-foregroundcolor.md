---
title: SLIDER.foregroundColor
description: Das foregroundColor-Attribut gibt die Vordergrundfarbe des Schieberegler-Steuerelements an oder ruft sie ab.
ms.assetid: 8c8de4a9-0021-41ed-aeb8-75653855b6f1
keywords:
- SLIDER.foregroundColor-Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111dca131351dedaf2080d16bffa4db1344e9993cabcfe8ca44f149fd97eb3c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118569088"
---
# <a name="sliderforegroundcolor"></a>SLIDER.foregroundColor

Das **foregroundColor-Attribut** gibt die Vordergrundfarbe des Schieberegler-Steuerelements an oder ruft sie ab.

``` syntax
        elementID.foregroundColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die einen beliebigen Microsoft Internet Explorer-Farbwert enthält. Der Standardwert ist "white".

## <a name="remarks"></a>Hinweise

Ein einfaches Schieberegler-Steuerelement kann erstellt werden, indem eines von zwei Attributpaaren angegeben wird: **backgroundColor** und **foregroundColor** oder **backgroundImage** **und foregroundImage**.

Wenn Sie ein Schieberegler-Steuerelement mithilfe der Farbattribute erstellen, definieren die Abmessungen des Schieberegler-Steuerelements den Bereich, der von der Hintergrundfarbe ausgefüllt wird. Die Vordergrundfarbe deckt die Hintergrundfarbe ab, wenn die Position des Schiebereglers zunimmt.

Geben Sie die Attribute **backgroundEndColor** oder **foregroundEndColor** an, um eine Farbverlaufsfüllung in dem Bereich zu erstellen, der von der Hintergrund- oder Vordergrundfarbe belegt wird.

Weitere Informationen *finden Sie unter DER -1000-000-0* [positionImage-Attribut](customslider-positionimage.md) für ein Beispiel, das veranschaulicht, wie die Attribute des **SLIDER-Elements** verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Farbreferenz**](color-reference.md)
</dt> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundColor**](slider-backgroundcolor.md)
</dt> <dt>

[**SLIDER.backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





