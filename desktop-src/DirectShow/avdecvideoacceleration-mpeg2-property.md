---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für MPEG-2-Video Decodierung.
ms.assetid: 2e05f9e5-28a6-48f3-956d-a14eaf3bf4ba
title: AVDecVideoAcceleration_MPEG2-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d943459ae3810e1a0dc668c1f11c4c5d2354afaf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103747249"
---
# <a name="avdecvideoacceleration_mpeg2-property"></a>Avdecvideoacceleration- \_ Eigenschaft (Eigenschaft)

Aktiviert oder deaktiviert die Hardwarebeschleunigung für MPEG-2-Video Decodierung.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideoacceleration \_ MPEG2**

## <a name="remarks"></a>Bemerkungen

Wenn der Wert 0 (null) ist, verwendet der Decoder keine DirectX-Videobeschleunigung (DXVA) für die MPEG-2-Video Decodierung. Legen Sie diese Eigenschaft für DirectShow-Filter fest, bevor die Ausgabe-PIN des Decoders verbunden ist.

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

 

 




