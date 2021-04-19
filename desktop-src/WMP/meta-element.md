---
title: Meta-Element
description: Das Meta-Element gibt Metadaten an, die auf die gesamte Wiedergabeliste angewendet werden.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- Media Player des Meta-Element-Windows
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f3c41c25a0df0895c645c34f97495712b113ffc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106359329"
---
# <a name="meta-element"></a>Meta-Element

Das **Meta** -Element gibt Metadaten an, die auf die gesamte Wiedergabeliste angewendet werden.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                       | BESCHREIBUNG                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**Benennen**<br/>          | Der Name eines Elements von Metadaten.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**inhaltliche**<br/> | Der Wert eines Elements von Metadaten. Wenn das Namensattribut z. b. "Genre" lautet, könnte das Inhalts Attribut "Rock" lauten.<br/> |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Untergeordnet     | Keine                     |



 

## <a name="remarks"></a>Bemerkungen

Der Ersteller einer Windows-Medienwiedergabe Liste kann das Name-Attribut eines Meta-Elements auf eine beliebige Zeichenfolge festlegen. In der folgenden Liste sind einige typische namens Attribute aufgeführt, die in Windows Media-Wiedergabelisten enthalten sind, die von Windows Media Player und anderen Microsoft-Komponenten erstellt wurden.

-   Autor
-   Category
-   Genre
-   UserName
-   UserRating
-   Generator

## <a name="examples"></a>Beispiele


```
<head>
    <meta name = "Author" content = "Frank Lee"/>
    <meta name = "Category" content = "Classic"/>
    <meta name = "Genre" content = "Rock"/>
</head>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Head-Element**](head-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





