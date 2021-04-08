---
description: Bei einem Named Pipe handelt es sich um eine benannte, unidirektionale oder Duplex Pipe für die Kommunikation zwischen dem Pipeserver und mindestens einem Pipe-Client.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Named Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0675244e09b7c202b4fa6b67f6268392b1b260f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103959888"
---
# <a name="named-pipes"></a>Named Pipes

Bei einem *Named Pipe* handelt es sich um eine benannte, unidirektionale oder Duplex Pipe für die Kommunikation zwischen dem Pipeserver und mindestens einem Pipe-Client. Alle Instanzen eines Named Pipe haben denselben Pipenamen, aber jede Instanz verfügt über eigene Puffer und Handles und stellt einen separaten Kanal für die Client-/Serverkommunikation bereit. Die Verwendung von-Instanzen ermöglicht es mehreren Pipe-Clients, dieselbe Named Pipe gleichzeitig zu verwenden.

Jeder Prozess kann auf Named Pipes zugreifen, unterliegt den Sicherheitsüberprüfungen, sodass benannte Pipes eine einfache Form der Kommunikation zwischen Verwandten oder nicht verknüpften Prozessen darstellen.

Jeder Prozess kann sowohl als Server als auch als Client fungieren, sodass eine Peer-zu-Peer-Kommunikation möglich ist. Wie hier verwendet, verweist der Begriff Pipe-Server auf einen Prozess, der eine Named Pipe erstellt, und der Begriff Pipe-Client verweist auf einen Prozess, der eine Verbindung mit einer Instanz eines Named Pipe herstellt. Die serverseitige Funktion zum Instanziieren eines Named Pipe ist " [**anatamedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)". Die serverseitige Funktion zum Akzeptieren einer Verbindung ist [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe). Ein Client Prozess stellt eine Verbindung mit einem Named Pipe mithilfe [**der Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion" oder " [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) " her.

Named Pipes können verwendet werden, um die Kommunikation zwischen Prozessen auf demselben Computer oder zwischen Prozessen auf verschiedenen Computern in einem Netzwerk bereitzustellen. Wenn der Server Dienst ausgeführt wird, sind alle Named Pipes Remote zugänglich. Wenn Sie eine Named Pipe nur lokal verwenden möchten, verweigern Sie den Zugriff auf das NT-Autorität- \\ Netzwerk, oder wechseln Sie zum lokalen RPC.

Weitere Informationen finden Sie unter den folgenden Themen:

-   [Pipenamen](pipe-names.md)
-   [Named Pipe-Öffnungs Modi](named-pipe-open-modes.md)
-   [Named Pipe-Typ, Lese-und warte Modi](named-pipe-type-read-and-wait-modes.md)
-   [Named Pipe-Instanzen](named-pipe-instances.md)
-   [Named Pipe-Vorgänge](named-pipe-operations.md)
-   [Synchrone und überlappende Eingabe und Ausgabe](synchronous-and-overlapped-input-and-output.md)
-   [Sicherheit und Zugriffsrechte für benannte Pipe](named-pipe-security-and-access-rights.md)
-   [Annehmen der Identität eines Named Pipe-Clients](impersonating-a-named-pipe-client.md)
-   [Verwenden von Pipes](using-pipes.md)

 

 
