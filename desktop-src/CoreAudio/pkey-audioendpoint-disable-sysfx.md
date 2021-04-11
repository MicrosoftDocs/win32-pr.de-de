---
description: Die pkey \_ audioendpoint \_ - \_ Eigenschaft "sysfx deaktivieren" gibt an, ob System Effekte im freigegebenen modusstream aktiviert sind, der zum oder vom audioendpunktgerät fließt.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127309"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a>Pkey \_ audioendpoint \_ Deaktivieren von \_ sysfx

Die **pkey \_ audioendpoint-Eigenschaft " \_ \_ sysfx deaktivieren** " gibt an, ob System Effekte im freigegebenen modusstream aktiviert sind, der zum oder vom audioendpunktgerät fließt.

System Effekte werden als audioverarbeitungsobjekte (apos) implementiert, die in einen Audiostream eingefügt werden können. APOS sind Softwaremodule, die audioverarbeitungsfunktionen wie z. b. volumesteuerung und Formatkonvertierung ausführen. Durch das Deaktivieren der System Effekte für ein Endpunkt Gerät kann der zugehörige Stream die apos unverändert durchlaufen.

Weitere Informationen zu System Effekten in Windows Vista finden Sie in den Whitepapers mit dem Titel "benutzerdefinierte Audioeffekte in Windows Vista" und "wieder verwenden von Windows Vista-audiosystemeffekten" auf der Website " [audiogerätetechnologien für Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) ".

Diese Eigenschaft gilt nur für die lokalen Effekte und globalen Effekte, die von der INF-Datei installiert wurden, die den Audioadapter installiert hat, mit dem das Endpunkt Gerät verbunden ist. Außerdem wirkt sich diese Eigenschaft nur auf das Ziel Endpunkt Gerät aus – Sie wirkt sich nicht auf die Auswirkungen auf die System Auswirkungen anderer Endpunkt Geräte aus, auch wenn Sie eine Verbindung mit dem gleichen Adapter herstellen.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf **VT \_ UI4** festgelegt.

Der **ulVal** -Member der **PROPVARIANT** -Struktur ist auf **EndPoint \_ sysfx \_ aktiviert** festgelegt, wenn System Effekte aktiviert sind, oder wenn der **Endpunkt \_ sysfx \_ deaktiviert** ist, wenn Sie deaktiviert sind.

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

 

 




