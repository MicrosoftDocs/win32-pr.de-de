---
title: Schieberegler. Folie
description: Mit dem Folie-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Vordergrundbild über das Hintergrundbild bewegt wird oder in einer statischen Position über das Hintergrundbild angezeigt wird.
ms.assetid: dc68c2a0-d3fe-4984-9607-12703a27edbd
keywords:
- Schieberegler. Folien Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.slide
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b9f79b5016b323380c5a4d06c8af7ab5fb0b8a2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367717"
---
# <a name="sliderslide"></a>Schieberegler. Folie

Mit dem **Folie** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Vordergrundbild über das Hintergrundbild bewegt wird oder in einer statischen Position über das Hintergrundbild angezeigt wird.

``` syntax
        elementID.slide
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                          |
|-------|----------------------------------------------------------------------|
| true  | Standard. Das Vordergrundbild bewegt sich über das Hintergrundbild.      |
| false | Das Vordergrundbild wird direkt über das Hintergrundbild angezeigt. |



 

## <a name="remarks"></a>Bemerkungen

Wenn der Schieberegler " **thumbimage** " mit der Maus bewegt wird und " **Folie** " auf "true" festgelegt ist, wird das Vordergrundbild so bewegt, als ob es vom Schieberegler abgerufen wird, um das Hintergrundbild abzudecken. Wenn **Folie** auf false festgelegt ist, wird das Vordergrundbild nicht verschoben, sondern direkt angezeigt, als ob der Schieberegler das Hintergrundbild aus dem Vordergrundbild verschiebt.

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

[**Slider. foregroundimage**](slider-foregroundimage.md)
</dt> </dl>

 

 





