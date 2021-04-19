---
title: Endmarker-Element
description: Das Endmarker-Element gibt einen Marker an, bei dem Windows Media Player das Rendern des Streams beendet.
ms.assetid: 554f0612-1669-4da4-9c5f-cc8984ef897c
keywords:
- Endmarker-Element Fenster Media Player
topic_type:
- apiref
api_name:
- ENDMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94d00eae3681775476af9c3169134b636e2904c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367188"
---
# <a name="endmarker-element"></a>Endmarker-Element

Das **Endmarker** -Element gibt einen Marker an, bei dem Windows Media Player das Rendern des Streams beendet.

``` syntax
<ENDMARKER
   NUMBER = "marker number" |
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Attribute

**Einigen**

Die Nummer eines numerischen Markers im Index. Der Standardwert ist das Ende des Inhalts.

**NAME**

Der Name eines benannten Markers im Index. Der Standardwert ist das Ende des Inhalts.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **Eintrag**, **ref** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element gibt den Marker an, in dem Windows Media Player das Rendern des Datenstroms beendet, der im übergeordneten **Eintrag** oder **ref** -Element definiert ist.

Hinweis

Verwenden Sie das **Endmarker** -Element entweder mit dem **Number** -oder dem **Name** -Attribut, jedoch nicht mit beiden.

Im Vorschaumodus wird durch das Erreichen eines endmarkers die Vorschau beendet, auch wenn die vom **previewduration** -Element angegebene Zeit nicht verstrichen ist. Das **Endmarker** -Element hat auch Vorrang vor dem **Duration** -Element.

Ein in einem **ref** -Element definiertes **endmarkerelement** hat Vorrang vor einem **Endmarker** , der im übergeordneten **Entry** -Element des **ref** -Elements definiert ist.

Wenn der von einem **endmarkerelement** angegebene Marker vor dem durch ein **Startmarker** -Element definierten Marker auftritt, wird kein Inhalt abgespielt, es wird jedoch kein Fehler generiert.

## <a name="examples"></a>Beispiele


```XML
<ENDMARKER NUMBER="17" />
<ENDMARKER NAME="Marker_StopHere" />

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

 

 





