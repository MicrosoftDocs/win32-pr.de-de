---
title: ButtonGroup. hoverimage
description: Das hoverimage-Attribut gibt den Namen des Bilds an, das den Hover-Zustand einer Schaltfläche in der ButtonGroup darstellt, oder ruft ihn ab. Der Hover-Zustand tritt auf, wenn sich die Schaltfläche im Zustand "up" befindet und der Benutzer mit der Maus darauf zeigt.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- ButtonGroup. hoverimage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 702a7aa73f5800628fdf14deb0dbfe142cd80dbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360256"
---
# <a name="buttongrouphoverimage"></a>ButtonGroup. hoverimage

Das **hoverimage** -Attribut gibt den Namen des Bilds an, das den Hover-Zustand einer Schaltfläche in der **ButtonGroup** darstellt, oder ruft ihn ab. Der Hover-Zustand tritt auf, wenn sich die Schaltfläche im Zustand "up" befindet und der Benutzer mit der Maus darauf zeigt.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.

Das Standardbild ist das im **Image** -Attribut angegebene oder sein Standardbild.

Wenn das Hover-Bild größer als der definierte Bereich ist, wird das Hover-Bild beschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="examples"></a>Beispiele

Siehe *ButtonElement*. [mappingColor](buttonelement-mappingcolor.md) -Attribut für ein Beispiel, das die Verwendung dieses Attributs veranschaulicht.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonGroup-Element**](buttongroup-element.md)
</dt> <dt>

[**ButtonGroup. hueshift**](buttongroup-hueshift.md)
</dt> <dt>

[**ButtonGroup. Image**](buttongroup-image.md)
</dt> <dt>

[**ButtonGroup. Sättigung**](buttongroup-saturation.md)
</dt> </dl>

 

 





