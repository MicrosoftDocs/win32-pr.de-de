---
title: BUTTON.tiled
description: Das gekachelte Attribut gibt einen Wert an, der angibt, ob das BUTTON-Bild gekachelt wird, oder ruft einen Wert ab.
ms.assetid: 5526477d-a235-4960-adef-5cf0ef9c46be
keywords:
- BUTTON.tiled Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.tiled
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32f4f1dda0b5a79749cfbffaa30f29522ff318a763ad50fcd005479afa9c8997
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118581374"
---
# <a name="buttontiled"></a>BUTTON.tiled

Das **gekachelte** Attribut gibt einen Wert an, der angibt, ob das **BUTTON-Bild** gekachelt wird, oder ruft einen Wert ab.

``` syntax
        elementID.tiled
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Lese-/Schreib-Wert.



| Wert | BESCHREIBUNG                       |
|-------|-----------------------------------|
| true  | Das Bild wird gekachelt.              |
| false | Standard. Das Bild wird nicht gekachelt. |



 

## <a name="remarks"></a>Hinweise

Wenn das Bild kleiner als der tatsächliche Bereich des Steuerelements ist, wird es beim Kacheln des Bilds wiederholt, bis es den gesamten Bereich ausfüllt. Wenn ein Bild nicht angegeben ist oder nicht abgerufen werden kann, wird **gekachelt** auf FALSE festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 





