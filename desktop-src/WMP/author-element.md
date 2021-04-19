---
title: Author-Element
description: Das Author-Element enthält den Namen des Autors einer Windows Media-Metadatei oder eines Medienclips.
ms.assetid: d80aad3d-4471-4310-8d43-2733ed83103c
keywords:
- Fenster "Author Element Windows Media Player"
topic_type:
- apiref
api_name:
- AUTHOR Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d20498ebd7c8a56edc2e32bc2e76422c9b22242
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357954"
---
# <a name="author-element"></a>Author-Element

Das **Author** -Element enthält den Namen des Autors einer Windows Media-Metadatei oder eines Medienclips.

``` syntax
<AUTHOR>   
   text string
</AUTHOR>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Element            |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element enthält eine Text Zeichenfolge, die den Namen des Autors einer Windows Media-Metadatei oder eines Medienclips darstellt. Sie können das **Author** -Element innerhalb des **ASX** -Elements und innerhalb der **Entry** -Elemente verwenden.

Wenn dieses Element im Element " **ASX** " angezeigt wird, wird der Text als "Informationen **anzeigen** " angezeigt.

Wenn dieses Element in einem **Entry** -Element angezeigt wird, wird der Text als Clip-Autor angezeigt.

Jedes über **geordnete-** und- **Entry** -Element muss höchstens ein untergeordnetes **Author** -Element enthalten. Mehrere **Autoren** Elemente nach dem ersten werden ignoriert und werden nicht angezeigt.

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
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





