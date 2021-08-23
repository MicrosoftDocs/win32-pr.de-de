---
description: Informationen zu Windows Core-Audio-APIs
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Informationen zu Windows Core-Audio-APIs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07d5336522a681fc5f2d6e8ee5db0c17eacccfa46ea4cc4559bf00e6ea629031
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018548"
---
# <a name="about-the-windows-core-audio-apis"></a>Informationen zu Windows Core-Audio-APIs

Diese Dokumentation enthält Informationen zu Core Audio-APIs für die Microsoft Windows-Betriebssystemfamilie.

Die Core Audio-APIs wurden in Windows Vista eingeführt. Dies ist ein neuer Satz von Audiokomponenten im Benutzermodus, der Clientanwendungen verbesserte Audiofunktionen bietet. Diese Funktionen umfassen Folgendes:

-   Geringe Latenz, Störungsresilienz beim Audiostreaming.
-   Verbesserte Zuverlässigkeit (viele Audiofunktionen wurden vom Kernelmodus in den Benutzermodus verschoben).
-   Verbesserte Sicherheit (die Verarbeitung geschützter Audioinhalte erfolgt in einem sicheren Prozess mit niedrigeren Berechtigungen).
-   Zuweisung bestimmter systemweiter Rollen (Konsole, Multimedia und Kommunikation) zu einzelnen Audiogeräten.
-   Softwareabstraktion der Audioendpunktgeräte (z. B. Lautsprecher, Mikrofone und Mikrofone), die der Benutzer direkt bearbeitet.

Die Core Audio-APIs wurden in Windows 7 verbessert. Weitere Informationen zu den Verbesserungen und neuen Features, die hinzugefügt wurden, finden Sie unter What [es New for Core Audio APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).

In dieser Dokumentation werden die Kernaudio-APIs beschrieben. Diese APIs dienen als Grundlage für die folgenden APIs auf höherer Ebene:

-   Directsound
-   Directmusic
-   Windows multimedia **waveXxx- und** **mixerXxx-Funktionen**
-   Media Foundation

Diese apIs auf höherer Ebene verwenden die Core Audio-APIs, um den Zugriff auf Audiogeräte zu teilen. Media Foundation ist neu in Windows Vista, während DirectSound, DirectIndex und die **Funktionen waveXxx** und **mixerXxx** in Windows 98, Windows Edition edition und in Windows 2000 und höher unterstützt werden.

Die meisten Audioanwendungen kommunizieren mit den APIs der höheren Ebene, anstatt direkt mit den Core Audio-APIs zu kommunizieren. Beispiele für Anwendungen, die APIs auf höherer Ebene verwenden:

-   Media Player
-   DVD-Player
-   Spiele
-   Geschäftsanwendungen, z. B. Microsoft Office PowerPoint, die Sounddateien wiederklangen

In der Regel kommunizieren diese Anwendungen mit den DirectSound- oder Media Foundation-APIs.

Die direkte Kommunikation mit den Core Audio-APIs eignet sich möglicherweise nicht für viele allgemeine Audioanwendungen. Beispielsweise erfordern die Core Audio-APIs Audiostreams, um die nativen Datenformate eines Audiogeräts zu verwenden. Allerdings benötigen Softwareentwickler von Drittanbietern, die die folgenden Produkttypen entwickeln, möglicherweise die speziellen Funktionen der Core Audio-APIs:

-   Professional von Audioanwendungen ("Pro Audio")
-   Echtzeitkommunikationsanwendungen (RTC)
-   Audio-APIs von Drittanbietern

Eine Pro-Audio- oder RTC-Anwendung benötigt möglicherweise direkten Zugriff auf die low-level-Features der Core Audio-APIs, um eine minimale Latenz zu erzielen, indem sie exklusiven Zugriff auf Audiohardware erhält. Eine Audio-API eines Drittanbieters erfordert möglicherweise direkten Zugriff auf die Core Audio-APIs, um eine Reihe von Features zu implementieren, die möglicherweise nicht vollständig von einer einzelnen, mit Windows.

Eine Anwendung, die eine Legacy-Audio-API zum Wieder- oder Aufzeichnen von Audio verwendet, erfordert möglicherweise zusätzliche Funktionen, die von der Legacy-Audio-API nicht unterstützt werden, aber von den Core Audio-APIs unterstützt werden. In vielen Fällen kann die Anwendung direkt über die Core Audio-APIs auf diese Funktionen zugreifen, die in Verbindung mit der Legacy-Audio-API verwendet werden können.

Die Kernaudio-APIs sind:

-   [MMDevice-API (Multimediagerät).](mmdevice-api.md) Clients verwenden diese API, um die Audioendpunktgeräte im System zu aufzählen.
-   [Windows AudioSitzungs-API (WASAPI)](wasapi.md). Clients verwenden diese API, um Audiostreams zu und von Audioendpunktgeräten zu erstellen und zu verwalten.
-   [DeviceTopology-API](devicetopology-api.md). Clients verwenden diese API, um direkt auf die topologien Features (z. B. Volumesteuerelemente und Multiplexer) zuzugreifen, die sich entlang der Datenpfade innerhalb von Hardwaregeräten in Audioadaptern befindet.
-   [EndpointVolume-API](endpointvolume-api.md). Clients verwenden diese API, um direkt auf die Volumesteuerelemente auf Audioendpunktgeräten zuzugreifen. Diese API wird hauptsächlich von Anwendungen verwendet, die Audiostreams im exklusiven Modus verwalten.

Diese APIs unterstützen das benutzerfreundliche Konzept eines Endpunktgeräts, das unter [Audioendpunktgeräte beschrieben wird.](audio-endpoint-devices.md)

Microsoft plant nicht, die hier beschriebenen Core Audio-APIs für die Verwendung mit früheren Versionen von Windows verfügbar zu machen, einschließlich Microsoft Windows Server 2003, Windows XP, Windows Edition, Windows 2000 und Windows 98.

Diese Übersicht enthält die folgenden Themen.



| **Thema**                                                                                      | **Beschreibung**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Neues bei Core Audio-APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Fasst die neuen Features und die Verbesserungen der Core Audio-APIs zusammen.                   |
| [Headerdateien und Systemkomponenten](header-files-and-system-components.md)                   | Beschreibt die Headerdateien und Systemkomponenten für die Core Audio-APIs.                 |
| [SDK-Beispiele, die die Kernaudio-APIs verwenden](sdk-samples-that-use-the-core-audio-apis.md)       | Listet die Beispiele im Windows SDK auf, die die Core Audio-APIs verwenden.                        |




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernaudio-APIs](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



