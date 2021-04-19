---
title: Duration-Element
description: Mit dem Duration-Element wird die Zeitspanne definiert, mit der Windows Media Player den zugehörigen Wiedergabelisten Eintrag render.
ms.assetid: fe5c242e-08c9-44f0-a6fc-3f0fa432ba38
keywords:
- Fenster "Duration"-Element Media Player
topic_type:
- apiref
api_name:
- DURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0446fd207ce04ab08d4c7bd2e055ef8d11a5a36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371711"
---
# <a name="duration-element"></a>Duration-Element

Mit dem **Duration** -Element wird die Zeitspanne definiert, mit der Windows Media Player den zugehörigen Wiedergabelisten Eintrag render.

``` syntax
<DURATION
    VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attribute

**Wert** (erforderlich)

Die Zeitspanne in Stunden, Minuten, Sekunden und Hundertstel Sekunden, in der ein Eintrag von Windows Media Player gerendert wird. Der Standardwert ist die gesamte Länge des Eintrags. Wenn es sich bei dem Eintrag um eine Grafikdatei handelt, muss ein Duration-Wert angegeben werden.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **Eintrag**, **ref** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert die Zeitspanne, für die ein Stream gerendert werden soll. Wenn das **value** -Attribut die Länge des Inhaltsstreams überschreitet, wird der Stream am normalen Endpunkt beendet.

Dieses Element kann entweder in einem **ref** -Element oder in einem **Entry** -Element vorkommen. Ein Duration-Element, das in einem **ref** -Element definiert ist, überschreibt jedoch ein **Duration** -Element, das im übergeordneten **Entry** -Element des **ref** -Elements

Das **Duration** -Element überschreibt ein **previewduration** -Element.

## <a name="examples"></a>Beispiele


```XML
<DURATION VALUE="00:00:30" />   <!-- 30 seconds -->
<DURATION VALUE="1:01.5" />     <!-- 61.5 seconds -->

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





