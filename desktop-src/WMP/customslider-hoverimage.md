---
title: Customslider. hoverimage
description: Das hoverimage-Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Maus über dem benutzerdefinierten Schieberegler befindet
ms.assetid: b5d10289-280c-4578-83e8-6259249ff448
keywords:
- Windows-Media Player "customslider. hoverimage"
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.hoverImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 361f7d903b6231e92f331ab38a3a9f51bc3ec679
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354722"
---
# <a name="customsliderhoverimage"></a>Customslider. hoverimage

Das **hoverimage** -Attribut gibt das Bild an oder ruft es ab, das angezeigt wird, wenn sich die Maus über dem benutzerdefinierten Schieberegler befindet

``` syntax
        elementID.hoverImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional. Wenn kein Wert angegeben ist, wird die im **Image** -Attribut angegebene Datei verwendet.

Das **hoverimage** stellt den Hover-Zustand des customslider-Steuer Elements dar. Das heißt, der Status, der angezeigt wird, wenn der Mauszeiger darüber bewegt wird. Dabei kann es sich um ein einzelnes Bild oder eine Reihe von Bildern handeln, die die verschiedenen Zustände des Schiebereglers darstellen. Wenn mehrere Images verwendet werden, werden Sie auf die gleiche Weise wie die **Bilddatei** angeordnet.

Die unterstützten Bild Dateitypen sind BMP, JPG, PNG und GIF (keine animierten GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Customslider-Element**](customslider-element.md)
</dt> <dt>

[**Customslider. Image**](customslider-image.md)
</dt> </dl>

 

 





