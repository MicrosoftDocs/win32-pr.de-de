---
title: Informationen zum Gerätezugriffs-API
description: Die Gerätezugriffs-API richtet sich an C++-Entwickler, die eine Windows Store-App erstellen, um mit spezialisierten Geräten in Windows 8 zu interagieren.
ms.assetid: DDF115A2-A811-450A-80F7-AAFB0EEA4037
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 08d603e74ff33250bbc5a65e440fc47a0103cd6eb996badf94dbdc51b6b2d3e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755020"
---
# <a name="about-the-device-access-api"></a>Informationen zum Gerätezugriffs-API

Die Gerätezugriffs-API richtet sich an C++-Entwickler, die eine Windows Store-App erstellen, um mit spezialisierten Geräten in Windows 8 zu interagieren. In diesem Thema werden die Szenarien beschrieben, für die die Gerätezugriffs-API gilt. Außerdem wird erläutert, wie der Gerätezugriffs-API Sicherheitsregeln für Windows Store Apps in Windows 8 anwendet.

- [Aktivieren von benutzerdefinierten Gerätefunktionen in Windows Store Geräte-Apps](#enabling-custom-device-functionality-in-windows-store-device-apps)

## <a name="enabling-custom-device-functionality-in-windows-store-device-apps"></a>Aktivieren von benutzerdefinierten Gerätefunktionen in Windows Store Geräte-Apps

Entwickler für unabhängige Hardwarehersteller (Independent Hardware Vendors, IHVs) und OEMs können eine Windows Store-App erstellen, die mit ihrem Gerät gekoppelt und automatisch bei der Installation des Geräts erworben wird. Diese App, die als Windows Store-Geräte-App bezeichnet wird, kann einzigartige Gerätefunktionen bereitstellen.

Geräte ohne integrierte Klassentreiber oder Windows Runtime-APIs für die Kommunikation mit dem Gerät in Windows 8 werden als *spezialisierte Geräte* bezeichnet. Für diese Geräte ist möglicherweise ein benutzerdefinierter Treiber erforderlich. Weitere Informationen zu den Gerätetypen, die benutzerdefinierte Treiber erfordern, finden Sie im Windows Store Geräte-App-Entwurfshandbuch für spezialisierte Geräte.

Die Windows Store Geräte-App für ein spezialisiertes Gerät, das mit dem benutzerdefinierten Treiber eines Geräts kommunizieren muss, kann keine Microsoft Win32-APIs wie [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) und [**CreateFile**](/windows/win32/api/fileapi/nf-fileapi-createfilea) verwenden, um IOCTLs an das Gerät zu senden. Die eingeschränkte Sicherheitsumgebung, in der Windows Store Geräte-Apps ausgeführt werden, erfordert, dass Sie die Gerätezugriffs-API verwenden, um über eine Windows Store-App mit Ihrem benutzerdefinierten Treiber zu kommunizieren.

Der Entwickler eines benutzerdefinierten Geräts schränkt den Zugriff auf genehmigte, privilegierte Anwendungen ein. Der Hersteller eines Media Player-Geräts möchte beispielsweise, dass Benutzer Musik nur über die von der IHV bereitgestellte Musik-App wiedergeben und die Synchronisierung von Medien vom Gerät durch die App eines Beliebigen Mitbewerbers einschränken. Wenn Sie den Gerätetreiber erstellen, legen Sie eine Eigenschaft in der Informationsdatei (INF) fest, um anzugeben, dass nur privilegierte Apps auf das Gerät zugreifen können. Metadaten auf dem Gerät selbst geben die Paket-IDs für den Satz genehmigter Apps an. Weitere Informationen zum Festlegen dieser Metadaten auf Ihrem Gerät finden Sie unter [UWP-Geräte-Apps für interne Geräte.](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices)

## <a name="related-topics"></a>Zugehörige Themen

Beispiel für [benutzerdefinierten Treiberzugriff,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [UWP-Geräte-Apps für interne Geräte](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)