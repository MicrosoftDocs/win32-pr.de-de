---
title: STARTMARKER-Element
description: Das STARTMARKER-Element gibt einen Marker an, von dem Windows Media Player mit dem Rendern des Streams beginnen.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- STARTMARKER-Element Windows Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2fa80da249edc4b9e3ab7d8796bc6ff135cb7cfb2b19a1cb11216ebe4a9c122c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123040"
---
# <a name="startmarker-element"></a>STARTMARKER-Element

Das **STARTMARKER-Element** gibt einen Marker an, von dem Windows Media Player mit dem Rendern des Streams beginnen.

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Attribute

**Anzahl**

Die Nummer eines numerischen Markers im Index. Der Standardwert ist der Anfang von bedarfsorientiertem Inhalt oder die aktuelle Position in einem Echtzeitstream.

**NAME**

Der Name eines benannten Markers im Index. Der Standardwert ist der Anfang von bedarfsorientiertem Inhalt oder die aktuelle Position in einem Echtzeitstream.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ENTRY**, **REF** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element gibt den Marker an, von dem Windows Media Player mit dem Rendern des im übergeordneten **ENTRY-** oder **REF-Element** definierten Streams beginnen soll.

**Hinweis**

Verwenden Sie dieses Element entweder mit dem **NUMBER-** oder **DEM NAME-Attribut,** aber nicht mit beiden.

Ein innerhalb eines **REF-Elements** definiertes **STARTMARKER-Element** hat Vorrang vor einem **STARTMARKER-Element,** das im übergeordneten **ENTRY-Element** des **REF-Elements** definiert ist. Ein **STARTMARKER-Element** hat auch Vorrang vor einem **STARTTIME-Element.**

Wenn der von einem **STARTMARKER-Element** angegebene Marker später im Stream auftritt als der marker, der durch ein **ENDMARKER-Element** definiert wird, wird kein Inhalt wiedergegeben, aber es wird kein Fehler generiert.

## <a name="examples"></a>Beispiele


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
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

 

 





