---
title: STARTTIME-Element
description: Das STARTTIME-Element definiert einen Zeitindex, ab dem Windows Media Player mit dem Rendern des Streams beginnt.
ms.assetid: 9b0199c8-5c95-4b4e-a943-e3bd037bf0bc
keywords:
- STARTTIME-Element Windows Media Player
topic_type:
- apiref
api_name:
- STARTTIME Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9138b05b949098c59996c69143059de5cb5b25cafcd8da7d922de120d586b356
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118568792"
---
# <a name="starttime-element"></a>STARTTIME-Element

Das **STARTTIME-Element** definiert einen Zeitindex, ab dem Windows Media Player mit dem Rendern des Streams beginnt.

``` syntax
<STARTTIME
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attribute

**VALUE** (erforderlich)

Der Zeitindex (in Stunden, Minuten, Sekunden und Hundertstelsekunden), ab dem Windows Media Player mit der Wiedergabe eines im zugeordneten Element definierten Streams beginnt.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ENTRY**, **REF** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert einen Zeitindex für den Inhalt, in dem Windows Media Player mit dem Rendern des Streams beginnen soll. Dieses Element kann nur mit gespeicherten on-demand-Inhalten verwendet werden, die indiziert wurden.

## <a name="examples"></a>Beispiele


```XML
<STARTTIME VALUE="1:30.0" />
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





