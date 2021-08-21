---
title: BUTTONGROUP.image
description: Das Imageattribut gibt den Namen des Bilds an, das die Schaltflächen einer BUTTONGROUP darstellt, oder ruft diesen ab.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- BUTTONGROUP.image Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2fcd8d76bd217087b6b948cec3216efc2bbc6c9845e9c18b5a7619d292232b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342633"
---
# <a name="buttongroupimage"></a>BUTTONGROUP.image

Das  Imageattribut gibt den Namen des Bilds an, das die Schaltflächen einer BUTTONGROUP darstellt, oder **ruft diesen ab.**

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff.**

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können die Farbton- und Sättigungswerte mithilfe der **Attribute hueShift** und **Sättigung** dynamisch geändert werden.

Wenn das Bild des Steuerelements größer als der definierte Bereich ist, wird das Bild zugeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

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

 

 





