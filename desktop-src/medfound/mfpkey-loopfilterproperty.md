---
description: Gibt an, ob der Codec den Schleifen Filter für die Schleife während der Codierung verwenden soll.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: MFPKEY_LOOPFILTER-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fbb723c4145f9769cc157d5db8eb7893d89b389
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106355649"
---
# <a name="mfpkey_loopfilter-property"></a>Mfpkey \_ loopfilter (Eigenschaft)

Gibt an, ob der Codec den Schleifen Filter für die Schleife während der Codierung verwenden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszwmvcloopfilter

## <a name="data-type"></a>Datentyp

VT \_ bool

## <a name="remarks"></a>Bemerkungen

Der Schleifen Filter ist eine Blockierungs Methode, die während der Codierung und Decodierung angewendet wird, um blockierende Artefakte bei der Codierungs Zeit ("in der Schleife") zu reduzieren, sodass zukünftige P-Frames und B-Frames Sie nicht weiterleiten.

Die Anwendung des Schleifen Filters wirkt sich darauf aus, dass die Ränder der Makroblöcke in den Ausgabevideo Frames weniger bemerkbar sind. Gleichzeitig kann das Bild in der Darstellung weicher werden.

Obwohl der Schleifen Filter in einigen Frames zu reduzierten Bilddetails führen kann, wird die Qualität des gesamten Videos merklich beeinträchtigt. Der größte Nachteil bei der Verwendung der Schleifen Filterung ist die zusätzliche Decodierung der Leistung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften von Media Foundation](media-foundation-properties.md)
</dt> </dl>

 

 




