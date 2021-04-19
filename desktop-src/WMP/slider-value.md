---
title: Slider. Wert
description: Das value-Attribut gibt die aktuelle Position des Schiebereglers an oder ruft diese ab. | Slider. Wert
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- Schieberegler. Wert-Fenster Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87aeff5c97808efb812f530236227b07f463855
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369516"
---
# <a name="slidervalue"></a>Slider. Wert

Das **value** -Attribut gibt die aktuelle Position des Schiebereglers an oder ruft diese ab.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibnummer (**float**) mit einem Standardwert von **Min**. 

## <a name="remarks"></a>Bemerkungen

Der **Wert** muss immer größer als oder gleich **Min** und kleiner oder gleich dem **maximalen** Wert sein. Wenn Sie einen Wert außerhalb dieses Bereichs angeben, werden der **Wert** und die Position des Schiebereglers nicht geändert.

Weitere Informationen finden Sie unter **customslider**. [positionImage](customslider-positionimage.md) -Attribut für ein Beispiel, das veranschaulicht, wie die Attribute des **Slider** -Elements verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Schieberegler. min.**](slider-min.md)
</dt> </dl>

 

 





