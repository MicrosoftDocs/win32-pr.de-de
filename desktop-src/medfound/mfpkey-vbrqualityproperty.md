---
description: Gibt den tatsächlichen Qualitätsgrad für die qualitätsbasierte Codierung (1-Pass) variabler Bitrate (VBR) an.
ms.assetid: e45d583a-323b-4394-9df3-949a3f713708
title: MFPKEY_VBRQUALITY-Eigenschaft (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e95320d7306d9167f2f4e433f0661ef3c895646c6a36aab7ffeaff26d2afbf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119343990"
---
# <a name="mfpkey_vbrquality-property"></a>MFPKEY \_ VBRQUALITY-Eigenschaft

Gibt den tatsächlichen Qualitätsgrad für die qualitätsbasierte Codierung (1-Pass) variabler Bitrate (VBR) an.

## <a name="constant-for-ipropertybag"></a>Konstante für IPropertyBag

g \_ wszWMVCVBRQuality, g \_ wszWMCPAudioVBRQuality

## <a name="data-type"></a>Datentyp

VT \_ I4

## <a name="remarks"></a>Hinweise

Nicht alle Werte im Bereich haben eine eindeutige Bedeutung. Die Werte, die einen Qualitätsschritt gegenüber der vorherigen Ebene darstellen, sind: 1, 4, 8, 11, 15, 18, 22, 25, 29, 33, 36, 40, 43, 47, 50, 54, 58, 61, 65, 68, 72, 75, 79, 83, 86, 90, 93, 97 und 100.

Bei Audioencoderobjekten werden die Qualitätsmodi in der [**WAVEFORMATEX-Struktur**](/previous-versions/dd757713(v=vs.85)) der Ausgabetypen bereitgestellt, die Sie mit [**IMediaObject::GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)abrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                    |
| Header<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Aufzählen von Audiotypen für bestimmte Codierungsmodi](enumeratingaudiotypesforspecificencodingmodes.md)
</dt> <dt>

[Media Foundation-Eigenschaften](media-foundation-properties.md)
</dt> </dl>

 

 
