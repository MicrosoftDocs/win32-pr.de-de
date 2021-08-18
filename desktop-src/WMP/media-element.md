---
title: media-Element
description: Das Medienelement gibt eines der Medienelemente in einer Wiedergabeliste an.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- media-Element Windows Media Player
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c67f4321d85ec52babbc6f24c2cd9e3512f7c970eb3360ba2ddfd7ba53f82152
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996320"
---
# <a name="media-element"></a>media-Element

Das **Medienelement** gibt eines der Medienelemente in einer Wiedergabeliste an.

``` syntax
<media
    src = "URL"
    cid = "WPL_GUID"
    tid = "WPL_GUID"
>
</media>
```

## <a name="attributes"></a>Attribute



| Begriff                                                                                                                       | BESCHREIBUNG                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (erforderlich) <br/> | Die URL eines Medienelements.<br/>                                                              |
| <span id="cid"></span><span id="CID"></span>**Cid**<br/>                                                             | Die Inhalts-ID, die für dieses Medienelement eindeutig ist.<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**Tid**<br/>                                                             | Die Nachverfolgungs-ID, die zum Nachverfolgen des Dateisystemobjekts für dieses Medienelement verwendet werden kann.<br/> |



 

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente               |
|-----------|------------------------|
| Parent    | [Seq](seq-element.md) |
| Untergeordnet     | Keine                   |



 

## <a name="remarks"></a>Bemerkungen

Das **cid-Attribut** (die Inhalts-ID) wird vom Windows Media Player aufgefüllt, um einen Medieninhalt eindeutig zu identifizieren, auch wenn seine Metadatenattribute geändert wurden. Dies ermöglicht die computerübergreifende Freigabe von Wiedergabelisten, da der Inhalt auf einem anderen Computer identifiziert werden kann und der Pfad zu dieser Wiedergabeliste von der Windows Medienwiedergabeliste automatisch repariert werden kann. Das **attribut tid** (die Nachverfolgungs-ID) verwendet das Windows Dateisystem, um den Pfad zu den Medien automatisch zu reparieren, wenn der Name oder Speicherort der Datei geändert wird.

## <a name="examples"></a>Beispiele


```
<media
    src = "laure.wma"
    cid = "ABCDEFGH-abcd-1234-WXYZ-ABCDEF000000"
    tid = "12345678-1234-abcd-ABCD-123456abcDEF"
>
</media>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player serie 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**seq-Element**](seq-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





