---
description: Neue Funktionen wurden mit der Windows Sockets-Schnittstelle eingeführt, die speziell für die Vereinfachung der Windows Sockets-Programmierung konzipiert wurde. Einer der Vorteile dieser neuen Windows Sockets-Funktionen ist die integrierte Unterstützung für IPv6 und IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Funktionsaufrufe für IPv6-Winsock-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a56fe5087e17a9a4eb1337ac803b8500b1fe9c27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359832"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a><span data-ttu-id="96411-104">Funktionsaufrufe für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="96411-104">Function Calls for IPv6 Winsock Applications</span></span>

<span data-ttu-id="96411-105">Neue Funktionen wurden mit der Windows Sockets-Schnittstelle eingeführt, die speziell für die Vereinfachung der Windows Sockets-Programmierung konzipiert wurde.</span><span class="sxs-lookup"><span data-stu-id="96411-105">New functions have been introduced to the Windows Sockets interface specifically designed to make Windows Sockets programming easier.</span></span> <span data-ttu-id="96411-106">Einer der Vorteile dieser neuen Windows Sockets-Funktionen ist die integrierte Unterstützung für IPv6 und IPv4.</span><span class="sxs-lookup"><span data-stu-id="96411-106">One of the benefits of these new Windows Sockets functions is integrated support for both IPv6 and IPv4.</span></span>

<span data-ttu-id="96411-107">Diese neuen Windows Sockets-Funktionen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="96411-107">These new Windows Sockets functions include the following:</span></span>

