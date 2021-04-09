---
title: Verwenden von Funktionen
description: Die Verwendung von Netzwerk Verwaltungsfunktionen untersuchen und Verwalten von Verbindungen (Verwendungen) zwischen Arbeitsstationen und Servern. Die use-Funktionen sind nachfolgend aufgeführt.
ms.assetid: ddf1b8dc-f13b-402a-9e4e-e4944a29ac31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cbd2660b911fd87c39b9db10b0dbfea0e47c484c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858427"
---
# <a name="use-functions"></a>Verwenden von Funktionen

Die Verwendung von Netzwerk Verwaltungsfunktionen untersuchen und Verwalten von Verbindungen (Verwendungen) zwischen Arbeitsstationen und Servern. Die use-Funktionen sind nachfolgend aufgeführt.



| Funktion                               | BESCHREIBUNG                                                                               |
|----------------------------------------|-------------------------------------------------------------------------------------------|
| [**"Nettuseadd"**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd)         | Erstellt eine Verbindung zwischen einem lokalen Computer und einem Server.                               |
| [**"Nettusedel"**](/windows/desktop/api/Lmuse/nf-lmuse-netusedel)         | Beendet eine Verbindung mit einer freigegebenen Ressource.                                                   |
| [**"Nettuseenum"**](/windows/desktop/api/Lmuse/nf-lmuse-netuseenum)       | Listet alle aktuellen Verbindungen zwischen dem lokalen Computer und den Ressourcen auf Remote Servern. |
| [**"Nettusegetinfo"**](/windows/desktop/api/Lmuse/nf-lmuse-netusegetinfo) | Gibt Informationen zu einer Verbindung mit einer freigegebenen Ressource zurück.                              |



 

Diese Funktion gilt nur für den Server Message Block-Client (LAN Manager-Arbeitsstation). Die Funktion " **nettusegetinfo** " unterstützt keine verteiltes Dateisystem Freigaben (DFS). Um Verbindungsinformationen für eine freigegebene Ressource mithilfe eines anderen Netzwerk Anbieters (z. b. WebDAV oder eine DFS-Freigabe) abzurufen, verwenden Sie die [**WNetGetConnection**](/windows/desktop/api/winnetwk/nf-winnetwk-wnetgetconnectiona) -Funktion.

Verbindungen werden von Sitzungen unterschieden: eine *Sitzung* wird erstellt, wenn eine Arbeitsstation das erste Mal eine Verbindung mit einer freigegebenen Ressource auf dem Server herstellt. Bis zum Ende der Sitzung sind alle zusätzlichen Verbindungen zwischen der Arbeitsstation und dem Serverteil derselben Sitzung. Es können zwei Arten von Verbindungen hergestellt werden: Gerätenamen Verbindungen (die nur explizit sein können) und UNC (Universal Naming Convention)-Verbindungen (die explizit oder implizit sein können).

*Verbindungen* werden pro Benutzer hergestellt. Eine Verbindung, die von einem Benutzer hergestellt wird, wird gelöscht, wenn sich der Benutzer abmeldet. Aus diesem Grund sind die Verwendungs Funktionen der Netzwerkverwaltung nur lokal, da eine von einem Remote Benutzer aufgelegte Verbindung für andere Benutzer nicht zugänglich ist, auch für den Benutzer, der auf diesem Computer interaktiv angemeldet war.

Die Funktion " [**nettuseadd**](/windows/desktop/api/Lmuse/nf-lmuse-netuseadd) " richtet eine explizite Verbindung zwischen dem lokalen Computer und einer auf einem Server freigegebenen Ressource ein, indem ein lokaler Gerätename an den Freigabe Namen einer Remote Server Ressource umgeleitet wird ( \\ \\ *Server* Name \\ *ShareName*). Nachdem eine Gerätenamen Verbindung hergestellt wurde, können Benutzer oder Anwendungen die Remote Ressource verwenden, indem Sie den Namen des lokalen Geräts angeben.

Implizite UNC-Verbindungen werden von der Funktion hergestellt, die für die Verbindung verantwortlich ist. Zum Einrichten einer impliziten UNC-Verbindung übergibt eine Anwendung den Freigabe Namen einer Ressource an jede Funktion, die UNC-Pfade akzeptiert. Die-Funktion akzeptiert den UNC-Namen und stellt eine Verbindung mit dem angegebenen Freigabe Namen her. Alle weiteren Anforderungen für diese Verbindung erfordern den vollständigen Freigabe Namen.

Die use-Funktionen sind auf den folgenden Informationsebenen verfügbar:

-   [**Verwenden von \_ Informationen \_ 0**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_0)
-   [**Verwenden von \_ Informationen \_ 1**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_1)
-   [**Verwenden von \_ Informationen \_ 2**](/windows/desktop/api/Lmuse/ns-lmuse-use_info_2)

 

 