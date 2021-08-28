---
title: AmbientAttributes.height
description: Das Height-Attribut gibt die Höhe des Steuerelements an oder ruft sie ab.
ms.assetid: a5c85d86-15d4-451d-b8bc-ed3b6e0dfd7d
keywords:
- AmbientAttributes.height-Windows Media Player
topic_type:
- apiref
api_name:
- AmbientAttributes.height
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbc03f631fffc4d1544906721476f229cbeb926e5d56b08dc1647f2dfd3b243
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098950"
---
# <a name="ambientattributesheight"></a>AmbientAttributes.height

Das **Height-Attribut** gibt die Höhe des Steuerelements an oder ruft sie ab.

``` syntax
        elementID.height
```

## <a name="possible-values"></a>Mögliche Werte

Dieses Attribut ist eine Lese-/Schreibnummer (**long**), die die Höhe des Steuerelements in Pixel darstellt.  Der Standardwert ist 0 (null) oder die Höhe des Bilds, das im Imageattribut des **Steuerelements angegeben** ist.

## <a name="remarks"></a>Hinweise

Wenn die angegebene Höhe kleiner als die Höhe des bereitgestellten Bilds ist, wird das Bild abgeschnitten. Wenn die Höhe größer als die Höhe des Bilds ist, geht der Klickbereich über die Bildgrenze hinaus. Unabhängig davon, welcher Wert diesem Attribut gegeben wird, kann das Bild nicht über das übergeordnete **VIEW-** oder **SUBVIEW-Element hinaus wachsen.**

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ambient-Attribute**](ambient-attributes.md)
</dt> </dl>

 

 





