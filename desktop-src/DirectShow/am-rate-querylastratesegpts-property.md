---
description: Diese Eigenschaft fragt den Decoder unabhängig von seiner Position in der Rate-Change-Warteschlange nach der Startzeit der Änderungsrate ab, die zuletzt in die Warteschlange gestellt wurde.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34e7b54e618829d9768b4d08a0a76defcf2c91758be6b916b6e570b368191e89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824834"
---
# <a name="am_rate_querylastratesegpts-property"></a>AM \_ RATE \_ QueryLastRateSegPTS-Eigenschaft

Diese Eigenschaft fragt den Decoder unabhängig von seiner Position in der Rate-Change-Warteschlange nach der Startzeit der Änderungsrate ab, die zuletzt in die Warteschlange gestellt wurde.

Diese Eigenschaft wird für Version 1.1 dieses Eigenschaftensets definiert. siehe [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Bezeichnung | Wert |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange |
| Eigenschafts-ID       | AM \_ RATE \_ QueryLastRateSegPTS |
| Datentyp         | **\_REFERENZZEIT**           |



 

## <a name="remarks"></a>Hinweise

Der Quellfilter kann diese Eigenschaft verwenden, um Änderungsraten über mehrere Audio- und Videostreams hinweg zu synchronisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Rate Change Property Set**](rate-change-property-set.md)
</dt> </dl>

 

 




