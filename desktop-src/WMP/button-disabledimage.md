---
title: BUTTON.disabledImage
description: Das disabledImage-Attribut gibt das Bild an, das angezeigt wird, wenn button deaktiviert ist, oder ruft es ab.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- BUTTON.disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78c3768afd8b1356a1c0ca67a43f951e19143258dfc4f27a3a5e9d861fe9e930
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864480"
---
# <a name="buttondisabledimage"></a>BUTTON.disabledImage

Das **disabledImage-Attribut** gibt das Bild an, das angezeigt wird, wenn **button** deaktiviert ist, oder ruft es ab.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die den Namen der Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.

Dieses Bild wird immer dann angezeigt, wenn das **deaktivierte** Attribut des Steuerelements auf TRUE festgelegt ist. Wenn das deaktivierte Bild größer als der definierte Bereich ist, wird das deaktivierte Bild zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das bild red-x) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> </dl>

 

 





