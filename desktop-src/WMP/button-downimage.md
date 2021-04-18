---
title: Button. downImage
description: Das downImage-Attribut gibt das Bild an, das den Zustand der Schaltfläche darstellt, oder ruft es ab.
ms.assetid: 18149668-5be6-4b64-8adf-8904585ff0be
keywords:
- Button. Fenster Media Player Windows-
topic_type:
- apiref
api_name:
- BUTTON.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca7a405a5df20a04ae9d093f2b28ee4c68cab67d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365183"
---
# <a name="buttondownimage"></a>Button. downImage

Das **downImage** -Attribut gibt das Bild an, das den Zustand der **Schaltfläche** darstellt, oder ruft es ab.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen der Bilddatei enthält

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF.

Das Standardbild ist das im **Image** -Attribut angegebene oder sein Standardbild.

Wenn das nach-unten-Bild größer als der definierte Bereich im Ambient-Attribut ist, wird das Bild mit dem Bild abgeschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Button-Element**](button-element.md)
</dt> <dt>

[**Schaltfläche. nach unten**](button-down.md)
</dt> <dt>

[**Button. Bild**](button-image.md)
</dt> </dl>

 

 





