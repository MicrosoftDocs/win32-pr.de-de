---
title: Ambientattribute. Width
description: Das width-Attribut gibt die Breite des-Steuer Elements an oder ruft diese ab.
ms.assetid: f246958a-563c-40c0-8a74-4511103b95b2
keywords:
- Ambientattribute. Width-Windows-Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.width
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c3f91ee47277dc511d54747197edfa44e80e251
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369981"
---
# <a name="ambientattributeswidth"></a>Ambientattribute. Width

Das **Width** -Attribut gibt die Breite des-Steuer Elements an oder ruft diese ab.

``` syntax
        elementID.width
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine 16-Bit- **Ganzzahl** mit Lese-/Schreibzugriff (0 bis 32.767), die die Breite des Steuer Elements in Pixel darstellt. Der Standardwert ist 0 (null) oder die Breite des Bilds, das im **Image** -Attribut des Steuer Elements angegeben ist.

## <a name="remarks"></a>Bemerkungen

Wenn die angegebene Breite schmaler als die Breite des bereitgestellten Bilds ist, wird das Bild abgeschnitten. Wenn die Breite größer als die Breite des Bilds ist, geht der Klick Bereich über die Bild Begrenzung hinaus. Unabhängig davon, welcher Wert diesem Attribut zugewiesen wird, kann das Bild nicht über seine übergeordnete **Ansicht** oder **unter Ansicht** hinaus wachsen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





