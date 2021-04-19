---
title: ButtonGroup. showbackground
description: Mit dem showbackground-Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob in der ButtonGroup nur die Schaltflächen angezeigt werden, oder es wird die im Image-Attribut angegebene vollständige Bitmap angezeigt.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- ButtonGroup. showbackground-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31cc87260d4b0fca74d6063c757e6c3dae0db850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364643"
---
# <a name="buttongroupshowbackground"></a>ButtonGroup. showbackground

Mit dem **showbackground** -Attribut wird ein Wert angegeben oder abgerufen, der angibt, ob in der **ButtonGroup** nur die Schaltflächen angezeigt werden, oder es wird die im **Image** -Attribut angegebene vollständige Bitmap angezeigt.

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Wert mit Lese-/Schreibzugriff.



| Wert | BESCHREIBUNG                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Schaltflächen werden angezeigt, und der Bereich, der nicht von Schaltflächen besetzt ist, wird aus der Bild Bitmap gezeichnet. |
| false | Standard. Es werden nur die Schaltflächen angezeigt.                                                   |



 

## <a name="remarks"></a>Bemerkungen

Wenn **showbackground** den Wert true hat, wird das gesamte **Hauptbild** angezeigt.

Wenn **showbackground** den Wert false hat, werden nur die Bereiche gerendert, die den zugewiesenen **mappingImage** -Farben entsprechen. Das heißt, dass nur **buttonelements** mit ihrer zugewiesenen **mappingColor** sichtbar sind.

Wenn ein ungültiger Wert angegeben wird, wird der vorherige Zustand beibehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonGroup-Element**](buttongroup-element.md)
</dt> <dt>

[**ButtonElement. mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**ButtonGroup. Image**](buttongroup-image.md)
</dt> <dt>

[**ButtonGroup. mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





