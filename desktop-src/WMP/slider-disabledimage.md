---
title: SLIDER.disabledImage
description: Das attribut disabledImage gibt das Bild des Schiebereglers an, der beim Deaktivieren des Schieberegler-Steuerelements verwendet wird, oder ruft es ab.
ms.assetid: b6c4237d-8eb0-44ce-a23f-9bdc5c21aca8
keywords:
- SLIDER.disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 596afbed41fa1a864d8ed4e5fd217cb4856a716623ad2a60db080b3e965ab48d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123070"
---
# <a name="sliderdisabledimage"></a>SLIDER.disabledImage

Das **attribut disabledImage** gibt das Bild des Schiebereglers an, der beim Deaktivieren des Schieberegler-Steuerelements verwendet wird, oder ruft es ab.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Hinweise

**DisabledImage** ist optional. Wenn es nicht angegeben wird, wird **backgroundImage** für alle deaktivierten Zustände verwendet. Wenn ein Schieberegler-Steuerelement deaktiviert ist, ist kein Vordergrundbild sichtbar.

Die unterstützten Formate sind BMP, JPG, PNG und GIF (ohne animierte GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SLIDER-Element**](slider-element.md)
</dt> <dt>

[**SLIDER.backgroundImage**](slider-backgroundimage.md)
</dt> </dl>

 

 





