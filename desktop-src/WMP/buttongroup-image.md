---
title: ButtonGroup. Image
description: Das Image-Attribut gibt den Namen des Bilds an, das die Schaltflächen einer ButtonGroup darstellt, oder ruft ihn ab.
ms.assetid: dad50a1e-d147-4e0f-b5d6-8cbfeef32438
keywords:
- ButtonGroup. Image-Windows-Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fa395edc149671ad05a38a5ff7c77053b6e3d82
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361677"
---
# <a name="buttongroupimage"></a>ButtonGroup. Image

Das **Image** -Attribut gibt den Namen des Bilds an, das die Schaltflächen einer **ButtonGroup** darstellt, oder ruft ihn ab.

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.

Wenn das Bild des Steuer Elements größer als der definierte Bereich ist, wird das Bild beschnitten.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ButtonGroup-Element**](buttongroup-element.md)
</dt> <dt>

[**ButtonGroup. hueshift**](buttongroup-hueshift.md)
</dt> <dt>

[**ButtonGroup. Sättigung**](buttongroup-saturation.md)
</dt> </dl>

 

 





