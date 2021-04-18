---
title: Media-Element
description: Das Media-Element gibt eines der Medienelemente in einer Wiedergabeliste an.
ms.assetid: 7329bf48-3b23-4bc6-8488-506efca284bb
keywords:
- Windows-Media Player für Medien Element
topic_type:
- apiref
api_name:
- media Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2e693c8b17345d3ba7875d48b83b5e3e90d682dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361263"
---
# <a name="media-element"></a>Media-Element

Das **Media** -Element gibt eines der Medienelemente in einer Wiedergabeliste an.

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
| <span id="src__required______________"></span><span id="SRC__REQUIRED______________"></span>**src** (erforderlich) <br/> | Die URL eines Medien Elements.<br/>                                                              |
| <span id="cid"></span><span id="CID"></span>**zid**<br/>                                                             | Die Inhalts-ID, die für dieses Medien Element eindeutig ist.<br/>                                     |
| <span id="tid"></span><span id="TID"></span>**Drüse**<br/>                                                             | Die Nachverfolgungs-ID, die verwendet werden kann, um das Datei System Objekt für dieses Medien Element nachzuverfolgen.<br/> |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente               |
|-----------|------------------------|
| Parent    | [Seq](seq-element.md) |
| Untergeordnet     | Keine                   |



 

## <a name="remarks"></a>Bemerkungen

Das **CID** -Attribut (die Inhalts-ID) wird durch den Windows-Media Player als Möglichkeit zum eindeutigen Identifizieren eines Medien Inhalts aufgefüllt, auch wenn seine Metadatenattribute geändert wurden. Dies ermöglicht die gemeinsame Nutzung von Wiedergabelisten auf allen Computern, da der Inhalt auf einem anderen Computer identifiziert werden kann und der Pfad zu ihm von der Windows Media-Wiedergabeliste automatisch repariert werden kann. Das **TID** -Attribut (die Überwachungs-ID) verwendet das Windows-Dateisystem, um den Pfad zu den Medien automatisch zu reparieren, wenn der Name oder Speicherort der Datei geändert wird.

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
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ENQ-Element**](seq-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





