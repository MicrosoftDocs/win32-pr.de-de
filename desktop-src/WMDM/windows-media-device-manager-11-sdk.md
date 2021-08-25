---
title: Windows Media Geräte-Manager 11 SDK
description: Windows Media Geräte-Manager 11 SDK
ms.assetid: 9c0c9a96-1335-4ae2-9393-bfab0dfe24c6
keywords:
- Windows Media Geräte-Manager,About
- Geräte-Manager, Informationen
- Media Transfer Protocol (MTP)
- MTP (Media Transfer Protocol)
- Mass Storage-Klasse (MSC)
- MSC (Mass Storage-Klasse)
- Windows Medien Geräte-Manager, Desktopanwendungen
- Geräte-Manager,Desktopanwendungen
- Desktopanwendungen, Informationen
- Windows Medien Geräte-Manager, Dienstanbieter
- Geräte-Manager,Dienstanbieter
- Dienstanbieter, Informationen
- Windows Medien Geräte-Manager, Plug-Ins
- Geräte-Manager,Plug-Insp
- Plug-Ins, Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57e8b19b035f0210b7928dcc42c19d9519a63fe4eac3e5adaeded780c9d4c729
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004810"
---
# <a name="windows-media-device-manager-11-sdk"></a>Windows Media Geräte-Manager 11 SDK

> [!IMPORTANT]
> Die Windows Media Geräte-Manager-APIs sind jetzt im Windows SDK enthalten. Es sind keine zusätzlichen SDK-Downloads erforderlich.

 

Mit dem Microsoft Windows Media Geräte-Manager Software Development Kit (SDK) können Sie Desktopanwendungen und -komponenten erstellen, die mit verbundenen portablen Geräten kommunizieren können. Windows Media Geräte-Manager ermöglicht Es Ihrer Anwendung oder Komponente, Dateien mit einem Gerät aufzuzählen, zu untersuchen und auszutauschen, Metadaten abzufragen und Informationen zur Wiedergabeanzahl anzufordern. Anwendungen oder Komponenten, die auf Windows Media Geräte-Manager aufbauen, verfügen über eine konsistente API für die Kommunikation mit einer Vielzahl von Geräten, einschließlich Media Transfer Protocol (MTP), Mass Storage Class (MSC), MSCI und anderen Geräten, die auf der neuesten und früheren Version der Windows Medientechnologie aufbauen.

Sie können die folgenden Elemente mit dem Windows Media Geräte-Manager SDK erstellen:

-   Desktopanwendungen, z. B. benutzerdefinierte Medienplayer. Die gesamte Kommunikation zwischen einer Anwendung und einem portablen Gerät muss über Windows Media Geräte-Manager erfolgen, der als Broker zwischen der Anwendung, dem Microsoft Digital Rights Management-System und dem Dienstanbieter fungiert.
-   Dienstanbieter, die als Kommunikationslink zwischen einem benutzerdefinierten Gerät und einer Desktopanwendung fungieren. Obwohl Microsoft eine Reihe von Dienstanbietern bereitstellt, die sofort mit den meisten Geräten kommunizieren können, können Sie einen benutzerdefinierten Dienstanbieter erstellen, um die Kommunikation zwischen einem Gerät und einer Desktopanwendung anzupassen.
-   Plug-Ins, die Aufgaben wie das Anfordern und Protokollieren der Wiedergabeanzahl auf Geräten ausführen können. Diese Plug-Ins können an andere Desktopanwendungen angefügt werden, z. B. an die Windows Media Player zum Senden von Informationen an Inhaltsanbieter, um lizenzgebührenbasierte Zahlungen an Diener zu verarbeiten.

Informationen zum Herunterladen des Windows Media Geräte-Manager SDK finden Sie auf der MSDN-Website auf [der Seite zum Herunterladen von Windows Medien.](https://msdn.microsoft.com/windows/desktop/aa904949)

Dieses SDK ist eine Komponente des Microsoft Windows Media Software Development Kit. Weitere Komponenten sind das Windows Media Format SDK, das Windows Media-Dienste SDK, das Windows Media Encoder SDK, das Windows Media Rights Manager SDK und das Windows Media Player SDK.

Diese Dokumentation enthält die folgenden Abschnitte.



| `Section`                                            | BESCHREIBUNG                                                                                                                                                                                                                                                     |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Erste Schritte](getting-started.md)             | Beschreibt die Neuerungen in dieser Version von Windows Media Geräte-Manager, bietet eine Übersicht über die Funktionsweise Windows Media Geräte-Manager, beschreibt, was zum Entwickeln einer Anwendung oder eines Dienstanbieters erforderlich ist, und erläutert die mit dem SDK gelieferten Beispiele. |
| [Programmierhandbuch](programming-guide.md)         | Erläutert das Erstellen von Anwendungen und Dienstanbietern.                                                                                                                                                                                                      |
| [Programmierverzeichnis](programming-reference.md) | Stellt C++-Referenzinformationen für die Schnittstellen, Methoden, Klassen und Strukturen bereit, die vom Windows Media Geräte-Manager SDK unterstützt werden.                                                                                                                      |
| [*Glossar*](wmdm-glossary.md)                    | Definiert begriffe, die in dieser Dokumentation verwendet werden.                                                                                                                                                                                                                       |



 

 

 




