---
description: Grundlegendes zu Sitzungsfunktionen in der Verwaltung von Netzwerkfreigaben. Diese Funktionen steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern eingerichtet werden.
ms.assetid: 931455e3-1301-4a68-93c3-2674b3d4c491
title: Sitzungsfunktionen (Netzwerkfreigabeverwaltung)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa914bd747f8b47e4bc4086245f425ba2d290fb9b0a6de256781a9fbca7e1516
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119580340"
---
# <a name="session-functions-network-share-management"></a>Sitzungsfunktionen (Netzwerkfreigabeverwaltung)

Die Netzwerkverwaltungssitzungsfunktionen steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern eingerichtet werden. Die Funktionen erfordern, dass der Serverdienst auf dem Server gestartet wird.

Die Sitzungsfunktionen sind im Folgenden aufgeführt.



| Funktion                                       | Beschreibung                                                                                       |
|------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**NetSessionDel**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel)         | Löscht die aktuellen Verbindungen zwischen einer Arbeitsstation und einem Server. beendet die Netzwerksitzung. |
| [**NetSessionEnum**](/windows/desktop/api/Lmshare/nf-lmshare-netsessionenum)       | Gibt Informationen zu allen aktuellen Sitzungen zurück, die für einen Server eingerichtet wurden.                          |
| [**NetSessionGetInfo**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiongetinfo) | Gibt Informationen zu einer bestimmten Sitzung zurück.                                                   |



 

Eine *Sitzung* ist eine Verknüpfung zwischen einer Arbeitsstation und einem Server. Beim ersten Herstellen einer Verbindung zwischen einer Arbeitsstation und einer freigegebenen Ressource auf dem Server wird eine Sitzung eingerichtet. Bis zum Ende der Sitzung sind alle weiteren Verbindungen zwischen der Arbeitsstation und dem Server Teil derselben Sitzung. Um eine Sitzung zu beenden, ruft eine Anwendung auf dem Serverende einer Verbindung die [**NetSessionDel-Funktion**](/windows/desktop/api/Lmshare/nf-lmshare-netsessiondel) auf.

Die Netzwerkverwaltungssitzungsfunktionen verwalten Informationen pro Benutzer mit dem *Parameter username.* Da es mehrere Benutzer pro Sitzung geben kann, ist dieser Parameter erforderlich, um auf die benutzerspezifischen Informationen für die Sitzung zuzugreifen.

Sitzungsfunktionen sind auf fünf Informationsebenen verfügbar:

<dl>

[**\_SITZUNGSINFORMATIONEN \_ 0**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_0)  
[**\_SITZUNGSINFORMATIONEN \_ 1**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_1)  
[**\_SITZUNGSINFORMATIONEN \_ 2**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_2)  
[**\_SITZUNGSINFORMATIONEN \_ 10**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_10)  
[**\_SITZUNGSINFORMATIONEN \_ 502**](/windows/desktop/api/Lmshare/ns-lmshare-session_info_502)  
</dl>

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte ADSI-Methoden (Active Directory Service Interface) aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Netzwerkverwaltungssitzungsfunktionen erreichen können. Weitere Informationen finden Sie unter [**IADsSession**](/windows/desktop/api/iads/nn-iads-iadssession) und [**IADsFileServiceOperations.**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations)

 

 
