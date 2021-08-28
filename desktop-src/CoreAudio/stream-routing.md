---
description: Streamrouting ist die Möglichkeit einer Medienanwendung, Streams zwischen Geräten mit minimaler Unterbrechung der Wiedergabe oder Aufzeichnungssitzung zu wechseln.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2e76944954c969ce458175585076d23ce015ea573a86e3f89dbbcd296aff444
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018228"
---
# <a name="stream-routing"></a>Streamrouting

*Streamrouting* ist die Möglichkeit einer Medienanwendung, Streams zwischen Geräten mit minimaler Unterbrechung der Wiedergabe- oder Aufzeichnungssitzung zu wechseln.

Ein Computer kann über mehrere Rendering- und Erfassungsgeräte verfügen. Das System listet  diese Geräte in der Sound-Systemsteuerung auf. In dieser Liste kann ein Benutzer ein Gerät als Standardgerät für jede Rolle festlegen: Wiedergabe, Aufzeichnung oder die vier Kommunikationsrollen (Konsolenrendering, Konsolenerfassung, Kommunikationsrendering oder Kommunikationserfassung). Die Liste der Geräte kann dynamisch geändert werden, da einige dieser Geräte vorübergehend verfügbar sein können, z. B. ein USB-Headset. Wenn mehrere Geräte verfügbar sind, kann der Benutzer die Standardeinstellung auf ein anderes Gerät ändern. Der Benutzer kann auch das Format eines Geräts (Abtastrate, Bits pro Stichprobe usw.) auf der Registerkarte **Erweitert** für die Geräteeigenschaften ändern.

Stellen Sie sich ein Szenario vor, in dem ein Benutzer **Speakers** als Standardgerät zum Rendern von Audiostreams auswählt. Der Benutzer verbindet dann ein USB-Headset, wählt das Headset als neues Standardgerät aus und ändert die Abtastrate des Geräts von 44,1 kHz in 48 kHz. Der Benutzer möchte den Audiostream auf dem Headset mit der neuen Abtastrate mit minimaler Unterbrechung der Streamingsitzung wiedergeben.

In diesem Szenario muss die Medienanwendung zwei Fälle behandeln:

-   Der Stream muss mit minimaler Unterbrechung der Wiedergabe auf das neue Standardgerät übertragen werden.
-   Das neue Gerät muss die Wiedergabe im neuen Format fortsetzen (das heißt, der Benutzer kann mehr als die Abtastrate ändern).

In Windows Vista musste die Medienanwendung die Implementierung für das Streamrouting bereitstellen, um dieses Szenario zu unterstützen. Die Anwendung war dafür verantwortlich, vorhandene Streams zu beenden und die Streams auf dem neuen Gerät neu zu starten. Wenn der Benutzer das Standardgerät oder sein Mischungsformat geändert hat, wurden alle zugehörigen Sitzungen geschlossen, und die Anwendung musste die Wiederherstellung verarbeiten.

In Windows 7 kann eine Anwendung nahtlos einen Stream von einem vorhandenen Standardgerät an einen neuen Standardaudioendpunkt übertragen. High-Level-Audio-API-Sätze wie Media Foundation, DirectSound und WAVE-APIs implementieren das Streamroutingfeature. Medienanwendungen, die diese API-Sätze zum Wiedergeben oder Erfassen eines Streams vom Standardgerät verwenden, verwenden die Standardimplementierungen und müssen die Anwendung nicht ändern. Wenn Ihre Medienanwendung jedoch MMDeviceAPI oder WASAPI direkt verwendet, muss die Anwendung die Implementierung des Streamroutings bereitstellen.

> [!Note]  
> MMDeviceAPI und WASAPI sind Kernkomponenten der Audio-API, die eine Anwendung zum Rendern oder Erfassen eines Streams auf einem Gerät verwenden kann. Die MMDeviceAPI ermittelt das neue Audioendpunktgerät, und WASAPI verwaltet den Fluss von Audiodaten zwischen einer Medienanwendung und dem Audioendpunktgerät.

 

Um das Streamroutingfeature zu implementieren, muss die Anwendung auf die von MMDeviceAPI und WASAPI gesendeten Benachrichtigungen lauschen, wenn:

-   Das Standardgerät wird vom Benutzer geändert.
-   Das vorhandene Standardgerät wird entfernt, und ein neues Standardgerät wird hinzugefügt.
-   Das Geräteformat wird geändert.

Durch die Verarbeitung dieser Benachrichtigungen kann eine Anwendung die erforderlichen Datenstromverwaltungsvorgänge ausführen, während der Datenstrom auf das neue Standardgerät übertragen wird. Darüber hinaus kann die Anwendung vorhandene Streams rendern oder erfassen, indem sie das neue Format verwendet, das vom Benutzer angegeben wird, während eine Renderingsitzung aktiv ist.

Dieser Abschnitt enthält die folgenden Themen:

-   [Abrufen des Geräteendpunkts für das Streamrouting](getting-the-default-device-endpoint-for-stream-routing.md)
-   [Relevante Benachrichtigungen für das Streamrouting](relevant-device-notifications-for-stream-routing.md)
-   [Überlegungen zur Implementierung des Streamroutings](stream-routing-implementation-considerations.md)

Die folgenden Beispiele, die im Windows SDK enthalten sind, veranschaulichen, wie eine Anwendung Streamroutingbenachrichtigungen verarbeiten kann.

-   [RenderSharedTimerDriven](rendersharedtimerdriven.md)
-   [RenderSharedEventDriven](rendersharedeventdriven.md)
-   [RenderExclusiveTimerDriven](renderexclusivetimerdriven.md)
-   [RenderExclusiveEventDriven](renderexclusiveeventdriven.md)
-   [CaptureSharedTimerDriven](capturesharedtimerdriven.md)
-   [CaptureSharedEventDriven](capturesharedeventdriven.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamverwaltung](stream-management.md)
</dt> <dt>

[Informationen zur MMDevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> </dl>

 

 



