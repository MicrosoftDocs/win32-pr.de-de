---
title: Netzwerk Verwaltungs Funktionsgruppen
description: Die Netzwerk Verwaltungsfunktionen können in die folgenden Gruppen unterteilt werden.
ms.assetid: 4b5d3554-f81a-4ecf-bf31-ee4753509f38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bce5c0fb3dd70facb0ebbbb2479b968d428c49e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039160"
---
# <a name="network-management-function-groups"></a>Netzwerk Verwaltungs Funktionsgruppen

Die Netzwerk Verwaltungsfunktionen können in die folgenden Gruppen unterteilt werden:

-   [Benachrichtigungsfunktionen](alert-functions.md)
-   [Apibuffer-Funktionen](apibuffer-functions.md)
-   [Verzeichnisdienst Funktionen](directory-service-functions.md)
-   [Verteiltes Dateisystem (DFS)-Funktionen](/previous-versions/windows/desktop/dfs/distributed-file-system-dfs-functions)
-   [Get-Funktionen](get-functions.md)
-   [Gruppenfunktionen](group-functions.md)
-   [Lokale Gruppenfunktionen](local-group-functions.md)
-   [Nachrichten Funktionen](message-functions.md)
-   [Netfile-Funktionen](netfile-functions.md)
-   [Remote Utility-Funktionen](remote-utility-functions.md)
-   [Zeit Plan Funktionen](schedule-functions.md)
-   [Server Funktionen](server-functions.md)
-   [Server-und Arbeitsstations Transport-Funktionen](server-and-workstation-transport-functions.md)
-   [Sitzungs Funktionen](session-functions.md)
-   [Freigabe Funktionen](share-functions.md)
-   [Statistikfunktionen](/windows/desktop/NetShare/statistics-functions)
-   [Verwenden von Funktionen](use-functions.md)
-   [Benutzer Funktionen](user-functions.md)
-   [Modale Benutzer Funktionen](user-modal-functions.md)
-   [Benutzer Funktionen für Arbeitsstationen und Arbeitsstationen](workstation-and-workstation-user-functions.md)

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Schnittstellen Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie erreichen können, indem Sie bestimmte Netzwerk Verwaltungsfunktionen aufrufen. Weitere Informationen finden Sie unter [Mapping von ADSI-Schnittstellen zu den Netzwerk Verwaltungsfunktionen](mapping-adsi-interfaces-to-the-network-management-functions.md).

Das System stellt auch einen Netzwerk unabhängigen Satz von Netzwerkfunktionen ([WNET-Funktionen](/windows/desktop/WNet/wnet-functions)) bereit, die es ermöglichen, dass Netzwerkfunktionen über unterschiedliche Produkte von Netzwerk Herstellern hinweg funktionieren. Wenn die Anwendung für die Verwendung einer WNET-Funktion konvertiert werden kann, sollten Sie die Konvertierung durchführen. Es gibt Gründe, die Änderungen vorzunehmen:

-   Die WNET-Funktionen sind Netzwerk unabhängig, während die Netzwerk Verwaltungsfunktionen nur in Microsoft-Netzwerken funktionieren.
-   Einige der Funktionen werden möglicherweise in zukünftigen Versionen von Microsoft-Betriebssystemen nicht unterstützt, wenn Sie abgelöst wurden. Microsoft plant nicht, bestimmte Funktionen zu entfernen, es sei denn, es ist eine entsprechende oder eine bessere Funktionalität verfügbar.

 

 