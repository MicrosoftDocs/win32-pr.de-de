---
title: SLIDER.slide
description: Das Slide-Attribut gibt einen Wert an oder ruft einen Wert ab, der angibt, ob das Vordergrundbild über das Hintergrundbild gleitet oder schrittweise an einer statischen Position über dem Hintergrundbild angezeigt wird.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- SLIDER.slide-Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5d1a9480a171372ff5c90990d07bd583bd880570472b25af8d1ada945b31a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117933508"
---
# <a name="sliderslide"></a>SLIDER.slide

Das **Slide-Attribut** gibt einen Wert an oder ruft einen Wert ab, der angibt, ob das Vordergrundbild über das Hintergrundbild gleitet oder schrittweise an einer statischen Position über dem Hintergrundbild angezeigt wird.

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein boolescher Wert mit **Lese-/Schreibzugriff.**



| Wert | BESCHREIBUNG                                                          |
|-------|----------------------------------------------------------------------|
| true  | Standard. Das Vordergrundbild wird über das Hintergrundbild geschiebet.      |
| false | Das Vordergrundbild wird an Ort und Stelle über dem Hintergrundbild angezeigt. |



 

## <a name="remarks"></a>Hinweise

Wenn der **ThumbImage-Schieberegler** mit  der Maus bewegt wird und die Folie auf TRUE festgelegt ist, wird das Vordergrundbild wie durch den Schieberegler gezogen, um das Hintergrundbild zu bedecken. Wenn **die** Folie auf FALSE festgelegt ist, wird das Vordergrundbild nicht bewegt, sondern an Ort und Stelle angezeigt, als würde der Schieberegler das Hintergrundbild vom Vordergrundbild verschieben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> <dt>

[**SLIDER.foregroundImage**](slider-foregroundimage.md)
</dt> </dl>

 

 





