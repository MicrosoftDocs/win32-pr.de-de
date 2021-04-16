---
description: 'Weitere Informationen finden Sie hier: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524080"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>Pkey \_ audioendpoint \_ physicalspeakers

Die Eigenschaft " **pkey \_ audioendpoint \_ physicalspeakers** " gibt die Kanal konfigurationsmaske für das audioendpunktgerät an. Die Maske gibt die physische Konfiguration eines Satzes von Referenten an und gibt die Zuweisung von Kanälen zu Referenten an. Weitere Informationen zu kanalkonfigurationsmasken finden Sie hier:

1.  Die Beschreibung der Eigenschaft "ksproperty \_ \_ AudioChannel \_ config" in der Windows-DDK-Dokumentation.
2.  Das Whitepaper "audiotreiberunterstützung für Home-Theater-Sprecher-Konfigurationen" auf der Website " [audiogerätetechnologien für Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) ".

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ UI4 festgelegt.

Der **uintval** -Member der **PROPVARIANT** -Struktur enthält eine kanalkonfigurationsmaske, die in den **uint**-Typ umgewandelt wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Eigenschaften des audioendpunkts**](audio-endpoint-properties.md)
</dt> <dt>

[Kernaudioeigenschaften](core-audio-properties.md)
</dt> </dl>

 

 




