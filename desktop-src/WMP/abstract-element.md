---
title: ABSTRACT-Element
description: Das ABSTRACT-Element enthält Text, der das zugeordnete ASX-, BANNER- oder ENTRY-Element beschreibt.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- ABSTRACT-Windows Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 153759dbe4bef47693cba13549b58215e4992686eab81cdcb4dadb33aa30279f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903050"
---
# <a name="abstract-element"></a>ABSTRACT-Element

Das **ABSTRACT-Element** enthält Text, der das zugeordnete **ASX-,** **BANNER-** oder **ENTRY-Element** beschreibt.

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über- und untergeordnete Elemente



| Hierarchy | Elemente                       |
|-----------|--------------------------------|
| Parent    | **ASX**, **ENTRY**, **BANNER** |
| Untergeordnet     | Keine                           |



 

## <a name="remarks"></a>Bemerkungen

Wenn dieses Element in einem **ASX-Element** angezeigt wird, wird der Text als QuickInfo angezeigt, wenn der Mauszeiger auf den Showtitel zeigt.

Wenn dieses Element in einem **ENTRY-Element** angezeigt wird, wird der Text als QuickInfo angezeigt, wenn der Mauszeiger auf den Cliptitel zeigt.

Wenn dieses Element innerhalb eines **BANNER-Elements angezeigt** wird, wird der Text als QuickInfo für die Bannergrafik angezeigt.

Verwenden Sie nur **ein ABSTRACT-Element** pro Bereich. Nur das erste **ABSTRACT-Element** innerhalb des Bereichs eines anderen Elements wird verwendet, wenn eine Metadateidatei verarbeitet wird. Alle **nachfolgenden ABSTRACT-Elemente** in diesem Bereich werden ignoriert.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
    <TITLE>The Title of the Show<TITLE>
    <ABSTRACT>
        Brief description of the show. 
    </ABSTRACT>

<ENTRY>    
    <REF HREF="YourMediaFilename.asf" />
    <TITLE>The Title of the Track</TITLE>
    <ABSTRACT>
        Brief description of the track.
    </ABSTRACT>
</ENTRY>
</ASX>
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zur Medienmetadatei**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





