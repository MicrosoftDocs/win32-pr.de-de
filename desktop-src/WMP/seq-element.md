---
title: ENQ-Element
description: Das Element "-q" enthält Elemente, die eine statische Wiedergabeliste oder Elemente definieren, die eine intelligente Wiedergabeliste definieren.
ms.assetid: 849f7b38-25f2-4708-a83c-e651812a1a72
keywords:
- Media Player für das Fenster "
topic_type:
- apiref
api_name:
- seq Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b08b3f4dfa448e48f3a9d2472c6ddb46a4d4dfaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354068"
---
# <a name="seq-element"></a>ENQ-Element

Das Element "- **q** " enthält Elemente, die eine statische Wiedergabeliste oder Elemente definieren, die eine intelligente Wiedergabeliste definieren.

``` syntax
<seq>
</seq>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                                                               |
|-----------|------------------------------------------------------------------------|
| Parent    | [body](body-element.md)                                               |
| Untergeordnet     | [Medien](media-element.md), [smartwiedergabe Liste](smartplaylist-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Wenn ein Element vom Typ "- **q** " nur **Medien** Elemente enthält, die auf bestimmte Medienelemente verweisen, wird die Wiedergabeliste als statisch betrachtet. Wenn ein Element vom Typ "- **q** " ein **smartwiedergabe** -Element enthält, wird es als dynamische "intelligente" Wiedergabeliste betrachtet.

## <a name="examples"></a>Beispiele


```
<seq>
    <media></media>
    <media></media>
</seq>

<seq>
    <smartPlaylist></smartPlaylist>
</seq>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Body-Element**](body-element.md)
</dt> <dt>

[**Media-Element**](media-element.md)
</dt> <dt>

[**smartwiedergabe-Element**](smartplaylist-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





