---
description: Der gesamte Beispielcode für die TCP/IP-Client-und-Serveranwendung wird ausgeführt.
ms.assetid: 617dfdf6-f7a7-4e72-8c77-8cfa3ab232e7
title: Ausführen des WinSock-Client-und Server Code Beispiels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9b3588af6bac668f0b7c785bafe2f69de4ef2b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958929"
---
# <a name="running-the-winsock-client-and-server-code-sample"></a><span data-ttu-id="585e9-103">Ausführen des WinSock-Client-und Server Code Beispiels</span><span class="sxs-lookup"><span data-stu-id="585e9-103">Running the Winsock Client and Server Code Sample</span></span>

<span data-ttu-id="585e9-104">Dieser Abschnitt enthält den gesamten Quellcode für die TCP/IP-Client-und-Server Anwendungen:</span><span class="sxs-lookup"><span data-stu-id="585e9-104">This section contains the complete source code for the TCP/IP Client and Server applications:</span></span>

-   [<span data-ttu-id="585e9-105">Vervollständigen des WinSock-Client Codes</span><span class="sxs-lookup"><span data-stu-id="585e9-105">Complete Winsock Client Code</span></span>](complete-client-code.md)
-   [<span data-ttu-id="585e9-106">Vervollständigen des Winsock-Server Codes</span><span class="sxs-lookup"><span data-stu-id="585e9-106">Complete Winsock Server Code</span></span>](complete-server-code.md)

<span data-ttu-id="585e9-107">Die Serveranwendung muss gestartet werden, bevor die Client Anwendung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="585e9-107">The server application should be started before the client application is started.</span></span>

<span data-ttu-id="585e9-108">Kompilieren Sie zum Ausführen des Servers den vollständigen Server Quellcode, und führen Sie die ausführbare Datei aus.</span><span class="sxs-lookup"><span data-stu-id="585e9-108">To execute the server, compile the complete server source code and run the executable file.</span></span> <span data-ttu-id="585e9-109">Die Serveranwendung lauscht an TCP-Port 27015, wenn ein Client eine Verbindung herstellen soll.</span><span class="sxs-lookup"><span data-stu-id="585e9-109">The server application listens on TCP port 27015 for a client to connect.</span></span> <span data-ttu-id="585e9-110">Nachdem ein Client eine Verbindung hergestellt hat, empfängt der Server die Daten vom Client und gibt die Daten zurück, die an den Client zurückgesendet werden.</span><span class="sxs-lookup"><span data-stu-id="585e9-110">Once a client connects, the server receives data from the client and echoes (sends) the data received back to the client.</span></span> <span data-ttu-id="585e9-111">Wenn der Client die Verbindung herunterfährt, fährt der Server den Clientsocket herunter, schließt den Socket und wird beendet.</span><span class="sxs-lookup"><span data-stu-id="585e9-111">When the client shuts down the connection, the server shuts down the client socket, closes the socket, and exits.</span></span>

<span data-ttu-id="585e9-112">Kompilieren Sie den vollständigen Client Quellcode, und führen Sie die ausführbare Datei aus, um den Client auszuführen.</span><span class="sxs-lookup"><span data-stu-id="585e9-112">To execute the client, compile the complete client source code and run the executable file.</span></span> <span data-ttu-id="585e9-113">Die Client Anwendung erfordert, dass der Name des Computers oder der IP-Adresse des Computers, auf dem die Serveranwendung ausgeführt wird, als Befehlszeilenparameter übergeben wird, wenn der Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="585e9-113">The client application requires that name of the computer or IP address of the computer where the server application is running is passed as a command-line parameter when the client is executed.</span></span> <span data-ttu-id="585e9-114">Wenn der Client und der Server auf dem Beispiel Computer ausgeführt werden, kann der Client wie folgt gestartet werden:</span><span class="sxs-lookup"><span data-stu-id="585e9-114">If the client and server are executed on the sample computer, the client can be started as follows:</span></span>

<span data-ttu-id="585e9-115">**Client localhost**</span><span class="sxs-lookup"><span data-stu-id="585e9-115">**client localhost**</span></span>

<span data-ttu-id="585e9-116">Der Client versucht, eine Verbindung mit dem Server über den TCP-Port 27015 herzustellen.</span><span class="sxs-lookup"><span data-stu-id="585e9-116">The client tries to connect to the server on TCP port 27015.</span></span> <span data-ttu-id="585e9-117">Sobald der Client eine Verbindung herstellt, sendet der Client Daten an den Server und empfängt alle vom Server zurückgesendeten Daten.</span><span class="sxs-lookup"><span data-stu-id="585e9-117">Once the client connects, the client sends data to the server and receives any data send back from the server.</span></span> <span data-ttu-id="585e9-118">Der Client schließt dann den Socket und wird beendet.</span><span class="sxs-lookup"><span data-stu-id="585e9-118">The client then closes the socket and exits.</span></span>

## <a name="related-topics"></a><span data-ttu-id="585e9-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="585e9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="585e9-120">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="585e9-120">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



