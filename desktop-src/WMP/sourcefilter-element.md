---
title: sourceFilter-Element
description: Das sourceFilter-Element enthält Elemente, die Elemente aus einer Bibliothek auswählen.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- sourceFilter-Windows Media Player
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 14294f227e5ebe29e422d60a95734f7b93207880ea82ef9fb70ed3f7cf6dac4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763270"
---
# <a name="sourcefilter-element"></a>sourceFilter-Element

Das **sourceFilter-Element** enthält Elemente, die Elemente aus einer Bibliothek auswählen.

``` syntax
<sourceFilter
    type = "string"
    id = "WPL_GUID"
    name = "string"
>
</sourceFilter>
```

## <a name="attributes"></a>Attribute

<dl> <dt>

<span id="type"></span><span id="TYPE"></span>**Typ**
</dt> <dd>

Der Typ des Filterobjekts. Es gibt keine vordefinierten Werte für dieses Attribut.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**id** (erforderlich) 
</dt> <dd>

Die GUID, die das Quellfilterobjekt eindeutig identifiziert. Die Methoden des Quellfilterobjekts werden aufgerufen, um die im **sourceFilter-Element** enthaltenen **Fragmentelemente** zu interpretieren.



| Wert                                  | Beschreibung                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947A-A563-4B05-A754-A1B4B5989849} | Die GUID für den Quellfilter "Musik in meiner Bibliothek".    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | Die GUID für den Quellfilter "Video in meiner Bibliothek".    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | Die GUID für den Quellfilter "Bilder in meiner Bibliothek". |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | Die GUID für den Quellfilter "TV shows in my library" (TV-Shows in meiner Bibliothek). |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**name** (erforderlich) 
</dt> <dd>

Der Name des Filterobjekts.



| Wert                  | Beschreibung                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Musik in meiner Bibliothek    | Ein Filterobjekt, das angegebene Elemente aus dem Satz von Musikelementen in der Bibliothek des Benutzers auswählt. |
| Video in meiner Bibliothek    | Ein Filterobjekt, das angegebene Elemente aus dem Satz von Videoelementen in der Bibliothek des Benutzers auswählt. |
| Bilder in meiner Bibliothek | Ein Filterobjekt, das angegebene Elemente aus dem Satz von Fotoelementen in der Bibliothek des Benutzers auswählt. |
| TV-Shows in meiner Bibliothek | Ein Filterobjekt, das angegebene Elemente aus dem Satz von TV-Elementen in der Bibliothek des Benutzers auswählt.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy | Elemente                         |
|-----------|----------------------------------|
| Parent    | [querySet](queryset-element.md) |
| Untergeordnet     | [Fragment](fragment-element.md) |



 

## <a name="remarks"></a>Hinweise

Das **element sourceFilter** wählt Elemente aus der Bibliothek aus, ohne die Größe des Resultsets zu betrachten. Das **Filterelement** schränkt hingegen die Größe des Resultsets ein.

## <a name="examples"></a>Beispiele


```
<sourceFilter 
    type = "smartFilterObject" 
    id = "{4202947A-A563-4B05-A754-A1B4B5989849}" 
    name = "Music in my library">
        <fragment name = "Genre">
            <argument name = "condition">Is</argument>
            <argument name = "value">Rock</argument>
        </fragment>
        <fragment name = "Album Artist">
            <argument name = "condition">Is Not</argument>
            <argument name = "value">Brenda Diaz</argument>
        </fragment>
</sourceFilter>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|----------------------------------------------------|
| Version<br/> | Windows Media Player 9-Serie oder höher.<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**filter-Element**](filter-element.md)
</dt> <dt>

[**fragment-Element**](fragment-element.md)
</dt> <dt>

[**querySet-Element**](queryset-element.md)
</dt> <dt>

[**Windows Referenz zu Medienwiedergabelistenelementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





