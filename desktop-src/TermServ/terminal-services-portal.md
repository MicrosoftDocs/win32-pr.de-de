---
title: Remotedesktopdienste (Remotedesktopdienste)
description: Microsoft-Remotedesktop Dienste sind Remote-PC-Zugriffssoftware, die den Remotedesktopzugriff unterstützt. Remotedesktopdienste verbindet mehrere Clients mit einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost).
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste
- Remotedesktopdienste Remotedesktopdienste , Startseite
- Terminaldienste Siehe Remotedesktopdienste Remotedesktopdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 525f62433c10c8c4f750a8ae1abbfa9496f2f096139c182a677c9dbf69ce4a17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999901"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>Remotedesktopdienste (Remotedesktopdienste)

## <a name="purpose"></a>Zweck

Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 mit Remotedesktopdienste (früher als Terminaldienste bezeichnet) ermöglichen einem Server das Hosten mehrerer gleichzeitiger Clientsitzungen. Remotedesktop verwendet Remotedesktopdienste Technologie, damit eine einzelne Sitzung remote ausgeführt werden kann. Ein Benutzer kann eine Verbindung mit einem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) (früher als Terminalserver bezeichnet) herstellen, indem er Remotedesktopverbindung-Clientsoftware (RDC) verwendet. Der Remotedesktop-Webverbindung erweitert Remotedesktopdienste Technologie auf das Web.

> [!Note]  
> Dieses Thema richtet sich an Softwareentwickler. Wenn Sie Benutzerinformationen für Remotedesktop Verbindungen suchen, lesen Sie [Remotedesktopverbindung: häufig gestellte Fragen.](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8)

 

## <a name="where-applicable"></a>Anwendungsbereich

Ein Remotedesktopverbindung-Client (RDC) kann in einer Vielzahl von Formen vorhanden sein. Thin-Clienthardwaregeräte, auf denen ein eingebettetes Windows-basiertes Betriebssystem ausgeführt wird, können die RDC-Clientsoftware ausführen, um eine Verbindung mit einem RD-Sitzungshost-Server herzustellen. Windows-, Macintosh- oder UNIX-basierte Computer können RDC-Clientsoftware ausführen, um eine Verbindung mit einem RD-Sitzungshost Server herzustellen, um Windows-basierte Anwendungen anzuzeigen. Diese Kombination von RDC-Clients ermöglicht den Zugriff auf Windows-basierten Anwendungen von praktisch jedem Betriebssystem aus.

## <a name="developer-audience"></a>Entwicklergruppe

Entwickler, die Remotedesktopdienste verwenden, sollten mit den Programmiersprachen C und C++ und der Windows-basierten Programmierumgebung vertraut sein. Kenntnisse der Client-/Serverarchitektur sind erforderlich. Die Remotedesktop-Webverbindung umfasst skriptfähige Schnittstellen zum Erstellen und Bereitstellen von skriptfähigen virtuellen Kanälen in Remotedesktopdienste Webanwendungen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Anwendungen, die Remotedesktopdienste verwenden, erfordern Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 oder Windows Vista. Um Remotedesktop-Webverbindung Funktionalität zu verwenden, erfordert die Remotedesktopdienste-Clientanwendung Internet Explorer und eine Verbindung mit dem World Wide Web. Informationen zu Laufzeitanforderungen für ein bestimmtes Programmierelement finden Sie im Abschnitt Anforderungen der Referenzseite für dieses Element.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Remotedesktop ActiveX-Steuerelement](remote-desktop-activex-control.md)
</dt> <dd>

Beschreibt die Verwendung des Remotedesktop ActiveX-Steuerelements.

</dd> <dt>

[Remotedesktopprotokoll-Anbieter-API](custom-remote-desktop-protocols.md)
</dt> <dd>

Sie verwenden die Remotedesktopprotokoll-Anbieter-API, um ein Protokoll für die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients zu erstellen.

</dd> <dt>

[Remotedesktopdienste virtueller Kanäle](terminal-services-virtual-channels.md)
</dt> <dd>

*Virtuelle Kanäle* sind Softwareerweiterungen, die verwendet werden können, um einer Remotedesktopdienste Anwendung funktionale Verbesserungen hinzuzufügen.

</dd> <dt>

[RemoteFX Medienumleitungs-API](remotefx-api.md)
</dt> <dd>

Die RemoteFX-Medienumleitungs-API wird in einer Remotedesktop Sitzung verwendet, um Bereiche des Servers zu identifizieren, die sich schnell ändernde Inhalte anzeigen, z. B. Videos. Dieser Inhalt kann dann videocodiert und im codierten Format an den Client gesendet werden.

</dd> <dt>

[Remotedesktopverbindung Broker-Client-API](connection-broker-client-api.md)
</dt> <dd>

Beschreibt die Verwendung der Remotedesktopverbindung Broker-Client-API.

</dd> <dt>

[API-Referenz für den Task-Agent für persönliche Desktops](task-agent-api-reference.md)
</dt> <dd>

Die API des Personal Desktop-Task-Agents wird verwendet, um geplante Updates für einen persönlichen virtuellen Desktop zu verarbeiten.

</dd> <dt>

[Informationen Remotedesktopdienste](about-terminal-services.md)
</dt> <dd>

Remotedesktopdienste (früher als Terminaldienste bezeichnet) bietet Funktionen, die einer terminalbasierten, zentralisierten Host- oder Mainframeumgebung ähneln, in der mehrere Terminals eine Verbindung mit einem Hostcomputer herstellen.

</dd> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> <dd>

Der RDMS-Anbieter (Remotedesktop Management Services) verwaltet VDI-Umgebungen (Virtual Desktop Infrastructure).

</dd> <dt>

[Remotedesktopdienste Referenz](terminal-services-reference.md)
</dt> <dd>

Dokumentation zu Eigenschaftenmethoden, mit denen Sie Remotedesktopdienste Benutzereigenschaften untersuchen und konfigurieren können. Remotedesktopdienste Funktionen, Strukturen und Remotedesktop-Webverbindung skriptfähigen Schnittstellen sind ebenfalls dokumentiert.

</dd> <dt>

[Remotedesktopdienste Tastenkombinationen](terminal-services-shortcut-keys.md)
</dt> <dd>

Eine Liste der Remotedesktopdienste Tastenkombinationen.

</dd> <dt>

[Remotedesktopdienste WMI-Anbieter](terminal-services-wmi-provider.md)
</dt> <dd>

Der Remotedesktopdienste WMI-Anbieter bietet programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom MMC-Snap-In (Remotedesktopdienste Configuration/Connections Microsoft Management Console) verfügbar gemacht werden.

</dd> <dt>

[Verwenden von Remotedesktopdienste](using-terminal-services.md)
</dt> <dd>

Hier erfahren Sie, wie Sie in der Remotedesktopdienste-Umgebung programmieren und Remotedesktopdienste -Technologie (früher als Terminaldienste bezeichnet) mithilfe von Remotedesktop-Webverbindung auf das Web ausdehnen.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Terminaldienste sind jetzt Remotedesktopdienste](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




