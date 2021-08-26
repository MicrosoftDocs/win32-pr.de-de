---
title: Remotedesktop Sitzungen
description: Da jede Anmeldung bei einem Remotedesktopverbindung-Client (RDC) eine separate Sitzungs-ID empfängt, ähnelt die Benutzererfahrung der gleichzeitigen Anmeldung bei mehreren Computern. z. B. ein Bürocomputer und ein Heimcomputer.
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac5093e9da70301fc4258ce2df88527c87940e455050a0673ac36d2fb04a8cd0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987160"
---
# <a name="remote-desktop-sessions"></a>Remotedesktop Sitzungen

Wenn sich ein Benutzer bei einem Remotedesktopdienste-fähigen Computer anmeldet, wird eine Sitzung für den Benutzer gestartet. Jede Sitzung wird durch eine eindeutige Sitzungs-ID identifiziert. Da jede Anmeldung bei einem Remotedesktopverbindung-Client (RDC) eine separate Sitzungs-ID empfängt, ähnelt die Benutzererfahrung der gleichzeitigen Anmeldung bei mehreren Computern. z. B. ein Bürocomputer und ein Heimcomputer.

Jede Remotedesktopsitzung ist einer interaktiven Fensterstation zugeordnet. Der einzige unterstützte Name der Fensterstation für eine interaktive Fensterstation ist "WinSta0". daher ist jede Sitzung einer eigenen WinSta0-Fensterstation zugeordnet. Es gibt drei Standarddesktops für jede Fensterstation: den Winlogon-Desktop, den Desktop des Bildschirmschoners und den interaktiven Desktop.

Der Benutzer, der der interaktiven Fensterstation für eine Sitzung zugeordnet ist, wird als *interaktiver Benutzer bezeichnet.* Auf einem Remotedesktopverbindung(RDC)-Client können zusätzlich zum interaktiven Benutzer in der konsole mehrere Remotedesktopdienste werden. Verwenden Sie die [**WTSGetActiveConsoleSessionId-Funktion,**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) um den Bezeichner der derzeit an die Konsole angefügten Sitzung abzurufen.

Wenn sich ein Benutzer von einem Remotedesktopverbindung-Client (RDC) abmeldet, wird die Sitzung, die der Client auf dem Remotedesktop-Sitzungshost-Server (RD-Sitzungshost) (früher als Terminalserver bezeichnet) hat, gelöscht, und die dieser Sitzung zugeordneten Fensterstationen und Desktops werden entfernt. Da die Konsolensitzung Remotedesktopdienste nicht gelöscht wird, werden die der Konsolensitzung zugeordneten Fensterstationen jedoch nicht gelöscht. Dies wirkt sich darauf aus, wie sich Anwendungen in einer Remotedesktopdienste-Umgebung verhalten, wenn sie für die Ausführung im Sicherheitskontext des interaktiven Benutzers konfiguriert sind, der auch als Objektaktivierungsmodus "Interaktiver RunAs-Benutzer" bezeichnet wird.

Weitere Informationen zum Starten eines lokalen Serverprozesses in einer angegebenen Sitzung finden Sie unter [Sitzungs-zu-Sitzung-Aktivierung](session-to-session-activation-with-a-session-moniker.md) mit einem Sitzungsmoniker und [Verwenden eines Sitzungsmonikers.](using-a-session-moniker.md) Weitere Informationen zu Sicherheitskontexten finden Sie unter [Sicherheitskontext des Clients.](/windows/desktop/SecAuthZ/the-client-security-context)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Untergeordnete Sitzungen](child-sessions.md)
</dt> </dl>

 

 