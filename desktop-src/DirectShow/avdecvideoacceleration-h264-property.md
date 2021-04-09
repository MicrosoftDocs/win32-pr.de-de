---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für die H. 264-Video Decodierung.
ms.assetid: 3912136d-0fc1-49b0-bc79-0785d63041e6
title: AVDecVideoAcceleration_H264-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cbcedf2d038c010ee781030baf0a8289e68eab4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103860448"
---
# <a name="avdecvideoacceleration_h264-property"></a>Avdecvideoacceleration \_ H264 Property

Aktiviert oder deaktiviert die Hardwarebeschleunigung für die H. 264-Video Decodierung.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideoacceleration \_ H264**

## <a name="remarks"></a>Bemerkungen

Wenn der Wert 0 (null) ist, verwendet der Decoder keine DirectX-Videobeschleunigung (DXVA) für die H. 264-Video Decodierung. Legen Sie diese Eigenschaft für DirectShow-Filter fest, bevor die Ausgabe-PIN des Decoders verbunden ist.

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

 

 




