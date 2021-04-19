---
title: ENTRYREF-Element
description: Das ENTRYREF-Element verweist auf die Eintrags Elemente in einer externen Metadatei.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- Fenster "ENTRYREF-Element" Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 520a4262baf17badb136b55e7b2e216bf89d7edf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369570"
---
# <a name="entryref-element"></a>ENTRYREF-Element

Das **ENTRYREF** -Element verweist auf die **Eintrags** Elemente in einer externen Metadatei.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attribute

**Href** (erforderlich)

URL zu einer Metadatei, auf die verwiesen wird.

**Clientbind**

Dieses Attribut wird nicht mehr unterstützt.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                       |
|-----------------|--------------------------------|
| Übergeordnete Elemente | **ASX**, **Ereignis**, **Wiederholung** |
| Untergeordnete Elemente  | Keine                           |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element verweist auf den Inhalt einer externen Metadatendatei. Windows Media Player verarbeitet die **Einstiegs** Elemente der Metadatei, auf die verwiesen wird, als wären Sie in der primären Metadatendatei an der Position des **ENTRYREF** -Elements enthalten. Allerdings werden alle **Eingabe** Elemente in der Metadatei, auf die verwiesen wird, ausgelassen, deren **skipifref** -Attribut auf "yes" festgelegt ist.

In Windows Media Player 7,0, 7,1 und Windows Media Player für Windows XP werden alle **ENTRYREF** -Elemente in der Metadatei ignoriert, auf die verwiesen wird. Folglich können Metadateien nur eine Ebene tief verschachtelt werden, wenn diese Versionen des Players verwendet werden. Windows Media Player ignoriert auch das Element " **ASX** " in der Datei, auf die verwiesen wird, sowie die zugehörigen Attribute. Windows Media Player 9 oder höher unterstützt das Schachteln von Metadateien mit einer Tiefe von bis zu fünf Ebenen.

Die im **href** -Attribut angegebene URL wird zur Basis-URL für alle relativen URLs in der externen Metadatendatei. Diese URL wird verwendet, wenn ein Eintrag aus der externen Metadatei abgespielt wird und der Benutzer Sie der Bibliothek hinzufügt.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
   <TITLE>Example of Using EntryRef</TITLE>
   <ENTRYREF HREF="https://sample.microsoft.com/metafile.asx" />
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

 

 





