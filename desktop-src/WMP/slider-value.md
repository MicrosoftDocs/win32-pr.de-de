---
title: SLIDER.value
description: Das Value-Attribut gibt die aktuelle Position des Schiebereglers an oder ruft sie ab. | SLIDER.value
ms.assetid: 2cd2f8b2-d3f1-4897-98b0-af551d6693e6
keywords:
- SLIDER.value Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.value
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30f9ae7c0dc45f3a14cad2aa5b7332b037302b6658043233bbd98b1d99a12e10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118118628"
---
# <a name="slidervalue"></a>SLIDER.value

Das **Value-Attribut** gibt die aktuelle Position des Schiebereglers an oder ruft sie ab.

``` syntax
        elementID.value
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Lese-/Schreibnummer **(float)** mit dem Standardwert **min.**

## <a name="remarks"></a>Hinweise

Der **Wert** sollte immer größer oder gleich **min** und kleiner als oder gleich **max** sein. Wenn Sie einen Wert außerhalb dieses Bereichs angeben, werden **der Wert** und die Position des Schiebereglers nicht geändert.

Weitere Informationen finden Sie unter **DEM UNTERENLIDER.** [das attribut positionImage](customslider-positionimage.md) für ein Beispiel, das veranschaulicht, wie die Attribute des **SLIDER-Elements** verwendet werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.min**](slider-min.md)
</dt> </dl>

 

 





