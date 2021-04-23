---
description: Diese Eigenschaft fragt den Decoder nach der Startzeit der Rateänderung ab, die zuletzt in die Warteschlange eingereiht wurde, unabhängig von ihrer Position in der Ratenänderungswarteschlange.
ms.assetid: 3c7006e7-48fd-4df8-b446-8ee2b024278b
title: AM_RATE_QueryLastRateSegPTS-Eigenschaft (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c6e3e00985ba6e714bf48d349fd5af5c9593b9
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910268"
---
# <a name="am_rate_querylastratesegpts-property"></a>AM \_ RATE \_ QueryLastRateSegPTS-Eigenschaft

Diese Eigenschaft fragt den Decoder nach der Startzeit der Rateänderung ab, die zuletzt in die Warteschlange eingereiht wurde, unabhängig von ihrer Position in der Ratenänderungswarteschlange.

Diese Eigenschaft ist für Version 1.1 dieses Eigenschaftensatzes definiert. siehe [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md).



| Bezeichnung | Wert |
|-------------------|-------------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ TSRateChange |
| Eigenschafts-ID       | AM \_ RATE \_ QueryLastRateSegPTS |
| Datentyp         | **\_REFERENZZEIT**           |



 

## <a name="remarks"></a>Bemerkungen

Der Quellfilter kann diese Eigenschaft verwenden, um Rateänderungen über mehrere Audio- und Videostreams hinweg zu synchronisieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ratenänderungseigenschaftensatz**](rate-change-property-set.md)
</dt> </dl>

 

 




