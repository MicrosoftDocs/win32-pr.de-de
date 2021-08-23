---
title: LIDER.disabledImage
description: Das disabledImage-Attribut gibt das Bild des Schiebereglers an, der beim Deaktivieren des Schiebereglers verwendet wird, oder ruft es ab.
ms.assetid: 91b1c2e3-6c92-4baa-b1f3-e44707157f4b
keywords:
- LIDER.disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9b5d75e26204fc362dfa714bc8720d6db87e511bbfda03096d60f58f91c3335
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119651560"
---
# <a name="customsliderdisabledimage"></a>LIDER.disabledImage

Das **disabledImage-Attribut** gibt das Bild des Schiebereglers an, der beim Deaktivieren des Schiebereglers verwendet wird, oder ruft es ab.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine  Zeichenfolge mit Lese-/Schreibzugriff, die den Namen einer Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Dieses Attribut ist optional. Wenn sie nicht angegeben wird, wird die im **Imageattribut** angegebene Datei verwendet.

Das **disabledImage stellt** den deaktivierten Zustand des **STEUERELEMENTS VERDRLIDER** dar. Dabei kann es sich um ein einzelnes Bild oder eine Reihe von Bildern, die die verschiedenen Zustände des Schiebereglers darstellen. Wenn mehrere Bilder verwendet werden, werden sie auf die gleiche Weise wie die **Bilddatei** angeordnet.

Die unterstützten Bilddateitypen sind BMP, JPG, PNG und GIF (ohne animierte GIFs).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**LIDER-Element**](customslider-element.md)
</dt> <dt>

[**LIDER.image**](customslider-image.md)
</dt> </dl>

 

 





