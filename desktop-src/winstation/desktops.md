---
title: Desktops
description: Ein Desktop verfügt über eine logische Anzeige Oberfläche und enthält Benutzeroberflächen Objekte wie Fenster, Menüs und Hooks. Sie kann verwendet werden, um Windows zu erstellen und zu verwalten.
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- Desktop Objekte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ca0b390ec4d34cc943c9d18d958cdea6466634
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106338074"
---
# <a name="desktops"></a>Desktops

Ein *Desktop* verfügt über eine logische Anzeige Oberfläche und enthält Benutzeroberflächen Objekte wie Fenster, Menüs und Hooks. Sie kann verwendet werden, um Windows zu erstellen und zu verwalten. Jedes Desktop Objekt ist ein Sicherungs fähiges Objekt. Wenn ein Desktop erstellt wird, wird er der aktuellen [Fenster Station](window-stations.md) des aufrufenden Prozesses zugeordnet und dem aufrufenden Thread zugewiesen.

Fenster Meldungen können nur zwischen Prozessen gesendet werden, die sich auf demselben Desktop befinden. Außerdem kann die Hook-Prozedur eines Prozesses, der auf einem bestimmten Desktop ausgeführt wird, nur Nachrichten empfangen, die für Windows erstellt wurden, die auf demselben Desktop erstellt wurden.

Die Desktops, die der interaktiven Fenster Station (Winsta0) zugeordnet sind, können so erstellt werden, dass eine Benutzeroberfläche angezeigt und Benutzereingaben empfangen werden. es ist jedoch jeweils nur einer der Desktops aktiv. Dieser aktive Desktop, auch als *Eingabe Desktop* bezeichnet, ist der derzeit für den Benutzer sichtbare Benutzer, der Benutzereingaben empfängt. Anwendungen können die [**openinputdesktop-**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) Funktion verwenden, um ein Handle für den Eingabe Desktop zu erhalten. Anwendungen, die über den erforderlichen Zugriff verfügen, können die [**switchdesktop-**](/windows/win32/api/winuser/nf-winuser-switchdesktop) Funktion verwenden, um einen anderen Eingabe Desktop anzugeben.

Standardmäßig befinden sich drei Desktops auf der interaktiven Fenster Station: Standard, Bildschirmschoner und Winlogon.

Der Standard Desktop wird erstellt, wenn der anfängliche Prozess von Winlogon als angemeldeter Benutzer gestartet wird. An diesem Punkt wird der Standard Desktop aktiviert und für die Interaktion mit dem Benutzer verwendet.

Wenn ein sicherer Bildschirmschoner aktiviert wird, wechselt das System automatisch zum Bildschirmschoner-Desktop, der die Prozesse auf dem Standard Desktop vor nicht autorisierten Benutzern schützt. Unsichere Bildschirmschoner werden unter Winsta0 \\ Standard ausgeführt.

Der Winlogon-Desktop ist aktiv, während sich ein Benutzer anmeldet. Das System wechselt zum Standard Desktop, wenn die Shell anzeigt, dass es bereit ist, etwas anzuzeigen, oder nach dreißig Sekunden, je nachdem, was zuerst eintritt. Während der Benutzersitzung wechselt das System zum Winlogon-Desktop, wenn der Benutzer die Tastenkombination STRG + ALT + ENTF drückt oder wenn das Dialogfeld Benutzerkontensteuerung (User Account Control, UAC) geöffnet ist.

**Windows Server 2003 und Windows XP/2000:** Das UAC-Dialogfeld wird nicht unterstützt.

Die Sicherheits Beschreibung des Windows-Logon-Desktops ermöglicht den Zugriff auf einen sehr eingeschränkten Satz von Konten, einschließlich des [LocalSystem-Kontos](/windows/desktop/Services/localsystem-account). Anwendungen enthalten im Allgemeinen keine der SIDs dieser Konten in ihren Token und können daher nicht auf den Winlogon-Desktop zugreifen oder zu einem anderen Desktop wechseln, während der Winlogon-Desktop aktiv ist.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Fenster Station und Desktop Erstellung](window-station-and-desktop-creation.md)
-   [Thread Verbindung mit einem Desktop](thread-connection-to-a-desktop.md)
-   [Desktop Sicherheit und Zugriffsrechte](desktop-security-and-access-rights.md)

 

 