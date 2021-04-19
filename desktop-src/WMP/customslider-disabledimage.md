---
title: Customslider. disabledImage
description: Das disabledImage-Attribut gibt das Bild des Schiebereglers an, das verwendet wird, wenn der Schieberegler deaktiviert ist.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- Customslider. disabledImage-Windows-Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 169057d952170fb92c4e3a98617c7db22f5456b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367762"
---
# <a name="customsliderdisabledimage"></a>Customslider. disabledImage

Das **disabledImage** -Attribut gibt das Bild des Schiebereglers an, das verwendet wird, wenn der Schieberegler deaktiviert ist.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge** , die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Bemerkungen

Dieses Attribut ist optional. Wenn kein Wert angegeben ist, wird die im **Image** -Attribut angegebene Datei verwendet.

**DisabledImage** stellt den deaktivierten Zustand des **customslider** -Steuer Elements dar. Dabei kann es sich um ein einzelnes Bild oder eine Reihe von Bildern handeln, die die verschiedenen Zustände des Schiebereglers darstellen. Wenn mehrere Images verwendet werden, werden Sie auf die gleiche Weise wie die **Bilddatei** angeordnet.

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

 

 





