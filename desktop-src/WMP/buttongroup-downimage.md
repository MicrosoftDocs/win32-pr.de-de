---
title: BUTTONGROUP.downImage
description: Das downImage-Attribut gibt den Namen des Bilds an, das den Downstatus der BUTTONGROUP darstellt, oder ruft den Namen ab.
ms.assetid: 022e77e7-d3c0-41b5-984a-84d016a5a25a
keywords:
- BUTTONGROUP.downImage-Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 233c56951ec88444ab58de901732517a4ced4c249f8a9b75f3461eb38e86c975
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997750"
---
# <a name="buttongroupdownimage"></a>BUTTONGROUP.downImage

Das **downImage-Attribut** gibt den Namen des Bilds an, das den Zustand "Down" der BUTTONGROUP darstellt, **oder ruft sie ab.**

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können die Farbton- und Sättigungswerte mithilfe der **Attribute hueShift** und **Sättigung** dynamisch geändert werden.

Das Standardbild ist das im **Imageattribut angegebene** Bild.

Wenn das Bild nach unten größer als der definierte Bereich ist, wird das Bild nach unten zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTONGROUP-Element**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.image**](buttongroup-image.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





