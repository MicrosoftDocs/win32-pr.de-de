---
title: BUTTON.hoverImage
description: Das hoverImage-Attribut gibt das Bild an, das angezeigt wird, wenn sich button im Auf-Zustand befindet, und der Benutzer mit dem Mauszeiger darauf zeigt, oder ruft es ab.
ms.assetid: 6704e63d-1def-4e8e-808f-131c3cc1c0de
keywords:
- BUTTON.hoverImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8488fb599a958a96ef7b5aaa5afbf4c219110f0da5be7016a8190efe2004475d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003720"
---
# <a name="buttonhoverimage"></a>BUTTON.hoverImage

Das **hoverImage-Attribut** gibt das Bild an, das angezeigt wird, wenn sich **button** im Auf-Zustand befindet, und der Benutzer mit dem Mauszeiger darauf zeigt, oder ruft es ab.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff,** die den Namen der Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.

Das Standardbild ist das  im Imageattribut angegebene Image oder dessen Standardbild.

Wenn das Bild mit dem Hover größer als der definierte Bereich im Ambient-Attribut ist, wird das Hoverbild zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> <dt>

[**BUTTON.image**](button-image.md)
</dt> </dl>

 

 





