---
title: Title-Element (Metadatei)
description: Das Title-Element definiert eine Text Zeichenfolge, die den Titel für ein ASX-oder Entry-Element angibt.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- Title-Element (Metafile) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bdb58edbb3ffd99e8be557fdb05a7e51298fda14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356027"
---
# <a name="title-element-metafile"></a>Title-Element (Metadatei)

Das **Title** -Element definiert eine Text Zeichenfolge, die den Titel für ein **ASX** -oder **Entry** -Element angibt.

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert eine Text Zeichenfolge, die den Titel eines **ASX** -oder **Entry** -Elements angibt. Der Titel wird im Anzeigebereich und im **Eigenschaften** Dialogfeld angezeigt.

Wenn dieses Element in einem **ASX** -Element angezeigt wird, wird der Text als **Anzeige** Informationen angezeigt. Wenn dieses Element in einem **Entry** -Element angezeigt wird, wird der Text als **Clip** Informationen angezeigt.

Wenn ein **morumfo** -Element auch mit dem zugeordneten (übergeordneten) Element verwendet wird, ist dies der Titeltext, auf den der Benutzer klickt, um auf die im **Moran FO** -Element definierte URL zuzugreifen.

Jedes über **geordnete-** und- **Entry** -Element muss höchstens ein untergeordnetes **Title** -Element enthalten. Mehrere **Titel** Elemente nach dem ersten werden ignoriert und werden nicht angezeigt.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
   <TITLE>Title of the Show</TITLE>
   <ENTRY>
      <TITLE>Title of the Clip</TITLE>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
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

 

 





