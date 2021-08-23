---
title: Netzwerkverwaltungsfunktionsgruppen
description: Die Netzwerkverwaltungsfunktionen können in die folgenden Gruppen unterteilt werden.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e49a8c45c59031a12653f5cb863fef320a33c93bc60cabdd4cd6fb4aece9dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012508"
---
# <a name="network-management-function-groups"></a>Netzwerkverwaltungsfunktionsgruppen

Die Netzwerkverwaltungsfunktionen können in die folgenden Gruppen unterteilt werden:

-   [Warnungsfunktionen](alert-functions.md)
-   [ApiBuffer-Funktionen](apibuffer-functions.md)
-   [Verzeichnisdienstfunktionen](directory-service-functions.md)
-   [verteiltes Dateisystem (Dfs)-Funktionen](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Get-Funktionen](get-functions.md)
-   [Gruppenfunktionen](group-functions.md)
-   [Lokale Gruppenfunktionen](local-group-functions.md)
-   [Nachrichtenfunktionen](message-functions.md)
-   [NetFile-Funktionen](netfile-functions.md)
-   [Remote-Hilfsprogrammfunktionen](remote-utility-functions.md)
-   [Zeitplanfunktionen](schedule-functions.md)
-   [Serverfunktionen](server-functions.md)
-   [Server- und Arbeitsstationstransportfunktionen](server-and-workstation-transport-functions.md)
-   [Sitzungsfunktionen](session-functions.md)
-   [Freigeben von Funktionen](share-functions.md)
-   [Statistikfunktionen](/windows/desktop/NetShare/statistics-functions)
-   [Verwenden von Funktionen](use-functions.md)
-   [Benutzerfunktionen](user-functions.md)
-   [Modale Benutzerfunktionen](user-modal-functions.md)
-   [Arbeitsstations- und Arbeitsstationsbenutzerfunktionen](workstation-and-workstation-user-functions.md)

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Schnittstellenmethoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie erreichen können, indem Sie bestimmte Netzwerkverwaltungsfunktionen aufrufen. Weitere Informationen finden Sie unter [Zuordnen von ADSI-Schnittstellen zu den Netzwerkverwaltungsfunktionen.](mapping-adsi-interfaces-to-the-network-management-functions.md)

Das System stellt auch einen netzwerkunabhängigen Satz von Netzwerkfunktionen ([WNet-Funktionen](/windows/desktop/WNet/wnet-functions)) zur Verfügung, die es Netzwerkfunktionen ermöglichen, über die Produkte verschiedener Netzwerkanbieter hinweg zu funktionieren. Wenn Ihre Anwendung für die Verwendung einer WNet-Funktion konvertiert werden kann, sollten Sie die Konvertierung durchführen. Es gibt Gründe für die Änderung:

-   Die WNet-Funktionen sind netzwerkunabhängig, während die Netzwerkverwaltungsfunktionen nur in Microsoft-Netzwerken funktionieren.
-   Einige der Funktionen werden in zukünftigen Versionen von Microsoft-Betriebssystemen möglicherweise nicht unterstützt, wenn sie ersetzt wurden. Microsoft plant nicht, bestimmte Funktionen zu entfernen, es sei denn, es sind entsprechende oder bessere Funktionen verfügbar.

 

 