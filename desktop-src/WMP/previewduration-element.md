---
title: Previewduration-Element
description: Das previewduration-Element definiert die Zeitspanne, während der ein Clip im Vorschaumodus abgespielt wird.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- Previewduration-Element, Windows Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a944e86a4bd82bf57961d4d6b474c34afadba6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364618"
---
# <a name="previewduration-element"></a>Previewduration-Element

Das **previewduration** -Element definiert die Zeitspanne, während der ein Clip im Vorschaumodus abgespielt wird.

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attribute

**Wert** (erforderlich)

Zeitspanne (in Stunden, Minuten, Sekunden und Hundertstel Sekunden), die der Clip im Vorschaumodus abspielt.

## <a name="parentchild-elements"></a>Über-/unterordnungselemente



| Hierarchy       | Elemente                    |
|-----------------|-----------------------------|
| Übergeordnete Elemente | **ASX**, **Eintrag**, **ref** |
| Untergeordnete Elemente  | Keine                        |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert die Zeitspanne, in der ein Clip im Vorschaumodus abgespielt wird. Wenn dieses Element in einem **Entry** -Element oder einem **ref** -Element angezeigt wird, gilt es für den Clip, der durch dieses Element definiert wird. Wenn Sie im Gültigkeitsbereich eines **ASX** -Elements angezeigt wird, gilt sie für jeden Clip in der Metadatei. Ein **previewduration** -Element in einem **ref** - **Element hat Vorrang** vor einem Element in einem Entry-Element und hat entweder Vorrang vor einem **previewduration** -Element in einem **ASX** -Element. Wenn kein **previewduration** -Element für einen Clip definiert ist, beträgt die Standard Vorschau Zeit 10 Sekunden.

Wenn ein **StartTime** -oder **Startmarker** -Element für den Clip vorhanden ist, rendert Windows Media Player den Clip, beginnend an dem Punkt, der von einem dieser Elemente definiert wurde. Andernfalls wird Sie am Anfang des Clips gerendert. Der Clip wird normal beendet, wenn er kürzer ist als die Zeit, die vom **previewduration** -Element definiert wurde.

Das **Duration** -Element überschreibt ein **previewduration** -Element.

## <a name="examples"></a>Beispiele


```XML
<PREVIEWDURATION VALUE="0:30.0" />
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

 

 





