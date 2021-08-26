---
title: REPEAT-Element
description: Das REPEAT-Element definiert, wie oft Windows Media Player mindestens ein ENTRY- oder ENTRYREF-Element wiederholt.
ms.assetid: 1a825f2b-29a7-4180-93df-51b3b5dd14e5
keywords:
- REPEAT-Element Windows Media Player
topic_type:
- apiref
api_name:
- REPEAT Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 330eda0757acb29b48ed10636d8f479b6ebb1395d088020876c717a78f41ae6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002540"
---
# <a name="repeat-element"></a>REPEAT-Element

Das **REPEAT-Element** definiert, wie oft Windows Media Player mindestens ein **ENTRY-** oder **ENTRYREF-Element** wiederholt.

``` syntax
<REPEAT   
   COUNT = "integer"
>
</REPEAT>
```

## <a name="attributes"></a>Attribute

**COUNT**

Ganze Zahl, die angibt, wie oft Windows Media Player die **Elemente ENTRY** und **ENTRYREF** innerhalb des Bereichs dieses Elements wiederholt.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente                |
|-----------------|-------------------------|
| Übergeordnete Elemente | **Asx**                 |
| Untergeordnete Elemente  | **ENTRY**, **ENTRYREF** |



 

## <a name="remarks"></a>Hinweise

Dieses Element definiert die Anzahl der Wiederholungen Windows Media Player oder durchläuft die Clips, die durch die **ENTRY-** und **ENTRYREF-Elemente** innerhalb des Bereichs dieses Elements definiert werden. Nur das erste **REPEAT-Element** in einer Metadatei ist gültig. nachfolgende **REPEAT-Elemente** werden ignoriert.

Wenn kein **COUNT-Attribut** definiert ist, wiederholt sich der Inhalt in den zugeordneten **ENTRY-** und **ENTRYREF-Elementen** unendlich oft. Der Wert 0 führt dazu, dass Windows Media Player das **REPEAT-Element** ignoriert und den Inhalt einmal wiedergeben.

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
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





