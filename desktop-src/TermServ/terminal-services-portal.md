---
title: Remotedesktopdienste (Remotedesktopdienste)
description: Microsoft-Remotedesktop Services ist eine Remote-PC-Zugriffssoftware, die den Remote Desktop Zugriff unterstützt. Remotedesktopdienste verbindet mehrere Clients mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server.
ms.assetid: 90c40b7a-e324-43fc-a1e6-f29997ed9436
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste
- Remotedesktopdienste Remotedesktopdienste, Startseite
- Terminal Dienste finden Sie unter Remotedesktopdienste Remotedesktopdienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f39e176473c98f1e240d58592463df749a95f939
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/10/2020
ms.locfileid: "106341577"
---
# <a name="remote-desktop-services-remote-desktop-services"></a>Remotedesktopdienste (Remotedesktopdienste)

## <a name="purpose"></a>Zweck

Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2 oder Windows Server 2008 mit Remotedesktopdienste (früher als "Terminal Services" bezeichnet) ermöglichen es einem Server, mehrere gleichzeitige Client Sitzungen zu hosten. Remotedesktop verwendet Remotedesktopdienste Technologie, um eine Remote-Remote Sitzung auszuführen. Ein Benutzer kann eine Verbindung mit einem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server (früher als Terminal Server bezeichnet) herstellen, indem er Remotedesktopverbindung (RDC)-Client Software verwendet. Der Remotedesktop-Webverbindung erweitert Remotedesktopdienste Technologie auf das Web.

> [!Note]  
> Dieses Thema ist für Softwareentwickler konzipiert. Wenn Sie nach Benutzerinformationen für Remotedesktop-Verbindungen suchen, finden Sie weitere Informationen unter [Remotedesktopverbindung: häufig gestellte Fragen](https://windows.microsoft.com/windows/remote-desktop-connection-faq#1TC=windows-8).

 

## <a name="where-applicable"></a>Anwendungsbereich

Ein Remotedesktopverbindung-Client (RDC) kann in einer Vielzahl von Formularen vorhanden sein. Bei Thin Client-Hardware Geräten, auf denen ein eingebettetes Windows-basiertes Betriebssystem ausgeführt wird, kann die RDC-Client Software ausgeführt werden, um eine Verbindung mit einem RD-Sitzungshost Server herzustellen Auf Windows-, Macintosh-oder UNIX-basierten Computern kann eine RDC-Client Software ausgeführt werden, um eine Verbindung mit einem RD-Sitzungshost Server herzustellen und Windows-basierte Anwendungen anzuzeigen. Diese Kombination aus RDC-Clients ermöglicht praktisch jedem Betriebssystem den Zugriff auf Windows-basierte Anwendungen.

## <a name="developer-audience"></a>Entwicklergruppe

Entwickler, die Remotedesktopdienste verwenden, sollten mit den Programmiersprachen C und C++ und der Windows-basierten Programmierumgebung vertraut sein. Vertrautheit mit der Client/Server-Architektur ist erforderlich. Der Remotedesktop-Webverbindung enthält Skript fähige Schnittstellen zum Erstellen und Bereitstellen von Skript fähigen virtuellen Kanälen in Remotedesktopdienste Webanwendungen.

## <a name="run-time-requirements"></a>Laufzeitanforderungen

Anwendungen, die Remotedesktopdienste verwenden, erfordern Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008 oder Windows Vista. Um Remotedesktop-Webverbindung Funktionalität verwenden zu können, benötigt die Remotedesktopdienste Client Anwendung Internet Explorer und eine Verbindung mit dem World Wide Web. Informationen zu den Lauf Zeitanforderungen für ein bestimmtes Programmier Element finden Sie im Abschnitt "Anforderungen" der Referenzseite für dieses Element.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Remotedesktop ActiveX-Steuerelement](remote-desktop-activex-control.md)
</dt> <dd>

Beschreibt, wie das Remotedesktop ActiveX-Steuerelement verwendet wird.

