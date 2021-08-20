---
description: Gibt an, ob der Codec den In-Loop-Deblockierungsfilter während der Codierung verwenden soll.
ms.assetid: 395a356a-5f58-46b4-b2ff-47f98106f487
title: MFPKEY_LOOPFILTER-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd157f6f473a40107d4a9a0958407795762df555946f08c030cc4f9ce4f36417
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117689897"
---
# <a name="mfpkey_loopfilter-property"></a>MFPKEY \_ LOOPFILTER-Eigenschaft

Gibt an, ob der Codec den In-Loop-Deblockierungsfilter während der Codierung verwenden soll.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCLoopFilter

## <a name="data-type"></a>Datentyp

VT \_ BOOL

## <a name="remarks"></a>Hinweise

Der In-Loop-Filter ist eine Deblockierungsmethode, die sowohl beim Codieren als auch beim Decodieren angewendet wird, um blockierende Artefakte zur Codierungszeit ("in der Schleife") zu reduzieren, damit zukünftige P- und B-Frames sie nicht weiter tragen.

Das Anwenden des In-Loop-Filters hat zur Folge, dass die Ränder der Makroblöcke in den Ausgabevideoframes weniger wahrnehmbar sind. Gleichzeitig kann das Bild in der Darstellung weicher werden.

Obwohl der In-Loop-Filter in einigen Frames zu reduzierten Bilddetails führen kann, profitiert die Videoqualität insgesamt erheblich. Der größte Nachteil bei der Verwendung der In-Loop-Filterung sind die zusätzlichen Kosten für die Decodierungsleistung.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                             |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 




