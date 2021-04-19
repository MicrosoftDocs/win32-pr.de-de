---
title: Schieberegler. useforegroundprogress
description: Mit dem useforegroundprogress-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob die Statusleiste des Vordergrunds verwendet wird.
ms.assetid: 10f3b4d9-ba82-4e30-affa-50c15a809ed6
keywords:
- Schieberegler. useforegroundprogress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.useForegroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b572933549417713158acea1a24fa9e1434c9dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360323"
---
# <a name="slideruseforegroundprogress"></a>Schieberegler. useforegroundprogress

Mit dem **useforegroundprogress** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob die Statusleiste des Vordergrunds verwendet wird.

``` syntax
        elementID.useForegroundProgress
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                              |
|-------|------------------------------------------|
| true  | Verwenden Sie den Vordergrund Fortschritt.                 |
| false | Standard. Verwenden Sie den Vordergrund Status nicht. |



 

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ermöglicht die Verwendung des **foregroundprogress** -Attributs, das hauptsächlich verwendet wird, um den Download Fortschritt einer Mediendatei zu verfolgen, während gleichzeitig die aktuelle Wiedergabe Position der Datei mithilfe des **value** -Attributs nachverfolgt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Slider-Element**](slider-element.md)
</dt> <dt>

[**Schieberegler. foregroundprogress**](slider-foregroundprogress.md)
</dt> <dt>

[**Slider. Wert**](slider-value.md)
</dt> </dl>

 

 





