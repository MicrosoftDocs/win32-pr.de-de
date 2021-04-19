---
title: smil-Element
description: Das smil-Element ist immer das Element der obersten Ebene in einer Windows Media-Wiedergabe Datei (WPL). Er gibt an, dass die Datei SMIL-Syntax und-Grammatik (synchronisiert Multimedia Integration Language) verwendet.
ms.assetid: bb14f1b8-53d0-47ff-9fd3-4620a1467985
keywords:
- smil-Element Windows-Media Player
topic_type:
- apiref
api_name:
- smil Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 78ec8900139cfbd5982228c59010674bbc14765e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359739"
---
# <a name="smil-element"></a>smil-Element

Das **SMIL** -Element ist immer das Element der obersten Ebene in einer Windows Media-Wiedergabe Datei (WPL). Er gibt an, dass die Datei SMIL-Syntax und-Grammatik (synchronisiert Multimedia Integration Language) verwendet.

``` syntax
<smil>
</smil>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                                           |
|-----------|----------------------------------------------------|
| Parent    | Keine                                               |
| Untergeordnet     | [Kopf](head-element.md), [Text](body-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Jede Windows-Medienwiedergabe Liste muss über das **SMIL** -Element im Stammverzeichnis verfügen.

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
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Body-Element**](body-element.md)
</dt> <dt>

[**Head-Element**](head-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





