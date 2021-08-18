---
title: BUTTONGROUP.disabledImage
description: Das disabledImage-Attribut gibt den Namen des Bilds an, das den deaktivierten Zustand der Schaltflächen in BUTTONGROUP darstellt, oder ruft den Namen des Bilds ab.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- BUTTONGROUP.disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7eeef37bbc25185a64e767f00f9ce17934e8b445327606b552ad69d282e42e4b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764350"
---
# <a name="buttongroupdisabledimage"></a>BUTTONGROUP.disabledImage

Das **disabledImage-Attribut** gibt den Namen des Bilds an, das den deaktivierten Zustand der Schaltflächen in **buttongroup darstellt,** oder ruft den Namen des Bilds ab.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff.

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können die Farbton- und Sättigungswerte mithilfe der Attribute **hueShift** und **saturation** dynamisch geändert werden.

Wenn das **disabled-Attribut** eines **BUTTONELEMENT-Elements** auf TRUE festgelegt ist, wird der entsprechende Bereich von **disabledImage** für **BUTTONGROUP** angezeigt. Wenn das deaktivierte Bild größer als der definierte Bereich ist, wird das deaktivierte Bild zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das bild red-x) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**BUTTONGROUP-Element**](buttongroup-element.md)
</dt> <dt>

[**BUTTONGROUP.hueShift**](buttongroup-hueshift.md)
</dt> <dt>

[**BUTTONGROUP.saturation**](buttongroup-saturation.md)
</dt> </dl>

 

 





