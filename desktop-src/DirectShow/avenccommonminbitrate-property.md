---
description: Gibt die minimale Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für die Codierungsmodi Constant Bit Rate (CBR) und Variable Bit Rate (VBR).
ms.assetid: 57ef6c08-3bad-4d8d-8daf-61041b878802
title: AVEncCommonMinBitRate-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 65488b3a855d4b664c96a1d7abfc1718a35e94c466877c68848a1acf25a3bfe4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159856"
---
# <a name="avenccommonminbitrate-property"></a>AVEncCommonMinBitRate (Eigenschaft)

Gibt die minimale Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für die Codierungsmodi Constant Bit Rate (CBR) und Variable Bit Rate (VBR).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonMinBitRate**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich zu erhalten, rufen [**Sie ICodecAPI::GetParameterRange auf.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)

## <a name="remarks"></a>Hinweise

Der Encoder erzwingt die minimale Bitrate, indem er die Codierungsqualität bei Bedarf erhöht.

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

 

 




