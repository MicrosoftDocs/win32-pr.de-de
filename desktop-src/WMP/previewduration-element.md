---
title: PREVIEWDURATION-Element
description: Das PREVIEWDURATION-Element definiert die Zeitdauer, die ein Clip im Vorschaumodus abspielt.
ms.assetid: 428a4e3d-9c08-4b6c-acc7-b630aab37de3
keywords:
- PREVIEWDURATION-Element Windows Media Player
topic_type:
- apiref
api_name:
- PREVIEWDURATION Element
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dd01180b56816aa3458396f1c6183518d4365dce2f41643328e899057ed1ee72
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119862020"
---
# <a name="previewduration-element"></a>PREVIEWDURATION-Element

Das **PREVIEWDURATION-Element** definiert die Zeitdauer, die ein Clip im Vorschaumodus abspielt.

``` syntax
<PREVIEWDURATION
   VALUE = "hh:mm:ss.fract"
/>
```

## <a name="attributes"></a>Attribute

**VALUE** (erforderlich)

Die Dauer (in Stunden, Minuten, Sekunden und Hundertstelsekunden), die der Clip im Vorschaumodus abspielt.

## <a name="parentchild-elements"></a>Übergeordnete/untergeordnete Elemente



| Hierarchy       | Elemente                    |
|-----------------|-----------------------------|
| Übergeordnete Elemente | **ASX**, **ENTRY**, **REF** |
| Untergeordnete Elemente  | Keine                        |



 

## <a name="remarks"></a>Bemerkungen

Dieses Element definiert die Zeitdauer, die ein Clip im Vorschaumodus abspielt. Wenn dieses Element innerhalb eines **ENTRY-** oder **REF-Elements** angezeigt wird, gilt es für den Clip, der von diesem Element definiert wird. Wenn sie innerhalb des Bereichs eines **ASX-Elements** angezeigt wird, gilt sie für jeden Clip in der Metadatei. Ein **PREVIEWDURATION-Element** in einem **REF-Element** hat Vorrang vor einem in einem **ENTRY-Element** und hat entweder Vorrang vor einem **PREVIEWDURATION-Element** in einem **ASX-Element.** Wenn kein **PREVIEWDURATION-Element** für einen Clip definiert ist, beträgt die Standardvorschauzeit 10 Sekunden.

Wenn es ein **STARTTIME- oder** **STARTMARKER-Element** für den Clip gibt, rendert Windows Media Player den Clip beginnend mit dem Punkt, der von einem dieser Elemente definiert wird. Andernfalls wird sie vom Anfang des Clips gerendert. Der Clip wird normal beendet, wenn er kürzer als die vom **PREVIEWDURATION-Element definierte Zeit** ist.

Das **DURATION-Element** überschreibt ein **PREVIEWDURATION-Element.**

## <a name="examples"></a>Beispiele


```XML
<PREVIEWDURATION VALUE="0:30.0" />
```



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------|
| Version<br/> | Windows Media Player Version 70 oder höher<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Windows Referenz zu Medienmetadateielementen**](windows-media-metafile-elements-reference.md)
</dt> <dt>

[**Windows Referenz zur Medienmetadatei**](windows-media-metafile-reference.md)
</dt> </dl>

 

 





