---
description: Die ursprüngliche Includedatei für die Verwendung mit Windows Sockets 1,1 war die Header Datei "Winsock. h".
ms.assetid: 0536abcc-4277-4bd8-927c-3bf429bc65bb
title: Includedateien
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adf7a4edcd70e6a6280b26f7b6ab9f0f1dab674e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343499"
---
# <a name="include-files"></a><span data-ttu-id="6faf3-103">Includedateien</span><span class="sxs-lookup"><span data-stu-id="6faf3-103">Include Files</span></span>

<span data-ttu-id="6faf3-104">Die ursprüngliche Includedatei für die Verwendung mit Windows Sockets 1,1 war die Header Datei " *Winsock. h* ".</span><span class="sxs-lookup"><span data-stu-id="6faf3-104">The original include file for use with Windows Sockets 1.1 was the *Winsock.h* header file.</span></span> <span data-ttu-id="6faf3-105">Zum Vereinfachen der Portierung von vorhandenem Quellcode auf der Grundlage von Berkeley-socketsockets auf Windows Sockets wurde empfohlen, dass Windows Sockets Development Kits für Winsock 1,1 mit mehreren Includedateien mit denselben Namen wie standardmäßige UNIX-Includedateien (z. b. *sys/Socket. h* -und ARPA/inet. h-Header Dateien) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6faf3-105">To ease porting existing source code based on Berkeley UNIX sockets to Windows sockets, Windows Sockets development kits for Winsock 1.1 were encouraged to be supplied with several include files with the same names as standard UNIX include files (the *sys/socket.h* and arpa/inet.h header files, for example).</span></span> <span data-ttu-id="6faf3-106">Diese Winsock-Header Dateien mit ähnlichen Namen enthielten jedoch lediglich eine-Direktive, um die Header Datei " *Winsock2. h* " einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="6faf3-106">However, these similarly-name Winsock header files merely contained a directive to include the *Winsock2.h* header file.</span></span>

<span data-ttu-id="6faf3-107">Wenn Windows Sockets 2 freigegeben wurde, wurde die primäre Includedatei für die Verwendung mit Windows Sockets in *Winsock2. h* umbenannt.</span><span class="sxs-lookup"><span data-stu-id="6faf3-107">When Windows Sockets 2 was released, the primary include file for use with Windows Sockets was renamed to *Winsock2.h*.</span></span> <span data-ttu-id="6faf3-108">Die ältere Original- *Winsock. h* -Header Datei für Winsock 1,1 wurde ebenfalls für die Kompatibilität mit älteren Anwendungen beibehalten.</span><span class="sxs-lookup"><span data-stu-id="6faf3-108">The older original *Winsock.h* header file for Winsock 1.1 was also retained for compatibility with older applications.</span></span> <span data-ttu-id="6faf3-109">Die Entwicklung von mit Winsock 1,1 kompatiblen Anwendungen wurde seit der Veröffentlichung von Windows 2000 als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="6faf3-109">The development of Winsock 1.1 compatible applications has been deprecated since Windows 2000 was released.</span></span> <span data-ttu-id="6faf3-110">Alle Anwendungen sollten jetzt die include *Winsock2. h* -Direktive in Winsock-Anwendungs Quelldateien verwenden.</span><span class="sxs-lookup"><span data-stu-id="6faf3-110">All applications should now use use the include *Winsock2.h* directive in Winsock application source files.</span></span>

<span data-ttu-id="6faf3-111">Die Header Datei " *Winsock2. h* " enthält die meisten WinSock-Funktionen,-Strukturen und-Definitionen.</span><span class="sxs-lookup"><span data-stu-id="6faf3-111">The *Winsock2.h* header file contains most of the Winsock functions, structures, and definitions.</span></span> <span data-ttu-id="6faf3-112">Die Header Datei " *Ws2tcpip. h* " enthält Definitionen, die im Winsock 2-Protocol-Specific Anhang-Dokument für TCP/IP eingeführt wurden und neuere Funktionen und Strukturen enthalten, die zum Abrufen von IP-Adressen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6faf3-112">The *Ws2tcpip.h* header file contains definitions introduced in the WinSock 2 Protocol-Specific Annex document for TCP/IP that includes newer functions and structures used to retrieve IP addresses.</span></span> <span data-ttu-id="6faf3-113">Hierzu gehören die [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -und die [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) -Familie von Funktionen, die die Namensauflösung für IPv4-oder IPv6-Adressen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6faf3-113">These include the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions that provide name resolution for both IPv4 or IPv6 addresses.</span></span> <span data-ttu-id="6faf3-114">Die Header Datei " *Ws2tcpip. h* " ist nur erforderlich, wenn diese IP-agnostischen Benennungs Funktionen von der Anwendung benötigt werden.</span><span class="sxs-lookup"><span data-stu-id="6faf3-114">The *Ws2tcpip.h* header file is only needed if these IP-agnostic naming functions are required by the application.</span></span>

