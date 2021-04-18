---
title: Remotedesktop Sitzungen
description: Da jede Anmeldung bei einem Remotedesktopverbindung-Client (RDC) eine separate Sitzungs-ID erhält, ist die Benutzer Darstellung ähnlich wie bei mehreren Computern gleichzeitig. beispielsweise ein Office-Computer und ein Heimcomputer.
ms.assetid: 09a990cd-7590-4d73-b1f5-8736f0b4f17e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bb99f9745e382bdff1099eabae9a8e8ef0b8333
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106337852"
---
# <a name="remote-desktop-sessions"></a>Remotedesktop Sitzungen

Wenn sich ein Benutzer an einem Remotedesktopdienste – aktivierten Computer anmeldet, wird eine Sitzung für den Benutzer gestartet. Jede Sitzung wird durch eine eindeutige Sitzungs-ID identifiziert. Da jede Anmeldung bei einem Remotedesktopverbindung-Client (RDC) eine separate Sitzungs-ID erhält, ist die Benutzer Darstellung ähnlich wie bei mehreren Computern gleichzeitig. beispielsweise ein Office-Computer und ein Heimcomputer.

Jede Remote Desktop Sitzung ist einer interaktiven Fenster Station zugeordnet. Der einzige unterstützte Fenster Stationsname für eine interaktive Fenster Station ist "WinSta0"; Daher ist jede Sitzung ihrer eigenen "WinSta0"-Fenster Station zugeordnet. Es gibt drei Standard Desktops für jede Fenster Station: den Desktop Winlogon, den Bildschirmschoner Desktop und den interaktiven Desktop.

Der Benutzer, der der interaktiven Fenster Station für eine Sitzung zugeordnet ist, wird als *interaktiver Benutzer* bezeichnet. Auf einem Remotedesktopverbindung-Client (RDC) können neben dem interaktiven Benutzer in der Remotedesktopdienste Konsole mehrere interaktive Benutzer vorhanden sein. Um den Bezeichner der aktuell an die Konsole angefügten Sitzung abzurufen, verwenden Sie die [**wzgetactiveconsolesessionid**](/windows/desktop/api/Winbase/nf-winbase-wtsgetactiveconsolesessionid) -Funktion.

Wenn ein Benutzer sich von einem Remotedesktopverbindung-Client (RDC) abmeldet, wird die Sitzung, die der Client auf dem Remotedesktop-Sitzungshost (RD-Sitzungshost)-Server (früher als Terminal Server bezeichnet) hat, gelöscht, und die dieser Sitzung zugeordneten Fenster Stationen und Desktops werden entfernt. Da die Remotedesktopdienste Konsolen Sitzung jedoch nie gelöscht wird, werden die der Konsolen Sitzung zugeordneten Fenster Stationen nicht gelöscht. Dies wirkt sich darauf aus, wie sich Anwendungen in einer Remotedesktopdienste Umgebung Verhalten, wenn Sie für die Ausführung im Sicherheitskontext des interaktiven Benutzers konfiguriert sind, der auch als "runas Interactive User"-Objekt Aktivierungs Modus bezeichnet wird.

Weitere Informationen zum Starten eines lokalen Server Prozesses für eine bestimmte Sitzung finden Sie unter [Sitzungs-zu-Sitzung-Aktivierung mit einem sitzungsmoniker](session-to-session-activation-with-a-session-moniker.md) und [Verwenden eines sitzungsmonikers](using-a-session-moniker.md). Weitere Informationen zu Sicherheits Kontexten finden Sie [im Sicherheitskontext des Clients](/windows/desktop/SecAuthZ/the-client-security-context).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Untergeordnete Sitzungen](child-sessions.md)
</dt> </dl>

 

 