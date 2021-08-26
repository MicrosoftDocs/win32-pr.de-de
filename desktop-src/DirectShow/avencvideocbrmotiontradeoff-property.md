---
description: Gibt den Kompromiss zwischen Bewegungs- und Stillbildern an. Diese Eigenschaft gilt nur für den Steuerungsmodus mit konstanter Bitrate (CONSTANT Bit Rate, CBR).
ms.assetid: e657e971-4624-4c87-ad51-6bf0cd1f9246
title: AVEncVideoCBRMotionMotionMotionoff-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 21d3db1f310de6468b57d469fbf699919ab86429e7242344622ca498b9e59f39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057940"
---
# <a name="avencvideocbrmotiontradeoff-property"></a>AVEncVideoCBRMotionMotionMotionoff (Eigenschaft)

Gibt den Kompromiss zwischen Bewegungs- und Stillbildern an. Diese Eigenschaft gilt nur für den Steuerungsmodus mit konstanter Bitrate (CONSTANT Bit Rate, CBR).

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncVideoCBRMotionMotionMotionoff**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert | BESCHREIBUNG               |
|-------|---------------------------|
| 0     | Optimieren für Still-Images |
| 100   | Optimieren sie für Bewegung.      |



 

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

 

 




