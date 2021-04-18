---
description: Gibt das Flag für die audioproduktionsinformationen in einem Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.
ms.assetid: 72f5f988-37c3-40d4-9c1c-07086e60ea51
title: Avencddproductioninfoist-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5069c8d30f0266b0727f735ede822be491c4a4a2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106344575"
---
# <a name="avencddproductioninfoexists-property"></a>Avencddproductioninfoist (Eigenschaft)

Gibt das Flag für die audioproduktionsinformationen in einem Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**Variant \_ bool** (**VT \_ bool**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencddproductioninfovorhanden**

## <a name="remarks"></a>Bemerkungen

Wenn der Wert **Variant \_ true** ist, sind die Einstellungen für die Mischungs Ebene und den Raum Typen gültig. Geben Sie diese Einstellungen mit den Eigenschaften " [**avencddproductionroomtype**](avencddproductionroomtype-property.md) " und " [**avencddproductionmixlevel**](avencddproductionmixlevel-property.md) " an.

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

 

 




