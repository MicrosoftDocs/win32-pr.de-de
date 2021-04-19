---
title: Title-Element (WPL)
description: Das Title-Element gibt einen Titel für die Wiedergabeliste an.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- Windows-Media Player des title-Elements (WPL)
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5649553ab51a43bd1fb0aeb78d505d7e922bf80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367061"
---
# <a name="title-element-wpl"></a>Title-Element (WPL)

Das **Title** -Element gibt einen Titel für die Wiedergabeliste an.

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Untergeordnet     | Keine                     |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Titel für eine Windows Media-Wiedergabeliste (WPL) auswählen, sollten Sie Bedenken, dass der Inhalt der Wiedergabeliste dynamisch sein kann. Ein guter Ansatz besteht darin, den Titel auf der Logik in den **Argument** Elementen zu basieren, da der Inhalt der Wiedergabeliste von diesem definiert wird. Beispiele hierfür sind "meine bevorzugten Rock-Lieder aus 1966" oder "Tanzlieder, die ich vor kurzem nicht gespielt habe".

## <a name="examples"></a>Beispiele


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Argument-Element**](argument-element.md)
</dt> <dt>

[**Head-Element**](head-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





