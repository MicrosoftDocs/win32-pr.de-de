---
title: Ambientattribute. ninegridmargin
description: Das ninegridmargin-Attribut gibt die Rand breiten für die nicht einheitliche Skalierung des Skin-Elements an.
ms.assetid: b8a7efd0-6c12-4436-9d53-0dcfa1600aa5
keywords:
- Ambientattribute. ninegridmargins-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.nineGridMargins
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3cf77c1fcfdb64fb9e4b0dde8753572255c17eda
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372291"
---
# <a name="ambientattributesninegridmargins"></a>Ambientattribute. ninegridmargin

Das **ninegridmargin** -Attribut gibt die Rand breiten für die nicht einheitliche Skalierung des Skin-Elements an.

``` syntax
        elementID.nineGridMargins
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die die Breite der Ränder in der Form "*widthleft*,*widthtop*,*widthright*,*widthbottom*" enthält. Jeder width-Wert ist eine Zahl, die die Breite eines Randes neun Rasters in Pixel darstellt.

## <a name="remarks"></a>Bemerkungen

Ein *neun Raster* ist eine Technik, mit der Benutzeroberflächen Elemente in neun rechteckige Bereiche aufgeteilt werden, die in einer 3 x 3-Matrix angeordnet sind. Wenn die Größe eines Elements geändert wird, können die neun Raster Bereiche jeweils mit einem anderen Faktor skaliert werden.

Jeder der vier Width-Werte, die Sie angeben, stellt die Breite einer Zeile oder Spalte von drei angrenzenden Regionen dar. Jede Zeile oder Spalte bildet die linke Seite, die obere, die Rechte Seite oder das Ende des neun Rasters.

" [Ambientattribute. resizeimages](ambientattributes-resizeimages.md) " muss auf "true" festgelegt werden, damit dieses Attribut funktioniert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------|
| Version<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





