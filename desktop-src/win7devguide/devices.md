---
title: Geräte (Windows 7 Entwicklerhandbuch)
description: Geräte sind ein grundlegender Bestandteil der PC-Erfahrung, und Windows 7 bietet Entwicklern von Anwendungen, die mit Geräten interagieren, neue Möglichkeiten.
ms.assetid: faed8ec8-2f12-4090-a003-b14b3d26e02a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 775389f1a3548e2e94b8b2c25f9b46560cef5fc61a5e486f5dff28871da9f9e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086733"
---
# <a name="devices-windows-7-developer-guide"></a>Geräte (Windows 7 Entwicklerhandbuch)

Geräte sind ein grundlegender Bestandteil der PC-Erfahrung, und Windows 7 bietet Entwicklern von Anwendungen, die mit Geräten interagieren, neue Möglichkeiten. Die Plattform für die Geräteerfahrung ermöglicht die Zuordnung von Anwendungen und Diensten zu einem bestimmten Gerät, sodass Benutzer sofort nach der Verbindung von ihren Peripheriegeräten profitieren können. Die Sensorplattform bietet eine Reihe von APIs für die Ermittlung und Kommunikation mit Sensorgeräten, die eine neue Generation von Anwendungen ermöglichen, die ihre Umgebungen kennen. Die Standortplattform bietet neue APIs für die Verwendung von Standortdaten eines GPS-Empfängers (Global Positioning Systems) oder anderer Dienste, die standortspezifisches Anwendungsverhalten für mobile Benutzer ermöglichen. (Weitere Informationen [finden Sie unter Geräteprinzipien – Übersicht.)](https://www.microsoft.com/whdc/device/default.mspx)

## <a name="device-experience-platform"></a>Plattform für die Geräteerfahrung

Windows 7 kombiniert Software und Dienste, um interessante neue Erfahrungen für Mobiltelefone, portable Medienplayer, Kameras und Drucker zu schaffen. Windows 7 erleichtert die direkte Verwendung dieser Geräte über den Windows Desktop. Außerdem bietet es Geräteherstellern eine wichtige Platzierung auf dem Windows-Desktop mit Brandingmöglichkeiten und einer einfachen Schnittstelle zum Präsentieren der Funktionen und Dienste, die das Gerät unterstützt.

Über die Plattform für die Geräteerfahrung wird jede Windows-Sitzung zu einem Portal für Kunden, um von ihren Geräten mehr Nutzen zu erhalten. Die Geräteplattform ermöglicht es Benutzern, eine Verbindung mit dem Gerätehersteller herzustellen, verwandte Dienste zu entdecken und zu verwenden und sich über Zubehör zu informieren. Da die Geräteerfahrung mit den Webdiensten von Microsoft verbunden ist, können Geräteunternehmen die Benutzererfahrung auch nach dem Versand an Kunden aktualisieren. Die Device Experience Platform kann eine anwendungsspezifische Erfahrung für gerätespezifische Windows, z. B. Mobiltelefone, generieren.

Die Device Experience Platform ermöglicht Anwendungen den Zugriff auf Geräte wie Mobiltelefone und Medienplayer, die Dienste über das *Media Transfer Protocol (MTP)* oder das Windows [Portable Devices-Treibermodell](https://www.bing.com/search?q=Windows+Portable+Devices) implementieren.

Um die Synchronisierung persönlicher Informationen zwischen einem PC und einem Gerät zu aktivieren, hostet die Geräteplattform eine neue Synchronisierungsplattform für verbundene Geräte und stellt eine Benutzeroberfläche zum Auswählen von Zielanwendungen für die Datensynchronisierung bereit, z. B. **Kontakte,** **Kalender** und **Aufgaben**. (Siehe [Windows Geräteerfahrung.)](https://www.microsoft.com/whdc/device/DeviceExperience/default.mspx)

## <a name="windows-biometric-framework"></a>Windows-Biometrieframework

Das Windows Biometric Framework (WBF) stellt eine API bereit, mit der Anwendungen Fingerabdruckgeräte verwenden können, um Benutzeridentitäten zu registrieren, zu identifizieren und zu überprüfen, ohne direkten Zugriff auf biometrische Fingerabdruckhardware oder -stichproben zu erhalten. Sie können WBF mit Fingerabdruckgeräten verwenden, die über Windows-Treiber (Biometric Device Interface, WBDI) verfügen. WBF ist über Plug-In-Adapter erweiterbar, die die Sensorkommunikation, den biometrischen Abgleich und den Vorlagenspeicher verwalten. Dadurch wird sichergestellt, dass WBF mit einer Vielzahl von Fingerabdrucksensoren verwendet werden kann. In Windows 7 können Fingerabdruckleser WBF für die Authentifizierung während *der UAC* und Windows verwenden. (Siehe [Windows Biometrieframework-API](../secbiomet/biometric-service-api-portal.md).)

 

 
