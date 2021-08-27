---
description: Gibt die Qualitätsstufe für die Codierung an.
ms.assetid: 2c7f3836-2392-47c6-9a56-d5a9b52560ff
title: AVEncCommonQuality-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99202391e919fa1da9028a15a57154834feddd3039160b9b0562a713fe59ddaa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087670"
---
# <a name="avenccommonquality-property"></a>AVEncCommonQuality-Eigenschaft

Gibt die Qualitätsstufe für die Codierung an.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVEncCommonQuality**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft weist den folgenden Bereich auf.



| Wert | BESCHREIBUNG                           |
|-------|---------------------------------------|
| 0     | Minimale Qualität, kleinere Ausgabegröße. |
| 100   | Maximale Qualität, größere Ausgabegröße.  |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft steuert die Qualitätsstufe, wenn der Encoder keine eingeschränkte Bitrate verwendet. Die [**AVEncCommonRateControlMode-Eigenschaft**](avenccommonratecontrolmode-property.md) bestimmt, ob die Bitrate eingeschränkt ist.

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

 

 




