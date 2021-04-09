---
title: Sitzungs Funktionen (Netzwerkverwaltung)
description: Die Funktionen der Netzwerk Verwaltungssitzung Steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern hergestellt werden. Die Funktionen erfordern, dass der Server Dienst auf dem Server gestartet wird.
ms.assetid: ef912cd9-be5c-4202-89aa-e60f275e8938
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06b1e0236881b50f0363a6c872394cfe42f44748
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "103858604"
---
# <a name="session-functions-network-management"></a>Sitzungs Funktionen (Netzwerkverwaltung)

Die Funktionen der Netzwerk Verwaltungssitzung Steuern Netzwerksitzungen, die zwischen Arbeitsstationen und Servern hergestellt werden. Die Funktionen erfordern, dass der Server Dienst auf dem Server gestartet wird.

Die Sitzungs Funktionen sind nachfolgend aufgeführt.



| Funktion                                      | BESCHREIBUNG                                                                                       |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------|
| [**"Netzessiondel"**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel)         | Löscht die aktuellen Verbindungen zwischen einer Arbeitsstation und einem Server. beendet die Netzwerksitzung. |
| [**"Netzessionaufumum"**](/windows/desktop/api/lmshare/nf-lmshare-netsessionenum)       | Gibt Informationen zu allen aktuellen Sitzungen zurück, die für einen Server eingerichtet wurden.                          |
| [**"Netzessiongetinfo"**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) | Gibt Informationen zu einer bestimmten Sitzung zurück.                                                   |



 

Eine *Sitzung* ist eine Verknüpfung zwischen einer Arbeitsstation und einem Server. Eine Sitzung wird erstellt, wenn eine Arbeitsstation zum ersten Mal eine Verbindung mit einer freigegebenen Ressource auf dem Server herstellt. Bis zum Ende der Sitzung sind alle weiteren Verbindungen zwischen der Arbeitsstation und dem Serverteil derselben Sitzung. Um eine Sitzung zu beenden, ruft eine Anwendung auf dem Server Ende einer Verbindung die Funktion " [**netzessiondel**](/windows/desktop/api/lmshare/nf-lmshare-netsessiondel) " auf.

Die Funktionen der Netzwerk Verwaltungssitzung verwalten die Informationen auf Benutzerbasis mit dem *username* -Parameter. Da mehrere Benutzer pro Sitzung vorhanden sein können, ist dieser Parameter erforderlich, um auf die benutzerspezifischen Informationen der Sitzung zuzugreifen.

Sitzungs Funktionen sind auf den folgenden Informationsebenen verfügbar:

-   [**Sitzungs \_ Informationen \_ 0**](/windows/desktop/api/lmshare/ns-lmshare-session_info_0)
-   [**Sitzungs \_ Informationen \_ 1**](/windows/desktop/api/lmshare/ns-lmshare-session_info_1)
-   [**Sitzungs \_ Informationen \_ 2**](/windows/desktop/api/lmshare/ns-lmshare-session_info_2)
-   [**Sitzungs \_ Informationen \_ 10**](/windows/desktop/api/lmshare/ns-lmshare-session_info_10)
-   [**Sitzungs \_ Informationen \_ 502**](/windows/desktop/api/lmshare/ns-lmshare-session_info_502)

Wenn Sie für Active Directory programmieren, können Sie möglicherweise bestimmte Active Directory Service Interface (ADSI)-Methoden aufrufen, um die gleiche Funktionalität zu erreichen, die Sie durch Aufrufen der Funktionen der Netzwerk Verwaltungssitzung erreichen können. Weitere Informationen finden Sie unter [**iadssession**](/windows/desktop/api/iads/nn-iads-iadssession) und [**iadsfileserviceoperations**](/windows/desktop/api/iads/nn-iads-iadsfileserviceoperations).

 

 
