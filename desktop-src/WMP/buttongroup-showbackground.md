---
title: BUTTONGROUP.showBackground
description: Das showBackground-Attribut gibt einen Wert an, der angibt, ob buttongroup nur die Schaltflächen oder die vollständige Bitmap anzeigt, die im Imageattribut angegeben ist, oder ruft einen Wert ab.
ms.assetid: 5c3fc873-937c-4dad-ac18-e7a37004ee1e
keywords:
- BUTTONGROUP.showBackground Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.showBackground
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb95b707fa7e14b00e86c5a65949ff9fba3ce3db32745116fa65ca4c53ac1998
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342673"
---
# <a name="buttongroupshowbackground"></a>BUTTONGROUP.showBackground

Das **showBackground-Attribut** gibt einen Wert an, der angibt, ob **buttongroup** nur die Schaltflächen oder die vollständige Bitmap anzeigt, die im **Imageattribut** angegeben ist, oder ruft einen Wert ab.

``` syntax
        elementID.showBackground
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist ein **boolescher** Lese-/Schreib-Wert.



| Wert | BESCHREIBUNG                                                                                |
|-------|--------------------------------------------------------------------------------------------|
| true  | Schaltflächen werden angezeigt, und der Bereich, der nicht von Schaltflächen belegt ist, wird aus der Bildbitmap gezeichnet. |
| false | Standard. Nur die Schaltflächen werden angezeigt.                                                   |



 

## <a name="remarks"></a>Hinweise

Wenn **showBackground** true ist, wird das gesamte **Hauptbild** angezeigt.

Wenn **showBackground** false ist, werden nur die Bereiche gerendert, die zugewiesenen **MappingImage-Farben** entsprechen. Anders ausgedrückt: Nur **BUTTONELEMENTs,** deren **mappingColor** zugewiesen ist, sind sichtbar.

Wenn ein ungültiger Wert angegeben wird, wird der vorherige Zustand beibehalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTONGROUP-Element**](buttongroup-element.md)
</dt> <dt>

[**BUTTONELEMENT.mappingColor**](buttonelement-mappingcolor.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.mappingImage**](buttongroup-mappingimage.md)
</dt> </dl>

 

 





