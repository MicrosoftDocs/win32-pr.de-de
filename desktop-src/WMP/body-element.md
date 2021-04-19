---
title: Body-Element
description: Das Body-Element enthält die Elemente, die den Inhalt einer Wiedergabeliste definieren.
ms.assetid: 96d09635-c360-4a36-a56e-6cecbbd4ff30
keywords:
- Body-Element Fenster Media Player
topic_type:
- apiref
api_name:
- body Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb30885efe9e018bf8792b38facdc086c5473b3f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369182"
---
# <a name="body-element"></a>Body-Element

Das **Body** -Element enthält die Elemente, die den Inhalt einer Wiedergabeliste definieren.

``` syntax
<body>
</body>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                 |
|-----------|--------------------------|
| Parent    | [smil](smil-element.md) |
| Untergeordnet     | [Seq](seq-element.md)   |



 

## <a name="remarks"></a>Bemerkungen

Der Inhalt einer Wiedergabeliste ist innerhalb eines "Element"-Elements organisiert, das im **Body** **-Element enthalten** ist. In der Regel gibt es entweder ein **SEQ** -Element, das einen statischen Satz von Medien Elementen definiert und **Medien** Elemente enthält, oder es gibt ein Element, das einen dynamischen Satz von Medien Elementen definiert und ein **smartwiedergabe** -Element enthält.

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
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Media-Element**](media-element.md)
</dt> <dt>

[**ENQ-Element**](seq-element.md)
</dt> <dt>

[**smartwiedergabe-Element**](smartplaylist-element.md)
</dt> <dt>

[**smil-Element**](smil-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





