---
description: Audioendpunkteigenschaften
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Audioendpunkteigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf76ef70afaed98ed04ad2ee56e83c38c14ffde1bb6e4d43b557d25769afb2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117828501"
---
# <a name="audio-endpoint-properties"></a>Audioendpunkteigenschaften

Die Headerdatei Mmdeviceapi.h definiert mehrere Eigenschaften von [Audioendpunktgeräten](audio-endpoint-devices.md) in Windows Vista und höher. Der Windows Audiodienst legt die Werte dieser Eigenschaften fest. Clients können diese Eigenschaften lesen, sollten sie jedoch nicht festlegen. Eigenschaftswerte werden als **PROPVARIANT-Strukturen** gespeichert.

Die empfohlene Methode zum Lesen der Eigenschaften eines Audioeingabegeräts ist die Verwendung der APIs im [**Windows. Devices.Enumeration-Namespace.**](/uwp/api/Windows.Devices.Enumeration) Diese APIs werden für Windows Store-Apps und Desktop-Apps unterstützt. Informationen zu vorhandenen Desktop-Apps, die Geräteeigenschaften über die [**IMMDevice-Schnittstelle**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) lesen, finden Sie unter [Geräteeigenschaften.](device-properties.md) **IMMDevice** wird für Windows Store-Apps nicht unterstützt.

Codebeispiele für den Zugriff auf die Eigenschaften eines Audioendpunktgeräts finden Sie in den folgenden Themen:

-   [Geräteereignisse](device-events.md)
-   [Geräterollen für DirectSound-Anwendungen](device-roles-for-directsound-applications.md)

Informationen zu **PROPVARIANT** finden Sie in der Windows SDK-Dokumentation.

Die folgenden Eigenschaften gelten spezifisch für Audioendpunktgeräte.



| Eigenschaft                                                                                                            | Beschreibung                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PKEY \_ \_ AudioEndpoint-Zuordnung**](pkey-audioendpoint-association.md)                                          | Ordnet einem Audioendpunktgerät eine Kernelstreaming-Pinkategorie (KS) zu.                                                                                |
| [**PKEY \_ AudioEndpoint \_ ControlPanelPageProvider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Gibt die CLSID des registrierten Anbieters der Geräteeigenschaftenerweiterung für das Audioendpunktgerät an.                                              |
| [**PKEY \_ AudioEndpoint \_ Disable \_ SysFx**](pkey-audioendpoint-disable-sysfx.md)                                     | Gibt an, ob Systemeffekte im Stream im freigegebenen Modus aktiviert sind, der an das Audioendpunktgerät oder vom Audioendpunktgerät übertragen wird.                                       |
| [**PKEY \_ AudioEndpoint \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Gibt die physischen Attribute des Audioendpunktgeräts an.                                                                                               |
| [**PKEY \_ AudioEndpoint \_ FullRangeSpeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Gibt die Kanalkonfigurationsmaske für die Vollbereichslautgeber an, die mit dem Audioendpunktgerät verbunden sind.                                         |
| [**PKEY \_ AudioEndpoint \_ GUID**](pkey-audioendpoint-guid.md)                                                        | Gibt den DirectSound-Gerätebezeichner an, der dem Audioendpunktgerät entspricht.                                                                     |
| [**PKEY \_ AudioEndpoint \_ PhysicalSpeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Definiert die Konfiguration des physischen Lautsprechers für das Audioendpunktgerät.                                                                                     |
| [**PKEY \_ AudioEngine \_ DeviceFormat**](pkey-audioengine-deviceformat.md)                                            | Gibt das Geräteformat an. Dabei handelt es sich um das Format, das die Audio-Engine für den Datenstrom im freigegebenen Modus verwendet, der zum oder vom Audioendpunktgerät fließt.       |
| [**PKEY \_ AudioEngine \_ OEMFormat**](pkey-audioengine-oemformat.md)<br/>                                       | Gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt. <br/> |
| [**PKEY \_ AudioEndpoint \_ unterstützt den \_ EventDriven-Modus. \_**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.<br/>                                |



 

Die Kernaudio-APIs unterstützen zusätzliche Eigenschaften, die nicht ausschließlich für Audioendpunktgeräte gelten. Weitere Informationen zu diesen zusätzlichen Eigenschaften finden Sie unter [Geräteeigenschaften.](device-properties.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

