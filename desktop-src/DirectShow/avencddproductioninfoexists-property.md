---
description: Gibt das Audioproduktionsinformationsflag in einem Dolby Digital-Audiostream an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: AVEncDDProductionInfoExists-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d9d0341cf97b4641dc2ece7e93408e527458235620b32b7e25abe583a67c2ad
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103470"
---
# <a name="avencddproductioninfoexists-property"></a>AVEncDDProductionInfoExists-Eigenschaft

Gibt das Audioproduktionsinformationsflag in einem Dolby Digital-Audiostream an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**VARIANT \_ BOOL** (**VT \_ BOOL**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncDDProductionInfoExists**

## <a name="remarks"></a>Hinweise

Wenn der Wert **VARIANT \_ TRUE** ist, sind die Einstellungen für Die Mischungsebene und den Raumtyp gültig. Geben Sie diese Einstellungen mit den Eigenschaften [**AVEncDDProductionRoomType**](avencddproductionroomtype-property.md) und [**AVEncDDProductionMixLevel**](avencddproductionmixlevel-property.md) an.

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

 

 




