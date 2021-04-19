---
title: Button. disabledImage
description: Das disabledImage-Attribut gibt das Bild an, das angezeigt wird, wenn die Schaltfläche deaktiviert ist, oder ruft es ab.
ms.assetid: b5654323-589a-45da-9534-6fa67c3a4c4b
keywords:
- Button. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8eac407f6e7fbdd155f4bcabe98cecc0546f7d97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356321"
---
# <a name="buttondisabledimage"></a>Button. disabledImage

Das **disabledImage** -Attribut gibt das Bild an, das angezeigt wird, wenn die **Schaltfläche** deaktiviert ist, oder ruft es ab.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.

Dieses Bild wird immer dann angezeigt, wenn das **Deaktivierte** Attribut des-Steuer Elements auf true festgelegt ist. Wenn das deaktivierte Bild größer als der definierte Bereich ist, wird das deaktivierte Bild beschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> </dl>

 

 





