---
title: filter-Element
description: Das Filterelement enthält Elemente, die die Größe einer Wiedergabeliste, die Dauer einer Wiedergabeliste oder die Anzahl von Medienelementen in einer Wiedergabeliste einschränken.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- filter Element Windows Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8a059a6a2820d99541076775ac869de0767ffd739743f5b145a155efd0a25abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576777"
---
# <a name="filter-element"></a>filter-Element

Das **Filterelement** enthält Elemente, die die Größe einer Wiedergabeliste, die Dauer einer Wiedergabeliste oder die Anzahl von Medienelementen in einer Wiedergabeliste einschränken.

``` syntax
<filter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</filter>
            
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**Typ**
</dt> <dd>

Der Typ des Filterobjekts. Es gibt keine vordefinierten Werte für dieses Attribut.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (erforderlich) 
</dt> <dd>

Die GUID, die ein Filterobjekt eindeutig identifiziert. Die Methoden des Filterobjekts werden aufgerufen, um die im Filterelement enthaltenen **Fragmentelemente** **zu** interpretieren.



| Wert                                  | Beschreibung                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | Die ID für den Filter "Microsoft Auto Playlist Filter - Limits auto playlists by count, size or duration". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (erforderlich) 
</dt> <dd>

Der Name des Filterobjekts.



| Wert                                                                              | Beschreibung                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Filter für automatische Wiedergabelisten von Microsoft: Schränkt automatische Wiedergabelisten nach Anzahl, Größe oder Dauer ein. | Schränkt automatische Wiedergabelisten nach Anzahl, Größe oder Dauer ein. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                                   |
|-----------|--------------------------------------------|
| Parent    | [smartPlaylist](smartplaylist-element.md) |
| Untergeordnet     | [Fragment](fragment-element.md)           |



 

## <a name="remarks"></a>Hinweise

Das **Filterelement** fügt einer Wiedergabeliste keine Medienelemente hinzu. Es entfernt oder filtert einfach Inhalte heraus, die vom **sourceFilter-Element ausgewählt** wurden.

## <a name="examples"></a>Beispiele


```XML
<filter 
    type = "smartFilterObject" 
    id = "{BC5E21B0-504C-46F6-82BF-FB975C911AD6}" 
    name = "Microsoft Auto Playlist Filter -- Limits auto playlists by count,size or duration">
        <fragment name = "Limit Number of Items">
            <argument name = "number">25</argument>
        </fragment>
</filter>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**argument-Element**](argument-element.md)
</dt> <dt>

[**fragment-Element**](fragment-element.md)
</dt> <dt>

[**smartPlaylist-Element**](smartplaylist-element.md)
</dt> <dt>

[**sourceFilter-Element**](sourcefilter-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





