---
title: BUTTON.downImage
description: Das downImage-Attribut gibt das Bild an, das den Zustand "Down" der SCHALTFLÄCHE darstellt, oder ruft es ab.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- BUTTON.downImage-Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bff24c568ae607b5b67d766f28eb7c221844f1434a959952628cc2ad5a5d6d5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123740"
---
# <a name="buttondownimage"></a>BUTTON.downImage

Das **downImage-Attribut** gibt das Bild an oder ruft es ab, das den Zustand "Down" der **SCHALTFLÄCHE darstellt.**

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff,** die den Namen der Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.

Das Standardbild ist das  im Imageattribut angegebene Image oder dessen Standardbild.

Wenn das Bild nach unten größer als der definierte Bereich im Ambient-Attribut ist, wird das Bild nach unten zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> <dt>

[**BUTTON.down**](button-down.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 





