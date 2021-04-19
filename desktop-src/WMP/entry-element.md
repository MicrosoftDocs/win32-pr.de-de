---
title: Entry-Element
description: Das Entry-Element gibt eine Windows Media-Datei an, die als Clip dargestellt werden soll.
ms.assetid: 7fd16aff-2eed-4f95-92b3-b48a9d785e7c
keywords:
- Fenster "Entry Element Windows Media Player"
topic_type:
- apiref
api_name:
- ENTRY Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 13da18c72022c916f91bcffe7382f673ba3d4fa4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367187"
---
# <a name="entry-element"></a>Entry-Element

Das **Entry** -Element gibt eine Windows Media-Datei an, die als Clip dargestellt werden soll.

``` syntax
<ENTRY
   CLIENTSKIP = "YES" | "NO"
   SKIPIFREF = "YES" | "NO"
>
</ENTRY>
```

## <a name="attributes"></a>Attribute

**Clientskip**

Ein Wert, der angibt, ob der Benutzer den Clip vorwärts überspringen kann.

Die folgenden Werte sind möglich.



| Wert | BESCHREIBUNG                                   |
|-------|-----------------------------------------------|
| YES   | Standard. Der Benutzer kann den Clip vorwärts überspringen. |
| Nein    | Der Benutzer kann den Clip nicht überspringen.       |



 

**Skipifref**

Ein Wert, der angibt, ob Windows Media Player diesen Clip überspringen soll, wenn das **Entry** -Element durch die Verwendung eines **ENTRYREF** -Elements in einer zweiten Metadatendatei enthalten ist.

Die folgenden Werte sind möglich.



| Wert | BESCHREIBUNG                                                                                 |
|-------|---------------------------------------------------------------------------------------------|
| YES   | Windows Media Player ignoriert diesen Eintrag, wenn er über ein **ENTRYREF** -Element referenziert wird. |
| Nein    | Standard. Dieser Eintrag wird von Windows Media Player nicht ignoriert.                                   |



 

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                                                                                                                                                                                     |
|-----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Übergeordnete Elemente | **ASX**, **Ereignis**, **Wiederholung**                                                                                                                                                               |
| Untergeordnete Elemente  | **abstract**, **Author**, **Banner**, **Base**, **Copyright**, **Duration**, **Endmarker**, **moreinfo**, **param**, **previewduration**, **ref**, **Startmarker**, **StartTime**, **Title** |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element ist das grundlegende Konstrukt in einer Windows Media-Metadatei. Das **Entry** -Element und die zugehörigen Attribute definieren Meta-Informationen für ein einzelnes, logisches Inhalts Element, das als Clip bezeichnet wird. Untergeordnete Elemente im Bereich eines **Eintrags** Elements definieren Medieninhalte für Windows-Media Player geöffnet (**ref**), Informationen zu dem Clip, den Windows Media Player als Text (**Autor**, **Copyright**, **Titel**) und andere Einstellungen im Zusammenhang mit dem Clip anzeigen wird. Das untergeordnete **ref** -Element verknüpft den Inhalt, der für das übergeordnete **Entry** -Element gestreamt werden soll. Obwohl das Skript nicht unterbricht, ist der **Eintrag** ohne untergeordnetes  Verweis bedeutungslos.

Wenn der Wert des **clientskip** -Attributs "No" ist, kann der Benutzer den Inhalt nicht überspringen, der durch das **Entry** -Element definiert ist. Dies funktioniert nicht, wenn das untergeordnete **ref** -Element auf eine andere Metadatei verweist. Auf die auf die netsted-Metadateien sollte mithilfe des **ENTRYREF** -Elements verwiesen werden.

Das **skipifref** -Attribut bezieht sich nur auf **Einstiegs** Elemente, die in einer zweiten Metadatendatei durch die Verwendung eines **ENTRYREF** -Elements enthalten sind. Das **ENTRYREF** -Element verweist auf eine andere Metadatendatei für die logische Einbindung in die aktuelle Datei. Wenn der Wert des **skipifref** -Attributs für ein **Entry** -Element aus der Metadatendatei, auf die verwiesen wird, auf "yes" gesetzt ist, ignoriert Windows Media Player diesen gezogenen Eintrag und wechselt zum nächsten **Entry** -Element, sofern vorhanden. Das nächste **Einstiegs** Element kann der nächste Eintrag in der ursprünglichen Datei oder der nächste Eintrag in der Metadatei sein, auf die im **ENTRYREF** -Element verwiesen wird.

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
| Version<br/> | Windows Media Player, Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





