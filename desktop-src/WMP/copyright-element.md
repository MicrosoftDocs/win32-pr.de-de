---
title: Copyright-Element (msfeeds. h)
description: Das Copyright-Element definiert eine Text Zeichenfolge, die die Copyright Informationen für ein ASX-oder Entry-Element angibt.
ms.assetid: 264b92de-b10c-41b9-b219-727879079f15
keywords:
- Copyright Element-Fenster Media Player
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
ms.openlocfilehash: 83b757528cfb14a01854346854a342ee9faced65
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358640"
---
# <a name="copyright-element"></a>Copyright-Element

Das **Copyright** -Element definiert eine Text Zeichenfolge, die die Copyright Informationen für ein **ASX** -oder **Entry** -Element angibt.

``` syntax
<COPYRIGHT>
    text string
</COPYRIGHT>
```

## <a name="attributes"></a>Attribute

Dieses Element weist keine Attribute auf.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert eine Text Zeichenfolge, die die Copyright Informationen für ein **ASX** -oder **Entry** -Element angibt.

Wenn dieses Element in einem **ASX** -Element angezeigt wird, wird die Copyright Zeichenfolge nur als **Anzeige** Informationen angezeigt. Wenn dieses Element in einem **Entry** -Element angezeigt wird, wird der Text als Clip Informationen angezeigt. Jedes über **geordnete-** und- **Entry** -Element muss höchstens ein untergeordnetes **Copyright** Element enthalten. Mehrere **Copyright** Elemente nach dem ersten werden ignoriert und werden nicht angezeigt.

Die Zeichen für Copyright-und Marken Registrierungs Symbole (oder) werden möglicherweise nicht ordnungsgemäß angezeigt, wenn die Metadatei nicht mit dem UTF-8-Codierungsschema codiert ist. Wenn Sie in diesem Fall eines dieser Symbole für alle Benutzer ordnungsgemäß anzeigen möchten, können Sie stattdessen die ASCII-Entsprechungen (c) und (R) verwenden.

Wenn die Metadatendatei mit UTF-8 codiert wird, werden Copyright-und Marken Symbole ordnungsgemäß angezeigt.

## <a name="examples"></a>Beispiele


```XML
<COPYRIGHT>Copyright (c) 1998, Microsoft Corporation</COPYRIGHT>

```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------|
| Version<br/> | Windows Media Player, Version 7,0 oder höher<br/>                                 |
| Header<br/>  | <dl> <dt>Msfeeds. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Hinzufügen von Copyright Zeichen zu Metafiles**](adding-copyright-characters-to-metafiles.md)
</dt> <dt>

[**Verweis auf Windows Media-Metadateielemente**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Referenz zu Windows Media-Metadateien**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





