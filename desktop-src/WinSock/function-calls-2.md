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
# <a name="function-calls-for-ipv6-winsock-applications"></a>Funktionsaufrufe für IPv6-Winsock-Anwendungen

Neue Funktionen wurden mit der Windows Sockets-Schnittstelle eingeführt, die speziell für die Vereinfachung der Windows Sockets-Programmierung konzipiert wurde. Einer der Vorteile dieser neuen Windows Sockets-Funktionen ist die integrierte Unterstützung für IPv6 und IPv4.

Diese neuen Windows Sockets-Funktionen umfassen Folgendes:

-   [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**Wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktions Familie (**getaddrinfo**, [**getaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**getaddrinfow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**freaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**freaddrinfow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)und [**abstaddrinfoex**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))
-   [**getnameingefo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) -Funktions Familie (**getnameingefo** und [**getnameingefow**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))

Außerdem wurden neue IP-Hilfsfunktionen mit Unterstützung für IPv6 und IPv4 hinzugefügt, um die Windows-Socketprogrammierung zu vereinfachen. Diese neuen IP-Hilfsfunktionen umfassen Folgendes:

-   [**Getadaptersadressen**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

Beim Hinzufügen von IPv6-Unterstützung zu einer Anwendung sollten die folgenden Richtlinien verwendet werden:

-   Verwenden Sie [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) , um eine Verbindung mit einem Endpunkt bei Angabe eines Host Namens und-Ports herzustellen. Die **WSAConnectByName** -Funktion ist unter Windows Vista und höher verfügbar.
-   Verwenden Sie [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) , um eine Verbindung mit einer aus einer Sammlung möglicher Endpunkte herzustellen, die durch eine Gruppe von Zieladressen (Hostnamen und Ports) dargestellt werden. Die **wsaconnectbylist** -Funktion ist unter Windows Vista und höher verfügbar.
-   Ersetzen Sie die [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) -Funktionsaufrufe durch Aufrufe einer der neuen Windows Sockets-Funktionen [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . Die **getaddrinfo** -Funktion mit Unterstützung für das IPv6-Protokoll ist unter Windows XP und höher verfügbar. Das IPv6-Protokoll wird auch unter Windows 2000 unterstützt, wenn die IPv6-Technologievorschau für Windows 2000 installiert ist.
-   Ersetzen Sie die [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) -Funktionsaufrufe durch Aufrufe einer der neuen Windows Sockets-Funktionen von [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) . Die **getnaminfo** -Funktion mit Unterstützung für das IPv6-Protokoll ist unter Windows XP und höher verfügbar. Das IPv6-Protokoll wird auch unter Windows 2000 unterstützt, wenn die IPv6-Technologievorschau für Windows 2000 installiert ist.

## <a name="wsaconnectbyname"></a>WSAConnectByName

Die [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion vereinfacht das Herstellen einer Verbindung mit einem Endpunkt mithilfe eines streambasierten Sockets unter Berücksichtigung des Host Namens oder der IP-Adresse des Ziels (IPv4 oder IPv6). Diese Funktion reduziert den Quellcode, der erforderlich ist, um eine IP-Anwendung zu erstellen, die unabhängig von der verwendeten Version des IP-Protokolls ist. **WSAConnectByName** ersetzt die folgenden Schritte in einer typischen TCP-Anwendung zu einem einzelnen Funktions aufzurufen:

-   Lösen Sie einen Hostnamen in einen Satz von IP-Adressen auf.
-   Für jede IP-Adresse:
    -   Erstellen Sie einen Socket der entsprechenden Adressfamilie.
    -   Versucht, eine Verbindung mit der Remote-IP-Adresse herzustellen. Wenn die Verbindung erfolgreich hergestellt wurde, wird zurückgegeben. Andernfalls wird die nächste Remote-IP-Adresse für den Host ausprobiert.

Die [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion geht über das Auflösen des Namens hinaus und versucht dann, eine Verbindung herzustellen. Die Funktion verwendet alle Remote Adressen, die von der Namensauflösung und allen Quell-IP-Adressen des lokalen Computers zurückgegeben werden. Zuerst wird versucht, die Verbindung mithilfe von Adress Paaren mit der höchsten Erfolgschance herzustellen. Daher stellt **WSAConnectByName** nicht nur sicher, dass nach Möglichkeit eine Verbindung hergestellt wird, sondern auch die Zeit zum Herstellen der Verbindung minimiert wird.

Verwenden Sie die folgende Methode, um sowohl IPv6-als auch IPv4-Kommunikation zu aktivieren:

-   Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion muss für einen Socket aufgerufen werden, der für die inet6-Adressfamilie des AF erstellt wurde \_ , um die **IPv6 \_ V6ONLY** Socket-Option vor dem Aufrufen von [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)zu deaktivieren. Dies wird erreicht, indem die **setsockopt** -Funktion für den Socket aufgerufen wird, wobei der *Level* -Parameter auf **ipproto \_ IPv6** festgelegt ist (siehe [ipproto \_ IPv6-Socketoptionen](ipproto-ipv6-socket-options.md)), der *optname* -Parameter auf **IPv6 \_ V6ONLY** und der *optvalue* -Parameterwert auf NULL festgelegt ist.

Wenn eine Anwendung eine Bindung an eine bestimmte lokale Adresse oder einen bestimmten Port herstellen muss, kann [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) nicht verwendet werden, da der socketparameter für **WSAConnectByName** ein ungebundener Socket sein muss.

Das folgende Codebeispiel zeigt nur einige Codezeilen, die erforderlich sind, um diese Funktion zu verwenden, um eine Anwendung zu implementieren, die für die IP-Version agnostisch ist.

Herstellen einer Verbindung mithilfe von [ **WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)


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



## <a name="wsaconnectbylist"></a>Wsaconnectbylist

Die [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) -Funktion stellt eine Verbindung mit einem Host fest, wenn ein Satz möglicher Hosts vorhanden ist (dargestellt durch einen Satz von Ziel-IP-Adressen und Ports). Die Funktion nimmt alle IP-Adressen und Ports für den Endpunkt und alle IP-Adressen des lokalen Computers an und versucht, eine Verbindung mit allen möglichen Adress Kombinationen herzustellen.

[**Wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) ist mit der [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion verknüpft. Anstatt einen einzelnen Hostnamen zu verwenden, akzeptiert **wsaconnectbylist** eine Liste von Hosts (Zieladressen und Port Paare) und stellt eine Verbindung mit einer der Adressen und Ports in der angegebenen Liste her. Diese Funktion ist für die Unterstützung von Szenarien konzipiert, in denen eine Anwendung eine Verbindung mit einem beliebigen verfügbaren Host aus einer Liste potenzieller Hosts herstellen muss.

Ähnlich wie [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)reduziert die [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) -Funktion den Quellcode, der zum Erstellen, binden und Verbinden eines Sockets erforderlich ist, erheblich. Diese Funktion vereinfacht die Implementierung einer Anwendung, die mit der IP-Version agnostisch ist. Die Liste der Adressen eines Hosts, der von dieser Funktion akzeptiert wird, ist möglicherweise IPv6-oder IPv4-Adressen.

Die folgenden Schritte müssen ausgeführt werden, bevor die-Funktion aufgerufen wird, damit IPv6-und IPv4-Adressen in der von der Funktion akzeptierten einzelnen Adressliste übermittelt werden können:

-   Die [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -Funktion muss für einen Socket aufgerufen werden, der für die inet6-Adressfamilie des AF erstellt wurde \_ , um die **IPv6 \_ V6ONLY** Socket-Option vor dem Aufrufen von [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)zu deaktivieren. Dies wird erreicht, indem die **setsockopt** -Funktion für den Socket aufgerufen wird, wobei der *Level* -Parameter auf **ipproto \_ IPv6** festgelegt ist (siehe [ipproto \_ IPv6-Socketoptionen](ipproto-ipv6-socket-options.md)), der *optname* -Parameter auf **IPv6 \_ V6ONLY** und der *optvalue* -Parameterwert auf NULL festgelegt ist.
-   Alle IPv4-Adressen müssen im IPv4-zugeordneten IPv6-Adressformat dargestellt werden, das einer reinen IPv6-Anwendung die Kommunikation mit einem IPv4-Knoten ermöglicht. Das IPv4-zugeordnete IPv6-Adressformat ermöglicht die Darstellung der IPv4-Adresse eines IPv4-Knotens als IPv6-Adresse. Die IPv4-Adresse wird in die 32 Bits der IPv6-Adresse mit niedriger Reihenfolge codiert, und die höherwertigen 96 Bits enthalten das feste Präfix 0:0: 0:0: 0: FFFF. Das IPv4-zugeordnete IPv6-Adressformat wird in RFC 4291 angegeben. Weitere Informationen finden Sie unter [www.ietf.org/RFC/rfc4291.txt](https://tools.ietf.org/html/rfc4291). Das IN6ADDR \_ SETV4MAPPED-Makro in *MSTCPIP. h* kann verwendet werden, um eine IPv4-Adresse in das erforderliche IPv4-zugeordnete IPv6-Adressformat zu konvertieren.

Herstellen einer Verbindung mithilfe von [ **wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)


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



## <a name="getaddrinfo"></a>getaddrinfo

Die **getaddrinfo** -Funktion führt auch die Verarbeitungs Arbeit vieler Funktionen aus. Zuvor waren Aufrufe an eine Reihe von Windows Sockets-Funktionen erforderlich, um eine Adresse zu erstellen, zu öffnen und anschließend an einen Socket zu binden. Mit der **getaddrinfo** -Funktion können die Zeilen des Quellcodes, die für diese Arbeit erforderlich sind, erheblich reduziert werden. Die folgenden beiden Beispiele veranschaulichen den Quellcode, der zum Ausführen dieser Aufgaben mit und ohne die **getaddrinfo** -Funktion erforderlich ist.

Ausführen eines öffnenden, verbinden und Binden mithilfe von **getaddrinfo**


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



Ausführen eines geöffneten, verbinden und binden ohne Verwendung von **getaddrinfo**


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



Beachten Sie, dass beide Quell Codebeispiele dieselben Aufgaben ausführen, das erste Beispiel, bei dem die **getaddrinfo** -Funktion verwendet wird, jedoch weniger Zeilen von Quellcode erfordert und entweder IPv6-oder IPv4-Adressen verarbeiten kann. Die Anzahl der Zeilen des Quellcodes, die mit der **getaddrinfo** -Funktion eliminiert werden, variiert.

> [!Note]  
> In der Produktionsquelle durchläuft Ihre Anwendung den Satz von Adressen, die von der [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) -Funktion oder der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zurückgegeben werden. In diesen Beispielen wird dieser Schritt aus Gründen der Einfachheit ausgelassen.

 

Ein weiteres Problem, das beim Ändern einer vorhandenen IPv4-Anwendung zur Unterstützung von IPv6 behandelt werden muss, ist der Reihenfolge zugeordnet, in der Funktionen aufgerufen werden. Sowohl " [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) " als auch " [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) " erfordern, dass eine Abfolge von Funktionsaufrufen in einer bestimmten Reihenfolge durchgeführt wird.

Auf Plattformen, auf denen sowohl IPv4 als auch IPv6 verwendet werden, ist die Adressfamilie des Remote Host Namens nicht vor der Zeit bekannt. Daher muss die Adress Auflösung mit der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zuerst ausgeführt werden, um die IP-Adresse und die Adressfamilie des Remote Hosts zu ermitteln. Anschließend kann die [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktion aufgerufen werden, um einen Socket der von [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)zurückgegebenen Adressfamilie zu öffnen. Dies ist eine wichtige Änderung in der Art und Weise, wie Windows Sockets-Anwendungen geschrieben werden, da viele IPv4-Anwendungen tendenziell eine andere Reihenfolge von Funktionsaufrufen verwenden.

Die meisten IPv4-Anwendungen erstellen zuerst einen Socket für die AF \_ -Adressfamilie "AF" und führen dann eine Namensauflösung durch und verwenden dann den Socket, um eine Verbindung mit der aufgelösten IP-Adresse herzustellen. Wenn solche Anwendungen IPv6-fähig sind, muss der [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -Funktions Aufrufvorgang bis nach der Namensauflösung verzögert werden, wenn die Adressfamilie determiniert wurde. Beachten Sie Folgendes: Wenn die Namensauflösung IPv4-und IPv6-Adressen zurückgibt, müssen separate IPv4-und IPv6-Sockets verwendet werden, um eine Verbindung mit diesen Zieladressen herzustellen. Alle diese Komplexitäten können mithilfe der [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion unter Windows Vista und höher vermieden werden, sodass Anwendungsentwicklern empfohlen wird, diese neue Funktion zu verwenden.

Im folgenden Codebeispiel wird die richtige Reihenfolge für die erstmalige Namensauflösung (in der vierten Zeile im folgenden Quell Codebeispiel) veranschaulicht. Anschließend wird ein Socket geöffnet (der in der 19<sup>.</sup> Zeile im folgenden Codebeispiel ausgeführt wird). Dieses Beispiel ist ein Auszug aus der Datei "Client. c", die sich im [IPv6-fähigen Client Code](ipv6-enabled-client-code-2.md) in Anhang B befindet. Die Funktion "Printerror", die im folgenden Codebeispiel aufgerufen wird, wird im Beispiel "Client. c" aufgeführt.


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



## <a name="ip-helper-functions"></a>Funktionen des IP-Hilfsprogramms

Und schließlich müssen Anwendungen, die die IP-Hilfsfunktion [**getadaptersinfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)verwenden, und die zugehörigen Struktur [**-IP- \_ Adapter \_ Informationen**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)erkennen, dass diese Funktion und Struktur auf IPv4-Adressen beschränkt sind. IPv6-fähige Ersetzungen für diese Funktion und Struktur sind die Funktion " [**getadaptersadressen**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) " und die [**IP- \_ Adapter \_ adressierte**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) Struktur. IPv6-fähige Anwendungen, die die IP-hilfsprogrammapi verwenden, sollten die Funktion **getadaptersadressen** und die zugehörige Struktur IPv6-fähiger **IP- \_ Adapter \_ Adressen** verwenden, die beide im Microsoft Windows Software Development Kit (SDK) definiert sind.

## <a name="recommendations"></a>Empfehlungen

Der beste Ansatz, um sicherzustellen, dass Ihre Anwendung IPv6-kompatible Funktionsaufrufe verwendet, ist die Verwendung der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zum Abrufen von Host-zu-Adresse-Übersetzungen. Ab Windows XP macht die Funktion " **getaddrinfo** " die Funktion " [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) " unnötig, und die Anwendung sollte daher stattdessen die Funktion " **getaddrinfo** " für zukünftige Programmier Projekte verwenden. Microsoft unterstützt zwar weiterhin " **gethostbyname**", diese Funktion wird jedoch nicht für die Unterstützung von IPv6 erweitert. Um eine transparente Unterstützung für das Abrufen von IPv6-und IPv4-Hostinformationen zu erhalten, müssen Sie **getaddrinfo** verwenden.

Im folgenden Beispiel wird gezeigt, wie die **getaddrinfo** -Funktion am besten verwendet werden kann. Beachten Sie, dass die-Funktion bei ordnungsgemäßer Verwendung wie in diesem Beispiel sowohl IPv6-als auch IPv4-Host-zu-Adresse-Übersetzung ordnungsgemäß verarbeitet, aber auch weitere nützliche Informationen über den Host erhält, z. b. den Typ der unterstützten Sockets. Dieses Beispiel ist ein Auszug aus dem Beispiel "Client. c" in Anhang B.


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
> Die Version der [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion, die IPv6 unterstützt, ist neu in der Windows XP-Version von Windows.

 

Zu Vermeider Code

Die Host Adressübersetzung wurde bisher mithilfe der [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) -Funktion erreicht. Ab Windows XP:

-   Die Funktion " **getaddrinfo** " macht die Funktion " **gethostbyname** " veraltet.
-   Ihre Anwendungen sollten die **getaddrinfo** -Funktion anstelle der **gethostbyname** -Funktion verwenden.

Codierungs Aufgaben

**So ändern Sie eine vorhandene IPv4-Anwendung, um Unterstützung für IPv6 hinzuzufügen**

1.  Erwerben Sie das Checkv4.exe-Hilfsprogramm. Dieses Hilfsprogramm wird als Teil des Windows SDK installiert. Der Windows SDK ist über ein MSDN-Abonnement verfügbar und kann auch von der Microsoft-Website heruntergeladen werden ( https://msdn.microsoft.com) . Eine ältere Version des *Checkv4.exe* Tools ist auch als Teil der Microsoft IPv6-Technologievorschau für Windows 2000 enthalten.
2.  Führen Sie das *Checkv4.exe* -Hilfsprogramm für den Code aus. Weitere Informationen zum Ausführen des Versions Dienstprogramms für Ihre Dateien finden Sie unter [Verwenden des Checkv4.exe Hilfsprogramms](using-the-checkv4-exe-utility-2.md) .
3.  Das Hilfsprogramm warnt Sie bei der Verwendung von [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname), [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)und anderen reinen IPv4-Funktionen und bietet Empfehlungen darüber, wie Sie diese durch die IPv6-kompatible Funktion wie [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)ersetzen können.
4.  Ersetzen Sie alle Instanzen der **gethostbyname** -Funktion und den zugehörigen Code nach Bedarf mit der **getaddrinfo** -Funktion. Verwenden Sie unter Windows Vista die [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -oder [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) -Funktion, wenn dies angebracht ist.
5.  Ersetzen Sie alle Instanzen der [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) -Funktion und den zugehörigen Code nach Bedarf mit der [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) -Funktion.

Alternativ dazu können Sie Ihre Codebasis nach Instanzen der Funktionen " **gethostbyname** " und " [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) " Durchsuchen und die gesamte Verwendung (und ggf. einen anderen zugeordneten Code) in die Funktionen " **getaddrinfo** " und " [**GetNameInfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) " ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Handbuch für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Ändern von Datenstrukturen für IPv6-Winsock-Appications](changing-data-structures-2.md)
</dt> <dt>

[Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)
</dt> <dt>

[Verwendung von hart codierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Probleme mit der Benutzeroberfläche für IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6-Winsock-Anwendungen](underlying-protocols-2.md)
</dt> </dl>

 

 