</dd> <dt>

[Remotedesktopprotokoll Anbieter-API](custom-remote-desktop-protocols.md)
</dt> <dd>

Verwenden Sie die Remotedesktopprotokoll Anbieter-API, um ein Protokoll zu erstellen, um die Kommunikation zwischen dem Remotedesktopdienste-Dienst und mehreren Clients bereitzustellen.

</dd> <dt>

[Virtuelle Kanäle Remotedesktopdienste](terminal-services-virtual-channels.md)
</dt> <dd>

*Virtuelle Kanäle* sind Software Erweiterungen, die verwendet werden können, um einer Remotedesktopdienste Anwendung funktionale Verbesserungen hinzuzufügen.

</dd> <dt>

[Remotefx-Medien Umleitungs-API](remotefx-api.md)
</dt> <dd>

Die remotefx-Medien Umleitungs-API wird in einer Remotedesktop Sitzung verwendet, um Bereiche des Servers zu identifizieren, die schnell veränderliche Inhalte, z. b. Video, anzeigen. Dieser Inhalt kann dann Video codiert und im codierten Format an den Client gesendet werden.

</dd> <dt>

[Remotedesktopverbindung Broker-Client-API](connection-broker-client-api.md)
</dt> <dd>

Beschreibt, wie die Remotedesktopverbindung Broker-Client-API verwendet wird.

</dd> <dt>

[API-Referenz für den persönlichen Desktop Task-Agent](task-agent-api-reference.md)
</dt> <dd>

Die API für den Personal Desktop Task-Agent wird verwendet, um geplante Updates für einen persönlichen virtuellen Desktop zu verarbeiten.

</dd> <dt>

[Informationen zu Remotedesktopdienste](about-terminal-services.md)
</dt> <dd>

Remotedesktopdienste (früher als "Terminal Services" bezeichnet) bietet ähnliche Funktionen wie eine Terminal basierte, zentralisierte Host-oder Mainframe-Umgebung, in der mehrere Terminals eine Verbindung mit einem Host Computer herstellen.

</dd> <dt>

[Remotedesktop Management Services-Anbieter](rdms-api-reference.md)
</dt> <dd>

Der RDMs-Anbieter (Remotedesktop Management Services) verwaltet virtuelle Desktop Infrastruktur (VDI)-Umgebungen.

</dd> <dt>

[Remotedesktopdienste Referenz](terminal-services-reference.md)
</dt> <dd>

Dokumentation zu Eigenschaften Methoden, die Sie verwenden können, um Remotedesktopdienste Benutzereigenschaften zu überprüfen und zu konfigurieren. Remotedesktopdienste Funktionen, Strukturen und Remotedesktop-Webverbindung Skript fähige-Schnittstellen werden ebenfalls dokumentiert.

</dd> <dt>

[Remotedesktopdienste Tastenkombinationen](terminal-services-shortcut-keys.md)
</dt> <dd>

Eine Liste der Remotedesktopdienste Tastenkombinationen.

</dd> <dt>

[WMI-Anbieter Remotedesktopdienste](terminal-services-wmi-provider.md)
</dt> <dd>

Der Remotedesktopdienste WMI-Anbieter ermöglicht programmgesteuerten Zugriff auf die Informationen und Einstellungen, die vom Microsoft Management Console (MMC)-Snap-in "Remotedesktopdienste Configuration/Connections" verfügbar gemacht werden.

</dd> <dt>

[Verwenden von Remotedesktopdienste](using-terminal-services.md)
</dt> <dd>

Erfahren Sie, wie Sie in der Remotedesktopdienste Umgebung programmieren und Remotedesktopdienste (ehemals Terminaldienstetechnologie) mithilfe Remotedesktop-Webverbindung auf das Web erweitern.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Terminal Dienste sind jetzt Remotedesktopdienste](terminal-services-is-now-remote-desktop-services.md)
</dt> </dl>

 

 