-   [<span data-ttu-id="96411-108">**WSAConnectByName**</span><span class="sxs-lookup"><span data-stu-id="96411-108">**WSAConnectByName**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [<span data-ttu-id="96411-109">**Wsaconnectbylist**</span><span class="sxs-lookup"><span data-stu-id="96411-109">**WSAConnectByList**</span></span>](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   <span data-ttu-id="96411-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktions Familie (**getaddrinfo**, [**getaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**getaddrinfow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**freaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**freaddrinfow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)und [**abstaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span><span class="sxs-lookup"><span data-stu-id="96411-110">[**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) family of functions (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow), and [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))</span></span>
-   <span data-ttu-id="96411-111">[**getnameingefo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) -Funktions Familie (**getnameingefo** und [**getnameingefow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span><span class="sxs-lookup"><span data-stu-id="96411-111">[**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) family of functions (**getnameinfo** and [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))</span></span>

<span data-ttu-id="96411-112">Außerdem wurden neue IP-Hilfsfunktionen mit Unterstützung für IPv6 und IPv4 hinzugefügt, um die Windows-Socketprogrammierung zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="96411-112">In addition, new IP Helper functions with support for both IPv6 and IPv4 have been added to simplify Windows Sockets programming.</span></span> <span data-ttu-id="96411-113">Diese neuen IP-Hilfsfunktionen umfassen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="96411-113">These new IP Helper functions include the following:</span></span>

-   [<span data-ttu-id="96411-114">**Getadaptersadressen**</span><span class="sxs-lookup"><span data-stu-id="96411-114">**GetAdaptersAddresses**</span></span>](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

<span data-ttu-id="96411-115">Beim Hinzufügen von IPv6-Unterstützung zu einer Anwendung sollten die folgenden Richtlinien verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="96411-115">When adding IPv6 support to an application the following guidelines should be used:</span></span>

-   <span data-ttu-id="96411-116">Verwenden Sie [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) , um eine Verbindung mit einem Endpunkt bei Angabe eines Host Namens und-Ports herzustellen.</span><span class="sxs-lookup"><span data-stu-id="96411-116">Use [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) to establish a connection to an endpoint given a host name and port.</span></span> <span data-ttu-id="96411-117">Die **WSAConnectByName** -Funktion ist unter Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="96411-117">The **WSAConnectByName** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="96411-118">Verwenden Sie [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) , um eine Verbindung mit einer aus einer Sammlung möglicher Endpunkte herzustellen, die durch eine Gruppe von Zieladressen (Hostnamen und Ports) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="96411-118">Use [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) to establish a connection to one out of a collection of possible endpoints represented by a set of destination addresses (host names and ports).</span></span> <span data-ttu-id="96411-119">Die **wsaconnectbylist** -Funktion ist unter Windows Vista und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="96411-119">The **WSAConnectByList** function is available on Windows Vista and later.</span></span>
-   <span data-ttu-id="96411-120">Ersetzen Sie die [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) -Funktionsaufrufe durch Aufrufe einer der neuen Windows Sockets-Funktionen [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) .</span><span class="sxs-lookup"><span data-stu-id="96411-120">Replace [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function calls with calls to one of the new [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Windows Sockets functions.</span></span> <span data-ttu-id="96411-121">Die **getaddrinfo** -Funktion mit Unterstützung für das IPv6-Protokoll ist unter Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="96411-121">The **getaddrinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="96411-122">Das IPv6-Protokoll wird auch unter Windows 2000 unterstützt, wenn die IPv6-Technologievorschau für Windows 2000 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="96411-122">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>
-   <span data-ttu-id="96411-123">Ersetzen Sie die [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) -Funktionsaufrufe durch Aufrufe einer der neuen Windows Sockets-Funktionen von [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) .</span><span class="sxs-lookup"><span data-stu-id="96411-123">Replace [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function calls with calls to one of the new [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Windows Sockets functions.</span></span> <span data-ttu-id="96411-124">Die **getnaminfo** -Funktion mit Unterstützung für das IPv6-Protokoll ist unter Windows XP und höher verfügbar.</span><span class="sxs-lookup"><span data-stu-id="96411-124">The **getnameinfo** function with support for the IPv6 protocol is available on Windows XP and later.</span></span> <span data-ttu-id="96411-125">Das IPv6-Protokoll wird auch unter Windows 2000 unterstützt, wenn die IPv6-Technologievorschau für Windows 2000 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="96411-125">The IPv6 protocol is also supported on Windows 2000 when the IPv6 Technology Preview for Windows 2000 is installed.</span></span>

## <a name="wsaconnectbyname"></a><span data-ttu-id="96411-126">WSAConnectByName</span><span class="sxs-lookup"><span data-stu-id="96411-126">WSAConnectByName</span></span>

<span data-ttu-id="96411-127">Die [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion vereinfacht das Herstellen einer Verbindung mit einem Endpunkt mithilfe eines streambasierten Sockets unter Berücksichtigung des Host Namens oder der IP-Adresse des Ziels (IPv4 oder IPv6).</span><span class="sxs-lookup"><span data-stu-id="96411-127">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function simplifies connecting to an endpoint using a stream-based socket given the destination's hostname or IP address (IPv4 or IPv6).</span></span> <span data-ttu-id="96411-128">Diese Funktion reduziert den Quellcode, der erforderlich ist, um eine IP-Anwendung zu erstellen, die unabhängig von der verwendeten Version des IP-Protokolls ist.</span><span class="sxs-lookup"><span data-stu-id="96411-128">This function reduces the source code required to create an IP application that is agnostic to the version of the IP protocol used.</span></span> <span data-ttu-id="96411-129">**WSAConnectByName** ersetzt die folgenden Schritte in einer typischen TCP-Anwendung zu einem einzelnen Funktions aufzurufen:</span><span class="sxs-lookup"><span data-stu-id="96411-129">**WSAConnectByName** replaces the following steps in a typical TCP application to a single function call:</span></span>

-   <span data-ttu-id="96411-130">Lösen Sie einen Hostnamen in einen Satz von IP-Adressen auf.</span><span class="sxs-lookup"><span data-stu-id="96411-130">Resolve a hostname to a set of IP addresses.</span></span>
-   <span data-ttu-id="96411-131">Für jede IP-Adresse:</span><span class="sxs-lookup"><span data-stu-id="96411-131">For each IP address:</span></span>
    -   <span data-ttu-id="96411-132">Erstellen Sie einen Socket der entsprechenden Adressfamilie.</span><span class="sxs-lookup"><span data-stu-id="96411-132">Create a socket of the appropriate address family.</span></span>
    -   <span data-ttu-id="96411-133">Versucht, eine Verbindung mit der Remote-IP-Adresse herzustellen.</span><span class="sxs-lookup"><span data-stu-id="96411-133">Attempts to connect to the remote IP address.</span></span> <span data-ttu-id="96411-134">Wenn die Verbindung erfolgreich hergestellt wurde, wird zurückgegeben. Andernfalls wird die nächste Remote-IP-Adresse für den Host ausprobiert.</span><span class="sxs-lookup"><span data-stu-id="96411-134">If the connection was successful, it returns; otherwise the next remote IP address for the host is tried.</span></span>

<span data-ttu-id="96411-135">Die [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion geht über das Auflösen des Namens hinaus und versucht dann, eine Verbindung herzustellen.</span><span class="sxs-lookup"><span data-stu-id="96411-135">The [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function goes beyond just resolving the name and then attempting to connect.</span></span> <span data-ttu-id="96411-136">Die Funktion verwendet alle Remote Adressen, die von der Namensauflösung und allen Quell-IP-Adressen des lokalen Computers zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="96411-136">The function uses all of the remote addresses returned by name resolution and all of the local machine's source IP addresses.</span></span> <span data-ttu-id="96411-137">Zuerst wird versucht, die Verbindung mithilfe von Adress Paaren mit der höchsten Erfolgschance herzustellen.</span><span class="sxs-lookup"><span data-stu-id="96411-137">It first attempts to connect using address pairs with the highest chance of success.</span></span> <span data-ttu-id="96411-138">Daher stellt **WSAConnectByName** nicht nur sicher, dass nach Möglichkeit eine Verbindung hergestellt wird, sondern auch die Zeit zum Herstellen der Verbindung minimiert wird.</span><span class="sxs-lookup"><span data-stu-id="96411-138">Therefore, **WSAConnectByName** not only ensures that a connection will be established if possible, but it also minimizes the time to establish the connection.</span></span>

<span data-ttu-id="96411-139">Verwenden Sie die folgende Methode, um sowohl IPv6-als auch IPv4-Kommunikation zu aktivieren:</span><span class="sxs-lookup"><span data-stu-id="96411-139">To enable both IPv6 and IPv4 communications, use the following method:</span></span>

-   <span data-ttu-id="96411-140">Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion muss für einen Socket aufgerufen werden, der für die inet6-Adressfamilie des AF erstellt wurde \_ , um die **IPv6 \_ V6ONLY** Socket-Option vor dem Aufrufen von [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="96411-140">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea).</span></span> <span data-ttu-id="96411-141">Dies wird erreicht, indem die **setsockopt** -Funktion für den Socket aufgerufen wird, wobei der *Level* -Parameter auf **ipproto \_ IPv6** festgelegt ist (siehe [ipproto \_ IPv6-Socketoptionen](ipproto-ipv6-socket-options.md)), der *optname* -Parameter auf **IPv6 \_ V6ONLY** und der *optvalue* -Parameterwert auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="96411-141">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>

<span data-ttu-id="96411-142">Wenn eine Anwendung eine Bindung an eine bestimmte lokale Adresse oder einen bestimmten Port herstellen muss, kann [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) nicht verwendet werden, da der socketparameter für **WSAConnectByName** ein ungebundener Socket sein muss.</span><span class="sxs-lookup"><span data-stu-id="96411-142">If an application needs to bind to a specific local address or port, then [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) cannot be used since the socket parameter to **WSAConnectByName** must be an unbound socket.</span></span>

<span data-ttu-id="96411-143">Das folgende Codebeispiel zeigt nur einige Codezeilen, die erforderlich sind, um diese Funktion zu verwenden, um eine Anwendung zu implementieren, die für die IP-Version agnostisch ist.</span><span class="sxs-lookup"><span data-stu-id="96411-143">The code example below shows only a few lines of code are needed to use this function to implement an application that is agnostic to the IP version.</span></span>

<span data-ttu-id="96411-144">Herstellen einer Verbindung mithilfe von [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span><span class="sxs-lookup"><span data-stu-id="96411-144">Establish a connection using [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(LPWSTR NodeName, LPWSTR PortName) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);
  
    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    bSuccess = WSAConnectByName(ConnSocket, NodeName, 
            PortName, &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="wsaconnectbylist"></a><span data-ttu-id="96411-145">Wsaconnectbylist</span><span class="sxs-lookup"><span data-stu-id="96411-145">WSAConnectByList</span></span>

<span data-ttu-id="96411-146">Die [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) -Funktion stellt eine Verbindung mit einem Host fest, wenn ein Satz möglicher Hosts vorhanden ist (dargestellt durch einen Satz von Ziel-IP-Adressen und Ports).</span><span class="sxs-lookup"><span data-stu-id="96411-146">The [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function establishes a connection to a host given a set of possible hosts (represented by a set of destination IP addresses and ports).</span></span> <span data-ttu-id="96411-147">Die Funktion nimmt alle IP-Adressen und Ports für den Endpunkt und alle IP-Adressen des lokalen Computers an und versucht, eine Verbindung mit allen möglichen Adress Kombinationen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="96411-147">The function takes all IP addresses and ports for the endpoint and all of the local machine's IP addresses, and attempts a connection using all possible address combinations.</span></span>

<span data-ttu-id="96411-148">[**Wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) ist mit der [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion verknüpft.</span><span class="sxs-lookup"><span data-stu-id="96411-148">[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) is related to the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function.</span></span> <span data-ttu-id="96411-149">Anstatt einen einzelnen Hostnamen zu verwenden, akzeptiert **wsaconnectbylist** eine Liste von Hosts (Zieladressen und Port Paare) und stellt eine Verbindung mit einer der Adressen und Ports in der angegebenen Liste her.</span><span class="sxs-lookup"><span data-stu-id="96411-149">Instead of taking a single hostname, **WSAConnectByList** accepts a list of hosts (destination addresses and port pairs) and connects to one of the addresses and ports in the provided list.</span></span> <span data-ttu-id="96411-150">Diese Funktion ist für die Unterstützung von Szenarien konzipiert, in denen eine Anwendung eine Verbindung mit einem beliebigen verfügbaren Host aus einer Liste potenzieller Hosts herstellen muss.</span><span class="sxs-lookup"><span data-stu-id="96411-150">This function is designed to support scenarios in which an application needs to connect to any available host out of a list of potential hosts.</span></span>

<span data-ttu-id="96411-151">Ähnlich wie [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)reduziert die [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) -Funktion den Quellcode, der zum Erstellen, binden und Verbinden eines Sockets erforderlich ist, erheblich.</span><span class="sxs-lookup"><span data-stu-id="96411-151">Similar to [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea), the [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function significantly reduces the source code required to create, bind and connect a socket.</span></span> <span data-ttu-id="96411-152">Diese Funktion vereinfacht die Implementierung einer Anwendung, die mit der IP-Version agnostisch ist.</span><span class="sxs-lookup"><span data-stu-id="96411-152">This function makes it much easier to implement an application that is agnostic to the IP version.</span></span> <span data-ttu-id="96411-153">Die Liste der Adressen eines Hosts, der von dieser Funktion akzeptiert wird, ist möglicherweise IPv6-oder IPv4-Adressen.</span><span class="sxs-lookup"><span data-stu-id="96411-153">The list of addresses for a host accepted by this function may be IPv6 or IPv4 addresses.</span></span>

<span data-ttu-id="96411-154">Die folgenden Schritte müssen ausgeführt werden, bevor die-Funktion aufgerufen wird, damit IPv6-und IPv4-Adressen in der von der Funktion akzeptierten einzelnen Adressliste übermittelt werden können:</span><span class="sxs-lookup"><span data-stu-id="96411-154">To enable both IPv6 and IPv4 addresses to be passed in the single address list accepted by the function, the following steps must be performed prior to calling the function:</span></span>

-   <span data-ttu-id="96411-155">Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion muss für einen Socket aufgerufen werden, der für die inet6-Adressfamilie des AF erstellt wurde \_ , um die **IPv6 \_ V6ONLY** Socket-Option vor dem Aufrufen von [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="96411-155">The [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) function must be called on a socket created for the AF\_INET6 address family to disable the **IPV6\_V6ONLY** socket option before calling [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist).</span></span> <span data-ttu-id="96411-156">Dies wird erreicht, indem die **setsockopt** -Funktion für den Socket aufgerufen wird, wobei der *Level* -Parameter auf **ipproto \_ IPv6** festgelegt ist (siehe [ipproto \_ IPv6-Socketoptionen](ipproto-ipv6-socket-options.md)), der *optname* -Parameter auf **IPv6 \_ V6ONLY** und der *optvalue* -Parameterwert auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="96411-156">This is accomplished by calling the **setsockopt** function on the socket with the *level* parameter set to **IPPROTO\_IPV6** (see [IPPROTO\_IPV6 Socket Options](ipproto-ipv6-socket-options.md)), the *optname* parameter set to **IPV6\_V6ONLY**, and the *optvalue* parameter value set to zero.</span></span>
-   <span data-ttu-id="96411-157">Alle IPv4-Adressen müssen im IPv4-zugeordneten IPv6-Adressformat dargestellt werden, das einer reinen IPv6-Anwendung die Kommunikation mit einem IPv4-Knoten ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="96411-157">Any IPv4 addresses must be represented in the IPv4-mapped IPv6 address format which enables an IPv6 only application to communicate with an IPv4 node.</span></span> <span data-ttu-id="96411-158">Das IPv4-zugeordnete IPv6-Adressformat ermöglicht die Darstellung der IPv4-Adresse eines IPv4-Knotens als IPv6-Adresse.</span><span class="sxs-lookup"><span data-stu-id="96411-158">The IPv4-mapped IPv6 address format allows the IPv4 address of an IPv4 node to be represented as an IPv6 address.</span></span> <span data-ttu-id="96411-159">Die IPv4-Adresse wird in die 32 Bits der IPv6-Adresse mit niedriger Reihenfolge codiert, und die höherwertigen 96 Bits enthalten das feste Präfix 0:0: 0:0: 0: FFFF.</span><span class="sxs-lookup"><span data-stu-id="96411-159">The IPv4 address is encoded into the low-order 32 bits of the IPv6 address, and the high-order 96 bits hold the fixed prefix 0:0:0:0:0:FFFF.</span></span> <span data-ttu-id="96411-160">Das IPv4-zugeordnete IPv6-Adressformat wird in RFC 4291 angegeben.</span><span class="sxs-lookup"><span data-stu-id="96411-160">The IPv4-mapped IPv6 address format is specified in RFC 4291.</span></span> <span data-ttu-id="96411-161">Weitere Informationen finden Sie unter [www.ietf.org/RFC/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span><span class="sxs-lookup"><span data-stu-id="96411-161">For more information, see [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291).</span></span> <span data-ttu-id="96411-162">Das IN6ADDR \_ SETV4MAPPED-Makro in *MSTCPIP. h* kann verwendet werden, um eine IPv4-Adresse in das erforderliche IPv4-zugeordnete IPv6-Adressformat zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="96411-162">The IN6ADDR\_SETV4MAPPED macro in *Mstcpip.h* can be used to convert an IPv4 address to the required IPv4-mapped IPv6 address format.</span></span>

<span data-ttu-id="96411-163">Herstellen einer Verbindung mithilfe von [ **wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span><span class="sxs-lookup"><span data-stu-id="96411-163">Establish a Connection Using [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(SOCKET_ADDRESS_LIST *AddressList) 
{
    SOCKET ConnSocket;
    DWORD ipv6only = 0;
    int iResult;
    BOOL bSuccess;
    SOCKADDR_STORAGE LocalAddr = {0};
    SOCKADDR_STORAGE RemoteAddr = {0};
    DWORD dwLocalAddr = sizeof(LocalAddr);
    DWORD dwRemoteAddr = sizeof(RemoteAddr);

    ConnSocket = socket(AF_INET6, SOCK_STREAM, 0);
    if (ConnSocket == INVALID_SOCKET){
        return INVALID_SOCKET;
    }

    iResult = setsockopt(ConnSocket, IPPROTO_IPV6,
        IPV6_V6ONLY, (char*)&ipv6only, sizeof(ipv6only) );
    if (iResult == SOCKET_ERROR){
        closesocket(ConnSocket);
        return INVALID_SOCKET;       
    }

    // AddressList may contain IPv6 and/or IPv4Mapped addresses
    bSuccess = WSAConnectByList(ConnSocket,
            AddressList,
            &dwLocalAddr,
            (SOCKADDR*)&LocalAddr,
            &dwRemoteAddr,
            (SOCKADDR*)&RemoteAddr,
            NULL,
            NULL);
    if (bSuccess){
        return ConnSocket;
    } else {
        return INVALID_SOCKET;
    }
}
```



## <a name="getaddrinfo"></a><span data-ttu-id="96411-164">getaddrinfo</span><span class="sxs-lookup"><span data-stu-id="96411-164">getaddrinfo</span></span>

<span data-ttu-id="96411-165">Die **getaddrinfo** -Funktion führt auch die Verarbeitungs Arbeit vieler Funktionen aus.</span><span class="sxs-lookup"><span data-stu-id="96411-165">The **getaddrinfo** function also performs the processing work of many functions.</span></span> <span data-ttu-id="96411-166">Zuvor waren Aufrufe an eine Reihe von Windows Sockets-Funktionen erforderlich, um eine Adresse zu erstellen, zu öffnen und anschließend an einen Socket zu binden.</span><span class="sxs-lookup"><span data-stu-id="96411-166">Previously, calls to a number of Windows Sockets functions were required to create, open, and then bind an address to a socket.</span></span> <span data-ttu-id="96411-167">Mit der **getaddrinfo** -Funktion können die Zeilen des Quellcodes, die für diese Arbeit erforderlich sind, erheblich reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="96411-167">With the **getaddrinfo** function, the lines of source code necessary to perform such work can be significantly reduced.</span></span> <span data-ttu-id="96411-168">Die folgenden beiden Beispiele veranschaulichen den Quellcode, der zum Ausführen dieser Aufgaben mit und ohne die **getaddrinfo** -Funktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="96411-168">The following two examples illustrate the source code necessary to perform these tasks with and without the **getaddrinfo** function.</span></span>

<span data-ttu-id="96411-169">Ausführen eines öffnenden, verbinden und Binden mithilfe von **getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="96411-169">Perform an Open, Connect, and Bind Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, char *PortName, int SocketType)
{
    SOCKET ConnSocket;
    ADDRINFO *AI;

    if (getaddrinfo(ServerName, PortName, NULL, &AI) != 0) {
        return INVALID_SOCKET;
    }

    ConnSocket = socket(AI->ai_family, SocketType, 0);
    if (ConnSocket == INVALID_SOCKET) {
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) == SOCKET_ERROR) {
        closesocket(ConnSocket);
        freeaddrinfo(AI);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="96411-170">Ausführen eines geöffneten, verbinden und binden ohne Verwendung von **getaddrinfo**</span><span class="sxs-lookup"><span data-stu-id="96411-170">Perform an Open, Connect, and Bind Without Using **getaddrinfo**</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *ServerName, unsigned short Port, int SocketType) 
{
    SOCKET ConnSocket;
    LPHOSTENT hp;
    SOCKADDR_IN ServerAddr;
    
    ConnSocket = socket(AF_INET, SocketType, 0); /* Open a socket */
    if (ConnSocket < 0 ) {
        return INVALID_SOCKET;
    }

    memset(&ServerAddr, 0, sizeof(ServerAddr));
    ServerAddr.sin_family = AF_INET;
    ServerAddr.sin_port = htons(Port);

    if (isalpha(ServerName[0])) {   /* server address is a name */
        hp = gethostbyname(ServerName);
        if (hp == NULL) {
            return INVALID_SOCKET;
        }
        ServerAddr.sin_addr.s_addr = (ULONG) hp->h_addr;
    } else { /* Convert nnn.nnn address to a usable one */
        ServerAddr.sin_addr.s_addr = inet_addr(ServerName);
    } 

    if (connect(ConnSocket, (LPSOCKADDR)&ServerAddr, 
        sizeof(ServerAddr)) == SOCKET_ERROR)
    {
        closesocket(ConnSocket);
        return INVALID_SOCKET;
    }

    return ConnSocket;
}
```



<span data-ttu-id="96411-171">Beachten Sie, dass beide Quell Codebeispiele dieselben Aufgaben ausführen, das erste Beispiel, bei dem die **getaddrinfo** -Funktion verwendet wird, jedoch weniger Zeilen von Quellcode erfordert und entweder IPv6-oder IPv4-Adressen verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="96411-171">Notice that both of these source code examples perform the same tasks, but the first example, using the **getaddrinfo** function, requires fewer lines of source code, and can handle either IPv6 or IPv4 addresses.</span></span> <span data-ttu-id="96411-172">Die Anzahl der Zeilen des Quellcodes, die mit der **getaddrinfo** -Funktion eliminiert werden, variiert.</span><span class="sxs-lookup"><span data-stu-id="96411-172">The number of lines of source code eliminated by using the **getaddrinfo** function varies.</span></span>

> [!Note]  
> <span data-ttu-id="96411-173">In der Produktionsquelle durchläuft Ihre Anwendung den Satz von Adressen, die von der [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) -Funktion oder der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="96411-173">In production source code, your application would iterate through the set of addresses returned by the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) or [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function.</span></span> <span data-ttu-id="96411-174">In diesen Beispielen wird dieser Schritt aus Gründen der Einfachheit ausgelassen.</span><span class="sxs-lookup"><span data-stu-id="96411-174">These examples omit that step in favor of simplicity.</span></span>

 

<span data-ttu-id="96411-175">Ein weiteres Problem, das beim Ändern einer vorhandenen IPv4-Anwendung zur Unterstützung von IPv6 behandelt werden muss, ist der Reihenfolge zugeordnet, in der Funktionen aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="96411-175">Another issue you must address when modifying an existing IPv4 application to support IPv6 is associated with the order in which functions are called.</span></span> <span data-ttu-id="96411-176">Sowohl " [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) " als auch " [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) " erfordern, dass eine Abfolge von Funktionsaufrufen in einer bestimmten Reihenfolge durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="96411-176">Both [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) require that a sequence of function calls are made in a specific order.</span></span>

<span data-ttu-id="96411-177">Auf Plattformen, auf denen sowohl IPv4 als auch IPv6 verwendet werden, ist die Adressfamilie des Remote Host Namens nicht vor der Zeit bekannt.</span><span class="sxs-lookup"><span data-stu-id="96411-177">On platforms where both IPv4 and IPv6 are used, the address family of the remote host name is not known ahead of time.</span></span> <span data-ttu-id="96411-178">Daher muss die Adress Auflösung mit der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zuerst ausgeführt werden, um die IP-Adresse und die Adressfamilie des Remote Hosts zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="96411-178">So address resolution using the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function must be executed first to determine the IP address and address family of the remote host.</span></span> <span data-ttu-id="96411-179">Anschließend kann die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktion aufgerufen werden, um einen Socket der von [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)zurückgegebenen Adressfamilie zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="96411-179">Then the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function can be called to open a socket of the address family returned by [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo).</span></span> <span data-ttu-id="96411-180">Dies ist eine wichtige Änderung in der Art und Weise, wie Windows Sockets-Anwendungen geschrieben werden, da viele IPv4-Anwendungen tendenziell eine andere Reihenfolge von Funktionsaufrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="96411-180">This is an important change in how Windows Sockets applications are written, since many IPv4 applications tend to use a different order of function calls.</span></span>

<span data-ttu-id="96411-181">Die meisten IPv4-Anwendungen erstellen zuerst einen Socket für die AF \_ -Adressfamilie "AF" und führen dann eine Namensauflösung durch und verwenden dann den Socket, um eine Verbindung mit der aufgelösten IP-Adresse herzustellen.</span><span class="sxs-lookup"><span data-stu-id="96411-181">Most IPv4 applications first create a socket for the AF\_INET address family, then do name resolution, and then use the socket to connect to the resolved IP address.</span></span> <span data-ttu-id="96411-182">Wenn solche Anwendungen IPv6-fähig sind, muss der [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktions Aufrufvorgang bis nach der Namensauflösung verzögert werden, wenn die Adressfamilie determiniert wurde.</span><span class="sxs-lookup"><span data-stu-id="96411-182">When making such applications IPv6-capable, the [**socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) function call must be delayed until after name resolution when the address family has been deteremined.</span></span> <span data-ttu-id="96411-183">Beachten Sie Folgendes: Wenn die Namensauflösung IPv4-und IPv6-Adressen zurückgibt, müssen separate IPv4-und IPv6-Sockets verwendet werden, um eine Verbindung mit diesen Zieladressen herzustellen.</span><span class="sxs-lookup"><span data-stu-id="96411-183">Note that if name resolution returns both IPv4 and IPv6 addresses, then separate IPv4 and IPv6 sockets must be used to connect to these destination addresses.</span></span> <span data-ttu-id="96411-184">Alle diese Komplexitäten können mithilfe der [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion unter Windows Vista und höher vermieden werden, sodass Anwendungsentwicklern empfohlen wird, diese neue Funktion zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="96411-184">All of these complexities can be avoided by using the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) function on Windows Vista and later, so application developers are encouraged to use this new function.</span></span>

<span data-ttu-id="96411-185">Im folgenden Codebeispiel wird die richtige Reihenfolge für die erstmalige Namensauflösung (in der vierten Zeile im folgenden Quell Codebeispiel) veranschaulicht. Anschließend wird ein Socket geöffnet (der in der 19<sup>.</sup> Zeile im folgenden Codebeispiel ausgeführt wird).</span><span class="sxs-lookup"><span data-stu-id="96411-185">The following code example shows the proper sequence for performing name resolution first (performed in the fourth line in the following source code example), then opening a socket (performed in the 19<sup>th</sup> line in the following code example).</span></span> <span data-ttu-id="96411-186">Dieses Beispiel ist ein Auszug aus der Datei "Client. c", die sich im [IPv6-fähigen Client Code](ipv6-enabled-client-code-2.md) in Anhang B befindet. Die Funktion "Printerror", die im folgenden Codebeispiel aufgerufen wird, wird im Beispiel "Client. c" aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="96411-186">This example is an excerpt from the Client.c file found in the [IPv6-Enabled Client Code](ipv6-enabled-client-code-2.md) in Appendix B. The PrintError function called in the following code example is listed in the Client.c sample.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

SOCKET OpenAndConnect(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;
    SOCKET ConnSocket = INVALID_SOCKET;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

    char *AddrName = NULL;

    memset(&Hints, 0, sizeof (Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;

    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return INVALID_SOCKET;
    }
    //
    // Try each address getaddrinfo returned, until we find one to which
    // we can successfully connect.
    //
    for (AI = AddrInfo; AI != NULL; AI = AI->ai_next) {

        // Open a socket with the correct address family for this address.
        ConnSocket = socket(AI->ai_family, AI->ai_socktype, AI->ai_protocol);
        if (ConnSocket == INVALID_SOCKET) {
            printf("Error Opening socket, error %d\n", WSAGetLastError());
            continue;
        }
        //
        // Notice that nothing in this code is specific to whether we 
        // are using UDP or TCP.
        //
        // When connect() is called on a datagram socket, it does not 
        // actually establish the connection as a stream (TCP) socket
        // would. Instead, TCP/IP establishes the remote half of the
        // (LocalIPAddress, LocalPort, RemoteIP, RemotePort) mapping.
        // This enables us to use send() and recv() on datagram sockets,
        // instead of recvfrom() and sendto().
        //

        printf("Attempting to connect to: %s\n", Server ? Server : "localhost");
        if (connect(ConnSocket, AI->ai_addr, (int) AI->ai_addrlen) != SOCKET_ERROR)
            break;

        if (getnameinfo(AI->ai_addr, (socklen_t) AI->ai_addrlen, AddrName,
                        sizeof (AddrName), NULL, 0, NI_NUMERICHOST) != 0) {
            strcpy_s(AddrName, sizeof (AddrName), "<unknown>");
            printf("connect() to %s failed with error %d\n", AddrName, WSAGetLastError());
            closesocket(ConnSocket);
            ConnSocket = INVALID_SOCKET;
        }    
    }
    return ConnSocket;
}

```



## <a name="ip-helper-functions"></a><span data-ttu-id="96411-187">Funktionen des IP-Hilfsprogramms</span><span class="sxs-lookup"><span data-stu-id="96411-187">IP Helper Functions</span></span>

<span data-ttu-id="96411-188">Und schließlich müssen Anwendungen, die die IP-Hilfsfunktion [**getadaptersinfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)verwenden, und die zugehörigen Struktur [**-IP- \_ Adapter \_ Informationen**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)erkennen, dass diese Funktion und Struktur auf IPv4-Adressen beschränkt sind.</span><span class="sxs-lookup"><span data-stu-id="96411-188">Finally, applications making use of the IP Helper function [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo), and its associated structure [**IP\_ADAPTER\_INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info), must recognize that both this function and structure are limited to IPv4 addresses.</span></span> <span data-ttu-id="96411-189">IPv6-fähige Ersetzungen für diese Funktion und Struktur sind die Funktion " [**getadaptersadressen**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) " und die [**IP- \_ Adapter \_ adressierte**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) Struktur.</span><span class="sxs-lookup"><span data-stu-id="96411-189">IPv6-enabled replacements for this function and structure are the [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) function and the [**IP\_ADAPTER\_ADDRESSES**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) structure.</span></span> <span data-ttu-id="96411-190">IPv6-fähige Anwendungen, die die IP-hilfsprogrammapi verwenden, sollten die Funktion **getadaptersadressen** und die zugehörige Struktur IPv6-fähiger **IP- \_ Adapter \_ Adressen** verwenden, die beide im Microsoft Windows Software Development Kit (SDK) definiert sind.</span><span class="sxs-lookup"><span data-stu-id="96411-190">IPv6-enabled applications making use of the IP Helper API should use the **GetAdaptersAddresses** function and the corresponding IPv6-enabled **IP\_ADAPTER\_ADDRESSES** structure, both defined in the Microsoft Windows Software Development Kit (SDK).</span></span>

## <a name="recommendations"></a><span data-ttu-id="96411-191">Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="96411-191">Recommendations</span></span>

<span data-ttu-id="96411-192">Der beste Ansatz, um sicherzustellen, dass Ihre Anwendung IPv6-kompatible Funktionsaufrufe verwendet, ist die Verwendung der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zum Abrufen von Host-zu-Adresse-Übersetzungen.</span><span class="sxs-lookup"><span data-stu-id="96411-192">The best approach to ensure your application is using IPv6-compatible function calls is to use the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function for obtaining host-to-address translation.</span></span> <span data-ttu-id="96411-193">Ab Windows XP macht die Funktion " **getaddrinfo** " die Funktion " [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) " unnötig, und die Anwendung sollte daher stattdessen die Funktion " **getaddrinfo** " für zukünftige Programmier Projekte verwenden.</span><span class="sxs-lookup"><span data-stu-id="96411-193">Beginning with Windows XP, the **getaddrinfo** function makes the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function unnecessary, and your application should therefore use the **getaddrinfo** function instead for future programming projects.</span></span> <span data-ttu-id="96411-194">Microsoft unterstützt zwar weiterhin " **gethostbyname**", diese Funktion wird jedoch nicht für die Unterstützung von IPv6 erweitert.</span><span class="sxs-lookup"><span data-stu-id="96411-194">While Microsoft will continue to support **gethostbyname**, this function will not be extended to support IPv6.</span></span> <span data-ttu-id="96411-195">Um eine transparente Unterstützung für das Abrufen von IPv6-und IPv4-Hostinformationen zu erhalten, müssen Sie **getaddrinfo** verwenden.</span><span class="sxs-lookup"><span data-stu-id="96411-195">For transparent support for obtaining IPv6 and IPv4 host information, you must use **getaddrinfo**.</span></span>

<span data-ttu-id="96411-196">Im folgenden Beispiel wird gezeigt, wie die **getaddrinfo** -Funktion am besten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="96411-196">The following example shows how to best use the **getaddrinfo** function.</span></span> <span data-ttu-id="96411-197">Beachten Sie, dass die-Funktion bei ordnungsgemäßer Verwendung wie in diesem Beispiel sowohl IPv6-als auch IPv4-Host-zu-Adresse-Übersetzung ordnungsgemäß verarbeitet, aber auch weitere nützliche Informationen über den Host erhält, z. b. den Typ der unterstützten Sockets.</span><span class="sxs-lookup"><span data-stu-id="96411-197">Notice that the function, when used properly as this example demonstrates, handles both IPv6 and IPv4 host-to-address translation properly, but it also obtains other useful information about the host, such as the type of sockets supported.</span></span> <span data-ttu-id="96411-198">Dieses Beispiel ist ein Auszug aus dem Beispiel "Client. c" in Anhang B.</span><span class="sxs-lookup"><span data-stu-id="96411-198">This sample is an excerpt from the Client.c sample found in Appendix B.</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#define WIN32_LEAN_AND_MEAN

#include <winsock2.h>
#include <Ws2tcpip.h>
#include <stdio.h>

// Link with ws2_32.lib
#pragma comment(lib, "Ws2_32.lib")

int ResolveName(char *Server, char *PortName, int Family, int SocketType)
{

    int iResult = 0;

    ADDRINFO *AddrInfo = NULL;
    ADDRINFO *AI = NULL;
    ADDRINFO Hints;

   //
    // By not setting the AI_PASSIVE flag in the hints to getaddrinfo, we're
    // indicating that we intend to use the resulting address(es) to connect
    // to a service.  This means that when the Server parameter is NULL,
    // getaddrinfo will return one entry per allowed protocol family
    // containing the loopback address for that family.
    //
    
    memset(&Hints, 0, sizeof(Hints));
    Hints.ai_family = Family;
    Hints.ai_socktype = SocketType;
    iResult = getaddrinfo(Server, PortName, &Hints, &AddrInfo);
    if (iResult != 0) {
        printf("Cannot resolve address [%s] and port [%s], error %d: %s\n",
               Server, PortName, WSAGetLastError(), gai_strerror(iResult));
        return SOCKET_ERROR;
    }
     return 0;
}
```



> [!Note]  
> <span data-ttu-id="96411-199">Die Version der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion, die IPv6 unterstützt, ist neu in der Windows XP-Version von Windows.</span><span class="sxs-lookup"><span data-stu-id="96411-199">The version of the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) function that supports IPv6 is new for the Windows XP release of Windows.</span></span>

 

<span data-ttu-id="96411-200">Zu Vermeider Code</span><span class="sxs-lookup"><span data-stu-id="96411-200">Code to Avoid</span></span>

<span data-ttu-id="96411-201">Die Host Adressübersetzung wurde bisher mithilfe der [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) -Funktion erreicht.</span><span class="sxs-lookup"><span data-stu-id="96411-201">Host address translation has traditionally been achieved using the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) function.</span></span> <span data-ttu-id="96411-202">Ab Windows XP:</span><span class="sxs-lookup"><span data-stu-id="96411-202">Beginning with Windows XP:</span></span>

-   <span data-ttu-id="96411-203">Die Funktion " **getaddrinfo** " macht die Funktion " **gethostbyname** " veraltet.</span><span class="sxs-lookup"><span data-stu-id="96411-203">The **getaddrinfo** function makes the **gethostbyname** function obsolete.</span></span>
-   <span data-ttu-id="96411-204">Ihre Anwendungen sollten die **getaddrinfo** -Funktion anstelle der **gethostbyname** -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="96411-204">Your applications should use the **getaddrinfo** function instead of the **gethostbyname** function.</span></span>

<span data-ttu-id="96411-205">Codierungs Aufgaben</span><span class="sxs-lookup"><span data-stu-id="96411-205">Coding Tasks</span></span>

<span data-ttu-id="96411-206">**So ändern Sie eine vorhandene IPv4-Anwendung, um Unterstützung für IPv6 hinzuzufügen**</span><span class="sxs-lookup"><span data-stu-id="96411-206">**To modify an existing IPv4 application to add support for IPv6**</span></span>

1.  <span data-ttu-id="96411-207">Erwerben Sie das Checkv4.exe-Hilfsprogramm.</span><span class="sxs-lookup"><span data-stu-id="96411-207">Acquire the Checkv4.exe utility.</span></span> <span data-ttu-id="96411-208">Dieses Hilfsprogramm wird als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="96411-208">This utility is installed as part of the Windows SDK.</span></span> <span data-ttu-id="96411-209">Der Windows SDK ist über ein MSDN-Abonnement verfügbar und kann auch von der Microsoft-Website heruntergeladen werden ( https://msdn.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="96411-209">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span> <span data-ttu-id="96411-210">Eine ältere Version des *Checkv4.exe* Tools ist auch als Teil der Microsoft IPv6-Technologievorschau für Windows 2000 enthalten.</span><span class="sxs-lookup"><span data-stu-id="96411-210">An older version of the *Checkv4.exe* tool was also as included as part of the Microsoft IPv6 Technology Preview for Windows 2000.</span></span>
2.  <span data-ttu-id="96411-211">Führen Sie das *Checkv4.exe* -Hilfsprogramm für den Code aus.</span><span class="sxs-lookup"><span data-stu-id="96411-211">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="96411-212">Weitere Informationen zum Ausführen des Versions Dienstprogramms für Ihre Dateien finden Sie unter [Verwenden des Checkv4.exe Hilfsprogramms](using-the-checkv4-exe-utility-2.md) .</span><span class="sxs-lookup"><span data-stu-id="96411-212">See [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md) to learn about running the version utility against your files.</span></span>
3.  <span data-ttu-id="96411-213">Das Hilfsprogramm warnt Sie bei der Verwendung von [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)und anderen reinen IPv4-Funktionen und bietet Empfehlungen darüber, wie Sie diese durch die IPv6-kompatible Funktion wie [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)ersetzen können.</span><span class="sxs-lookup"><span data-stu-id="96411-213">The utility alerts you to usage of the [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr), and other IPv4-only functions, and provides recommendations on how to replace them with the IPv6-compatible function such as [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo).</span></span>
4.  <span data-ttu-id="96411-214">Ersetzen Sie alle Instanzen der **gethostbyname** -Funktion und den zugehörigen Code nach Bedarf mit der **getaddrinfo** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="96411-214">Replace any instances of the **gethostbyname** function, and associated code as appropriate, with the **getaddrinfo** function.</span></span> <span data-ttu-id="96411-215">Verwenden Sie unter Windows Vista die [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -oder [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) -Funktion, wenn dies angebracht ist.</span><span class="sxs-lookup"><span data-stu-id="96411-215">On Windows Vista, use the [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) or [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) function when appropriate.</span></span>
5.  <span data-ttu-id="96411-216">Ersetzen Sie alle Instanzen der [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) -Funktion und den zugehörigen Code nach Bedarf mit der [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="96411-216">Replace any instances of the [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) function, and associated code as appropriate, with the [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) function.</span></span>

<span data-ttu-id="96411-217">Alternativ dazu können Sie Ihre Codebasis nach Instanzen der Funktionen " **gethostbyname** " und " [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) " Durchsuchen und die gesamte Verwendung (und ggf. einen anderen zugeordneten Code) in die Funktionen " **getaddrinfo** " und " [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) " ändern.</span><span class="sxs-lookup"><span data-stu-id="96411-217">Alternatively, you can search your code base for instances of the **gethostbyname** and [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) functions, and change all such usage (and other associated code, as appropriate) to the **getaddrinfo** and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96411-218">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="96411-218">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96411-219">IPv6-Handbuch für Windows Sockets-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="96411-219">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="96411-220">Ändern von Datenstrukturen für IPv6-Winsock-Appications</span><span class="sxs-lookup"><span data-stu-id="96411-220">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="96411-221">Dual-Stack-Sockets für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="96411-221">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="96411-222">Verwendung von hart codierten IPv4-Adressen</span><span class="sxs-lookup"><span data-stu-id="96411-222">Use of Hardcoded IPv4 Addresses</span></span>](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[<span data-ttu-id="96411-223">Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="96411-223">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="96411-224">Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen</span><span class="sxs-lookup"><span data-stu-id="96411-224">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 
