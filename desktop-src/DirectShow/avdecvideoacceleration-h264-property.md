---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für die H.264-Videodecodierung.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: AVDecVideoAcceleration_H264-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f84279c49e65586d07dbf1efa4c372a1b1f8770e19bd00eb827ba44b6ad43bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663964"
---
# <a name="avdecvideoacceleration_h264-property"></a>AVDecVideoAcceleration \_ H264-Eigenschaft

Aktiviert oder deaktiviert die Hardwarebeschleunigung für die H.264-Videodecodierung.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoAcceleration \_ H264**

## <a name="remarks"></a>Hinweise

Wenn der Wert 0 (null) ist, verwendet der Decoder keine DirectX Video Acceleration (DXVA) für die H.264-Videodecodierung. Legen Sie für DirectShow-Filter diese Eigenschaft fest, bevor der Ausgabepin des Decoders verbunden wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop-Apps \| UWP-Apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 \[ Server-Desktop-Apps \| UWP-Apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Codec-API-Eigenschaften](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




