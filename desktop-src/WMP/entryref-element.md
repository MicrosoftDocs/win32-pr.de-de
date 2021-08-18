---
title: ENTRYREF-Element
description: Das ENTRYREF-Element zeigt auf die ENTRY-Elemente in einer externen Metadatei.
ms.assetid: ba39db39-fa90-455b-b278-ca866ce0b69c
keywords:
- ENTRYREF-Element Windows Media Player
topic_type:
- apiref
api_name:
- ENTRYREF Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 61fa3403fc56c6a02f97330b3c2f62d1c3e3c723f50672520ea42fb4a2018705
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118996669"
---
# <a name="entryref-element"></a>ENTRYREF-Element

Das **ENTRYREF-Element** zeigt auf die **ENTRY-Elemente** in einer externen Metadatei.

``` syntax
<ENTRYREF
   HREF = "URL"
/>
```

## <a name="attributes"></a>Attribute

**HREF** (erforderlich)

URL zu einer Metadatei, auf die verwiesen wird.

**CLIENTBIND**

Dieses Attribut wird nicht mehr unterstützt.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente                       |
|-----------------|--------------------------------|
| Übergeordnete Elemente | **ASX**, **EVENT**, **REPEAT** |
| Untergeordnete Elemente  | Keine                           |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element verweist auf den Inhalt einer externen Metadatei. Windows Media Player verarbeitet die **ENTRY-Elemente** der Metadatei, auf die verwiesen wird, als ob sie in der primären Metadatei an der Position des **ENTRYREF-Elements enthalten** sind. Allerdings werden alle **ENTRY-Elemente** in der Metadatei, auf die verwiesen wird, übersprungen, für die das **SKIPIFREF-Attribut** auf YES festgelegt ist.

Windows Media Player 7.0, 7.1 und Windows Media Player für Windows XP ignorieren alle **ENTRYREF-Elemente** in der Metadatei, auf die verwiesen wird. Daher können Metadateien nur eine Ebene tief geschachtelt werden, wenn diese Versionen des Players verwendet werden. Windows Media Player ignoriert auch das **ASX-Element** in der Datei, auf die verwiesen wird, zusammen mit seinen Attributen. Windows Media Player 9-Serie oder höher unterstützt das Schachteln von Metadateien mit einer Tiefe von bis zu fünf Ebenen.

Die im **HREF-Attribut angegebene URL** wird zur Basis-URL für alle relativen URLs in der externen Metadatei. Diese URL wird verwendet, wenn ein Eintrag aus der externen Metadatei abspielt und der Benutzer ihn der Bibliothek hinzufügt.

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
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zur Medienmetadatei**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





