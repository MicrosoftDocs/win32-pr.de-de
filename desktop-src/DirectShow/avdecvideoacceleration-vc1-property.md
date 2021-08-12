---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für die VC-1-Videodecodierung.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: AVDecVideoAcceleration_VC1 -Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1767206fab479dbcae1dec5e768b21d768440a66776b1f41610b75be4190d6c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663839"
---
# <a name="avdecvideoacceleration_vc1-property"></a>AVDecVideoAcceleration \_ VC1-Eigenschaft

Aktiviert oder deaktiviert die Hardwarebeschleunigung für die VC-1-Videodecodierung.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecVideoAcceleration \_ VC1**

## <a name="remarks"></a>Hinweise

Wenn der Wert 0 (null) ist, verwendet der Decoder directX Video Acceleration (DXVA) nicht für die VC-1-Videodecodierung. Legen Sie für DirectShow-Filter diese Eigenschaft fest, bevor der Ausgabepin des Decoders verbunden wird.

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

 

 




