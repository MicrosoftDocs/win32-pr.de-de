---
title: body-Element
description: Das Body-Element enthält die Elemente, die den Inhalt einer Wiedergabeliste definieren.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- body-Element Windows Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c785b7db7b44177469596450ee75a460e2bc6224b191a2811baf95380bea25a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135953"
---
# <a name="body-element"></a>body-Element

Das **Body-Element** enthält die Elemente, die den Inhalt einer Wiedergabeliste definieren.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                 |
|-----------|--------------------------|
| Parent    | [Smil](smil-element.md) |
| Untergeordnet     | [Seq](seq-element.md)   |



 

## <a name="remarks"></a>Hinweise

Der Inhalt einer Wiedergabeliste ist in einem **seq-Element** organisiert, das im **Textelement** enthalten ist. In der Regel gibt es entweder ein seq-Element, das einen statischen Satz von Medienelementen definiert und **Medienelemente** enthält, oder ein **Seq-Element,** das einen dynamischen Satz von Medienelementen definiert und ein **smartPlaylist-Element** enthält.

## <a name="examples"></a>Beispiele


```XML
<body>
    <seq>
        <media></media>
        <media></media>
        <media></media>
    </seq>
</body>

<body>
    <seq>
        <smartPlaylist></smartPlaylist>
    </seq>
</body>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**media-Element**](media-element.md)
</dt> <dt>

[**seq-Element**](seq-element.md)
</dt> <dt>

[**smartPlaylist-Element**](smartplaylist-element.md)
</dt> <dt>

[**smil-Element**](smil-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





