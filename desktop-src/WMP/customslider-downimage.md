---
title: LIDER.downImage
description: Das downImage-Attribut gibt das Bild des benutzerdefinierten Schiebereglers an oder ruft es ab.
ms.assetid: e1efe703-df0a-4ef9-92a9-c9cfb991ee37
keywords:
- LIDER.downImage-Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.downImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3e151f825dab7170c3e3678f280303265af0df91561c7dc709323dd8043809e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750339"
---
# <a name="customsliderdownimage"></a>LIDER.downImage

Das **downImage-Attribut** gibt das Bild des benutzerdefinierten Schiebereglers an oder ruft es ab.

``` syntax
        elementID.downImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Dieses Attribut ist optional. Wenn sie nicht angegeben wird, wird die im **Imageattribut** angegebene Datei verwendet.

Das **downImage stellt** den Zustand "Down" des **STEUERELEMENTs VERDRLIDER** dar. Dabei kann es sich um ein einzelnes Bild oder eine Reihe von Bildern, die die verschiedenen Zustände des Schiebereglers darstellen. Wenn mehrere Bilder verwendet werden, werden sie auf die gleiche Weise wie die **Bilddatei** angeordnet.

Die unterstützten Bilddateitypen sind BMP, JPG, PNG und GIF (ohne animierte GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**LIDER-Element**](customslider-element.md)
</dt> <dt>

[**LIDER.image**](customslider-image.md)
</dt> </dl>

 

 





