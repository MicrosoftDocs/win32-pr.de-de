---
title: Startmarker-Element
description: Das Startmarker-Element gibt einen Marker an, aus dem Windows Media Player mit dem Rendern des Streams beginnt.
ms.assetid: b5c2422b-a59c-43f7-bac3-5722418192dc
keywords:
- Startmarker-Element, Windows Media Player
topic_type:
- apiref
api_name:
- STARTMARKER Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c3b3afbc3ab4a922d17f6a0269ed89c22f4dfeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370286"
---
# <a name="startmarker-element"></a>Startmarker-Element

Das **Startmarker** -Element gibt einen Marker an, aus dem Windows Media Player mit dem Rendern des Streams beginnt.

``` syntax
<STARTMARKER
   NUMBER = "marker number"
   NAME = "marker name"
/>
```

## <a name="attributes"></a>Attribute

**Einigen**

Die Nummer eines numerischen Markers im Index. Der Standardwert ist der Anfang von on-Demand-Inhalten oder die aktuelle Position in einem Echtzeitdaten Strom.

**NAME**

Der Name eines benannten Markers im Index. Der Standardwert ist der Anfang von on-Demand-Inhalten oder die aktuelle Position in einem Echtzeitdaten Strom.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente           |
|-----------------|--------------------|
| Übergeordnete Elemente | **Eintrag**, **ref** |
| Untergeordnete Elemente  | Keine               |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element gibt den Marker an, von dem Windows-Media Player das Rendern des Datenstroms beginnen soll, der im übergeordneten **Eintrag** oder **ref** -Element definiert ist.

**Hinweis**

Verwenden Sie dieses Element entweder mit dem **Number** -oder dem **Name** -Attribut, jedoch nicht mit beiden.

Ein in einem **ref** -Element definiertes **Startmarker** -Element hat Vorrang vor einem **Startmarker** -Element, das im übergeordneten **Entry** -Element des **ref** -Elements definiert ist. Ein **Startmarker** -Element hat auch Vorrang vor einem **StartTime** -Element.

Wenn der von einem **Startmarker** -Element angegebene Marker später im Stream als der von einem **endmarkerelement** definierte Marker auftritt, wird kein Inhalt wiedergegeben, aber es wird kein Fehler generiert.

## <a name="examples"></a>Beispiele


```XML
<STARTMARKER NUMBER="14" />
<STARTMARKER NAME="Marker_StartHere" />
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

 

 





