---
description: Gibt an, ob der Ausgabestream so strukturiert werden soll, dass der codierte Stream eine niedrige Decodierungslatenz aufgibt.
ms.assetid: a000a2d4-afcf-4b88-9bbc-f42758744de2
title: AVEncCommonLowLatency-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b53c4b0122e595c930828f400600fc22b5a03977a781adab0e3a2f42b1048ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119690230"
---
# <a name="avenccommonlowlatency-property"></a>AVEncCommonLowLatency (Eigenschaft)

Gibt an, ob der Ausgabestream so strukturiert werden soll, dass der codierte Stream eine niedrige Decodierungslatenz aufgibt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonLowLatency**

## <a name="remarks"></a>Hinweise

Die Decodierungslatenz wird als die Datenmenge definiert, die der Decoder puffern muss. Wenn Sie diese Eigenschaft beispielsweise auf **VARIANT \_ TRUE für** einen MPEG-Videoencoder festlegen, werden die Typen von GOP-Strukturen, die der Encoder verwenden kann, beschränkt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




