---
description: Strategien für die Kommunikation mit mehreren Pipeclients und die Wartung mehrerer Pipeinstanzen.
ms.assetid: c764bde5-e053-4124-b859-1d2839ada918
title: Named Pipe-Instanzen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 188ec90912132e5cdd972ac2b0a4ab3f4c1f97ebbb7bc35e20b75b04eebbfa15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118481961"
---
# <a name="named-pipe-instances"></a>Named Pipe-Instanzen

Der einfachste Pipeserver erstellt eine einzelne Instanz einer Pipe, stellt eine Verbindung mit einem einzelnen Client her, kommuniziert mit dem Client, trennt die Verbindung mit dem Client, schließt das Pipehandle und beendet. Es ist jedoch häufiger, dass ein Pipeserver mit mehreren Pipeclients kommuniziert. Ein Pipeserver kann eine einzelne Pipeinstanz verwenden, um eine Verbindung mit mehreren Pipeclients herzustellen, indem nacheinander eine Verbindung mit jedem Client hergestellt und die Verbindung mit diesem getrennt wird. Die Leistung wäre jedoch schlecht. Der Pipeserver muss mehrere Pipeinstanzen erstellen, um mehrere Clients effizient gleichzeitig zu verarbeiten.

Es gibt drei grundlegende Strategien für die Wartung mehrerer Pipeinstanzen.

-   Erstellen Sie einen separaten Thread für jede Instanz der Pipe. Ein Beispiel für einen Multithreadpipeserver finden Sie unter [Multithreadpipeserver.](multithreaded-pipe-server.md)
-   Verwenden Sie überlappende Vorgänge, indem Sie eine [**OVERLAPPED-Struktur**](/windows/desktop/api/minwinbase/ns-minwinbase-overlapped) in den Funktionen [**ReadFile,**](/windows/desktop/api/fileapi/nf-fileapi-readfile) [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)und [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) angeben. Ein Beispiel finden Sie unter [Named Pipe-Server mit überlappender E/A.](named-pipe-server-using-overlapped-i-o.md)
-   Verwenden Sie überlappende Vorgänge mithilfe der [**ReadFileEx-**](/windows/desktop/api/fileapi/nf-fileapi-readfileex) und [**WriteFileEx-Funktionen,**](/windows/desktop/api/fileapi/nf-fileapi-writefileex) die eine Vervollständigungsroutine angeben, die ausgeführt werden soll, wenn der Vorgang abgeschlossen ist. Ein Beispiel finden Sie unter [Named Pipe Server Using Completion Routines](named-pipe-server-using-completion-routines.md).

Der Multithreadpipeserver ist am einfachsten zu schreiben, da der Thread für jede Instanz die Kommunikation für einen einzelnen Pipeclient verarbeitet. Das System ordnet jedem Thread nach Bedarf Prozessorzeit zu. Jeder Thread verwendet jedoch Systemressourcen. Dies ist ein Nachteil für einen Pipeserver, der eine große Anzahl von Clients verarbeitet.

Mit einem Singlethreadserver ist es einfacher, Vorgänge zu koordinieren, die sich auf mehrere Clients auswirken, und es ist einfacher, freigegebene Ressourcen vor gleichzeitigem Zugriff durch mehrere Clients zu schützen. Die Herausforderung eines Singlethreadservers besteht darin, dass eine Koordination überlappender Vorgänge erforderlich ist, um Prozessorzeit für die Behandlung der gleichzeitigen Anforderungen von Clients zuzuweisen.

 

 
