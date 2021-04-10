---
description: Gibt den Raumtyp für einen Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.
ms.assetid: d19b6b9d-9606-48a8-ac8e-cdbf15588a8f
title: Avencddproductionroomtype-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc2eed0bb491fc982a5102507e5b55bf610880a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104125198"
---
# <a name="avencddproductionroomtype-property"></a>Avencddproductionroomtype (Eigenschaft)

Gibt den Raumtyp für einen Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencddproductionroomtype**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft ist ein Member der [**eavencddproductionroomtype**](/windows/win32/api/codecapi/ne-codecapi-eavencddproductionroomtype) -Enumeration.

## <a name="remarks"></a>Bemerkungen

Der *Raumtyp* bezieht sich auf die Größe des Raums, der während der Produktion verwendet wird. Wenn Sie diese Eigenschaft festlegen, legen Sie die Eigenschaft " [**avencddproductioninfoist**](avencddproductioninfoexists-property.md) " auf " **true**" fest.

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

 

