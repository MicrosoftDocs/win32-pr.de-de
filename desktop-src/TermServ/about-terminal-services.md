---
title: Informationen zu Remotedesktopdienste
description: Remotedesktopdienste (früher als "Terminal Services" bezeichnet) bietet ähnliche Funktionen wie eine Terminal basierte, zentralisierte Host-oder Mainframe-Umgebung, in der mehrere Terminals eine Verbindung mit einem Host Computer herstellen.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4644170cfca3b4bacdd6db647e35549d56844e9b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340651"
---
# <a name="about-remote-desktop-services"></a>Informationen zu Remotedesktopdienste

Remotedesktopdienste (früher als "Terminal Services" bezeichnet) bietet ähnliche Funktionen wie eine Terminal basierte, zentralisierte Host-oder Mainframe-Umgebung, in der mehrere Terminals eine Verbindung mit einem Host Computer herstellen. Jedes Terminal stellt einen Kanal für die Eingabe und die Ausgabe zwischen einem Benutzer und dem Host Computer bereit. Ein Benutzer kann sich an einem Terminal anmelden und dann Anwendungen auf dem Host Computer ausführen, auf Dateien, Datenbanken, Netzwerkressourcen usw. zugreifen. Jede Terminalsitzung ist unabhängig, und das Host Betriebssystem verwaltet Konflikte zwischen mehreren Benutzern für gemeinsame Ressourcen.

Der Hauptunterschied zwischen Remotedesktopdienste und der herkömmlichen Main Frame-Umgebung besteht darin, dass die dummyterminals in einer Main Frame-Umgebung nur zeichenbasierte Eingaben und Ausgaben bereitstellen. Ein-Remotedesktopverbindung (RDC)-Client oder-Emulator stellt eine komplette grafische Benutzeroberfläche bereit, einschließlich eines Windows-Betriebssystem Desktops und Unterstützung für eine Vielzahl von Eingabegeräten, z. b. Tastatur und Maus.

In der Remotedesktopdienste-Umgebung wird eine Anwendung vollständig auf dem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server (ehemals Terminal Server) ausgeführt. Der RDC-Client führt keine lokale Verarbeitung der Anwendungssoftware aus. Der Server überträgt die grafische Benutzeroberfläche an den Client. Der Client überträgt die Eingabe des Benutzers an den Server zurück.

Weitere Informationen finden Sie in den nachfolgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Ändern der Standardeinstellung für Geräte Umleitung](modify-device-redirection-default-.md)
</dt> <dd>

Da Remotedesktop Gatewayserver versuchen, sichere Geräte Umleitungs Richtlinien zu erzwingen, bevor Sie die Client Verbindung an einen Remotedesktop-Sitzungshost Server weiterleiten, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.

</dd> <dt>

[Remotedesktopprotokoll](remote-desktop-protocol.md)
</dt> <dd>

Das Microsoft-Remotedesktop Protokoll (RDP) bietet Remote Anzeige-und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden.

</dd> <dt>

[Remotedesktopdienste-API](terminal-services-api.md)
</dt> <dd>

Die Remotedesktopdienste-API ist in erster Linie für Client/Server-Anwendungen und-Anwendungen zur Remotedesktopdienste Verwaltung nützlich.

</dd> <dt>

[Remotedesktopdienste Verwaltungs Anwendungen](terminal-services-management-applications.md)
</dt> <dd>

Beschreibt die Verwaltungs Anwendungen, die von Remotedesktopdienste unterstützt werden.

</dd> <dt>

[Programmier Richtlinien für Remotedesktopdienste](terminal-services-programming-guidelines.md)
</dt> <dd>

Themen, in denen Richtlinien zum Entwickeln von Anwendungen in einer Remotedesktopdienste Umgebung bereitgestellt werden.

</dd> <dt>

[Remotedesktop Sitzungen](terminal-services-sessions.md)
</dt> <dd>

Da jede Anmeldung bei einem Remotedesktopverbindung-Client (RDC) eine separate Sitzungs-ID erhält, ist die Benutzer Darstellung ähnlich wie bei mehreren Computern gleichzeitig. beispielsweise ein Office-Computer und ein Heimcomputer.

</dd> <dt>

[Remotedesktop-Webverbindung](remote-desktop-web-connection.md)
</dt> <dd>

Hier wird beschrieben, wie ein Remotedesktop-Webverbindung installiert wird.

</dd> <dt>

[Ressourcen auf einem Remotedesktop-Sitzungshost Server](resources-on-a-terminal-server.md)
</dt> <dd>

Mehrere Benutzer können sich gleichzeitig bei einem einzelnen RD-Sitzungshost Server anmelden und die Hardware-und Software Ressourcen des Servers freigeben.

</dd> <dt>

[Neues in Remotedesktopdienste](what-s-new-in-terminal-services.md)
</dt> <dd>

Themen, in denen die Änderungen in den einzelnen Releases der Remotedesktopdienste-API beschrieben werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Herstellen einer Verbindung mit einem anderen Computer mithilfe von Remotedesktopverbindung](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




