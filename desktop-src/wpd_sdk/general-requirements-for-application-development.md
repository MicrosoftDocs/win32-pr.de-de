---
description: Allgemeine Anforderungen für die Anwendungsentwicklung
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Allgemeine Anforderungen für die Anwendungsentwicklung (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ad1ed207774494102f673bd7fb4f92acbdcb4629542d238613637d9509336c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118430879"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Allgemeine Anforderungen für die Anwendungsentwicklung (WPD-API)

Zum Erstellen einer Windows Portable Devices-Anwendung muss das [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) auf Ihrem Computer installiert sein. Die erforderlichen Header und Bibliotheken werden in der folgenden Liste angezeigt.

-   PortableDeviceGuids.lib
-   PortableDevice.h
-   PortableDeviceTypes.h
-   PortableDeviceApi.h
-   Alle anderen erforderlichen Bibliotheken und Header, die ihre Anwendung zum Nutzen oder Rendern von Mediendateien benötigt.

Wenn Ihre Anwendung die neuen Gerätedienstschnittstellen unterstützt, enthält sie auch eine oder mehrere der folgenden Headerdateien.

-   AnchorSyncDeviceService.h
-   BridgeDeviceService.h
-   CalendarDeviceService.h
-   ContactDeviceService.h
-   DeviceServices.h
-   FullEnumSyncDeviceService.h
-   HintsDeviceService.h
-   MessageDeviceService.h
-   MetadataDeviceService.h
-   NotesDeviceService.h
-   RingtoneDeviceService.h
-   StatusDeviceService.h
-   SyncDeviceService.h
-   TaskDeviceService.h

Von den Dateien in der vorherigen Liste sind BridgeDeviceService.h und DeviceService.h für fast jede Anwendung erforderlich, die Gerätedienste unterstützt. Die anderen Dateien definieren verschiedene Arten von Gerätediensten und werden entsprechend einbezogen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Windows Portable Geräte**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
