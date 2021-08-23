---
title: Verwenden von Funktionen
description: Die Netzwerkverwaltung verwendet Funktionen zum Untersuchen und Verwalten von Verbindungen (Verwendungen) zwischen Arbeitsstationen und Servern. Die Verwendungsfunktionen sind im Folgenden aufgeführt.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f61019f6c6e2785f03eb4e2e9a47ed1953e14662c5664dca41465bc83d7c683d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779510"
---
# <a name="use-functions"></a>Verwenden von Funktionen

Die Netzwerkverwaltung verwendet Funktionen zum Untersuchen und Verwalten von Verbindungen (Verwendungen) zwischen Arbeitsstationen und Servern. Die Verwendungsfunktionen sind im Folgenden aufgeführt.



| Funktion                               | Beschreibung                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**NetUseAdd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Erstellt eine Verbindung zwischen einem lokalen Computer und einem Server.                               |
| [**NetUseDel**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Beendet eine Verbindung mit einer freigegebenen Ressource.                                                   |
| [**NetUseEnum**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Listet alle aktuellen Verbindungen zwischen dem lokalen Computer und Ressourcen auf Remoteservern auf. |
| [**NetUseGetInfo**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Gibt Informationen zu einer Verbindung mit einer freigegebenen Ressource zurück.                              |



 

Diese Funktion gilt nur für den Server Message Block -Client (LAN-Manager-Arbeitsstation). Die **NetUseGetInfo-Funktion** unterstützt keine verteiltes Dateisystem (DFS)-Freigaben. Verwenden Sie die [**WNetGetConnection-Funktion,**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) um Verbindungsinformationen für eine freigegebene Ressource mithilfe eines anderen Netzwerkanbieters (z. B. WebDAV oder DFS-Freigabe) abzurufen.

Verbindungen unterscheiden sich von Sitzungen: Eine *Sitzung* wird hergestellt, wenn eine Arbeitsstation zum ersten Mal eine Verbindung mit einer freigegebenen Ressource auf dem Server stellt. Alle zusätzlichen Verbindungen zwischen der Arbeitsstation und dem Server sind Teil derselben Sitzung, bis die Sitzung beendet wird. Es können zwei Arten von Verbindungen hergestellt werden: Gerätenamenverbindungen (die nur explizit sein können) und UNC-Verbindungen (Universal Naming Convention), die explizit oder implizit sein können.

*Verbindungen* werden pro Benutzer hergestellt. Eine von einem Benutzer hergestellte Verbindung wird gelöscht, wenn sich dieser Benutzer abmeldet. Aus diesem Grund sind die Verwendungsfunktionen der Netzwerkverwaltung nur lokal, da eine von einem Remotebenutzer eingerichtete Verbindung nicht für andere Benutzer zugänglich wäre, auch nicht für den Benutzer, der interaktiv bei diesem Computer angemeldet war.

Die [**NetUseAdd-Funktion**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) stellt eine explizite Verbindung zwischen dem lokalen Computer und einer auf einem Server freigegebenen Ressource durch Umleiten eines lokalen Gerätenamens an den Freigabenamen einer Remoteserverressource \\ \\ *(servername* \\ *sharename*) ein. Sobald eine Gerätenamenverbindung hergestellt wurde, können Benutzer oder Anwendungen die Remoteressource verwenden, indem sie den Namen des lokalen Geräts angeben.

Implizite UNC-Verbindungen werden von der Funktion hergestellt, die für die Verbindung verantwortlich ist. Um eine implizite UNC-Verbindung herzustellen, übergibt eine Anwendung den Freigabenamen einer Ressource an jede Funktion, die UNC-Pfade akzeptiert. Die Funktion akzeptiert den UNC-Namen und stellt eine Verbindung mit dem angegebenen Freigabenamen herstellen. Alle weiteren Anforderungen für diese Verbindung erfordern den vollständigen Freigabenamen.

Die Verwendungsfunktionen sind auf den folgenden Informationsebenen verfügbar:

-   [**VERWENDEN \_ VON INFO \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**VERWENDEN \_ VON INFO \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**VERWENDEN \_ VON INFO \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 