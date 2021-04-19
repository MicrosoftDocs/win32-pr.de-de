---
title: Button. Bild
description: Das Image-Attribut gibt das Standardbild der Schaltfläche an oder ruft es ab.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- Button. Bild-Windows-Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d27363383d72110ebe7b3e94187013ab701a6a3c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367763"
---
# <a name="buttonimage"></a>Button. Bild

Das **Image** -Attribut gibt das Standardbild der **Schaltfläche** an oder ruft es ab.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF (einschließlich animierter Gifs).

Wenn das **Schalt** Flächen Bild größer als der durch die **Width** -und **height** -Attribute definierte Bereich ist, wird das Bild beschnitten.

Wenn das Bild nicht angegeben wird, aber **Höhe** und **Breite** sind, wird das Bild direkt hinter diesem Steuerelement angezeigt. Dies kann das Zeichnen des Bilds auf der **Ansicht** selbst vereinfachen, wodurch die Anzahl der erforderlichen getrennten Bilddateien reduziert wird.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> </dl>

 

 





