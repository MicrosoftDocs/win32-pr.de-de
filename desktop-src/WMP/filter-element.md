---
title: Filter-Element
description: Das Filter-Element enthält Elemente, die die Größe einer Wiedergabeliste, die Dauer einer Wiedergabeliste oder die Anzahl von Medien Elementen in einer Wiedergabeliste einschränken.
ms.assetid: 880885f6-493f-466b-b5ad-ab9b569f4cc5
keywords:
- Filter Element Fenster Media Player
topic_type:
- apiref
api_name:
- filter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 32d2d306faebef813996b59575220efeba99dfb6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366970"
---
# <a name="filter-element"></a>Filter-Element

Das **Filter** -Element enthält Elemente, die die Größe einer Wiedergabeliste, die Dauer einer Wiedergabeliste oder die Anzahl von Medien Elementen in einer Wiedergabeliste einschränken.

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

<span id="type"></span><span id="TYPE"></span>**Sorte**
</dt> <dd>

Der Typ des Filter Objekts. Es sind keine vordefinierten Werte für dieses Attribut vorhanden.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (erforderlich) 
</dt> <dd>

Die GUID, die ein Filter Objekt eindeutig identifiziert. Die Methoden des Filter Objekts werden aufgerufen, um die im **Filter** Element enthaltenen **fragmentelemente** zu interpretieren.



| Wert                                  | BESCHREIBUNG                                                                                                 |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------|
| {BC5E21B0-504C-46F6-82BF-FB975C911AD6} | Die ID für den Filter "Microsoft Auto-Wiedergabeliste--schränkt die automatische Wiedergabeliste nach Anzahl, Größe oder Dauer" ein. |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**Name** (erforderlich) 
</dt> <dd>

Der Name des Filter Objekts.



| Wert                                                                              | BESCHREIBUNG                                        |
|------------------------------------------------------------------------------------|----------------------------------------------------|
| Microsoft Auto-Wiedergabe Filter: schränkt automatische Wiedergabelisten nach Anzahl, Größe oder Dauer ein. | Schränkt automatische Wiedergabelisten nach Anzahl, Größe oder Dauer ein. |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                                   |
|-----------|--------------------------------------------|
| Parent    | [smartwiedergabe](smartplaylist-element.md) |
| Untergeordnet     | [Bruch](fragment-element.md)           |



 

## <a name="remarks"></a>Bemerkungen

Das **Filter** -Element fügt einer Wiedergabeliste keine Medienelemente hinzu. der Inhalt, der vom **SourceFilter** -Element ausgewählt wurde, wird einfach entfernt oder herausgefiltert.

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
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Argument-Element**](argument-element.md)
</dt> <dt>

[**Fragment-Element**](fragment-element.md)
</dt> <dt>

[**smartwiedergabe-Element**](smartplaylist-element.md)
</dt> <dt>

[**SourceFilter-Element**](sourcefilter-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





