---
description: Gibt die Größe des Puffers an, der während der Codierung verwendet wird. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.
ms.assetid: 3315785e-306f-44d6-ac39-796025a2da3a
title: Avenccommonbuffersize-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c677c483c320c9dceef391f45c5d8bf163eece0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125251"
---
# <a name="avenccommonbuffersize-property"></a>Avenccommonbuffersize (Eigenschaft)

Gibt die Größe des Puffers an, der während der Codierung verwendet wird. Diese Eigenschaft gilt nur für die Konstante Bitrate (CBR) und die Variablen Bitrate (VBR)-Codierungs Modi.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avenccommonbuffersize**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange). Parameter Bereiche werden für H. 264 UVC 1,5-Kamera Encoder nicht unterstützt.

## <a name="remarks"></a>Bemerkungen

Bei einigen Videoformaten wird die Puffergröße in Bits und für andere in Bytes angegeben. Informationen zu bestimmten Informationen finden Sie in den nachfolgenden hinweisen.

Bei MPEG-Videos definiert diese Eigenschaft die vbv-Puffergröße (Video Buffer Verifier). Die Größe des Puffers ist in Bits.

Bei H. 264-Videos und-Windows Media Video definiert die-Eigenschaft die Größe des hypothetischen Verweis Decoders (HRD). Die Größe des Puffers beträgt Byte.

Für UVC 1,5 H264 Encoding-Kameras muss der an den Kamera Encoder gesendete CPB-Wert 16-Bit-ausgerichtet sein. Die Größe des Puffers beträgt Byte.

Diese Eigenschaft wird auch mit [H. 264 UVC 1,5-Kamera Codierern](/windows/desktop/medfound/camera-encoder-h264-uvc-1-5)verwendet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]<br/>                     |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[ Desktop Apps \| UWP-apps\]<br/>                           |
| Header<br/>                   | <dl> <dt>Codecapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften der Codec-API](codec-api-properties.md)
</dt> <dt>

[**Icodecapi-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

