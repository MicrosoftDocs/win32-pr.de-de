---
title: title-Element (WPL)
description: Das title-Element gibt einen Titel für die Wiedergabeliste an.
ms.assetid: 8a214b96-d507-4dbf-b5f2-8fdfc4409fb0
keywords:
- title-Element (WPL) Windows Media Player
topic_type:
- apiref
api_name:
- title Element (WPL)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1de2679d5f78b48ceef569491ef21998fc13faf7126e61f76ad31959bdc2ac6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122780"
---
# <a name="title-element-wpl"></a>title-Element (WPL)

Das **title-Element** gibt einen Titel für die Wiedergabeliste an.

``` syntax
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                 |
|-----------|--------------------------|
| Parent    | [head](head-element.md) |
| Untergeordnet     | Keine                     |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie einen Titel für eine Windows Medienwiedergabeliste (WPL) auswählen, sollten Sie berücksichtigen, dass der Inhalt der Wiedergabeliste dynamisch sein kann. Ein guter Ansatz besteht darin, den Titel auf der Logik in den **Argumentelementen** zu basieren, da dies den Inhalt der Wiedergabeliste definiert. Beispiele hierfür sind "My Favorite Rock Song from 1966" oder "Music Music That I Haven't Played Recently".

## <a name="examples"></a>Beispiele


```
<head>
    <title>Dance Songs That I Haven't Played Recently</title>
</head>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**argument-Element**](argument-element.md)
</dt> <dt>

[**head-Element**](head-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





