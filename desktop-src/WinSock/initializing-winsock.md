---
description: Alle Prozesse (Anwendungen oder DLLs), die Winsock-Funktionen aufrufen, müssen die Verwendung der Windows Sockets-DLL initialisieren, bevor andere Winsock-Funktionen aufgerufen werden. Dadurch wird auch sicherstellt, dass Winsock auf dem System unterstützt wird.
ms.assetid: 300858d8-bed3-4a3c-abb5-2cecd100e5d7
title: Initialisieren von Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9d3d02805c684c677c4358cf79c421d6a577f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526159"
---
# <a name="initializing-winsock"></a><span data-ttu-id="b5622-104">Initialisieren von Winsock</span><span class="sxs-lookup"><span data-stu-id="b5622-104">Initializing Winsock</span></span>

<span data-ttu-id="b5622-105">Alle Prozesse (Anwendungen oder DLLs), die Winsock-Funktionen aufrufen, müssen die Verwendung der Windows Sockets-DLL initialisieren, bevor andere Winsock-Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b5622-105">All processes (applications or DLLs) that call Winsock functions must initialize the use of the Windows Sockets DLL before making other Winsock functions calls.</span></span> <span data-ttu-id="b5622-106">Dadurch wird auch sicherstellt, dass Winsock auf dem System unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="b5622-106">This also makes certain that Winsock is supported on the system.</span></span>

<span data-ttu-id="b5622-107">**So initialisieren Sie Winsock**</span><span class="sxs-lookup"><span data-stu-id="b5622-107">**To initialize Winsock**</span></span>

1.  <span data-ttu-id="b5622-108">Erstellen Sie ein [**wsadata**](/windows/desktop/api/winsock/ns-winsock-wsadata) -Objekt namens wsadata.</span><span class="sxs-lookup"><span data-stu-id="b5622-108">Create a [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) object called wsaData.</span></span>
    ```C++
    WSADATA wsaData;
    ```

    

2.  <span data-ttu-id="b5622-109">Nennen Sie [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) , und geben Sie den Wert als Ganzzahl zurück, und suchen Sie nach Fehlern.</span><span class="sxs-lookup"><span data-stu-id="b5622-109">Call [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) and return its value as an integer and check for errors.</span></span>
    ```C++
    int iResult;

    // Initialize Winsock
    iResult = WSAStartup(MAKEWORD(2,2), &wsaData);
    if (iResult != 0) {
        printf("WSAStartup failed: %d\n", iResult);
        return 1;
    }
    ```

    

<span data-ttu-id="b5622-110">Die [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) -Funktion wird aufgerufen, um die Verwendung von ws2-32.dll zu initiieren \_ .</span><span class="sxs-lookup"><span data-stu-id="b5622-110">The [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) function is called to initiate use of WS2\_32.dll.</span></span>

<span data-ttu-id="b5622-111">Die [**wsadata**](/windows/desktop/api/winsock/ns-winsock-wsadata) -Struktur enthält Informationen über die Windows Sockets-Implementierung.</span><span class="sxs-lookup"><span data-stu-id="b5622-111">The [**WSADATA**](/windows/desktop/api/winsock/ns-winsock-wsadata) structure contains information about the Windows Sockets implementation.</span></span> <span data-ttu-id="b5622-112">Der makeword (2, 2)-Parameter von [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) stellt eine Anforderung für die Version 2,2 von Winsock im System her und legt die übergebenen Version als höchste Version der Windows Sockets-Unterstützung fest, die der Aufrufer verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="b5622-112">The MAKEWORD(2,2) parameter of [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) makes a request for version 2.2 of Winsock on the system, and sets the passed version as the highest version of Windows Sockets support that the caller can use.</span></span>

<span data-ttu-id="b5622-113">Nächster Schritt für einen Client: [Erstellen eines Sockets für den Client](creating-a-socket-for-the-client.md)</span><span class="sxs-lookup"><span data-stu-id="b5622-113">Next Step for a Client: [Creating a Socket for the Client](creating-a-socket-for-the-client.md)</span></span>

<span data-ttu-id="b5622-114">Nächster Schritt für einen Server: [Erstellen eines Sockets für den Server](creating-a-socket-for-the-server.md)</span><span class="sxs-lookup"><span data-stu-id="b5622-114">Next Step for a Server: [Creating a Socket for the Server](creating-a-socket-for-the-server.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b5622-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b5622-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5622-116">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="b5622-116">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="b5622-117">Erstellen einer grundlegenden Winsock-Anwendung</span><span class="sxs-lookup"><span data-stu-id="b5622-117">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> </dl>

 

 



