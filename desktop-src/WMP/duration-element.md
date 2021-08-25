---
title: DURATION-Element
description: Das DURATION-Element definiert die Zeitspanne Windows Media Player den zugeordneten Wiedergabelisteneintrag rendert.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- DURATION-Element Windows Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5b06b497a6d31b03c4cbec23748f6995a1382fb806ad18fabaa542ed8ff33e4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119863350"
---
# <a name="duration-element"></a>DURATION-Element

Das **DURATION-Element** definiert die Zeitspanne, Windows Media Player den zugeordneten Wiedergabelisteneintrag rendert.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attribute

**VALUE** (erforderlich)

Die Zeitspanne in Stunden, Minuten, Sekunden und Hundertstelsekunden, die ein Eintrag von Windows Media Player gerendert wird. Der Standardwert ist die gesamte Länge des Eintrags. Wenn es sich bei dem Eintrag um eine Grafikdatei handelt, muss ein Duration-Wert angegeben werden.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ENTRY**, **REF** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert die Zeitdauer, die ein Stream gerendert werden soll. Wenn das **VALUE-Attribut** die Länge des Inhaltsstreams überschreitet, wird der Stream am normalen Endpunkt beendet.

Dieses Element kann entweder innerhalb eines **REF-Elements** oder in einem **ENTRY-Element** angezeigt werden. Ein **DURATION-Element,** das in einem **REF-Element** definiert ist, überschreibt jedoch eines, das innerhalb des übergeordneten **ENTRY-Elements** des **REF-Elements** angezeigt wird.

Das **DURATION-Element** überschreibt ein **PREVIEWDURATION-Element.**

## <a name="examples"></a>Beispiele


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





