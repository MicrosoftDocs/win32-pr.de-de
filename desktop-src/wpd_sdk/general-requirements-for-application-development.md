---
description: Allgemeine Anforderungen für die Anwendungsentwicklung
ms.assetid: 8ac88d6f-fc4b-4253-932d-aaa3c801b18f
title: Allgemeine Anforderungen für die Anwendungsentwicklung (WPD-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d16be9656f72324b8f3687bca72146320561b0d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216804"
---
# <a name="general-requirements-for-application-development-wpd-api"></a>Allgemeine Anforderungen für die Anwendungsentwicklung (WPD-API)

Zum Erstellen einer Anwendung für tragbare Windows-Geräte muss das [Windows Software Development Kit (SDK)](https://developer.microsoft.com/windows/downloads) auf dem Computer installiert sein. Die erforderlichen Header und Bibliotheken werden in der folgenden Liste angezeigt.

-   Portabledeviceguids. lib
-   Portabledevice. h
-   Portablede vicetypes. h
-   PortableDeviceApi. h
-   Alle anderen erforderlichen Bibliotheken und Header, die von Ihrer Anwendung für die Nutzung oder das Rendering von Mediendateien benötigt werden.

Wenn Ihre Anwendung die neuen Schnittstellen der Geräte Dienste unterstützt, umfasst Sie auch eine oder mehrere der folgenden Header Dateien.

-   Anchorsyncdeviceservice. h
-   Bridgedebug Service. h
-   Calendardebug Service. h
-   Contactdebug Service. h
-   Geräte bereitstell. h
-   Fullenum syncdeviceservice. h
-   Hintde viceservice. h
-   Messagedebug Service. h
-   MetadataDeviceService. h
-   Notesdebug Service. h
-   Ringtonedeviceservice. h
-   Status Update Service. h
-   Syncdeviceservice. h
-   Taskdebug Service. h

Von den Dateien in der vorherigen Liste sind bridgedeviceservice. h und deviceservice. h für fast jede Anwendung erforderlich, die Geräte Dienste unterstützt. die anderen Dateien definieren verschiedene Typen von Geräte Diensten und werden gegebenenfalls eingeschlossen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Tragbare Windows-Geräte**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
