---
title: Ambientattribute. Height
description: Das Height-Attribut gibt die Höhe des Steuer Elements an oder ruft diese ab.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- Ambientattribute. Height-Fenster Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 662268bfeaf00b3185d531ff10d8dd17c9127a66
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358706"
---
# <a name="ambientattributesheight"></a>Ambientattribute. Height

Das **height** -Attribut gibt die Höhe des Steuer Elements an oder ruft diese ab.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/schreibzahl (**Long**), die die Höhe des Steuer Elements in Pixel darstellt.  Der Standardwert ist 0 (null) oder die Höhe des Bilds, das im **Image** -Attribut des Steuer Elements angegeben ist.

## <a name="remarks"></a>Bemerkungen

Wenn die angegebene Höhe kleiner als die Höhe des angegebenen Bilds ist, wird das Bild abgeschnitten. Wenn die Höhe größer als die Höhe des Bilds ist, geht der Klick Bereich über die Bild Begrenzung hinaus. Unabhängig davon, welcher Wert diesem Attribut zugewiesen wird, kann das Bild nicht über seine übergeordnete **Ansicht** oder **unter Ansicht** hinaus wachsen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





