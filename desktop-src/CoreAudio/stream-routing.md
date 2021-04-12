---
description: Stream-Routing ist die Fähigkeit einer Medien Anwendung, Streams zwischen Geräten mit minimaler Unterbrechung der Wiedergabe oder der Erfassungs Sitzung zu wechseln.
ms.assetid: fc6efe89-013c-47af-870e-8705fa60c99c
title: Streamrouting
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b21cd15a4467cb9b08747119aab999882ae3b5f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483462"
---
# <a name="stream-routing"></a>Streamrouting

*Stream-Routing* ist die Fähigkeit einer Medien Anwendung, Streams zwischen Geräten mit minimaler Unterbrechung der Wiedergabe oder der Erfassungs Sitzung zu wechseln.

Ein Computer kann über mehrere renderinggeräte und Erfassungsgeräte verfügen. Das System listet diese Geräte in der Systemsteuerung **Sounds** auf. In dieser Liste kann ein Benutzer ein Gerät als Standardgerät für jede Rolle festlegen: Wiedergabe, Aufzeichnung oder die vier Kommunikations Rollen (Konsolen Rendering, Konsolen Erfassung, Kommunikations-Rendering oder Kommunikations Erfassung). Die Liste der Geräte kann dynamisch geändert werden, da einige dieser Geräte vorübergehend verfügbar sein können, z. b. ein USB-Headset. Wenn mehrere Geräte verfügbar sind, kann der Benutzer die Standardeinstellung auf ein anderes Gerät ändern. Der Benutzer kann auch das Format eines Geräts (Samplingrate, Bits pro Stichprobe usw.) auf der Registerkarte **erweitert** für die Geräteeigenschaften ändern.

Stellen Sie sich ein Szenario vor, in dem ein Benutzer **Referenten** als Standardgerät zum Rendern von Audiostreams auswählt. Der Benutzer stellt dann eine Verbindung mit einem USB-Headset her, wählt das Headset als neues Standardgerät aus und ändert die Samplingrate des Geräts von 44,1 kHz in 48 kHz. Der Benutzer möchte den Audiostream in der neuen Stichprobenrate mit minimaler Unterbrechung der Streamingsitzung auf dem Headset wiedergeben.

In diesem Szenario gibt es zwei Fälle, die die Medien Anwendung behandeln muss:

-   Der Stream muss mit minimaler Unterbrechung der Wiedergabe auf das neue Standardgerät übertragen werden.
-   Das neue Gerät muss die Wiedergabe im neuen Format fortsetzen (d. h., der Benutzer kann die Stichprobenrate ändern).

Um dieses Szenario in Windows Vista zu unterstützen, musste die Medien Anwendung die Implementierung für das Datenstrom Routing bereitstellen. Die Anwendung war dafür verantwortlich, vorhandene Streams zu beenden und die Streams auf dem neuen Gerät neu zu starten. Wenn der Benutzer das Standardgerät geändert hat oder das zugehörige Mischungs Format geändert wurde, wurden alle zugeordneten Sitzungen geschlossen, und die Anwendung musste die Wiederherstellung durchführen.

In Windows 7 kann eine Anwendung einen Stream nahtlos von einem vorhandenen Standardgerät an einen neuen standardaudioendpunkt übertragen. Allgemeine Audio-API-Sätze, wie Media Foundation-, DirectSound-und Wave-APIs, implementieren das Stream-Routing Feature. Medienanwendungen, die diese API-Sätze zum Wiedergeben oder Erfassen eines Streams vom Standardgerät verwenden, verwenden die Standard Implementierung und müssen die Anwendung nicht ändern. Wenn Ihre Medien Anwendung jedoch mmdeviceapi oder WASAPI direkt verwendet, muss die Anwendung die streamweiterleitungs-Implementierung bereitstellen.

> [!Note]  
> Mmdeviceapi und WASAPI sind Kerncode-API-Komponenten, die eine Anwendung verwenden kann, um einen Stream auf einem Gerät zu erzeugen oder zu erfassen. Die mmdeviceapi ermittelt das neue audioendpunktgerät, und WASAPI verwaltet den Fluss der Audiodaten zwischen einer Medien Anwendung und dem audioendpunktgerät.

 

Zum Implementieren der streamweiterleitungs Funktion muss die Anwendung die von mmdeviceapi und WASAPI gesendeten Benachrichtigungen überwachen, wenn Folgendes der Fall ist:

-   Das Standardgerät wird vom Benutzer geändert.
-   Das vorhandene Standardgerät wird entfernt und ein neues Standardgerät hinzugefügt.
-   Das Geräte Format wird geändert.

Durch die Behandlung dieser Benachrichtigungen kann eine Anwendung die erforderlichen Stream-Verwaltungsvorgänge ausführen, während der Datenstrom auf das neue Standardgerät übertragen wird. Außerdem kann die Anwendung vorhandene Streams mithilfe des neuen Formats rendern oder erfassen, das vom Benutzer angegeben wird, während eine renderingsitzung aktiv ist.

Dieser Abschnitt enthält die folgenden Themen:

-   [Der Geräte Endpunkt für das streamrouting wird erhalten.](getting-the-default-device-endpoint-for-stream-routing.md)
-   [Relevante Benachrichtigungen für das Datenstrom Routing](relevant-device-notifications-for-stream-routing.md)
-   [Überlegungen zur Implementierung von streamrouting](stream-routing-implementation-considerations.md)

Die folgenden Beispiele, die im Windows SDK enthalten sind, veranschaulichen, wie eine Anwendung Stream-Routing Benachrichtigungen verarbeiten kann.

-   [Rendersharedtimer-gesteuert](rendersharedtimerdriven.md)
-   [Rendersharedebug-gesteuert](rendersharedeventdriven.md)
-   [Renderexclusivetimer-gesteuert](renderexclusivetimerdriven.md)
-   [Renderexclusiveeventdriver](renderexclusiveeventdriven.md)
-   [Capturesharedtimer-gesteuert](capturesharedtimerdriven.md)
-   [Capturesharedebug](capturesharedeventdriven.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Datenstrom Verwaltung](stream-management.md)
</dt> <dt>

[Informationen über die mmdevice-API](mmdevice-api.md)
</dt> <dt>

[Informationen zu WASAPI](wasapi.md)
</dt> </dl>

 

 



