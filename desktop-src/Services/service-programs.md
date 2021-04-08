---
description: Ein Dienstprogramm enthält ausführbaren Code für einen oder mehrere Dienste.
ms.assetid: 697db543-6149-46ac-add3-c8c6ca3aadbe
title: Dienstprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b5e78574f46549956325bc19ffb6d51f4a114ff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868187"
---
# <a name="service-programs"></a>Dienstprogramme

Ein *Dienstprogramm* enthält ausführbaren Code für einen oder mehrere Dienste. Ein Dienstprogramm, das mit dem typdienst Win32-Prozess erstellt wurde, \_ \_ \_ enthält den Code für nur einen Dienst. Ein Dienstprogramm, das mit dem typdienst \_ Win32- \_ Freigabeprozess erstellt wurde \_ , enthält Code für mehr als einen Dienst, der Ihnen die Freigabe von Code ermöglicht. Ein Beispiel für ein Dienstprogramm, das dies tut, ist der generische Dienst Host Prozess, Svchost.exe, der interne Windows-Dienste hostet. Beachten Sie, dass Svchost.exe für die Verwendung durch das Betriebssystem reserviert ist und nicht von nicht-Windows-Diensten verwendet werden sollte. Stattdessen sollten Entwickler eigene Dienst hostingprogramme implementieren.

Ein Dienstprogramm kann so konfiguriert werden, dass es im Kontext eines Benutzerkontos entweder über die integrierte (lokale), primäre oder vertrauenswürdige Domäne ausgeführt wird. Sie kann auch so konfiguriert werden, dass Sie in einem speziellen [Dienst Benutzerkonto](service-user-accounts.md)ausgeführt wird.

In den folgenden Themen werden die Schnittstellen Anforderungen des [Dienststeuerungs-Managers](service-control-manager.md) (SCM) beschrieben, die ein Dienstprogramm enthalten muss:

-   [Dienst Einstiegspunkt](service-entry-point.md)
-   [ServiceMain-Dienstfunktion](service-servicemain-function.md)
-   [Dienststeuerungshandler-Funktion](service-control-handler-function.md)

Diese Themen gelten nicht für Treiber Dienste. Informationen zu den Schnittstellen Anforderungen für Treiber Dienste finden Sie im Windows-Treiberkit (WDK).

Ein Dienst wird als Hintergrundprozess ausgeführt, der sich auf die Systemleistung, Reaktionsfähigkeit, Energieeffizienz und Sicherheit auswirkt. Richtlinien zur Dienst Optimierung finden Sie unter [entwickeln effizienter Hintergrundprozesse für Windows](/windows-hardware/drivers/kernel/implementing-power-management). In den folgenden Themen werden zusätzliche Überlegungen zur Programmierung beschrieben:

-   [Dienststatus Übergänge](service-status-transitions.md)
-   [Empfangen von Ereignissen in einem Dienst](receiving-events-in-a-service.md)
-   [Multithread-Dienste](multithreaded-services.md)
-   [Dienste und die Registrierung](services-and-the-registry.md)
-   [Dienste und umgeleitete Laufwerke](services-and-redirected-drives.md)
-   [Dienst Triggerereignisse](service-trigger-events.md)

Beachten Sie Folgendes: Wenn das Dienstprogramm als RPC-Server fungiert, sollte es dynamische Endpunkte und gegenseitige Authentifizierung verwenden.

 

 
