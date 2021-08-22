---
description: WPD-Anwendungsprogrammierschnittstelle
ms.assetid: 3e2be15f-7af7-4e76-89b1-f9bc591c4f1b
title: WPD-Anwendungsprogrammierschnittstelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c5937cf14e7679bb9d9ca487b12ec546fb1751e3c94930f83c4aed3be5ed71a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083364"
---
# <a name="wpd-application-programming-interface"></a>WPD-Anwendungsprogrammierschnittstelle

Anwendungen, die auf Windows portablen Geräten erstellt wurden, können ein Gerät untersuchen, Inhalte senden und empfangen und sogar das Gerät steuern, z. B. ein Bild oder eine SMS senden. Das System ist so konzipiert, dass es flexibel ist, sodass viele Arten von Geräten untersucht und erweiterbar werden können, sodass Treiberentwickler benutzerdefinierte Eigenschaften und Befehle für benutzerdefinierte Geräte definieren können.

In der folgenden Tabelle werden die Hauptthemen dieser Dokumentation beschrieben.



| Thema                                                                                                                  | Beschreibung                                                                                                |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [Allgemeine Anforderungen für die Anwendungsentwicklung](general-requirements-for-application-development.md)               | Hardware- und Softwareanforderungen für die Entwicklung von Treibern und Anwendungen mit Windows Portable Devices.     |
| [Anforderungen für Windows Media DRM-Enabled Anwendungen](requirements-for-windows-media-drm-enabled-applications.md) | Eigenschaften, die zum Aktivieren Windows medien-DRM-geschützten Inhaltsübertragungen erforderlich sind.                      |
| [Beispiele](sample.md)                                                                                                  | Beschreibung von zwei Befehlszeilendesktopanwendungen, die mit diesem Software Development Kit bereitgestellt werden. |
| [Anwendungsübersicht](application-overview.md)                                                                       | Wichtige Konzepte, die in Windows portablen Geräten verwendet werden.                                                             |
| [Programmierhandbuch](programming-guide.md)                                                                             | Wichtige Aufgaben, die eine Anwendung mit schrittweisen Anweisungen und Codeausschnitten ausführen wird.              |
| [Programmierverzeichnis](programming-reference.md)                                                                     | Referenzhandbuch zu den Schnittstellen und Datentypen, die von portierbaren Windows definiert werden.                      |



 

Anwendungen, die auf Windows Media Geräte-Manager oder Windows Image Acquisition erstellt wurden, können über eine Kompatibilitätsebene auf Windows portable Geräte zugreifen.

Microsoft stellt mehrere Treiber für Standardprotokolle und -geräte zur Verfügung, darunter MTP-Geräte (Media Transport Protocol) und MSC-Geräte (Mass Storage Class). Wenn Sie mit dem User-Mode Driver Framework vertraut sind, können Sie eigene Treiber für benutzerdefinierte Geräte entwickeln.

 

 



