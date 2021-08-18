---
description: Der Pipeserver steuert, ob seine Handles auf folgende Weise geerbt werden können.
ms.assetid: 72302f8b-f3a2-4efc-aab1-e596b8323984
title: Pipehandlevererbung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c5c2a5abc19164e0bf71f325f1d6e76b46de75e22513061f7f9634ef7212f26
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119829310"
---
# <a name="pipe-handle-inheritance"></a>Pipehandlevererbung

Der Pipeserver steuert auf folgende Weise, ob seine Handles geerbt werden können:

-   Die [**CreatePipe-Funktion**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) empfängt eine [**SECURITY \_ ATTRIBUTES-Struktur.**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) Wenn der Pipeserver den **bInheritHandle-Member** dieser Struktur auf **TRUE** festlegt, können die von **CreatePipe** erstellten Handles geerbt werden.
-   Der Pipeserver kann die [**DuplicateHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) verwenden, um die Vererbung eines Pipehandles zu ändern. Der Pipeserver kann ein nicht vererbbares Duplikat eines vererbbaren Pipehandle oder ein vererbbares Duplikat eines nicht vererbbaren Pipehandle erstellen.
-   Mit [**der CreateProcess-Funktion**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) kann der Pipeserver angeben, ob ein untergeordneter Prozess alle oder keinen vererbbaren Handles erbt.

Wenn ein untergeordneter Prozess ein Pipehandle erbt, ermöglicht das System dem Prozess den Zugriff auf die Pipe. Der übergeordnete Prozess muss jedoch den Handlewert an den untergeordneten Prozess weitergeben. Der übergeordnete Prozess führt dies in der Regel durch um, indem das Standardausgabehandle an den untergeordneten Prozess umgeleitet wird, wie in den folgenden Schritten gezeigt:

1.  Rufen Sie die [**GetStdHandle-Funktion**](/windows/console/getstdhandle) auf, um das aktuelle Standardausgabehandle abzurufen. Speichern Sie dieses Handle, damit Sie das ursprüngliche Standardausgabehandle wiederherstellen können, nachdem der untergeordnete Prozess erstellt wurde.
2.  Rufen Sie die [**SetStdHandle-Funktion**](/windows/console/setstdhandle) auf, um das Standardausgabehandle auf das Schreibhandle für die Pipe festzulegen. Jetzt kann der übergeordnete Prozess den untergeordneten Prozess erstellen.
3.  Rufen Sie die [**CloseHandle-Funktion**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) auf, um das Schreibhandle für die Pipe zu schließen. Nachdem der untergeordnete Prozess das Schreibhandle geerbt hat, benötigt der übergeordnete Prozess seine Kopie nicht mehr.
4.  Rufen [**Sie SetStdHandle**](/windows/console/setstdhandle) auf, um das ursprüngliche Standardausgabehandle wiederherzustellen.

Der untergeordnete Prozess verwendet die [**GetStdHandle-Funktion,**](/windows/console/getstdhandle) um das Standardausgabehandle abzurufen, das jetzt ein Handle am Schreibende einer Pipe ist. Der untergeordnete Prozess verwendet dann die [**WriteFile-Funktion,**](/windows/desktop/api/fileapi/nf-fileapi-writefile) um die Ausgabe an die Pipe zu senden. Wenn das untergeordnete Element mit der Pipe fertig ist, sollte es das Pipehandle durch Aufrufen von [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) oder durch Beenden schließen, wodurch das Handle automatisch geschlossen wird.

Der übergeordnete Prozess verwendet die [**ReadFile-Funktion,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) um Eingaben von der Pipe zu empfangen. Daten werden als Bytestream in eine anonyme Pipe geschrieben. Dies bedeutet, dass der übergeordnete Prozess, der aus einer Pipe liest, nicht zwischen den Bytes unterscheiden kann, die in separaten Schreibvorgängen geschrieben wurden, es sei denn, sowohl der übergeordnete als auch der untergeordnete Prozess verwenden ein Protokoll, um anzugeben, wo der Schreibvorgang endet. Wenn alle Schreibhandles für die Pipe geschlossen sind, gibt die **ReadFile-Funktion** 0 (null) zurück. Es ist wichtig, dass der übergeordnete Prozess sein Handle am Schreibende der Pipe schließt, bevor ReadFile aufgerufen **wird.** Wenn dies nicht erfolgt, kann der **ReadFile-Vorgang** keine Null zurückgeben, da der übergeordnete Prozess über ein offenes Handle für das Schreibende der Pipe verfügt.

Das Verfahren zum Umleiten des Standardeingabehandles ähnelt dem verfahren zum Umleiten des Standardausgabehandles, mit der Ausnahme, dass das Lesehandle der Pipe als Standardeingabehandle des untergeordneten Benutzers verwendet wird. In diesem Fall muss der übergeordnete Prozess sicherstellen, dass der untergeordnete Prozess das Schreibhandle der Pipe nicht erbt. Wenn dies nicht erfolgt, kann der vom untergeordneten Prozess ausgeführte [**ReadFile-Vorgang**](/windows/desktop/api/fileapi/nf-fileapi-readfile) keine Null zurückgeben, da der untergeordnete Prozess über ein offenes Handle zum Schreibende der Pipe verfügt.

Ein Beispielprogramm, das anonyme Pipes verwendet, um die Standardhandles eines untergeordneten Prozesses umzuleiten, finden Sie unter [Erstellen eines untergeordneten Prozesses mit umgeleiteter Eingabe und Ausgabe.](/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output)

 

 
