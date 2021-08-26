---
description: Eine Named Pipe ist eine benannte, einseitige oder Duplexpipe für die Kommunikation zwischen dem Pipeserver und mindestens einem Pipeclient.
ms.assetid: 7a4c11ac-14c0-4a93-b72e-02fb8852cc15
title: Named Pipes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f06e7f291776e2ecba3b9da93a94d235d4fbe7df151353a7c3d379eb4d50fdd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014900"
---
# <a name="named-pipes"></a>Named Pipes

Eine *Named Pipe* ist eine benannte, einseitige oder Duplexpipe für die Kommunikation zwischen dem Pipeserver und mindestens einem Pipeclient. Alle Instanzen einer Named Pipe verwenden denselben Pipenamen, aber jede Instanz verfügt über eigene Puffer und Handles und stellt einen separaten Kanal für die Client-/Serverkommunikation zurEntwickelung. Die Verwendung von -Instanzen ermöglicht es mehreren Pipeclients, dieselbe Named Pipe gleichzeitig zu verwenden.

Jeder Prozess kann auf Named Pipes zugreifen, die Sicherheitsüberprüfungen unterliegen, was Named Pipes zu einer einfachen Form der Kommunikation zwischen verwandten oder nicht verbundenen Prozessen macht.

Jeder Prozess kann sowohl als Server als auch als Client fungieren, was eine Peer-zu-Peer-Kommunikation ermöglicht. Wie hier verwendet, bezieht sich der Begriff Pipeserver auf einen Prozess, der eine Named Pipe erstellt, und der Begriff Pipeclient bezieht sich auf einen Prozess, der eine Verbindung mit einer Instanz einer Named Pipe herstellt. Die serverseitige Funktion zum Instanziieren einer Named Pipe ist [**CreateNamedPipe.**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea) Die serverseitige Funktion zum Akzeptieren einer Verbindung ist [**ConnectNamedPipe.**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe) Ein Clientprozess stellt mithilfe der [**CreateFile-**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) oder [**CallNamedPipe-Funktion**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) eine Verbindung mit einer Named Pipe-Datei herstellt.

Named Pipes können verwendet werden, um die Kommunikation zwischen Prozessen auf demselben Computer oder zwischen Prozessen auf verschiedenen Computern in einem Netzwerk zu ermöglichen. Wenn der Serverdienst ausgeführt wird, kann remote auf alle Named Pipes zugegriffen werden. Wenn Sie beabsichtigen, eine Named Pipe nur lokal zu verwenden, verweigern Sie den Zugriff auf NT AUTHORITY NETWORK, oder wechseln Sie \\ zu lokalem RPC.

Weitere Informationen finden Sie in den folgenden Themen:

-   [Pipenamen](pipe-names.md)
-   [Named Pipe-Open-Modi](named-pipe-open-modes.md)
-   [Named Pipe-Typ, Lese- und Wartemodi](named-pipe-type-read-and-wait-modes.md)
-   [Named Pipe-Instanzen](named-pipe-instances.md)
-   [Named Pipe-Vorgänge](named-pipe-operations.md)
-   [Synchrone und überlappende Eingabe und Ausgabe](synchronous-and-overlapped-input-and-output.md)
-   [Named Pipe-Sicherheit und -Zugriffsrechte](named-pipe-security-and-access-rights.md)
-   [Identitätswechsel für einen Named Pipe-Client](impersonating-a-named-pipe-client.md)
-   [Verwenden von Pipes](using-pipes.md)

 

 
