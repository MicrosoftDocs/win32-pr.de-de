---
title: smil-Element
description: Das smil-Element ist immer das Element der obersten Ebene in einer Windows Media Playlist(WPL)-Datei. Sie gibt an, dass die Datei die Syntax und Grammatik von SMIL (Synchronized Multimedia Integration Language) verwendet.
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- smil-Windows Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 15ed9c3d70b0af65019cd384bc68ab9c26f8d01673481b9ced3595730379bf1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763460"
---
# <a name="smil-element"></a>smil-Element

Das **smil-Element** ist immer das Element der obersten Ebene in einer Windows Media Playlist(WPL)-Datei. Sie gibt an, dass die Datei die Syntax und Grammatik von SMIL (Synchronized Multimedia Integration Language) verwendet.

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                                           |
|-----------|----------------------------------------------------|
| Parent    | Keine                                               |
| Untergeordnet     | [head,](head-element.md) [body](body-element.md) |



 

## <a name="remarks"></a>Hinweise

Jede Windows Medienwiedergabeliste muss das **smil-Element** im Stamm enthalten.

## <a name="examples"></a>Beispiele


```
<?wpl version = "1.0"?>
<smil>
    <head>
        <entity type="hellip"/>
    </head>

    <body>
        <entity type="hellip"/>
    </body>
</smil>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**body-Element**](body-element.md)
</dt> <dt>

[**head-Element**](head-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





