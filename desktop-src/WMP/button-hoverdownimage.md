---
title: Button. hoverdownimage
description: Das hoverdownimage-Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Schaltfläche im Zustand "gedrückt" befindet und der Benutzer mit dem Mauszeiger darüber bewegt wird.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- Button. hoverdownimage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bc8221875656c38a35eb6539dce25f58133984f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372258"
---
# <a name="buttonhoverdownimage"></a>Button. hoverdownimage

Das **hoverdownimage** -Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die **Schaltfläche** im Zustand "gedrückt" befindet und der Benutzer mit dem Mauszeiger darüber bewegt wird.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.

Das Standard Image ist das im " **downImage** "-Attribut angegebene Standard Image oder der Standardwert.

Wenn das Hover-Bild größer als der definierte Bereich im Ambient-Attribut ist, wird das Bild mit dem Mauszeiger abgeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> <dt>

[**Button. downImage**](button-downimage.md)
</dt> </dl>

 

 





