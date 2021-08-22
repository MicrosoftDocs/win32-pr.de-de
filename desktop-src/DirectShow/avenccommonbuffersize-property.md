---
description: Gibt die Größe des Puffers an, der während der Codierung verwendet wird. Diese Eigenschaft gilt nur für Codierungsmodi mit konstanter Bitrate (CBR) und variabler Bitrate (VBR).
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: AVEncCommonBufferSize-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69eb0c4829d30f3eff0297b7e591686f671d0d67967a65dc76695878d74b454e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794730"
---
# <a name="avenccommonbuffersize-property"></a>AVEncCommonBufferSize-Eigenschaft

Gibt die Größe des Puffers an, der während der Codierung verwendet wird. Diese Eigenschaft gilt nur für Codierungsmodi mit konstanter Bitrate (CBR) und variabler Bitrate (VBR).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonBufferSize**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Rufen Sie [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange)auf, um den unterstützten Bereich abzurufen. Parameterbereiche werden für H.264 UVC 1.5-Kameraencoder nicht unterstützt.

## <a name="remarks"></a>Hinweise

Bei einigen Videoformaten wird die Puffergröße in Bits und für andere in Bytes angegeben. Spezifische Informationen finden Sie in den hinweisen unten.

Für MPEG-Videos definiert diese Eigenschaft die Puffergröße der Videopufferüberprüfung (VBV). Die Größe des Puffers ist in Bits.

Für H.264-Video und Windows Media Video definiert die -Eigenschaft die Größe des hypothetischen Verweisdecoders (HRD). Die Größe des Puffers ist in Bytes.

Bei UVC 1.5 H264-Codierungskameras muss der an den Kameraencoder gesendete CPB-Wert 16-Bit ausgerichtet sein. Die Größe des Puffers ist in Bytes.

Diese Eigenschaft wird auch mit [H.264 UVC 1.5-Kameraencodern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.

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

 

