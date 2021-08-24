---
title: BUTTON.hoverDownImage
description: Das hoverDownImage-Attribut gibt das Bild an, das angezeigt wird, wenn sich button im Abwärtszustand befindet, und der Benutzer mit dem Mauszeiger darauf zeigt, oder ruft es ab.
ms.assetid: 06645307-50f1-400d-aa73-c48d0fba3ee1
keywords:
- BUTTON.hoverDownImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverDownImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcdb23f9806e36cebd2f5da6a46a8307c268861d73f68361e07f56e9ce09dcc5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119902400"
---
# <a name="buttonhoverdownimage"></a>BUTTON.hoverDownImage

Das **hoverDownImage-Attribut** gibt das Bild an, das angezeigt wird, wenn sich **button** im Abwärtszustand befindet, und der Benutzer mit dem Mauszeiger darauf zeigt, oder ruft es ab.

``` syntax
        elementID.hoverDownImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff,** die den Namen der Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.

Das Standardbild ist das im **downImage-Attribut** angegebene Image bzw. dessen Standardbild.

Wenn das Bild mit dem Hover nach unten größer als der definierte Bereich im Ambient-Attribut ist, wird das Bild mit dem Hover nach unten zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> <dt>

[**BUTTON.downImage**](button-downimage.md)
</dt> </dl>

 

 





