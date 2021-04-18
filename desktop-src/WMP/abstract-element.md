---
title: Abstract-Element
description: Das abstrakte Element enthält Text, der den zugeordneten ASX, das Banner oder das Einstiegs Element beschreibt.
ms.assetid: 7866fee8-1778-433a-be2f-9df0baa1c13e
keywords:
- Abstrakte Element Fenster Media Player
topic_type:
- apiref
api_name:
- ABSTRACT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4e90b6f52b697242be23303ab3597dac549a6177
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371247"
---
# <a name="abstract-element"></a>Abstract-Element

Das **abstrakte** Element enthält Text, der den zugeordneten **ASX**, das **Banner** oder das **Einstiegs** Element beschreibt.

``` syntax
<ABSTRACT>
   text string
</ABSTRACT>
      
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy | Elemente                       |
|-----------|--------------------------------|
| Parent    | **ASX**, **Eintrag**, **Banner** |
| Untergeordnet     | Keine                           |



 

## <a name="remarks"></a>Bemerkungen

Wenn dieses Element in einem **ASX** -Element angezeigt wird, wird der Text als QuickInfo angezeigt, wenn mit dem Mauszeiger auf den Show-Titel gezeigt wird.

Wenn dieses Element in einem **Entry** -Element angezeigt wird, wird der Text als QuickInfo angezeigt, wenn mit dem Mauszeiger auf den Clip Titel gezeigt wird.

Wenn dieses Element innerhalb eines **Banner** Elements angezeigt wird, wird der Text als QuickInfo für die Banner Grafik angezeigt.

Verwenden Sie nur ein **abstraktes** Element pro Bereich. Wenn eine Metadatendatei verarbeitet wird, wird nur das erste **abstrakte** Element innerhalb des Gültigkeits Bereichs eines anderen Elements verwendet. Alle nachfolgenden **abstrakten** Elemente in diesem Bereich werden ignoriert.

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
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





