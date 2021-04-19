---
title: ButtonGroup. disabledImage
description: Das disabledImage-Attribut gibt den Namen des Bilds an, das den deaktivierten Zustand der Schaltflächen in der ButtonGroup darstellt, oder ruft ihn ab.
ms.assetid: 34d4e6a9-de73-4dfa-9c23-4f17b55298f6
keywords:
- ButtonGroup. disabledImage Windows Media Player
topic_type:
- apiref
api_name:
- BUTTONGROUP.disabledImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9659c4d726313c0fb202a840e12891f00ad3fcf0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352854"
---
# <a name="buttongroupdisabledimage"></a>ButtonGroup. disabledImage

Das **disabledImage** -Attribut gibt den Namen des Bilds an, das den deaktivierten Zustand der Schaltflächen in der **ButtonGroup** darstellt, oder ruft ihn ab.

``` syntax
        elementID.disabledImage
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese- **/schreibzeichenfolge**.

## <a name="remarks"></a>Bemerkungen

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF. Wenn es sich bei dem Bild um eine 8-Bit-BMP-Datei handelt, können seine Farbton-und Sättigungswerte mithilfe der Attribute **hueshift** und **Sättigung** dynamisch geändert werden.

Wenn das **Deaktivierte** Attribut eines **ButtonElement** -Elements auf true festgelegt ist, wird der zugehörige Bereich von **disabledImage** für die **ButtonGroup** angezeigt. Wenn das deaktivierte Bild größer als der definierte Bereich ist, wird das deaktivierte Bild beschnitten.

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

 

 