<span data-ttu-id="6faf3-115">Die Header Datei " *mtausock. h* " enthält Definitionen für Microsoft-spezifische Erweiterungen für Windows Sockets 2 (z. b.[**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**Accept tex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)und [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)).</span><span class="sxs-lookup"><span data-stu-id="6faf3-115">The *Mswsock.h* header file contains definitions for Microsoft-specific extensions to the Windows Sockets 2 ([**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile), [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex), and [**ConnectEx**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex), for example).</span></span> <span data-ttu-id="6faf3-116">Die Header Datei " *mswap. h* " ist normalerweise nicht erforderlich, es sei denn, diese Microsoft-spezifischen Erweiterungen werden von der Anwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="6faf3-116">The *Mswsock.h* header file is not normally needed unless these Microsoft-specific extensions are used by the application.</span></span>

<span data-ttu-id="6faf3-117">Die Header Datei " *Winsock2. h* " enthält intern Kernelemente aus der Header Datei " *Windows. h* ", sodass \# in Winsock-Anwendungen normalerweise keine Include-Zeile für die Header Datei " *Windows. h* " vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="6faf3-117">The *Winsock2.h* header file internally includes core elements from the *Windows.h* header file, so there is not usually an \#include line for the *Windows.h* header file in Winsock applications.</span></span> <span data-ttu-id="6faf3-118">Wenn eine \# Include-Zeile für die Header Datei " *Windows. h* " erforderlich ist, sollte diesem das \# Win32 \_ \_ -und Mean-Makro definiert werden \_ .</span><span class="sxs-lookup"><span data-stu-id="6faf3-118">If an \#include line is needed for the *Windows.h* header file, this should be preceded with the \#define WIN32\_LEAN\_AND\_MEAN macro.</span></span> <span data-ttu-id="6faf3-119">Aus historischen Gründen hat der *Windows. h* -Header standardmäßig die *Winsock. h* -Header Datei für Windows Sockets 1,1.</span><span class="sxs-lookup"><span data-stu-id="6faf3-119">For historical reasons, the *Windows.h* header defaults to including the *Winsock.h* header file for Windows Sockets 1.1.</span></span> <span data-ttu-id="6faf3-120">Die Deklarationen in der Header Datei " *Winsock. h* " verursachen einen Konflikt mit den Deklarationen in der *Winsock2. h* -Header Datei, die von Windows Sockets 2 benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="6faf3-120">The declarations in the *Winsock.h* header file will conflict with the declarations in the *Winsock2.h* header file required by Windows Sockets 2.</span></span> <span data-ttu-id="6faf3-121">Das Win32 \_ \_ -und \_ Mean-Makro verhindert, dass die *Winsock. h* -Datei vom *Windows. h* -Header eingeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="6faf3-121">The WIN32\_LEAN\_AND\_MEAN macro prevents the *Winsock.h* from being included by the *Windows.h* header.</span></span> <span data-ttu-id="6faf3-122">Im folgenden wird ein Beispiel gezeigt, das dies veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="6faf3-122">An example illustrating this is shown below.</span></span>


```C++
#include <winsock2.h>
#include <ws2tcpip.h>
#include <stdio.h>

#pragma comment(lib, "Ws2_32.lib")

int main() {
  return 0;
}

```



## <a name="related-topics"></a><span data-ttu-id="6faf3-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="6faf3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6faf3-124">Erstellen einer grundlegenden Winsock-Anwendung</span><span class="sxs-lookup"><span data-stu-id="6faf3-124">Creating a Basic Winsock Application</span></span>](creating-a-basic-winsock-application.md)
</dt> <dt>

[<span data-ttu-id="6faf3-125">Einstieg in Winsock</span><span class="sxs-lookup"><span data-stu-id="6faf3-125">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> <dt>

[<span data-ttu-id="6faf3-126">Portieren von Socketanwendungen auf Winsock</span><span class="sxs-lookup"><span data-stu-id="6faf3-126">Porting Socket Applications to Winsock</span></span>](porting-socket-applications-to-winsock.md)
</dt> <dt>

[<span data-ttu-id="6faf3-127">Überlegungen zur Winsock-Programmierung</span><span class="sxs-lookup"><span data-stu-id="6faf3-127">Winsock Programming Considerations</span></span>](winsock-programming-considerations.md)
</dt> </dl>

 

 
