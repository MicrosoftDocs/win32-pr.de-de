---
title: Sitzungsfunktionen (Netzwerkverwaltung)
description: Überprüfen Sie Sitzungsfunktionen, bei denen es sich um eine Netzwerkverwaltungsfunktionsgruppe handelt. Diese Funktionen steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern eingerichtet wurden.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78479391e4dc2d2aa0ced8af16a8b6cf6f3a9b05
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406123"
---
# <a name="session-functions-network-management"></a>Sitzungsfunktionen (Netzwerkverwaltung)

Die Netzwerkverwaltungssitzungsfunktionen steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern eingerichtet wurden. Die Funktionen erfordern, dass der Serverdienst auf dem Server gestartet wird.

Die Sitzungsfunktionen sind im Folgenden aufgeführt.



| Funktion                                      | Beschreibung                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | Löscht die aktuellen Verbindungen zwischen einer Arbeitsstation und einem Server. beendet die Netzwerksitzung. |
| [**NetSessionEnum**](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | Gibt Informationen zu allen aktuellen Sitzungen zurück, die für einen Server eingerichtet wurden.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | Gibt Informationen zu einer bestimmten Sitzung zurück.                                                   |



 

Eine *Sitzung* ist eine Verknüpfung zwischen einer Arbeitsstation und einem Server. Eine Sitzung wird hergestellt, wenn eine Arbeitsstation zum ersten Mal eine Verbindung mit einer freigegebenen Ressource auf dem Server stellt. Bis zum Ende der Sitzung sind alle weiteren Verbindungen zwischen der Arbeitsstation und dem Server Teil derselben Sitzung. Um eine Sitzung zu beenden, ruft eine Anwendung am Serverende einer Verbindung die [**NetSessionDel-Funktion**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) auf.

Die Sitzungsfunktionen für die Netzwerkverwaltung verwalten Informationen auf Benutzerbasis mit dem *Parameter username.* Da es pro Sitzung mehrere Benutzer geben kann, ist dieser Parameter erforderlich, um auf die benutzerspezifischen Informationen für die Sitzung zu zugreifen.

Sitzungsfunktionen sind auf den folgenden Informationsebenen verfügbar:

-   [**\_SITZUNGSINFORMATIONEN \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [**\_SITZUNGSINFORMATIONEN \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [**\_ \_ SITZUNGSINFORMATIONEN 2**](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [**\_SITZUNGSINFORMATIONEN \_ 10**](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [**\_SITZUNGSINFORMATIONEN \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Methoden (Active Directory Service Interface) aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Sitzungsfunktionen für die Netzwerkverwaltung erreichen können. Weitere Informationen finden Sie unter [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) und [**IADsFileServiceOperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
