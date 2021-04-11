---
description: Pipe-Vorgänge, einschließlich Pipeclients und Server, können eine von mehreren Funktionen aufrufen – zusätzlich zu callnamedpipe –, um aus einer Named Pipe zu lesen und in diese zu schreiben.
ms.assetid: ae06455e-33bc-433d-be8f-aeb8eeb99b1d
title: Named Pipe-Vorgänge
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 703189a129fc44b956ab65c2f70bbf88bfd22700
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128140"
---
# <a name="named-pipe-operations"></a>Named Pipe-Vorgänge

Wenn der pipenserver das erste Mal die Funktion " [**comatenamedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) " aufruft, verwendet er den *nmaxinstance* -Parameter, um die maximale Anzahl von Instanzen der Pipe anzugeben, die gleichzeitig vorhanden sein können. Der Server kann " **kreatenamedpipe** " wiederholt aufrufen, um zusätzliche Instanzen der Pipe zu erstellen, solange die maximale Anzahl von Instanzen nicht überschritten wird. Wenn die Funktion erfolgreich ausgeführt wird, gibt jeder-Rückruf ein Handle an das Server Ende einer Named Pipe Instanz zurück.

Sobald der Pipeserver eine Pipe-Instanz erstellt, kann ein Pipeclient eine Verbindung mit ihm herstellen, indem er die [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) -oder [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) -Funktion aufruft. Wenn eine Pipe-Instanz verfügbar ist, gibt " **kreatefile** " ein Handle an das Client Ende der Pipe-Instanz zurück. Wenn keine Instanzen der Pipe verfügbar sind, kann ein Pipe-Client die [**WaitNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-waitnamedpipea) -Funktion verwenden, um zu warten, bis eine Pipe verfügbar wird.

Durch Aufrufen der [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) -Funktion kann ein pipenserver bestimmen, wann ein Pipe-Client mit einer Pipe-Instanz verbunden ist. Wenn sich das Pipehandle im blockierenden Wartemodus befindet, gibt **connectnamedpipe** erst dann zurück, wenn ein Client verbunden ist.

Pipeclients und Server können eine von mehreren Funktionen aufrufen – zusätzlich zu [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) –, um aus einer Named Pipe zu lesen und in diese zu schreiben. Das Verhalten dieser Funktionen hängt von der Art der Pipe und den Modi ab, die für das angegebene Pipehandle wirksam sind, wie im folgenden dargestellt:

-   Die Funktionen "read [**File**](/windows/desktop/api/fileapi/nf-fileapi-readfile) " und "Write file" können entweder mit [**Bytetyp**](/windows/desktop/api/fileapi/nf-fileapi-writefile) -oder Nachrichtentyp Pipes verwendet werden.
-   Die Funktionen "read [**fileex**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) " und "Write fileex" können entweder mit [**Bytetyp**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) -oder Nachrichtentyp Pipes verwendet werden, wenn das Pipehandle für überlappende Vorgänge geöffnet wurde.
-   Die Funktion " [**Peer NamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-peeknamedpipe) " kann zum Lesen verwendet werden, ohne dass der Inhalt einer Pipe mit Bytetyp oder einer Pipe vom Typ "Message" entfernt wird. " **Peer Name** " kann auch zusätzliche Informationen über die Pipe-Instanz zurückgeben.
-   Die [**transactnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-transactnamedpipe) -Funktion kann mit Nachrichtentyp-Duplex Pipes verwendet werden, wenn das Pipehandle für den aufrufenden Prozess auf den Nachrichten Lese Modus festgelegt ist. Die Funktion schreibt eine Anforderungs Nachricht und liest eine Antwortnachricht in einem einzelnen Vorgang, um die Netzwerkleistung zu verbessern.

Der Pipeserver sollte erst dann einen blockierenden Lesevorgang ausführen, wenn der Pipe-Client gestartet wurde. Andernfalls kann eine Racebedingung eintreten. Dies tritt normalerweise auf, wenn Initialisierungs Code, wie z. b. der C-Lauf Zeit Bibliothek, geerbte Handles Sperren und untersuchen muss.

Wenn ein Client und ein Server die Verwendung einer Pipeinstanz beenden, sollte der Server zuerst die [**FlushFileBuffers**](/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers) -Funktion aufrufen, um sicherzustellen, dass alle Bytes oder Meldungen, die in die Pipe geschrieben werden, vom Client gelesen werden. **FlushFileBuffers** gibt erst zurück, wenn der Client alle Daten aus der Pipe gelesen hat. Der Server ruft dann die [**disconnectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-disconnectnamedpipe) -Funktion auf, um die Verbindung mit dem Pipe-Client zu schließen. Diese Funktion macht das Handle des Clients ungültig, wenn es nicht bereits geschlossen wurde. Alle ungelesenen Daten in der Pipe werden verworfen. Nachdem der Client getrennt wurde, ruft der Server die [**CloseHandle**](/windows/desktop/api/handleapi/nf-handleapi-closehandle) -Funktion auf, um das Handle für die Pipeinstanz zu schließen. Alternativ kann der Server [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) verwenden, um einem neuen Client das Herstellen einer Verbindung mit dieser Instanz der Pipe zu ermöglichen.

Ein Prozess kann Informationen zu einem Named Pipe abrufen, indem er die [**getnamedpipeinfo**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-getnamedpipeinfo) -Funktion aufrufen, die den Typ der Pipe, die Größe der Eingabe-und Ausgabepuffer und die maximale Anzahl der zu erstellenden Pipe-Instanzen zurückgibt. Die [**getnamedpipelenker State**](/windows/desktop/api/Winbase/nf-winbase-getnamedpipehandlestatea) -Funktion meldet die Lese-und warte Modi eines Pipehandles, die aktuelle Anzahl der Pipe-Instanzen und zusätzliche Informationen für Pipes, die über ein Netzwerk kommunizieren. Die [**setnamedpipelenker State**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-setnamedpipehandlestate) -Funktion legt den Lesemodus und die Warte Modi eines Pipehandles fest. Für Pipe-Clients, die mit einem Remote Server kommunizieren, steuert die Funktion auch die maximale Anzahl der zu sammelnden Bytes oder die maximale Wartezeit, die vor dem übertragen einer Nachricht gewartet wird (vorausgesetzt, das Handle des Clients wurde nicht mit aktiviertem Schreibmodus geöffnet).

 

 
