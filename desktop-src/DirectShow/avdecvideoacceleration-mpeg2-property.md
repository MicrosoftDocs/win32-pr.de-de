---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für die MPEG-2-Videodecodierung.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: AVDecVideoAcceleration_MPEG2 (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc2aa5db2d738afc0097ee4e09e7562dd7a3ae30b6138b2a003d85c6058fb22b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159953"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a>MPEG2-Eigenschaft "AVDecVideoAcceleration" \_

Aktiviert oder deaktiviert die Hardwarebeschleunigung für die MPEG-2-Videodecodierung.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoAcceleration \_ MPEG2**

## <a name="remarks"></a>Hinweise

Wenn der Wert 0 (null) ist, verwendet der Decoder keine DirectX-Videobeschleunigung (DXVA) für die MPEG-2-Videodecodierung. Legen Sie diese Eigenschaft für DirectShow-Filter fest, bevor der Ausgabepin des Decoders verbunden ist.

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

 

 




