---
title: ButtonGroup. downImage
description: Das downImage-Attribut gibt den Namen des Bilds an oder Ruft den Namen des Bilds ab, das den Zustand der ButtonGroup darstellt.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- ButtonGroup. downImage-Fenster Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82b8a1d5bc2f4c68894a3bba1ad8ce9f2b3aa28a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352961"
---
# <a name="buttongroupdownimage"></a>ButtonGroup. downImage

Das **downImage** -Attribut gibt den Namen des Bilds an oder Ruft den Namen des Bilds ab, das den Zustand der **ButtonGroup** darstellt.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.

Das Standard Image ist das im **Image** -Attribut angegebene.

Wenn das Abbild größer als der definierte Bereich ist, wird das Bild mit dem Bild abgeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

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

 

 





