---
title: meta-Element
description: Das Metaelement gibt Metadaten an, die für die gesamte Wiedergabeliste gelten.
ms.assetid: 7248e1d9-ebd1-48cb-9019-89a35eac27ae
keywords:
- meta-Element Windows Media Player
topic_type:
- apiref
api_name:
- meta Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b2e4120b3eceea6d2a664edec9b48a46d33ad19b788bb820458a8802dccd2d9a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119415740"
---
# <a name="meta-element"></a>meta-Element

Das **Metaelement** gibt Metadaten an, die für die gesamte Wiedergabeliste gelten.

``` syntax
<meta
    name = "string"
    content = "string"
/>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                       | Beschreibung                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="name"></span><span id="NAME"></span>**Namen**<br/>          | Der Name eines Metadatenelements.<br/>                                                                                       |
| <span id="content"></span><span id="CONTENT"></span>**Inhalt**<br/> | Der Wert eines Metadatenelements. Wenn das Name-Attribut beispielsweise "Genre" ist, könnte das Inhaltsattribut "Rock" sein.<br/> |



 

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Untergeordnet     | Keine                     |



 

## <a name="remarks"></a>Bemerkungen

Der Ersteller einer Windows Medienwiedergabeliste kann das Namensattribut eines Metaelements auf eine beliebige Zeichenfolge festlegen. Die folgende Liste enthält einige typische Namensattribute, die sich in Windows Medienwiedergabelisten befinden, die von Windows Media Player und anderen Microsoft-Komponenten erstellt wurden.

-   Autor
-   Kategorie
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
| Version<br/> | Windows Media Player serie 9 oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**head-Element**](head-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





