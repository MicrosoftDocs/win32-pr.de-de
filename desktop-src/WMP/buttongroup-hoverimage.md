---
title: BUTTONGROUP.hoverImage
description: Das hoverImage-Attribut gibt den Namen des Bilds an, das den Hoverzustand einer Schaltfläche in BUTTONGROUP darstellt, oder ruft den Namen des Bilds ab. Der Hoverzustand tritt auf, wenn sich die Schaltfläche im Zustand "Up" befindet und der Benutzer mit der Maus darauf zeigen soll.
ms.assetid: 319b8770-8c4a-441a-ad03-9ff895958cf2
keywords:
- BUTTONGROUP.hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ee872c06d405d0f9cf5c09f59a86ba1962d0a5b349460c978e37fb5022f1d60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135903"
---
# <a name="buttongrouphoverimage"></a>BUTTONGROUP.hoverImage

Das **hoverImage-Attribut** gibt den Namen des Bilds an, das den Hoverzustand einer Schaltfläche in **buttongroup darstellt,** oder ruft den Namen des Bilds ab. Der Hoverzustand tritt auf, wenn sich die Schaltfläche im Zustand "Up" befindet und der Benutzer mit der Maus darauf zeigen soll.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können die Farbton- und Sättigungswerte mithilfe der Attribute **hueShift** und **saturation** dynamisch geändert werden.

Das Standardbild ist das  im Imageattribut angegebene Image oder dessen Standardbild.

Wenn das Bild mit dem Mauszeiger größer als der definierte Bereich ist, wird das Bild mit dem Mauszeiger zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das bild red-x) angezeigt.

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie unter *BUTTONELEMENT*. [mappingColor-Attribut](buttonelement-mappingcolor.md) für ein Beispiel, das die Verwendung dieses Attributs veranschaulicht.

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

 

 





