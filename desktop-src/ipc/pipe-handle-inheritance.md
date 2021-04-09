---
description: Der Pipeserver steuert, ob seine Handles auf folgende Weise geerbt werden können.
ms.assetid: 72302f8b-f3a2-4efc-aab1-e596b8323984
title: Vererbung von Pipehandles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21cf91d4393b43011a2df632806f96da1e713b96
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749672"
---
# <a name="pipe-handle-inheritance"></a>Vererbung von Pipehandles

Der Pipeserver steuert, ob seine Handles wie folgt geerbt werden können:

-   Die Funktion " [**kreatepipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-createpipe) " empfängt eine Struktur von [**Sicherheits \_ Attributen**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) . Wenn der Pipeserver den **binherithandle** -Member dieser Struktur auf " **true**" festlegt, können die von " **kreatepipe** " erstellten Handles geerbt werden.
-   Der Pipeserver kann die [**DuplicateHandle**](/windows/desktop/api/handleapi/nf-handleapi-duplicatehandle) -Funktion verwenden, um die Vererbung eines Pipehandles zu ändern. Der Pipeserver kann ein nicht Vererb bares Duplikat eines vererbbaren Pipehandles oder ein Vererb bares Duplikat eines nicht vererbbaren Pipehandles erstellen.
-   Mit der Funktion "up- [**Process**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) " kann der Pipeserver angeben, ob ein untergeordneter Prozess alle oder keine seiner vererbbaren Handles erbt.

Wenn ein untergeordneter Prozess ein Pipehandle erbt, ermöglicht das System dem Prozess den Zugriff auf die Pipe. Der übergeordnete Prozess muss den Handle-Wert jedoch an den untergeordneten Prozess übermitteln. Der übergeordnete Prozess bewirkt in der Regel, dass das Standardausgabe Handle an den untergeordneten Prozess umgeleitet wird, wie in den folgenden Schritten gezeigt:

1.  Ruft die [**getstdhandle**](/windows/console/getstdhandle) -Funktion auf, um das aktuelle Standardausgabe Handle abzurufen. Speichern Sie dieses Handle, damit Sie das ursprüngliche Standardausgabe handle wiederherstellen können, nachdem der untergeordnete Prozess erstellt wurde.
2.  Aufrufen der [**setstdhandle**](/windows/console/setstdhandle) -Funktion zum Festlegen des Standardausgabe Handles auf das Schreib Handle der Pipe. Nun kann der übergeordnete Prozess den untergeordneten Prozess erstellen.
3.  Ruft die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion auf, um das Schreib Handle für die Pipe zu schließen. Nachdem der untergeordnete Prozess das Schreib handle erbt, benötigt der übergeordnete Prozess seine Kopie nicht mehr.
4.  Aufrufen von [**setstdhandle**](/windows/console/setstdhandle) , um das ursprüngliche Standardausgabe handle wiederherzustellen.

Der untergeordnete Prozess verwendet die [**getstdhandle**](/windows/console/getstdhandle) -Funktion, um das Standardausgabe handle, das nun ein Handle für das schreibende einer Pipe ist, zu erhalten. Der untergeordnete Prozess verwendet dann die Funktion " [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile) ", um die Ausgabe an die Pipe zu senden. Wenn das untergeordnete Element mit der Pipe fertig ist, sollte es das Pipehandle schließen, indem [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) aufgerufen oder beendet wird, wodurch das Handle automatisch geschlossen wird.

Der übergeordnete Prozess verwendet die Funktion zum [**Lesen von Dateien**](/windows/desktop/api/fileapi/nf-fileapi-readfile) , um Eingaben aus der Pipe zu empfangen. Daten werden als Datenstrom von Bytes in eine anonyme Pipe geschrieben. Dies bedeutet, dass der übergeordnete Prozess, der aus einer Pipe liest, nicht zwischen den in separaten Schreibvorgängen geschriebenen Bytes unterscheiden kann, es sei denn, die über-und untergeordneten Prozesse verwenden ein Protokoll, um anzugeben, wo der Schreibvorgang Wenn alle Schreib Handles für die Pipe geschlossen sind, gibt die Funktion "read **File** " 0 (null) zurück. Es ist wichtig, dass der übergeordnete Prozess sein Handle bis zum schreibende der Pipe schließt, bevor "read **File**" aufgerufen wird. Wenn dies nicht erfolgt, kann der Vorgang zum **Lesen von Dateien** nicht 0 (null) zurückgeben, da der übergeordnete Prozess über ein geöffnetes Handle für das schreibende der Pipe verfügt.

Die Prozedur zum Umleiten des Standardeingabe Handles ähnelt der Vorgehensweise beim Umleiten des Standardausgabe Handles, mit dem Unterschied, dass das lesehandle der Pipe als Standardeingabe Handle des untergeordneten Elements verwendet wird. In diesem Fall muss der übergeordnete Prozess sicherstellen, dass der untergeordnete Prozess den Schreib Handle der Pipe nicht erbt. Wenn dies nicht der Fall ist, kann der vom untergeordneten Prozess ausgeführte Vorgang zum [**Lesen von Dateien**](/windows/desktop/api/fileapi/nf-fileapi-readfile) keine NULL zurückgeben, da der untergeordnete Prozess über ein geöffnetes Handle für das schreibende der Pipe verfügt.

Ein Beispielprogramm, das anonyme Pipes zum Umleiten der Standard Handles eines untergeordneten Prozesses verwendet, finden Sie unter [Erstellen eines untergeordneten Prozesses mit umgeleiteter Eingabe und Ausgabe](/windows/desktop/ProcThread/creating-a-child-process-with-redirected-input-and-output).

 

 
