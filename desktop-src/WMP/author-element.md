---
title: AUTHOR-Element
description: Das AUTHOR-Element enthält den Namen des Autors einer Windows Medienmetadatei oder eines Medienclips.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- AUTHOR-Windows Media Player
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 058753d73049debe01e442f49bf12476642111549ad890e931100026badaeb3d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120098890"
---
# <a name="author-element"></a>AUTHOR-Element

Das **AUTHOR-Element** enthält den Namen des Autors einer Windows Medienmetadatei oder eines Medienclips.

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Element            |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **ENTRY** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element enthält eine Textzeichenfolge, die den Namen des Autors einer Medienmetadatei Windows Medienclips darstellt. Sie können das **AUTHOR-Element** innerhalb des **ASX-Elements** und in **ENTRY-Elementen** verwenden.

Wenn dieses Element im **ASX-Element angezeigt** wird, wird der Text als Informationen **anzeigen** angezeigt.

Wenn dieses Element in einem **ENTRY-Element angezeigt** wird, wird der Text als Clipautor angezeigt.

Jedes übergeordnete **ASX-** **und ENTRY-Element** sollte mindestens ein untergeordnetes **AUTHOR-Element** enthalten. Mehrere **AUTHOR-Elemente** nach dem ersten werden ignoriert und nicht angezeigt.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
   <AUTHOR>Neal S.</AUTHOR>   <!-- Show author -->
   <ENTRY>
      <REF HREF="mms://example.microsoft.com/clip1.asf" />
      <AUTHOR>Robert P.</AUTHOR>  <!-- Clip author -->
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

 

 





