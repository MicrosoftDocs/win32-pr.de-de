---
title: BUTTON.image
description: Das Imageattribut gibt das Standardbild von BUTTON an oder ruft es ab.
ms.assetid: d0d97f14-2c4d-4769-b45c-c6cde7282bea
keywords:
- BUTTON.image-Windows Media Player
topic_type:
- apiref
api_name:
- BUTTON.image
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85874c79db8f3174b70af68c3ff1e58511c3f00cc7d648389dbca971c7efd96e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118342908"
---
# <a name="buttonimage"></a>BUTTON.image

Das  Imageattribut gibt das Standardbild von BUTTON an oder ruft **es ab.**

``` syntax
        elementID.image
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Zeichenfolge mit **Lese-/Schreibzugriff,** die den Namen der Bilddatei enthält.

## <a name="remarks"></a>Hinweise

Die unterstützten Bildformate sind BMP, JPG, PNG und GIF (einschließlich animierter GIFs).

Wenn das **BUTTON-Bild** größer als  der  durch die Breiten- und Höhenattribute definierte Bereich ist, wird das Bild zugeschnitten.

Wenn das Bild nicht angegeben ist, aber **höhe** und **breite,** wird das Bild direkt hinter diesem Steuerelement angezeigt. Dies kann das Zeichnen des Bilds in der ANSICHT selbst **vereinfachen,** was die Anzahl der benötigten separaten Bilddateien reduziert.

Wenn das Bild nicht abgerufen werden kann, wird ein Standardbild (das rot-x-Bild) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**BUTTON-Element**](button-element.md)
</dt> </dl>

 

 





