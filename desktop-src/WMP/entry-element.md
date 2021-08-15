---
title: ENTRY-Element
description: Das ENTRY-Element gibt eine Windows Mediendatei an, die als Clip gerendert werden soll.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- ENTRY-Element Windows Media Player
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8c292c08903fb788a00db5c320e9c41d5cef2a8f6b0ced5f2b3d008a2f7a14e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117935225"
---
# <a name="entry-element"></a>ENTRY-Element

Das **ENTRY-Element** gibt eine Windows Mediendatei an, die als Clip gerendert werden soll.

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a>Attribute

**CLIENTSKIP**

Wert, der angibt, ob der Benutzer den Clip überspringen kann.

Die folgenden Werte sind möglich.



| Wert | BESCHREIBUNG                                   |
|-------|-----------------------------------------------|
| YES   | Standard. Der Benutzer kann den Clip überspringen. |
| Nein    | Der Benutzer kann den Clip nicht überspringen.       |



 

**SKIPIFREF**

Wert, der angibt, ob Windows Media Player diesen Clip überspringen soll, wenn das **ENTRY-Element** durch die Verwendung eines **ENTRYREF-Elements** in eine zweite Metadatei eingefügt wird.

Die folgenden Werte sind möglich.



| Wert | BESCHREIBUNG                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| YES   | Windows Media Player ignoriert diesen Eintrag, wenn über ein **ENTRYREF-Element** darauf verwiesen wird. |
| Nein    | Standard. Windows Media Player ignoriert diesen Eintrag nicht.                                   |



 

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente | **ASX**, **EVENT**, **REPEAT**                                                                                                                                                               |
| Untergeordnete Elemente  | **ABSTRACT**, **AUTHOR**, **BANNER**, **BASE**, **COPYRIGHT**, **DURATION**, **ENDMARKER**, **MOREINFO**, **PARAM**, **PREVIEWDURATION**, **REF**, **STARTMARKER**, **STARTTIME**, **TITLE** |



 

## <a name="remarks"></a>Hinweise

Dieses Element ist das grundlegende Konstrukt in einer Windows Media-Metadatei. Das **ENTRY-Element** und die zugehörigen Attribute definieren Metainformationen für einen einzelnen logischen Inhalt, der als Clip bezeichnet wird. Untergeordnete Elemente innerhalb des Bereichs eines **ENTRY-Elements** definieren Medieninhalte für Windows Media Player zum Öffnen **(REF),** Informationen über den Clip, der Windows Media Player als Text (**AUTHOR**, **COPYRIGHT**, **TITLE**) und andere Einstellungen im Zusammenhang mit dem Clip anzeigen. Das untergeordnete **REF-Element** verknüpft den Inhalt, der für das übergeordnete **ENTRY-Element** gestreamt werden soll. Obwohl das Skript nicht unterbricht, **ist** entry ohne **untergeordnete REF-Datei** bedeutungslos.

Wenn der Wert des **CLIENTSKIP-Attributs** NO ist, kann der Benutzer den Durch das **ENTRY-Element** definierten Inhalt nicht überspringen. Dies funktioniert nicht, wenn das untergeordnete **REF-Element** auf eine andere Metadatei verweist. Auf geschachtelte Metadateien sollte mithilfe des **ENTRYREF-Elements** verwiesen werden.

Das **SKIPIFREF-Attribut** bezieht sich nur auf **ENTRY-Elemente,** die durch die Verwendung eines **ENTRYREF-Elements** in einer zweiten Metadatei enthalten sind. Das **ENTRYREF-Element** verweist auf eine andere Metadatei für die logische Aufnahme in die aktuelle Datei. Wenn der Wert des **SKIPIFREF-Attributs** für ein **ENTRY-Element** aus der Metadatei, auf die verwiesen wird, YES lautet, ignoriert Windows Media Player diesen abgerufenen Eintrag und fährt ggf. mit dem nächsten **ENTRY-Element** fort. Das nächste **ENTRY-Element** kann der nächste Eintrag in der ursprünglichen Datei oder der nächste Eintrag in der Metadatei sein, auf die im **ENTRYREF-Element** verwiesen wird.

## <a name="examples"></a>Beispiele


```XML
<ASX VERSION="3.0">
   <TITLE>Example Windows Media Player Show</TITLE>
   
   <ENTRY>
      <TITLE>Example Clip</TITLE>
      <REF HREF="https://example.microsoft.com/media.asf" />
   </ENTRY>
   
   <ENTRY>
      <TITLE>Another Clip</TITLE>
      <REF HREF="https://example.microsoft.com/more_media.asf" />
   </ENTRY>
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

 

 





