---
description: Informationen zu den Windows Core-audioapis
ms.assetid: 657cf75f-3d72-4a5f-ae29-299e826b2b86
title: Informationen zu den Windows Core-audioapis
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 30763d70bae4340436145a303763c0aad57171f5
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103861695"
---
# <a name="about-the-windows-core-audio-apis"></a>Informationen zu den Windows Core-audioapis

Diese Dokumentation enthält Informationen zu den Kerncode-APIs für die Microsoft Windows-Betriebssystem Familie.

Die Kern-audioapis wurden in Windows Vista eingeführt. Dies ist ein neuer Satz von Audiokomponenten im Benutzermodus, der Client Anwendungen verbesserte Audiofunktionen bietet. Diese Funktionen umfassen Folgendes:

-   Geringe Latenz, gleitrobustes Audiostreaming.
-   Verbesserte Zuverlässigkeit (viele Audiofunktionen wurden vom Kernel Modus in den Benutzermodus verschoben).
-   Verbesserte Sicherheit (die Verarbeitung geschützter Audioinhalte findet in einem sicheren Prozess mit niedrigerer Berechtigung statt).
-   Zuweisung von bestimmten systemweiten Rollen (Konsole, Multimedia und Kommunikation) zu einzelnen Audiogeräten.
-   Software Abstraktion der audioendpunktgeräte (z. b. Sprecher, Kopfhörer und Mikrofone), die der Benutzer direkt bearbeitet.

Die Kern-audioapis wurden in Windows 7 verbessert. Weitere Informationen zu den Verbesserungen und neuen Features finden Sie unter [What es New for Core audioapis in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md).

In dieser Dokumentation werden die Kern-API-APIs beschrieben. Diese APIs dienen als Grundlage für die folgenden APIs auf höherer Ebene:

-   DirectSound
-   DirectMusic
-   Windows Multimedia **wavexxx** -und **mixerxxx** -Funktionen
-   Media Foundation

Diese APIs auf höherer Ebene verwenden die Kerndatei-APIs, um den Zugriff auf Audiogeräte freizugeben. Media Foundation in Windows Vista neu ist, während die Funktionen DirectSound, DirectMusic und **wavexxx** und **mixerxxx** in Windows 98, Windows Millennium Edition und Windows 2000 und höher unterstützt werden.

Die meisten Audioanwendungen kommunizieren mit den APIs auf höherer Ebene, anstatt direkt mit den Kerncode-APIs zu kommunizieren. Einige Beispiele für Anwendungen, die APIs höherer Ebene verwenden, sind:

-   Media Player
-   DVD-Player
-   Spiele
-   Geschäftsanwendungen, wie z. b. Microsoft Office PowerPoint, die Sounddateien abspielen

In der Regel kommunizieren diese Anwendungen mit den DirectSound-oder Media Foundation-APIs.

Die direkte Kommunikation mit den kernaudioapis eignet sich möglicherweise nicht für viele allgemeine Audioanwendungen. Beispielsweise erfordern die Kern-audioapis Audiostreams, um die nativen Datenformate eines Audiogeräts zu verwenden. Softwareentwickler von Drittanbietern, die die folgenden Produkttypen entwickeln, benötigen jedoch möglicherweise die speziellen Funktionen der kernaudioapis:

-   Professionelle Audioanwendungen ("pro-Audiodatei")
-   Echtzeitkommunikation (RTC)-Anwendungen
-   Audioapis von Drittanbietern

Eine "pro-Audiodatei" oder RTC-Anwendung benötigt möglicherweise direkten Zugriff auf die Low-Level-Funktionen der kernaudioapis, um eine minimale Latenz zu erzielen, indem exklusiver Zugriff auf Audiohardware erhalten wird. Für eine audioapi von Drittanbietern ist möglicherweise direkter Zugriff auf die Kerndatei-APIs erforderlich, um eine Reihe von Features zu implementieren, die von einer einzelnen, in Windows bereitgestellten audioapi mit hoher Ebene möglicherweise nicht vollständig unterstützt werden.

Eine Anwendung, die eine Legacy-audioapi zum Abspielen oder Aufzeichnen von Audiodaten verwendet, erfordert möglicherweise zusätzliche Funktionen, die von der Legacy-audioapi nicht unterstützt werden, aber von den kernaudioapis unterstützt werden. In vielen Fällen kann die Anwendung direkt über die wichtigsten audioapis auf diese Funktionen zugreifen, die in Verbindung mit der Legacy-audioapi verwendet werden können.

Die Kern-audioapis lauten:

-   [API für Multimedia-Geräte (mmdevice)](mmdevice-api.md). Clients verwenden diese API, um die audioendpunktgeräte im System aufzuzählen.
-   [Windows-audiositzungs-API (WASAPI)](wasapi.md). Clients verwenden diese API, um audiodatenstreams zu und von audioendpunktgeräten zu erstellen und zu verwalten.
-   Die Geräte-API (Debug- [API](devicetopology-api.md)). Clients verwenden diese API, um direkt auf die topologischen Features zuzugreifen (z. b. volumesteuerelemente und Multiplexer), die sich auf den Daten Pfaden innerhalb von Hardware Geräten in audioadaptern befinden.
-   [Endpointvolume-API](endpointvolume-api.md). Clients verwenden diese API, um direkt auf die volumesteuerelemente auf audioendpunktgeräten zuzugreifen. Diese API wird hauptsächlich von Anwendungen verwendet, die Audiostreams im exklusiven Modus verwalten.

Diese APIs unterstützen das benutzerfreundliche Konzept eines Endpunkt Geräts, das in [audioendpunktgeräten](audio-endpoint-devices.md)beschrieben wird.

Microsoft plant nicht, die hier beschriebenen kernaudioapis für die Verwendung mit früheren Versionen von Windows, einschließlich Microsoft Windows Server 2003, Windows XP, Windows Millennium Edition, Windows 2000 und Windows 98, bereitzustellen.

Diese Übersicht enthält die folgenden Themen.



| **Thema**                                                                                      | **Beschreibung**                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [Neuerungen bei den Kerncode-APIs in Windows 7](what-s-new-for-core-audio-apis-in-windows-7.md) | Fasst die neuen Features und die Verbesserungen der kernaudioapis zusammen                   |
| [Header Dateien und System Komponenten](header-files-and-system-components.md)                   | Beschreibt die Header Dateien und Systemkomponenten für die Kerndatei-APIs.                 |
| [SDK-Beispiele für die Verwendung der kernaudioapis](sdk-samples-that-use-the-core-audio-apis.md)       | Listet die Beispiele in den Windows SDK auf, die die Kern-audioapis verwenden.                        |




 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kernaudioapis](core-audio-apis-in-windows-vista.md)
</dt> </dl>

 

 



