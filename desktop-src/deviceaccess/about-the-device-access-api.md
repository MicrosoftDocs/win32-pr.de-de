---
title: Informationen zur Geräte Zugriffs-API
description: Die Geräte Zugriffs-API ist für C++-Entwickler gedacht, die eine Windows Store-App für die Interaktion mit spezialisierten Geräten in Windows 8 erstellen.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 213c7ecc618e4b183ee879d23db3b2c0eca35397
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "104316730"
---
# <a name="about-the-device-access-api"></a>Informationen zur Geräte Zugriffs-API

Die Geräte Zugriffs-API ist für C++-Entwickler gedacht, die eine Windows Store-App für die Interaktion mit spezialisierten Geräten in Windows 8 erstellen. In diesem Thema werden die Szenarien beschrieben, auf die sich die Geräte Zugriffs-API bezieht. Außerdem wird erläutert, wie die Geräte Zugriffs-API Sicherheitsregeln für Windows Store-Apps in Windows 8 anwendet.

- [Aktivieren von benutzerdefinierter Gerätefunktionen in Windows Store-Geräte-apps](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Aktivieren von benutzerdefinierter Gerätefunktionen in Windows Store-Geräte-apps

Entwickler von unabhängigen Hardwareanbietern (IHVs) und OEMs können eine Windows Store-App erstellen, die mit Ihrem Gerät gekoppelt und automatisch abgerufen wird, wenn das Gerät installiert wird. Diese APP, die als Windows Store-Geräte-App bezeichnet wird, kann eindeutige Gerätefunktionen bereitstellen.

Geräte, die nicht über integrierte Klassen Treiber oder Windows-Runtime-APIs für die Kommunikation mit dem Gerät in Windows 8 verfügen, werden als *spezialisierte Geräte* bezeichnet. Diese Geräte erfordern möglicherweise einen benutzerdefinierten Treiber. Weitere Informationen zu den Gerätetypen, die benutzerdefinierte Treiber erfordern, finden Sie im Entwurfs Handbuch für Geräte-Apps für Windows Store für spezialisierte Geräte.

Die Windows Store-Geräte-App für ein spezielles Gerät, das mit dem benutzerdefinierten Treiber eines Geräts kommunizieren muss, kann nicht mit Microsoft-Win32-APIs wie [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) und " [**kreatefile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) " IOCTLs an das Gerät senden. Die eingeschränkte Sicherheitsumgebung, in der Windows Store-Geräte-apps ausgeführt werden, erfordert, dass Sie die Geräte Zugriffs-API für die Kommunikation mit Ihrem benutzerdefinierten Treiber über eine Windows Store-App verwenden

Der Entwickler eines benutzerdefinierten Geräts schränkt den Zugriff auf genehmigte, privilegierte Anwendungen ein. Beispielsweise möchte der Hersteller eines Media Player-Geräts möglicherweise, dass Benutzer Musik nur über die IHV-bereitgestellte Musik-app abspielen und die APP des Wettbewerbs auf das Synchronisieren von Medien vom Gerät einschränken. Wenn Sie den Gerätetreiber entwickeln, legen Sie eine Eigenschaft in der Informationsdatei (INF) fest, um anzugeben, dass nur privilegierte apps auf das Gerät zugreifen können. Mit den Metadaten auf dem Gerät selbst werden die Paket-IDs für den Satz genehmigter apps angegeben. Ausführlichere Informationen zum Festlegen dieser Metadaten auf Ihrem Gerät finden Sie unter [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) .

## <a name="related-topics"></a>Zugehörige Themen

[Beispiel für benutzerdefinierten Treiber Zugriff](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware dev Center](/windows-hardware/drivers/)