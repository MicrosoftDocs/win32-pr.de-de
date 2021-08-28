---
title: VERALTENLIDER.hoverImage
description: Das hoverImage-Attribut gibt das Bild an, das angezeigt wird, wenn sich der Mauszeiger über dem benutzerdefinierten Schieberegler befindet, oder ruft es ab.
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- WINDOWS MEDIA PLAYER
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d12f337c8d4889e0d2e94bac0c0a4dce74f3a80fda9261d245b91ce5612754d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651400"
---
# <a name="customsliderhoverimage"></a>VERALTENLIDER.hoverImage

Das **hoverImage-Attribut** gibt das Bild an, das angezeigt wird, wenn sich der Mauszeiger über dem benutzerdefinierten Schieberegler befindet, oder ruft es ab.

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine **Zeichenfolge** mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Dieses Attribut ist optional. Wenn sie nicht angegeben wird, wird die im **Imageattribut** angegebene Datei verwendet.

Das **hoverImage** stellt den Mauszeigerzustand des STEUERELEMENTS VOMLIDER dar. Das heißt, der Status, der angezeigt wird, wenn der Mauszeiger darauf zeigt. Dies kann ein einzelnes Bild oder eine Reihe von Bildern sein, die die verschiedenen Zustände des Schiebereglers darstellen. Wenn mehrere Bilder verwendet werden, werden sie auf die gleiche Weise wie die **Bilddatei** angeordnet.

Die unterstützten Bilddateitypen sind BMP, JPG, PNG und GIF (ohne animierte GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ELEMENTSLIDER-Element**](customslider-element.md)
</dt> <dt>

[**MSILIDER.image**](customslider-image.md)
</dt> </dl>

 

 





