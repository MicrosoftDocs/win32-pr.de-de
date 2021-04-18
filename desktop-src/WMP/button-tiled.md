---
title: Schaltfläche. Kachel
description: Mit dem gekachelten Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das Schaltflächen Bild angezeigt wird.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- Schaltfläche. gekachelte Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c6c1316f10ce9ae3135f4ac35ab214ecdd1096d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354826"
---
# <a name="buttontiled"></a>Schaltfläche. Kachel

Mit dem **gekachelten** Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob das **Schalt** Flächen Bild angezeigt wird.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                       |
|-------|-----------------------------------|
| true  | Das Bild wird gekachelt.              |
| false | Standard. Das Bild wird nicht gekachelt. |



 

## <a name="remarks"></a>Bemerkungen

Wenn das Bild kleiner als der tatsächliche Bereich des Steuer Elements ist, wird es durch das Zicken des Bilds wiederholt, bis die gesamte Region ausgefüllt ist. Wenn kein Bild angegeben ist oder nicht abgerufen werden kann, wird die **Kachel** auf false festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> <dt>

[**Button. Bild**](button-image.md)
</dt> </dl>

 

 





