---
title: Head-Element
description: Das Head-Element enthält Metadaten, die auf die gesamte Wiedergabeliste angewendet werden.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- Windows-Media Player des Head-Elements
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8708a8a683f7457e6568df3a897c71253ad76c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361956"
---
# <a name="head-element"></a>Head-Element

Das **Head** -Element enthält Metadaten, die auf die gesamte Wiedergabeliste angewendet werden.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                                                  |
|-----------|-----------------------------------------------------------|
| Parent    | [smil](smil-element.md)                                  |
| Untergeordnet     | [Title](title-element--wpl.md), [Meta](meta-element.md) |



 

## <a name="remarks"></a>Bemerkungen

In der Regel enthält das **Head** -Element ein **Title** -Element und ein oder mehrere **Meta** -Elemente, die globale Merkmale der Wiedergabeliste definieren.

## <a name="examples"></a>Beispiele


```
<head>
    <title>Party Playlist</title>
    <meta name = "Author" CONTENT = "Frank Lee"/>
    <meta name = "Category" CONTENT = "Party Music"/>
    <meta name = "Genre" CONTENT = "Pop"/>
    <meta name = "UserName1" CONTENT = "Frank001"/>
    <meta name = "UserRating1" CONTENT = "82"/>
</head>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Meta-Element**](meta-element.md)
</dt> <dt>

[**Title-Element (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





