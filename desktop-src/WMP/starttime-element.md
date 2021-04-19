---
title: StartTime-Element
description: Das StartTime-Element definiert einen Zeit Index, von dem aus Windows Media Player das Rendern des Streams startet.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- StartTime-Element Fenster Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a882da6c07ec76a94c8e214fe1da11c71680b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366952"
---
# <a name="starttime-element"></a>StartTime-Element

Das **StartTime** -Element definiert einen Zeit Index, von dem aus Windows Media Player das Rendern des Streams startet.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attribute

**Wert** (erforderlich)

Der Zeit Index (in Stunden, Minuten, Sekunden und Hundertstel Sekunden), aus dem Windows Media Player mit der Wiedergabe eines Datenstroms beginnt, der im zugeordneten Element definiert ist.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **Eintrag**, **ref** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert einen Zeit Index in den Inhalt, in dem Windows Media Player das Rendern des Streams starten soll. Dieses Element kann nur mit gespeicherten on-Demand-Inhalten verwendet werden, die indiziert wurden.

## <a name="examples"></a>Beispiele


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





