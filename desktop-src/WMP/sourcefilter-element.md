---
title: SourceFilter-Element
description: Das SourceFilter-Element enthält Elemente, die Elemente aus einer Bibliothek auswählen.
ms.assetid: c961990f-8c57-448d-b4dc-dcfe70300e5a
keywords:
- Windows Media Player SourceFilter-Element
topic_type:
- apiref
api_name:
- sourceFilter Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cb43a9577c5fe8857b63067db5be90d314037b84
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367760"
---
# <a name="sourcefilter-element"></a>SourceFilter-Element

Das **SourceFilter** -Element enthält Elemente, die Elemente aus einer Bibliothek auswählen.

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

<span id="type"></span><span id="TYPE"></span>**Sorte**
</dt> <dd>

Der Typ des Filter Objekts. Es sind keine vordefinierten Werte für dieses Attribut vorhanden.

</dd> <dt>

<span id="id__required______________"></span><span id="ID__REQUIRED______________"></span>**ID** (erforderlich) 
</dt> <dd>

Der GUID, der das Quell Filter Objekt eindeutig identifiziert. Die Methoden des Quell Filter Objekts werden aufgerufen, um die im **SourceFilter** -Element enthaltenen **fragmentelemente** zu interpretieren.



| Wert                                  | BESCHREIBUNG                                              |
|----------------------------------------|----------------------------------------------------------|
| {4202947a-a563-4b05-A754-a1b4b5989849} | Der GUID für den Quell Filter "Musik in meiner Bibliothek".    |
| {B2D9BDDC-8E49-444B-9BA4-193ABF9C7870} | Der GUID für den Quell Filter "Video in der Bibliothek".    |
| {CC823400-A8E4-4081-B073-D3B6D952FE69} | Der GUID für den Quell Filter "Bilder in der Bibliothek". |
| {E5415A66-7763-4BDE-B97F-5557CA73C303} | Der GUID für den Quell Filter "Fernsehsendungen in meiner Bibliothek". |



 

</dd> <dt>

<span id="name__required______________"></span><span id="NAME__REQUIRED______________"></span>**Name** (erforderlich) 
</dt> <dd>

Der Name des Filter Objekts.



| Wert                  | BESCHREIBUNG                                                                                     |
|------------------------|-------------------------------------------------------------------------------------------------|
| Musik in meiner Bibliothek    | Ein Filter Objekt, das angegebene Elemente aus dem Satz von Musikelementen in der Bibliothek des Benutzers auswählt. |
| Video in meiner Bibliothek    | Ein Filter Objekt, das angegebene Elemente aus dem Satz von Videoelementen in der Bibliothek des Benutzers auswählt. |
| Bilder in meiner Bibliothek | Ein Filter Objekt, das die angegebenen Elemente aus dem Satz von Fotoelementen in der Bibliothek des Benutzers auswählt. |
| Fernsehsendungen in meiner Bibliothek | Ein Filter Objekt, das die angegebenen Elemente aus der Gruppe der TV-Elemente in der Bibliothek des Benutzers auswählt.    |



 

</dd> </dl>

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                         |
|-----------|----------------------------------|
| Parent    | [Queryset](queryset-element.md) |
| Untergeordnet     | [Bruch](fragment-element.md) |



 

## <a name="remarks"></a>Bemerkungen

Das **SourceFilter** -Element wählt Elemente aus der Bibliothek ohne Berücksichtigung der Größe des Resultsets aus. Das **Filter** -Element hingegen schränkt die Größe des Resultsets ein.

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
| Version<br/> | Windows Media Player 9 oder höher.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Filter-Element**](filter-element.md)
</dt> <dt>

[**Fragment-Element**](fragment-element.md)
</dt> <dt>

[**Queryset-Element**](queryset-element.md)
</dt> <dt>

[**Referenz zu Windows Media-Wiedergabelisten Elementen**](windows-media-playlist-elements-reference.md)
</dt> </dl>

 

 





