---
title: Button. hoverimage
description: Das hoverimage-Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Schaltfläche im Zustand "up" befindet, und der Benutzer mit dem Mauszeiger darauf zeigt.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- Button. hoverimage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80b17a461ffde4b9f6777f3ce360c6b3f1747235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364833"
---
# <a name="buttonhoverimage"></a>Button. hoverimage

Das **hoverimage** -Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die **Schaltfläche** im Zustand "up" befindet, und der Benutzer mit dem Mauszeiger darauf zeigt.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.

Das Standardbild ist das im **Image** -Attribut angegebene oder sein Standardbild.

Wenn das Hover-Bild größer als der definierte Bereich im Ambient-Attribut ist, wird das Hover-Bild beschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

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

 

 





