---
title: TITLE-Element (Metadatei)
description: Das TITLE-Element definiert eine Textzeichenfolge, die den Titel für ein ASX- oder ENTRY-Element angibt.
ms.assetid: d7ad7f00-fcf2-456d-a106-98bf0a258b81
keywords:
- TITLE-Element (Metadatei) Windows Media Player
topic_type:
- apiref
api_name:
- TITLE Element (metafile)
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 085bec9a9937c8dbd02fad6df785f4bce7afea90a74117e745f09cb5135633d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118117720"
---
# <a name="title-element-metafile"></a>TITLE-Element (Metadatei)

Das **TITLE-Element** definiert eine Textzeichenfolge, die den Titel für ein **ASX-** oder **ENTRY-Element** angibt.

``` syntax
<TITLE>
   text string
</TITLE>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **ENTRY** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert eine Textzeichenfolge, die den Titel eines **ASX-** oder **ENTRY-Elements** angibt. Der Titel wird im Anzeigebereich und im Dialogfeld **Eigenschaften** angezeigt.

Wenn dieses Element in einem **ASX-Element** angezeigt wird, wird der Text als Show information (Informationen **anzeigen)** angezeigt. Wenn dieses Element in einem **ENTRY-Element** angezeigt wird, wird der Text als **Clip-Informationen** angezeigt.

Wenn ein **MOREINFO-Element** auch mit dem zugeordneten (übergeordneten) Element verwendet wird, ist dies der Titeltext, auf den der Benutzer klickt, um auf die im **MOREINFO-Element** definierte URL zuzugreifen.

Jedes übergeordnete **ASX-** und **ENTRY-Element** sollte höchstens ein untergeordnetes **TITLE-Element** enthalten. Mehrere **TITLE-Elemente** nach dem ersten werden ignoriert und nicht angezeigt.

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
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





