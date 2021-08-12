---
description: Aktiviert oder deaktiviert die Sprecherfüllung in einem Audiodecoder oder digital signal processor (DSP).
ms.assetid: 5a42d4c9-d593-4d7f-bfee-37271c48e5cf
title: AVDSPSpeakerFill-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9ff4886f1b6f1e6ae19f9f1b5bf78e20159df390f2d642ac2b9cb3c4c834d1bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118663431"
---
# <a name="avdspspeakerfill-property"></a>AVDSPSpeakerFill-Eigenschaft

Aktiviert oder deaktiviert die Sprecherfüllung in einem Audiodecoder oder digital signal processor (DSP).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDSPSpeakerFill**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVDSPSpeakerFill-Enumeration.**](/windows/desktop/api/codecapi/ne-codecapi-eavdspspeakerfill)

## <a name="remarks"></a>Hinweise

Die Sprecherfüllung ist ein DSP-Prozess, bei dem Mono- oder Stereoaudiodaten in Multichannel-Audio konvertiert werden.

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

 

 




