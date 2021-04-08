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
# <a name="named-pipes"></a><span data-ttu-id="c460f-103">Named Pipes</span><span class="sxs-lookup"><span data-stu-id="c460f-103">Named Pipes</span></span>

<span data-ttu-id="c460f-104">Bei einem *Named Pipe* handelt es sich um eine benannte, unidirektionale oder Duplex Pipe für die Kommunikation zwischen dem Pipeserver und mindestens einem Pipe-Client.</span><span class="sxs-lookup"><span data-stu-id="c460f-104">A *named pipe* is a named, one-way or duplex pipe for communication between the pipe server and one or more pipe clients.</span></span> <span data-ttu-id="c460f-105">Alle Instanzen eines Named Pipe haben denselben Pipenamen, aber jede Instanz verfügt über eigene Puffer und Handles und stellt einen separaten Kanal für die Client-/Serverkommunikation bereit.</span><span class="sxs-lookup"><span data-stu-id="c460f-105">All instances of a named pipe share the same pipe name, but each instance has its own buffers and handles, and provides a separate conduit for client/server communication.</span></span> <span data-ttu-id="c460f-106">Die Verwendung von-Instanzen ermöglicht es mehreren Pipe-Clients, dieselbe Named Pipe gleichzeitig zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c460f-106">The use of instances enables multiple pipe clients to use the same named pipe simultaneously.</span></span>

<span data-ttu-id="c460f-107">Jeder Prozess kann auf Named Pipes zugreifen, unterliegt den Sicherheitsüberprüfungen, sodass benannte Pipes eine einfache Form der Kommunikation zwischen Verwandten oder nicht verknüpften Prozessen darstellen.</span><span class="sxs-lookup"><span data-stu-id="c460f-107">Any process can access named pipes, subject to security checks, making named pipes an easy form of communication between related or unrelated processes.</span></span>

<span data-ttu-id="c460f-108">Jeder Prozess kann sowohl als Server als auch als Client fungieren, sodass eine Peer-zu-Peer-Kommunikation möglich ist.</span><span class="sxs-lookup"><span data-stu-id="c460f-108">Any process can act as both a server and a client, making peer-to-peer communication possible.</span></span> <span data-ttu-id="c460f-109">Wie hier verwendet, verweist der Begriff Pipe-Server auf einen Prozess, der eine Named Pipe erstellt, und der Begriff Pipe-Client verweist auf einen Prozess, der eine Verbindung mit einer Instanz eines Named Pipe herstellt.</span><span class="sxs-lookup"><span data-stu-id="c460f-109">As used here, the term pipe server refers to a process that creates a named pipe, and the term pipe client refers to a process that connects to an instance of a named pipe.</span></span> <span data-ttu-id="c460f-110">Die serverseitige Funktion zum Instanziieren eines Named Pipe ist " [**anatamedpipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea)".</span><span class="sxs-lookup"><span data-stu-id="c460f-110">The server-side function for instantiating a named pipe is [**CreateNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-createnamedpipea).</span></span> <span data-ttu-id="c460f-111">Die serverseitige Funktion zum Akzeptieren einer Verbindung ist [**connectnamedpipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span><span class="sxs-lookup"><span data-stu-id="c460f-111">The server-side function for accepting a connection is [**ConnectNamedPipe**](/windows/win32/api/namedpipeapi/nf-namedpipeapi-connectnamedpipe).</span></span> <span data-ttu-id="c460f-112">Ein Client Prozess stellt eine Verbindung mit einem Named Pipe mithilfe [**der Funktion**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) "Funktion" oder " [**callnamedpipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) " her.</span><span class="sxs-lookup"><span data-stu-id="c460f-112">A client process connects to a named pipe by using the [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) or [**CallNamedPipe**](/windows/desktop/api/Winbase/nf-winbase-callnamedpipea) function.</span></span>

<span data-ttu-id="c460f-113">Named Pipes können verwendet werden, um die Kommunikation zwischen Prozessen auf demselben Computer oder zwischen Prozessen auf verschiedenen Computern in einem Netzwerk bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c460f-113">Named pipes can be used to provide communication between processes on the same computer or between processes on different computers across a network.</span></span> <span data-ttu-id="c460f-114">Wenn der Server Dienst ausgeführt wird, sind alle Named Pipes Remote zugänglich.</span><span class="sxs-lookup"><span data-stu-id="c460f-114">If the server service is running, all named pipes are accessible remotely.</span></span> <span data-ttu-id="c460f-115">Wenn Sie eine Named Pipe nur lokal verwenden möchten, verweigern Sie den Zugriff auf das NT-Autorität- \\ Netzwerk, oder wechseln Sie zum lokalen RPC.</span><span class="sxs-lookup"><span data-stu-id="c460f-115">If you intend to use a named pipe locally only, deny access to NT AUTHORITY\\NETWORK or switch to local RPC.</span></span>

<span data-ttu-id="c460f-116">Weitere Informationen finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="c460f-116">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="c460f-117">Pipenamen</span><span class="sxs-lookup"><span data-stu-id="c460f-117">Pipe Names</span></span>](pipe-names.md)
-   [<span data-ttu-id="c460f-118">Named Pipe-Öffnungs Modi</span><span class="sxs-lookup"><span data-stu-id="c460f-118">Named Pipe Open Modes</span></span>](named-pipe-open-modes.md)
-   [<span data-ttu-id="c460f-119">Named Pipe-Typ, Lese-und warte Modi</span><span class="sxs-lookup"><span data-stu-id="c460f-119">Named Pipe Type, Read, and Wait Modes</span></span>](named-pipe-type-read-and-wait-modes.md)
-   [<span data-ttu-id="c460f-120">Named Pipe-Instanzen</span><span class="sxs-lookup"><span data-stu-id="c460f-120">Named Pipe Instances</span></span>](named-pipe-instances.md)
-   [<span data-ttu-id="c460f-121">Named Pipe-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="c460f-121">Named Pipe Operations</span></span>](named-pipe-operations.md)
-   [<span data-ttu-id="c460f-122">Synchrone und überlappende Eingabe und Ausgabe</span><span class="sxs-lookup"><span data-stu-id="c460f-122">Synchronous and Overlapped Input and Output</span></span>](synchronous-and-overlapped-input-and-output.md)
-   [<span data-ttu-id="c460f-123">Sicherheit und Zugriffsrechte für benannte Pipe</span><span class="sxs-lookup"><span data-stu-id="c460f-123">Named Pipe Security and Access Rights</span></span>](named-pipe-security-and-access-rights.md)
-   [<span data-ttu-id="c460f-124">Annehmen der Identität eines Named Pipe-Clients</span><span class="sxs-lookup"><span data-stu-id="c460f-124">Impersonating a Named Pipe Client</span></span>](impersonating-a-named-pipe-client.md)
-   [<span data-ttu-id="c460f-125">Verwenden von Pipes</span><span class="sxs-lookup"><span data-stu-id="c460f-125">Using Pipes</span></span>](using-pipes.md)

 

 
