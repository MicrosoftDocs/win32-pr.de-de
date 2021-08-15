---
title: head-Element
description: Das Hauptelement enthält Metadaten, die für die gesamte Wiedergabeliste gelten.
ms.assetid: 9554c84a-34af-4492-964a-4b262cd7c4a4
keywords:
- head-Element Windows Media Player
topic_type:
- apiref
api_name:
- head Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a865419a005927cd85ea6b03d4fabad2e2ac3ef15a840b3bd01209a4df00c075
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118339170"
---
# <a name="head-element"></a>head-Element

Das **Hauptelement** enthält Metadaten, die für die gesamte Wiedergabeliste gelten.

``` syntax
<head>
</head>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                                                  |
|-----------|-----------------------------------------------------------|
| Parent    | [Smil](smil-element.md)                                  |
| Untergeordnet     | [title](title-element--wpl.md), [meta](meta-element.md) |



 

## <a name="remarks"></a>Hinweise

In der Regel enthält das **Hauptelement** ein **Titelelement** und mindestens ein **Metaelement,** das globale Merkmale der Wiedergabeliste definiert.

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
| Version<br/> | Windows Media Player serie 9 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**meta-Element**](meta-element.md)
</dt> <dt>

[**title-Element (WPL)**](title-element--wpl.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





