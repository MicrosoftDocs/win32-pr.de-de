---
description: Gibt den Ratensteuerungsmodus an.
ms.assetid: 4a0d49b1-30da-4ebe-abff-3fceef6dd94a
title: AVEncCommonRateControlMode-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8aaa914f445fcbc535ec423b41306938890d64b747258cb0159add5e4fd43c3f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794670"
---
# <a name="avenccommonratecontrolmode-property"></a>AVEncCommonRateControlMode-Eigenschaft

Gibt den Ratensteuerungsmodus an.

Anwendungen können diese Eigenschaft festlegen, um den Ratensteuerungsmodus anzugeben. Encoder können diese Eigenschaft auch als Funktion zurückgeben.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonRateControlMode**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eAVEncCommonRateControlMode-Enumeration.**](/windows/win32/api/codecapi/ne-codecapi-eavenccommonratecontrolmode)

## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird auch mit [H.264 UVC 1.5-Kameraencodern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.

[CODECAPI \_ AVEncVideoTemporalLayerCount,](/windows/desktop/medfound/codecapi-avencvideotemporallayercount) [CODECAPI \_ AVEncVideoUsage](/windows/desktop/medfound/codecapi-avencvideousage)und CODECAPI \_ AVEncCommonRateControlMode sind statische Encodereigenschaften. Nach dem Festlegen werden diese erst wirksam, nachdem ein festgelegter Medientyp auf dem Ausgabepin der Kamera aufgerufen wurde.

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

 

