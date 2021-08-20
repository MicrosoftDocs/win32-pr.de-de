---
description: Gibt die maximale Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für Codierungsmodi mit konstanter Bitrate (CBR) und variabler Bitrate (VBR).
ms.assetid: 053fdad0-dc5f-4af1-84a6-bb7c0dac7e79
title: AVEncCommonMaxBitRate-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0981a8f3fea67fa6e3dc4564ef2d2777af130bc02079050e63f571d7199e626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159829"
---
# <a name="avenccommonmaxbitrate-property"></a>AVEncCommonMaxBitRate (Eigenschaft)

Gibt die maximale Bitrate in Bits pro Sekunde an. Diese Eigenschaft gilt nur für Codierungsmodi mit konstanter Bitrate (CBR) und variabler Bitrate (VBR).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonMaxBitRate**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich zu erhalten, rufen [**Sie ICodecAPI::GetParameterRange auf.**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)

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

 

 




