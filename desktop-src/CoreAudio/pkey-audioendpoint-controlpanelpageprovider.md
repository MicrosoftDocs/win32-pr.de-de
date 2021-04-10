---
description: Die pkey \_ audioendpoint \_ controlpanelpageprovider-Eigenschaft gibt die CLSID des registrierten Anbieters der Geräteeigenschaften Erweiterung für das audioendpunktgerät an.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861152"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>Pkey \_ audioendpoint \_ controlpanelpageprovider

Die **pkey \_ audioendpoint \_ controlpanelpageprovider** -Eigenschaft gibt die CLSID des registrierten Anbieters der Geräteeigenschaften Erweiterung für das audioendpunktgerät an. Die Erweiterung stellt die Eigenschaften für den audioendpunkt bereit, die auf der Seite Geräteeigenschaften der Windows-Multimedia-Systemsteuerung angezeigt werden, Mmsys.cpl. Weitere Informationen zu Mmsys.cpl finden Sie in der Windows-DDK-Dokumentation.

Der **VT** -Member der **PROPVARIANT** -Struktur ist auf VT \_ LPWSTR festgelegt.

Der **pwszval** -Member der **PROPVARIANT** -Struktur verweist auf eine mit NULL endenden Zeichenfolge mit breit Zeichen, die eine GUID enthält, die den Anbieter der Steuerelement Bereichs Erweiterung identifiziert.

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

 

 




