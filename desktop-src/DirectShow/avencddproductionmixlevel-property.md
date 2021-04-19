---
description: Gibt die Mischungs Ebene in Dezibel (DB) in einem Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.
ms.assetid: fcb16d02-af4f-4626-99ee-2831172e5280
title: Avencddproductionmixlevel-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8a1726db6ab4841b4603a61bcfe39504742db42
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106346003"
---
# <a name="avencddproductionmixlevel-property"></a>Avencddproductionmixlevel (Eigenschaft)

Gibt die Mischungs Ebene in Dezibel (DB) in einem Dolby Digital-Audiodatenstrom an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UInt32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**Codecapi \_ avencddproductionmixlevel**

## <a name="property-value"></a>Eigenschaftswert

Diese Eigenschaft verfügt über einen linearen Wertebereich. Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).

## <a name="remarks"></a>Bemerkungen

Wenn Sie diese Eigenschaft festlegen, legen Sie die Eigenschaft " [**avencddproductioninfoist**](avencddproductioninfoexists-property.md) " auf " **true**" fest.

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

 

 




