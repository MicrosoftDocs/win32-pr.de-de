---
title: Windows Media Device Manager 11 SDK
description: Windows Media Device Manager 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Device Manager, Informationen zu
- Device Manager, Informationen zu
- Media Transfer Protocol (MTP)
- MTP (Media Transfer Protocol)
- Massenspeicher Klasse (MSC)
- MSC (Massenspeicher Klasse)
- Windows Media Device Manager, Desktop Anwendungen
- Device Manager, Desktop Anwendungen
- Desktop Anwendungen, Informationen zu
- Windows Media Device Manager, Dienstanbieter
- Device Manager, Dienstanbieter
- Dienstanbieter, Informationen zu
- Windows Media Device Manager, Plug-ins
- Device Manager, Plug-in
- Plug-ins, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2b167e8244fb6f03a584dfb71255eabfa359c8e
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391147"
---
# <a name="windows-media-device-manager-11-sdk"></a>Windows Media Device Manager 11 SDK

> [!IMPORTANT]
> Die Windows Media Device Manager-APIs sind nun in der Windows SDK enthalten. Es sind keine zusätzlichen SDK-Downloads erforderlich.

 

Mit dem Microsoft Windows Media Device Manager Software Development Kit (SDK) können Sie Desktop Anwendungen und-Komponenten erstellen, die mit verbundenen tragbaren Geräten kommunizieren können. Windows Media Device Manager ermöglicht der Anwendung oder Komponente das auflisten, durchsuchen und Austauschen von Dateien mit einem Gerät, das Abfragen von Metadaten und das Anfordern von Informationen zur Wiedergabe Anzahl. Anwendungen oder Komponenten, die auf Windows Media-Device Manager erstellt wurden, verfügen über eine konsistente API für die Kommunikation mit einer großen Bandbreite von Geräten, einschließlich Media Transfer Protocol (MTP), Massenspeicher Klasse (MSC), RAPI und anderen Geräten, die auf der neuesten und früheren Version der Windows Media-Technologie basieren.

Mithilfe des Windows Media Device Manager SDK können Sie die folgenden Elemente erstellen:

-   Desktop Anwendungen, z. b. benutzerdefinierte Medien Player. Die gesamte Kommunikation zwischen einer Anwendung und einem tragbaren Gerät muss über Windows Media Device Manager durchlaufen werden, das als Broker zwischen der Anwendung, dem Microsoft Digital Rights Management System und dem Dienstanbieter fungiert.
-   Dienstanbieter, die als Kommunikationsverbindung zwischen einem benutzerdefinierten Gerät und einer Desktop Anwendung fungieren. Obwohl Microsoft eine Reihe von Dienstanbietern bereitstellt, die standardmäßig mit den meisten Geräten kommunizieren können, können Sie einen benutzerdefinierten Dienstanbieter erstellen, um die Kommunikation zwischen einem Gerät und einer Desktop Anwendung anzupassen.
-   Plug-ins, die Aufgaben ausführen können, z. b. das anfordern und Protokollieren der Wiedergabe Anzahl auf Geräten. Diese Plug-Ins können an andere Desktop Anwendungen angefügt werden, wie z. b. die Windows-Media Player, um Informationen an Inhaltsanbieter zu senden, um die Lizenzzahlungen an die Künstler zu verarbeiten

Informationen zum Herunterladen des Windows Media Device Manager SDK finden Sie auf der MSDN-Website auf [der Windows Media-Downloadseite](https://msdn.microsoft.com/windows/desktop/aa904949) .

Dieses SDK ist eine Komponente des Microsoft Windows Media Software Development Kit. Weitere Komponenten sind das Windows Media-Format-SDK, das Windows Media Services SDK, das Windows Media Encoder SDK, das Windows Media Rights Manager SDK und das Windows Media Player SDK.

Diese Dokumentation enthält die folgenden Abschnitte.



| `Section`                                            | BESCHREIBUNG                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erste Schritte](getting-started.md)             | Beschreibt die Neuerungen in dieser Version von Windows Media Device Manager, bietet einen Überblick über die Funktionsweise von Windows Media Device Manager, beschreibt, was zum Entwickeln einer Anwendung oder eines Dienstanbieters erforderlich ist, und erläutert die Beispiele, die mit dem SDK ausgeliefert werden. |
| [Programmierhandbuch](programming-guide.md)         | Erläutert, wie Anwendungen und Dienstanbieter erstellt werden.                                                                                                                                                                                                      |
| [Programmierverzeichnis](programming-reference.md) | Bietet C++-Referenzinformationen für die Schnittstellen, Methoden, Klassen und Strukturen, die vom Windows Media Device Manager SDK unterstützt werden.                                                                                                                      |
| [*Glossar*](wmdm-glossary.md)                    | Definiert Begriffe, die in dieser Dokumentation verwendet werden.                                                                                                                                                                                                                       |



 

 

 




