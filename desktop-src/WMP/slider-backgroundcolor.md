---
title: SLIDER.backgroundColor
description: Das backgroundColor-Attribut gibt die Hintergrundfarbe des Schiebereglersteuerelements an oder ruft sie ab.
ms.assetid: 8f2c48ec-29f5-4fbe-aa62-c7cfb8a8678c
keywords:
- SLIDER.backgroundColor Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.backgroundColor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc2de30392c58cfad151e2d3c209f0407880a47522a536bf08dbe42d7f56dc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995230"
---
# <a name="sliderbackgroundcolor"></a>SLIDER.backgroundColor

Das **backgroundColor-Attribut** gibt die Hintergrundfarbe des Schiebereglersteuerelements an oder ruft sie ab.

``` syntax
        elementID.backgroundColor
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die einen beliebigen Microsoft Internet Explorer Farbwert enthält. Er besitzt keinen Standardwert.

## <a name="remarks"></a>Hinweise

Ein einfaches Schieberegler-Steuerelement kann erstellt werden, indem **backgroundColor** oder **backgroundImage** und **foregroundColor** oder **foregroundImage** angegeben werden.

Bei Verwendung der Farben definieren die Abmessungen des Schieberegler-Steuerelements den Bereich, der durch die Hintergrundfarbe gefüllt wird. Die Vordergrundfarbe deckt die Hintergrundfarbe ab, wenn die Position des Schiebereglers zunimmt.

Um eine Farbverlaufsfüllung des Bereichs zu erstellen, der von der Hintergrund- oder Vordergrundfarbe belegt wird, geben Sie die Attribute **backgroundEndColor** oder **foregroundEndColor** an.

Weitere Informationen finden Sie unter *UNTER DEM -Artikel.* [das attribut positionImage](customslider-positionimage.md) für ein Beispiel, das veranschaulicht, wie die Attribute des **SLIDER-Elements** verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Farbreferenz**](color-reference.md)
</dt> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundEndColor**](slider-backgroundendcolor.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.foregroundColor**](slider-foregroundcolor.md)
</dt> <dt>

[**SLIDER.foregroundEndColor**](slider-foregroundendcolor.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





