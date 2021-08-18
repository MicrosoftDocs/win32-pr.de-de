---
title: Desktops
description: Ein Desktop verfügt über eine logische Anzeigeoberfläche und enthält Benutzeroberflächenobjekte wie Fenster, Menüs und Hooks. sie kann zum Erstellen und Verwalten von Fenstern verwendet werden.
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- Desktopobjekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b763c05c3d45c701da0bdd606fa906dec3f8af07ce72d256b402e7df5d9319b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587350"
---
# <a name="desktops"></a>Desktops

Ein *Desktop* verfügt über eine logische Anzeigeoberfläche und enthält Benutzeroberflächenobjekte wie Fenster, Menüs und Hooks. sie kann zum Erstellen und Verwalten von Fenstern verwendet werden. Jedes Desktopobjekt ist ein sicherungsfähiges Objekt. Wenn ein Desktop erstellt wird, wird [](window-stations.md) er der aktuellen Fensterstation des aufrufenden Prozesses zugeordnet und dem aufrufenden Thread zugewiesen.

Fenstermeldungen können nur zwischen Prozessen gesendet werden, die sich auf demselben Desktop befinden. Darüber hinaus kann die Hookprozedur eines Prozesses, der auf einem bestimmten Desktop ausgeführt wird, nur Nachrichten empfangen, die für Fenster vorgesehen sind, die auf demselben Desktop erstellt wurden.

Die Desktops, die der interaktiven Fensterstation Winsta0 zugeordnet sind, können so erstellt werden, dass sie eine Benutzeroberfläche anzeigen und Benutzereingaben empfangen, aber nur einer dieser Desktops gleichzeitig aktiv ist. Dieser aktive Desktop, auch als Eingabedesktop *bezeichnet,* ist der Desktop, der derzeit für den Benutzer sichtbar ist und Benutzereingaben empfängt. Anwendungen können die [**OpenInputDesktop-Funktion**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) verwenden, um ein Handle für den Eingabedesktop zu erhalten. Anwendungen mit dem erforderlichen Zugriff können die [**SwitchDesktop-Funktion**](/windows/win32/api/winuser/nf-winuser-switchdesktop) verwenden, um einen anderen Eingabedesktop anzugeben.

Standardmäßig gibt es drei Desktops in der interaktiven Fensterstation: Default, ScreenSaver und Winlogon.

Der Standarddesktop wird erstellt, wenn Winlogon den ersten Prozess als angemeldeter Benutzer startet. An diesem Punkt wird der Standarddesktop aktiv und für die Interaktion mit dem Benutzer verwendet.

Wenn ein sicherer Bildschirmschoner aktiviert wird, wechselt das System automatisch zum ScreenSaver-Desktop, der die Prozesse auf dem Standarddesktop vor nicht autorisierten Benutzern schützt. Ungesicherte Bildschirmschoner werden unter Winsta0 \\ Default ausgeführt.

Der Winlogon-Desktop ist aktiv, während sich ein Benutzer anmeldet. Das System wechselt zum Standarddesktop, wenn die Shell angibt, dass sie bereit ist, etwas anzuzeigen, oder nach 30 Sekunden, was zuerst ankommt. Während der Sitzung des Benutzers wechselt das System zum Winlogon-Desktop, wenn der Benutzer strg+ALT+ENTF drückt oder wenn das Dialogfeld Benutzerkontensteuerung (UAC) geöffnet ist.

**Windows Server 2003 und Windows XP/2000:** Das Dialogfeld "UAC" wird nicht unterstützt.

Die Sicherheitsbeschreibung des Winlogon-Desktops ermöglicht den Zugriff auf einen sehr eingeschränkten Satz von Konten, einschließlich [des LocalSystem-Kontos.](/windows/desktop/Services/localsystem-account) Anwendungen enthalten im Allgemeinen keine siDs dieser Konten in ihren Token und können daher nicht auf den Winlogon-Desktop zugreifen oder zu einem anderen Desktop wechseln, während der Winlogon-Desktop aktiv ist.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Fensterstation und Desktoperstellung](window-station-and-desktop-creation.md)
-   [Threadverbindung mit einem Desktop](thread-connection-to-a-desktop.md)
-   [Desktopsicherheit und Zugriffsrechte](desktop-security-and-access-rights.md)

 

 