---
description: Eigenschaften des audioendpunkts
ms.assetid: db85ff3b-dbb1-4ed0-b663-21ca9eb66352
title: Eigenschaften des audioendpunkts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6ce4ed9b853c2b73b73de014f3a4c8a90072a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214174"
---
# <a name="audio-endpoint-properties"></a>Eigenschaften des audioendpunkts

Die Header Datei "mmdeviceapi. h" definiert mehrere Eigenschaften von [audioendpunktgeräten](audio-endpoint-devices.md) in Windows Vista und höher. Der Windows-Audiodienst legt die Werte dieser Eigenschaften fest. Diese Eigenschaften können von Clients gelesen, jedoch nicht festgelegt werden. Eigenschaftswerte werden als **PROPVARIANT** -Strukturen gespeichert.

Die empfohlene Vorgehensweise zum Lesen der Eigenschaften eines Audioeingabegeräts besteht darin, die APIs im [**Windows. Devices. Enumeration**](/uwp/api/Windows.Devices.Enumeration) -Namespace zu verwenden. Diese APIs werden für Windows Store-Apps und Desktop-Apps unterstützt. Informationen zu vorhandenen Desktop-Apps, die Geräteeigenschaften mithilfe der [**immdevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) -Schnittstelle lesen, finden Sie unter [Geräteeigenschaften](device-properties.md). **Immdevice** wird für Windows Store-Apps nicht unterstützt.

Codebeispiele, die zeigen, wie Sie auf die Eigenschaften eines audioendpunktgeräts zugreifen, finden Sie in den folgenden Themen:

-   [Geräte Ereignisse](device-events.md)
-   [Geräte Rollen für DirectSound-Anwendungen](device-roles-for-directsound-applications.md)

Weitere Informationen zu **PROPVARIANT** finden Sie in der Windows SDK-Dokumentation.

Die folgenden Eigenschaften sind spezifisch für audioendpunktgeräte.



| Eigenschaft                                                                                                            | BESCHREIBUNG                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Pkey \_ audioendpoint-Zuordnung \_**](pkey-audioendpoint-association.md)                                          | Ordnet einem audioendpunktgerät eine-PIN-Kategorie (Kernel Streaming) zu.                                                                                |
| [**Pkey \_ audioendpoint \_ controlpanelpageprovider**](pkey-audioendpoint-controlpanelpageprovider.md)                | Gibt die CLSID des registrierten Anbieters der Geräteeigenschaften Erweiterung für das audioendpunkt-Gerät an.                                              |
| [**Pkey \_ audioendpoint \_ Deaktivieren von \_ sysfx**](pkey-audioendpoint-disable-sysfx.md)                                     | Gibt an, ob System Effekte im freigegebenen Modus-Stream aktiviert sind, der zum oder vom audioendpunktgerät fließt.                                       |
| [**Pkey- \_ audioendpoint- \_ FormFactor**](pkey-audioendpoint-formfactor.md)                                            | Gibt die physischen Attribute des audioendpunktgeräts an.                                                                                               |
| [**Pkey- \_ audioendpoint \_ fullrangespeakers**](pkey-audioendpoint-fullrangespeakers.md)                              | Gibt die Kanal konfigurationsmaske für die vollständig gültigen Referenten an, die mit dem audioendpunktgerät verbunden sind.                                         |
| [**Pkey- \_ audioendpunkt- \_ GUID**](pkey-audioendpoint-guid.md)                                                        | Gibt den DirectSound-Geräte Bezeichner an, der dem audioendpunktgerät entspricht.                                                                     |
| [**Pkey \_ audioendpoint \_ physicalspeakers**](pkey-audioendpoint-physicalspeakers.md)                                | Definiert die physische Lautsprecher Konfiguration für das audioendpunktgerät.                                                                                     |
| [**Pkey \_ Audioengine \_ deviceformat**](pkey-audioengine-deviceformat.md)                                            | Gibt das Geräte Format an. Hierbei handelt es sich um das Format, das die Audioengine für den Stream im freigegebenen Modus verwendet, der zum oder vom audioendpunktgerät fließt.       |
| [**Pkey \_ Audioengine- \_ oemformat**](pkey-audioengine-oemformat.md)<br/>                                       | Gibt das Standardformat des Geräts an, das zum Rendern oder Erfassen eines Streams verwendet wird. Die Werte werden vom OEM in einer INF-Datei aufgefüllt. <br/> |
| [**Pkey \_ audioendpoint \_ unterstützt den \_ ereignisbasierten \_ Modus**](pkey-audioendpoint-supports-eventdriven-mode.md)<br/> | Gibt an, ob der Endpunkt den ereignisgesteuerten Modus unterstützt. Die Werte werden vom OEM in einer INF-Datei aufgefüllt.<br/>                                |



 

Die Core-audioapis unterstützen zusätzliche Eigenschaften, die nicht ausschließlich für audioendpunktgeräte gelten. Weitere Informationen zu diesen zusätzlichen Eigenschaften finden Sie unter [Geräteeigenschaften](device-properties.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Audioendpunktgeräte](audio-endpoint-devices.md)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

