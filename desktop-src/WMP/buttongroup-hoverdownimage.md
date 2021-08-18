---
title: BUTTONGROUP.hoverDownImage
description: Das hoverDownImage-Attribut gibt den Namen des Bilds an, das den Hoverdownzustand einer Schaltfläche in buttongroup darstellt, oder ruft den Namen ab. Der Zustand des Mauszeigers tritt auf, wenn sich die Schaltfläche im Zustand "Unten" befindet und der Benutzer mit der Maus darauf zeigen soll.
ms.assetid: dc048303-21d1-40ba-99bb-8d1c2f46628b
keywords:
- BUTTONGROUP.hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c84d907a9b3fd1fc1a2eaf2dcf30337d016ae0732b147f435f49343d791b65c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119879"
---
# <a name="buttongrouphoverdownimage"></a>BUTTONGROUP.hoverDownImage

Das **hoverDownImage-Attribut** gibt den Namen des Bilds an, das den Hoverdownzustand einer Schaltfläche in **buttongroup darstellt,** oder ruft den Namen des Bilds ab. Der Zustand des Mauszeigers tritt auf, wenn sich die Schaltfläche im Zustand "Unten" befindet und der Benutzer mit der Maus darauf zeigen soll.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können die Farbton- und Sättigungswerte mithilfe der Attribute **hueShift** und **saturation** dynamisch geändert werden.

Das Standardimage ist das im **downImage-Attribut** angegebene Image oder dessen Standardimage.

Wenn das Bild mit dem Mauszeiger nach unten größer als der definierte Bereich ist, wird das Bild mit dem Mauszeiger nach unten zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das bild red-x) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTONGROUP-Element**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.downImage**](buttongroup-downimage.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





