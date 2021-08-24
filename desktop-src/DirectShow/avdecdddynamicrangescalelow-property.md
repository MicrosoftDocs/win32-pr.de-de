---
description: Gibt die Verstärkung auf niedriger Ebene an, wenn der Decoder eine dynamische Bereichssteuerung für einen Dolby AC-3-Audiostream ausführt.
ms.assetid: d723c825-f2f1-4ba0-a667-8285009764fd
title: AVDecDDDynamicRangeScaleLow-Eigenschaft (Codecapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91773eb20f3d0714223877acba4f26b01503202fc87f9f7b97dcde60ab99512e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119586740"
---
# <a name="avdecdddynamicrangescalelow-property"></a>AVDecDDDynamicRangeScaleLow (Eigenschaft)

Gibt die Verstärkung auf niedriger Ebene an, wenn der Decoder eine dynamische Bereichssteuerung für einen Dolby AC-3-Audiostream ausführt.

Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.

## <a name="data-type"></a>Datentyp

**UINT32** (**VT \_ UI4**)

## <a name="property-guid"></a>Eigenschaften-GUID

**CODECAPI \_ AVDecDDDynamicRangeScaleLow**

## <a name="property-value"></a>Eigenschaftswert

Der Wert dieser Eigenschaft hat den folgenden Bereich.



| Wert | Beschreibung                                                    |
|-------|----------------------------------------------------------------|
| 0     | Keine dynamische Bereichskomprimierung. Behalten Sie den vollständigen dynamischen Bereich bei. |
| 100   | Anwenden der vollständigen dynamischen Bereichskomprimierung.                          |



 

## <a name="remarks"></a>Hinweise

Diese Eigenschaft gilt nur, wenn der Wert der [**AVDecDDOperationalMode-Eigenschaft**](avdecddoperationalmode-property.md) eAVDecDDOperationalMode \_ LINE ist.

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

 

 




