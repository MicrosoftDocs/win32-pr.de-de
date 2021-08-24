---
title: Informationen Remotedesktopdienste
description: Remotedesktopdienste (früher als Terminaldienste bezeichnet) bietet Ähnliches wie eine terminalbasierte, zentralisierte Host- oder Mainframeumgebung, in der mehrere Terminals eine Verbindung mit einem Hostcomputer herstellen.
ms.assetid: 5b5b0f97-f973-4f52-a965-c9c2390e6c8d
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste , informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 680ccae3d8944c92d64da526831142d662ac5dc38157c741cf8f5426768fc745
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681460"
---
# <a name="about-remote-desktop-services"></a>Informationen Remotedesktopdienste

Remotedesktopdienste (früher als Terminaldienste bezeichnet) bietet Ähnliches wie eine terminalbasierte, zentralisierte Host- oder Mainframeumgebung, in der mehrere Terminals eine Verbindung mit einem Hostcomputer herstellen. Jedes Terminal stellt einen Kanal für die Eingabe und Ausgabe zwischen einem Benutzer und dem Hostcomputer zur Verfügung. Ein Benutzer kann sich an einem Terminal anmelden und dann Anwendungen auf dem Hostcomputer ausführen und auf Dateien, Datenbanken, Netzwerkressourcen und so weiter zugreifen. Jede Terminalsitzung ist unabhängig, und das Hostbetriebssystem führt Konflikte zwischen mehreren Benutzern aus, die um freigegebene Ressourcen konkurrieren.

Der Hauptunterschied zwischen Remotedesktopdienste und der herkömmlichen Mainframeumgebung ist, dass die dumb-Terminals in einer Mainframeumgebung nur zeichenbasierte Eingaben und Ausgaben bereitstellen. Ein Remotedesktopverbindung-Client oder -Emulator (RDC) bietet eine vollständige grafische Benutzeroberfläche, einschließlich eines Windows-Betriebssystemdesktops und Unterstützung für eine Vielzahl von Eingabegeräten, z. B. Tastatur und Maus.

In der Remotedesktopdienste wird eine Anwendung vollständig auf dem Remotedesktop-Sitzungshost(RD-Sitzungshost)-Server (ehemals Terminalserver) ausgeführt. Der RDC-Client führt keine lokale Verarbeitung von Anwendungssoftware durch. Der Server überträgt die grafische Benutzeroberfläche an den Client. Der Client überträgt die Eingabe des Benutzers zurück an den Server.

Weitere Informationen finden Sie in den folgenden Themen.

## <a name="in-this-section"></a>In diesem Abschnitt

<dl> <dt>

[Ändern der Standardeinstellung für die Geräteumleitung](modify-device-redirection-default-.md)
</dt> <dd>

Da Remotedesktop Gatewayserver versuchen, sichere Richtlinien für die Geräteumleitung zu erzwingen, bevor die Clientverbindung an einen Remotedesktop-Sitzungshost-Server übergeben wird, müssen Sie diese Standardeinstellung möglicherweise in einigen Fällen deaktivieren.

</dd> <dt>

[Remotedesktopprotokoll](remote-desktop-protocol.md)
</dt> <dd>

Das Microsoft-Remotedesktop Protocol (RDP) bietet Remoteanzeige- und Eingabefunktionen über Netzwerkverbindungen für Windows-basierte Anwendungen, die auf einem Server ausgeführt werden.

</dd> <dt>

[Remotedesktopdienste-API](terminal-services-api.md)
</dt> <dd>

Die Remotedesktopdienste-API ist in erster Linie für Client-/Serveranwendungen und Anwendungen für die Remotedesktopdienste nützlich.

</dd> <dt>

[Remotedesktopdienste-Verwaltungsanwendungen](terminal-services-management-applications.md)
</dt> <dd>

Beschreibt die Verwaltungsanwendungen, die Remotedesktopdienste werden.

</dd> <dt>

[Remotedesktopdienste Programmierrichtlinien](terminal-services-programming-guidelines.md)
</dt> <dd>

Themen, die Richtlinien für die Entwicklung von Anwendungen in einer Remotedesktopdienste bereitstellen.

</dd> <dt>

[Remotedesktop Sitzungen](terminal-services-sessions.md)
</dt> <dd>

Da jede Anmeldung bei einem Remotedesktopverbindung-Client (RDC) eine separate Sitzungs-ID empfängt, ähnelt die Benutzererfahrung der gleichzeitigen Anmeldung bei mehreren Computern. z. B. ein Bürocomputer und ein Heimcomputer.

</dd> <dt>

[Remotedesktop-Webverbindung](remote-desktop-web-connection.md)
</dt> <dd>

Beschreibt das Installieren eines Remotedesktop-Webverbindung.

</dd> <dt>

[Ressourcen auf einem Remotedesktop-Sitzungshost Server](resources-on-a-terminal-server.md)
</dt> <dd>

Mehrere Benutzer können sich gleichzeitig bei einem einzelnen RD-Sitzungshost anmelden und die Hardware- und Softwareressourcen des Servers gemeinsam nutzen.

</dd> <dt>

[Neues in Remotedesktopdienste](what-s-new-in-terminal-services.md)
</dt> <dd>

Themen, in denen die Änderungen in jedem Release der Remotedesktopdienste-API beschrieben werden.

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verbinden mit einem anderen Computer Remotedesktopverbindung](https://windows.microsoft.com/windows/connect-using-remote-desktop-connection#connect-using-remote-desktop-connection=windows-7)
</dt> </dl>

 

 




