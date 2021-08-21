---
description: Gibt das Zeitintervall an, für das die durchschnittliche Bitrate gilt. Diese Eigenschaft wird in Verbindung mit der AVEncCommonMeanBitRate-Eigenschaft verwendet.
ms.assetid: 3cf26f46-e8ac-448a-a031-800915cad1ef
title: AVEncCommonMeanBitRateInterval-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5cbd463ea67e281183dccde937f16978634e4103670b0e82b90b96139da5296
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118159795"
---
# <a name="avenccommonmeanbitrateinterval-property"></a>AVEncCommonMeanBitRateInterval-Eigenschaft

Gibt das Zeitintervall an, für das die durchschnittliche Bitrate gilt. Diese Eigenschaft wird in Verbindung mit der [**AVEncCommonMeanBitRate-Eigenschaft**](avenccommonmeanbitrate-property.md) verwendet.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT64** (**VT \_ UI8**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonMeanBitRateInterval**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Rufen Sie [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)auf, um den unterstützten Bereich abzurufen.

## <a name="remarks"></a>Hinweise

Bei der Codierung mit variabler Bitrate (VBR) mit zwei Durchlaufwerten gibt der Wert 0 (null) an, dass das Zeitintervall die gesamte Dauer des Inhalts ist. Bei der Codierung mit konstanter Bitrate (Single-Pass Constant Bit Rate, CBR) gibt der Wert 0 an, dass der Encoder das Intervall (in der Regel 0,5 Sekunden) auswählt.

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

 

 




