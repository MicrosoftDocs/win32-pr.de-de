---
title: REPEAT-Element
description: Das Repeat-Element definiert, wie oft Windows Media Player ein oder mehrere Entry-oder ENTRYREF-Elemente wiederholt.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- Windows-Element Media Player wiederholen
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: aff7d5eaa9594882b029f0b02f4888d93fff01d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371704"
---
# <a name="repeat-element"></a>REPEAT-Element

Das **Repeat** -Element definiert, wie oft Windows Media Player ein oder mehrere **Entry** -oder **ENTRYREF** -Elemente wiederholt.

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Attribute

**COUNT**

Eine ganze Zahl, die angibt, wie oft Windows Media Player den **Eintrag** und die **ENTRYREF** -Elemente innerhalb des Gültigkeits Bereichs dieses Elements wiederholt.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                |
|-----------------|-------------------------|
| Übergeordnete Elemente | **ASX**                 |
| Untergeordnete Elemente  | **Eintrag**, **ENTRYREF** |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert, wie oft Windows Media Player wiederholt oder durchläuft, die durch die **Entry** -und **ENTRYREF** -Elemente innerhalb des Gültigkeits Bereichs dieses Elements definierten Clips. Nur das erste **Wiederholungs** Element in einer Metadatei ist gültig. nachfolgende **Wiederholungs** Elemente werden ignoriert.

Wenn kein **count** -Attribut definiert ist, wiederholt der Inhalt im zugeordneten **Entry** -Element und im **ENTRYREF** -Element unendlich viele Male. Der Wert 0 (null) bewirkt, dass Windows Media Player das **Repeat** -Element ignoriert und den Inhalt einmal wieder gibt.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
   <ENTRY>
        <REF HREF="mms://example.microsoft.com/clip1.asf" />
<!-- This clip plays once. -->
   </ENTRY>

   <REPEAT COUNT="2">
      <ENTRY>
     <REF HREF="mms://example.microsoft.com/clip2.asf" />
     <REF HREF="mms://example.microsoft.com/clip3.asf" />
 <!-- These clips play twice. -->
      </ENTRY>
   </REPEAT>
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

 

 





