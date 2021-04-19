---
description: Strategien für die Kommunikation mit mehreren Pipe-Clients und die Wartung mehrerer Pipe-Instanzen.
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: Named Pipe-Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b7d1ec591996e83853ae6faede899ecd4e4ea2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359197"
---
# <a name="named-pipe-instances"></a>Named Pipe-Instanzen

Der einfachste Pipeserver erstellt eine einzelne Instanz einer Pipe, stellt eine Verbindung mit einem einzelnen Client her, kommuniziert mit dem Client, trennt die Verbindung mit dem Client, schließt das Pipehandle und wird beendet. Es ist jedoch eher üblich, dass ein Pipe-Server mit mehreren Pipe-Clients kommuniziert. Ein pipenserver kann eine einzelne Pipe-Instanz verwenden, um eine Verbindung mit mehreren Pipeclients herzustellen, indem er eine Verbindung mit einem Client in der Reihenfolge herstellt und die Verbindung trennt, aber die Leistung ist unzureichend. Der Pipeserver muss mehrere Pipeline Instanzen erstellen, um mehrere Clients gleichzeitig effizient zu verarbeiten.

Es gibt drei grundlegende Strategien für die Wartung mehrerer Pipe-Instanzen.

-   Erstellen Sie einen separaten Thread für jede Instanz der Pipe. Ein Beispiel für einen Multithread Pipe-Server finden Sie unter [Multithread Pipe-Server](multithreaded-pipe-server.md).
-   Verwenden Sie überlappende Vorgänge, indem Sie eine [**über**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) Lapp Ende Struktur in den Funktionen [**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile), [**Write File**](/windows/desktop/api/fileapi/nf-fileapi-writefile)und [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) angeben. Ein Beispiel finden Sie unter [Named Pipe-Server mit über](named-pipe-server-using-overlapped-i-o.md)Lapp enden e/a-Vorgängen.
-   Verwenden Sie überlappende Vorgänge mithilfe der Funktionen "read [**fileex**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) " und " [**schreitefileex**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) ", die eine Abschluss Routine angeben, die ausgeführt wird, wenn der Vorgang abgeschlossen ist. Ein Beispiel finden Sie unter [Named Pipe Server Using completion Routinen](named-pipe-server-using-completion-routines.md).

Der multithreadpipeserver ist am einfachsten zu schreiben, da der Thread für jede Instanz die Kommunikation für einen einzelnen Pipe-Client übernimmt. Das System ordnet jedem Thread die Prozessorzeit nach Bedarf zu. Jeder Thread verwendet jedoch Systemressourcen. Dies ist ein Nachteil für einen Pipeserver, der eine große Anzahl von Clients verarbeitet.

Bei einem Single Thread Server ist es einfacher, Vorgänge zu koordinieren, die sich auf mehrere Clients auswirken, und es ist einfacher, freigegebene Ressourcen vor gleichzeitigem Zugriff durch mehrere Clients zu schützen. Die Herausforderung eines Single Thread-Servers besteht darin, dass er überlappende Vorgänge koordiniert werden muss, um die Prozessorzeit für die Verarbeitung der gleichzeitigen Anforderungen von Clients zuzuordnen.

 

 
