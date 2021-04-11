---
title: Thread Verbindung mit einem Desktop
description: Nachdem ein Prozess eine Verbindung mit einer Fenster Station hergestellt hat, weist das System dem Thread, der die Verbindung herstellt, einen Desktop zu.
ms.assetid: 45016619-ed11-4b0c-84e3-f8662553c64d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a503390468ea5ed1771ece7a942a2d615ac6f0a9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104209250"
---
# <a name="thread-connection-to-a-desktop"></a>Thread Verbindung mit einem Desktop

Nachdem ein Prozess eine Verbindung mit einer Fenster Station hergestellt hat, weist das System dem Thread, der die Verbindung herstellt, einen Desktop zu. Das System bestimmt den Desktop, der dem Thread gemäß den folgenden Regeln zugewiesen werden soll:

1.  Wenn der Thread die Funktion " [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) " aufgerufen hat, stellt er eine Verbindung mit dem angegebenen Desktop her.
2.  Wenn der Thread [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop)nicht aufgerufen hat, stellt er eine Verbindung mit dem Desktop her, der vom übergeordneten Prozess geerbt wurde.
3.  Wenn der Thread [**SetThreadDesktop**](/windows/win32/api/winuser/nf-winuser-setthreaddesktop) nicht aufgerufen hat und keinen Desktop geerbt hat, versucht das System, den maximal \_ zulässigen Zugriff zu öffnen und wie folgt eine Verbindung mit einem Desktop herzustellen:
    -   Wenn im **lpdesktop-** Member der [**STARTUPINFO**](/windows/desktop/api/processthreadsapi/ns-processthreadsapi-startupinfoa) -Struktur, die beim Erstellen des Prozesses verwendet wurde, ein Desktop Name angegeben wurde, stellt der Thread eine Verbindung mit dem angegebenen Desktop her.
    -   Andernfalls stellt der Thread eine Verbindung mit dem Standard Desktop der Fenster Station her, mit der der Prozess verbunden ist.

Der während dieses Verbindungs Vorgangs zugewiesene Desktop kann nicht durch Aufrufen der [**closedesktop-**](/windows/win32/api/winuser/nf-winuser-closedesktop) Funktion geschlossen werden.

Wenn ein Prozess eine Verbindung mit einem Desktop herstellt, durchsucht das System die Handle-Tabelle des Prozesses nach geerbten Handles. Das System verwendet das erste gefundene Desktop handle. Wenn Sie möchten, dass ein untergeordneter Prozess eine Verbindung mit einem bestimmten geerbten Desktop herstellt, müssen Sie sicherstellen, dass nur das gewünschte Handle als vererbbar gekennzeichnet ist. Wenn ein untergeordneter Prozess mehrere Desktop Handles erbt, sind die Ergebnisse der Desktop Verbindung nicht definiert.

Handles für einen Desktop, den das System öffnet, während ein Prozess mit einem Desktop verbunden wird, können nicht vererbt werden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verarbeiten der Verbindung mit einer Fenster Station](process-connection-to-a-window-station.md)
</dt> </dl>

 

 