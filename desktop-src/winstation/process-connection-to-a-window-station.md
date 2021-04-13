---
title: Verarbeiten der Verbindung mit einer Fenster Station
description: Ein Prozess stellt automatisch eine Verbindung mit einer Fenster Station und einem Desktop her, wenn er zum ersten Mal eine User32-oder gdi32-Funktion aufruft (mit Ausnahme der Fenster Station-und Desktop Funktionen).
ms.assetid: 280f69e7-5c99-41a7-94e3-da13deaac9f5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a87e97b19ac1210b04447652268c5f53b7e2a6d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390737"
---
# <a name="process-connection-to-a-window-station"></a>Verarbeiten der Verbindung mit einer Fenster Station

Ein Prozess stellt automatisch eine Verbindung mit einer Fenster Station und einem Desktop her, wenn er zum ersten Mal eine User32-oder gdi32-Funktion aufruft (mit Ausnahme der Fenster Station-und Desktop Funktionen). Das System bestimmt die Fenster Station, mit der ein Prozess eine Verbindung herstellt, gemäß den folgenden Regeln:

1.  Wenn der Prozess die Funktion " [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) " aufgerufen hat, stellt er eine Verbindung mit der in diesem Aufruf angegebenen Fenster Station her.
2.  Wenn der Prozess [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation)nicht aufgerufen hat, stellt er eine Verbindung mit der Fenster Station her, die vom übergeordneten Prozess geerbt wurde.
3.  Wenn der Prozess [**SetProcessWindowStation**](/windows/win32/api/winuser/nf-winuser-setprocesswindowstation) nicht aufgerufen hat und keine Fenster Station geerbt hat, versucht das System, den maximal \_ zulässigen Zugriff zu öffnen und wie folgt eine Verbindung mit einer Fenster Station herzustellen:
    -   Wenn ein Fenster Stationsname im **lpdesktop-** Member der [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur angegeben wurde, die beim Erstellen des Prozesses verwendet wurde, stellt der Prozess eine Verbindung mit der angegebenen Fenster Station her.
    -   Andernfalls stellt der Prozess eine Verbindung mit der interaktiven Fenster Station her, wenn der Prozess in der Anmelde Sitzung des interaktiven Benutzers ausgeführt wird.
    -   Wenn der Prozess in einer nicht interaktiven Anmelde Sitzung ausgeführt wird, wird der Name der Fenster Station basierend auf dem Anmelde Sitzungs Bezeichner erstellt, und es wird versucht, die Fenster Station zu öffnen. Wenn der Öffnungsvorgang fehlschlägt, weil diese Fenster Station nicht vorhanden ist, versucht das System, die Fenster Station und einen Standard Desktop zu erstellen.

Die während dieses Verbindungs Vorgangs zugewiesene Fenster Station kann nicht durch Aufrufen der [**closewindowstation**](/windows/win32/api/winuser/nf-winuser-closewindowstation) -Funktion geschlossen werden.

Wenn ein Prozess eine Verbindung mit einer Fenster Station herstellt, durchsucht das System die Handle-Tabelle des Prozesses nach geerbten Handles. Das System verwendet das erste gefundene Fenster Station-handle. Wenn Sie möchten, dass ein untergeordneter Prozess eine Verbindung mit einer bestimmten geerbten Fenster Station herstellt, müssen Sie sicherstellen, dass nur das gewünschte Handle als vererbbar gekennzeichnet ist. Wenn ein untergeordneter Prozess mehrere Fenster Stations Handles erbt, sind die Ergebnisse der Fenster Stations Verbindung nicht definiert.

Behandelt eine Fenster Station, die das System öffnet, während ein Prozess mit einer Fenster Station verbunden wird, ist nicht vererbbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Thread Verbindung mit einem Desktop](thread-connection-to-a-desktop.md)
</dt> </dl>

 

 