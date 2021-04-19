---
title: ButtonGroup. hoverdownimage
description: Das hoverdownimage-Attribut gibt den Namen des Bilds an oder Ruft den Namen des Bilds ab, das den Hover-Down-Zustand einer Schaltfläche in der ButtonGroup darstellt. Der Hover-Down-Zustand tritt auf, wenn sich die Schaltfläche im Zustand "gedrückt" befindet und der Benutzer mit der Maus darauf zeigt.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- ButtonGroup. hoverdownimage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a40788fafffd6eb4626bc834a941f7330c988fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106353789"
---
# <a name="buttongrouphoverdownimage"></a>ButtonGroup. hoverdownimage

Das **hoverdownimage** -Attribut gibt den Namen des Bilds an oder Ruft den Namen des Bilds ab, das den Hover-Down-Zustand einer Schaltfläche in der **ButtonGroup** darstellt. Der Hover-Down-Zustand tritt auf, wenn sich die Schaltfläche im Zustand "gedrückt" befindet und der Benutzer mit der Maus darauf zeigt.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.

Das Standard Image ist das im " **downImage** "-Attribut angegebene Standard Image oder der Standardwert.

Wenn das Bild mit dem Mauszeiger größer als der definierte Bereich ist, wird das Bild mit dem Mauszeiger abgeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonGroup-Element**](buttongroup-element.md)
</dt> <dt>

[**ButtonGroup. downImage**](buttongroup-downimage.md)
</dt> <dt>

[**ButtonGroup. hueshift**](buttongroup-hueshift.md)
</dt> <dt>

[**ButtonGroup. Sättigung**](buttongroup-saturation.md)
</dt> </dl>

 

 





