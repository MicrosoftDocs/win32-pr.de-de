---
description: Die pkey \_ audioendpoint \_ fullrangespeakers-Eigenschaft gibt die Kanal konfigurationsmaske für die vollständig gültigen Referenten an, die mit dem audioendpunktgerät verbunden sind.
ms.assetid: c0a54b3d-84dc-4771-8891-167ce00e2218
title: PKEY_AudioEndpoint_FullRangeSpeakers (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0990d08e3d78eddf0fa6397e888b1e26c9f9a767
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127441"
---
# <a name="pkey_audioendpoint_fullrangespeakers"></a>Pkey- \_ audioendpoint \_ fullrangespeakers

Die **pkey \_ audioendpoint \_ fullrangespeakers** -Eigenschaft gibt die Kanal konfigurationsmaske für die vollständig gültigen Referenten an, die mit dem audioendpunktgerät verbunden sind. Die Maske gibt die physische Konfiguration der vollständigen Referenten an und gibt die Zuweisung von Kanälen zu diesen Referenten an.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ UI4 festgelegt.

Der **uintval** -Member der **PROPVARIANT** -Struktur enthält eine kanalkonfigurationsmaske, die in den **uint**-Typ umgewandelt wird.

Ein Volltext-Redner ist in der Lage, Sounds über den vollen Bereich von Bass bis Treble zu spielen. In der Regel sind größere Redner in vollem Umfang, aber kleinere Redner sind deutlich weniger in der Lage, Bass Sounds wiedergeben zu können. In Windows Vista verwendet die Audioengine diese Eigenschaft zum Verwalten von Bass Ebenen im audioausgabestream, der vom audioendpunktgerät wiedergegeben wird.

Die Kanal konfigurationsmaske für diese Eigenschaft hat das gleiche Format wie die channelkonfigurationsmaske für die [**pkey \_ audioendpoint \_ physicalspeakers**](pkey-audioendpoint-physicalspeakers.md) -Eigenschaft. Weitere Informationen zu kanalkonfigurationsmasken finden Sie hier:

-   Die Beschreibung der Eigenschaft "ksproperty \_ \_ AudioChannel \_ config" in der Windows-DDK-Dokumentation.
-   Das Whitepaper "audiotreiberunterstützung für Home-Theater-Sprecher-Konfigurationen" auf der Website " [audiogerätetechnologien für Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) ".

Das System ruft die Kanal konfigurationsmaske für die pkey \_ audioendpoint \_ fullrangespeakers-Eigenschaft des Benutzers ab. Der Benutzer gibt diese Informationen über die Windows-Multimedia-Systemsteuerung ein, Mmsys.cpl. Weitere Informationen zu Mmsys.cpl finden Sie in der Windows-DDK-Dokumentation.

Die Kanal konfigurationsmaske für die pkey \_ audioendpoint \_ fullrangespeakers-Eigenschaft eines audioendpunktgeräts ist eine Teilmenge der channelkonfigurationsmaske für die pkey \_ audioendpoint \_ physicalspeakers-Eigenschaft desselben Geräts.

Wenn ein audioendpunktgerät beispielsweise einen Satz von 5,1-umschließenden Lautsprechern steuert, ist die channelkonfigurationsmaske für die pkey \_ audioendpoint \_ physicalspeakers-Eigenschaft der ksaudio- \_ Sprecher \_ 5point1. Diese Maske gibt das vorhanden sein von Front-Left, Front-Right, Front-Center, Side-Left und Side-right Speakers – plus eines Subwoofers an. Wenn die nach-links-und Front-Right-Redner groß genug sind, um Bass Sounds zu bilden, aber die kleineren Front-Center-und Seite-Sprecher sind nicht, dann ist die channelkonfigurationsmaske für die pkey- \_ audioendpoint \_ fullrangespeakers-Eigenschaft ksaudio- \_ Sprecher \_ Stereo, der nur die Front-Left-und Front-Right-Sprecher anzeigt. Kanalkonfigurationsmasken \_ der ksaudiosprecher \_ 5point1 und \_ ksaudiosprecherstereo \_ sind in der Header Datei "ksmedia. h" definiert.

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
</dt> <dt>

[**Pkey \_ audioendpoint \_ physicalspeakers (Eigenschaft)**](pkey-audioendpoint-physicalspeakers.md)
</dt> </dl>

 

 




