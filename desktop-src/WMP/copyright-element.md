---
title: COPYRIGHT-Element (Msfeeds.h)
description: Das COPYRIGHT-Element definiert eine Textzeichenfolge, die die Copyrightinformationen für ein ASX- oder ENTRY-Element angibt.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- COPYRIGHT-Element Windows Media Player
topic_type:
- apiref
api_name:
- COPYRIGHT Element
api_location:
- msfeeds.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e5a01e97364aa47182e38e3e3066895c771e2d5edb6c480e8108cb168e7f8cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997460"
---
# <a name="copyright-element"></a>COPYRIGHT-Element

Das **COPYRIGHT-Element** definiert eine Textzeichenfolge, die die Copyrightinformationen für ein **ASX-** oder **ENTRY-Element** angibt.

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über- und untergeordnete Elemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **ENTRY** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert eine Textzeichenfolge, die die Copyrightinformationen für ein **ASX-** oder **ENTRY-Element** angibt.

Wenn dieses Element innerhalb eines **ASX-Elements** angezeigt wird, wird die Copyrightzeichenfolge nur als Show information **(Informationen anzeigen)** angezeigt. Wenn dieses Element in einem **ENTRY-Element angezeigt** wird, wird der Text als Clipinformationen angezeigt. Jedes übergeordnete **ASX-** **und ENTRY-Element** sollte mindestens ein untergeordnetes **COPYRIGHT-Element** enthalten. Mehrere **COPYRIGHT-Elemente** nach dem ersten werden ignoriert und nicht angezeigt.

Die Zeichen für Copyright- und Markenregistrierungssymbole ( oder ) werden möglicherweise nicht ordnungsgemäß angezeigt, wenn die Metadatei nicht mit dem UTF-8-Codierungsschema codiert ist. In diesem Fall können Sie die ASCII-Entsprechungen (c) und (R) verwenden, um eines dieser Symbole für alle Benutzer ordnungsgemäß anzuzeigen.

Wenn die Metadatei mit UTF-8 codiert wird, werden Copyright- und Markensymbole ordnungsgemäß angezeigt.

## <a name="examples"></a>Beispiele


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player Version 7.0 oder höher<br/>                                 |
| Header<br/>  | <dl> <dt>Msfeeds.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Copyrightzeichen zu Metadateien**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zur Medienmetadatei**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





