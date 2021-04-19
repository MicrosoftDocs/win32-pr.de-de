---
description: Aktiviert oder deaktiviert die Hardwarebeschleunigung für das Decodieren von VC-1-Videos.
ms.assetid: eee85330-098e-4f21-81b7-a493abbd599b
title: AVDecVideoAcceleration_VC1-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1fcdbe265f5a65212a2846b724f570b024ea0ab8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343147"
---
# <a name="avdecvideoacceleration_vc1-property"></a>Avdecvideoacceleration \_ VC1 (Eigenschaft)

Aktiviert oder deaktiviert die Hardwarebeschleunigung für das Decodieren von VC-1-Videos.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avdecvideoacceleration \_ VC1**

## <a name="remarks"></a>Bemerkungen

Wenn der Wert 0 (null) ist, verwendet der Decoder keine DirectX-Videobeschleunigung (DXVA) für die Video Decodierung von VC-1. Legen Sie diese Eigenschaft für DirectShow-Filter fest, bevor die Ausgabe-PIN des Decoders verbunden ist.

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

 

 




