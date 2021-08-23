---
description: Neue Funktionen wurden in die Windows Sockets-Schnittstelle eingeführt, die speziell entwickelt wurde, um Windows Sockets-Programmierung zu vereinfachen. Einer der Vorteile dieser neuen Windows Sockets-Funktionen ist die integrierte Unterstützung für IPv6 und IPv4.
ms.assetid: 83262f2b-a335-4bbd-b2e3-6c7744b3ee50
title: Funktionsaufrufe für IPv6-Winsock-Anwendungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 241db1f7e07264fe4f0c776834d17c48cff4780b06e6a42816d36a50fa22cef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051668"
---
# <a name="function-calls-for-ipv6-winsock-applications"></a>Funktionsaufrufe für IPv6-Winsock-Anwendungen

Neue Funktionen wurden in die Windows Sockets-Schnittstelle eingeführt, die speziell entwickelt wurde, um Windows Sockets-Programmierung zu vereinfachen. Einer der Vorteile dieser neuen Windows Sockets-Funktionen ist die integrierte Unterstützung für IPv6 und IPv4.

Diese neuen Windows Sockets-Funktionen umfassen Folgendes:

-   [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)
-   [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)
-   [**getaddrinfo-Funktionsfamilie**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) (**getaddrinfo**, [**GetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa), [**GetAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow), [**freeaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo), [**FreeAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex), [**FreeAddrInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow)und [**SetAddrInfoEx**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa))
-   [**getnameinfo-Funktionsfamilie**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) (**getnameinfo** und [**GetNameInfoW**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfow))

Darüber hinaus wurden neue IP-Hilfsfunktionen mit Unterstützung für IPv6 und IPv4 hinzugefügt, um die Programmierung von Windows Sockets zu vereinfachen. Diese neuen IP-Hilfsfunktionen umfassen Folgendes:

-   [**GetAdaptersAddresses**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses)

Beim Hinzufügen von IPv6-Unterstützung zu einer Anwendung sollten die folgenden Richtlinien verwendet werden:

-   Verwenden Sie [**WSAConnectByName,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) um eine Verbindung mit einem Endpunkt unter Angabe eines Hostnamens und Ports herzustellen. Die **WSAConnectByName-Funktion** ist auf Windows Vista und höher verfügbar.
-   Verwenden Sie [**WSAConnectByList,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) um eine Verbindung mit einem aus einer Sammlung möglicher Endpunkte herzustellen, die durch einen Satz von Zieladressen (Hostnamen und Ports) dargestellt werden. Die **WSAConnectByList-Funktion** ist auf Windows Vista und höher verfügbar.
-   Ersetzen Sie [**gethostbyname-Funktionsaufrufe**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) durch Aufrufe einer der neuen [**getaddrinfo-Windows**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) Sockets-Funktionen. Die **getaddrinfo-Funktion** mit Unterstützung für das IPv6-Protokoll ist auf Windows XP und höher verfügbar. Das IPv6-Protokoll wird auch auf Windows 2000 unterstützt, wenn die IPv6-Technologievorschau für Windows 2000 installiert ist.
-   Ersetzen Sie [**gethostbyaddr-Funktionsaufrufe**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) durch Aufrufe einer der neuen [**getnameinfo-Windows**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) Sockets-Funktionen. Die **getnameinfo-Funktion** mit Unterstützung für das IPv6-Protokoll ist auf Windows XP und höher verfügbar. Das IPv6-Protokoll wird auch auf Windows 2000 unterstützt, wenn die IPv6-Technologievorschau für Windows 2000 installiert ist.

## <a name="wsaconnectbyname"></a>WSAConnectByName

Die [**WSAConnectByName-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) vereinfacht das Herstellen einer Verbindung mit einem Endpunkt mithilfe eines streambasierten Sockets, wenn der Hostname oder die IP-Adresse des Ziels (IPv4 oder IPv6) angegeben ist. Diese Funktion reduziert den Quellcode, der zum Erstellen einer IP-Anwendung erforderlich ist, die unabhängig von der Version des verwendeten IP-Protokolls ist. **WSAConnectByName** ersetzt die folgenden Schritte in einer typischen TCP-Anwendung durch einen einzelnen Funktionsaufruf:

-   Lösen Sie einen Hostnamen in einen Satz von IP-Adressen auf.
-   Für jede IP-Adresse:
    -   Erstellen Sie einen Socket der entsprechenden Adressfamilie.
    -   Versucht, eine Verbindung mit der Remote-IP-Adresse herzustellen. Wenn die Verbindung erfolgreich war, wird zurückgegeben. andernfalls wird die nächste Remote-IP-Adresse für den Host versucht.

Die [**WSAConnectByName-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) geht über das auflösen des Namens hinaus und versucht dann, eine Verbindung herzustellen. Die Funktion verwendet alle Remoteadressen, die von der Namensauflösung zurückgegeben werden, und alle Quell-IP-Adressen des lokalen Computers. Zunächst wird versucht, mithilfe von Adresspaaren mit der höchsten Erfolgswahrscheinlichkeit eine Verbindung herzustellen. Daher stellt **WSAConnectByName** nicht nur sicher, dass nach Möglichkeit eine Verbindung hergestellt wird, sondern minimiert auch die Zeit zum Herstellen der Verbindung.

Verwenden Sie die folgende Methode, um die IPv6- und IPv4-Kommunikation zu aktivieren:

-   Die [**setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) muss für einen Socket aufgerufen werden, der für die AF \_ INET6-Adressfamilie erstellt wurde, um die **IPV6 \_ V6ONLY-Socketoption** zu deaktivieren, bevor [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)aufgerufen wird. Dies wird erreicht, indem die **setsockopt-Funktion** für den Socket aufgerufen wird, wobei der *Levelparameter* auf **IPPROTO \_ IPV6** festgelegt ist (siehe [IPPROTO \_ IPV6 Socket Options),](ipproto-ipv6-socket-options.md)der *optname-Parameter,* der auf **IPV6 \_ V6ONLY** festgelegt ist, und der *optvalue-Parameterwert* auf 0 (null) festgelegt wird.

Wenn eine Anwendung eine Bindung an eine bestimmte lokale Adresse oder einen bestimmten Port herstellen muss, kann [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) nicht verwendet werden, da der Socketparameter an **WSAConnectByName** ein ungebundener Socket sein muss.

Das folgende Codebeispiel zeigt, dass nur wenige Codezeilen erforderlich sind, um diese Funktion zum Implementieren einer Anwendung zu verwenden, die unabhängig von der IP-Version ist.

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



## <a name="wsaconnectbylist"></a>WSAConnectByList

Die [**WSAConnectByList-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) stellt eine Verbindung mit einem Host her, wenn eine Reihe möglicher Hosts (dargestellt durch einen Satz von Ziel-IP-Adressen und -Ports) angegeben wird. Die Funktion verwendet alle IP-Adressen und Ports für den Endpunkt und alle IP-Adressen des lokalen Computers und versucht, eine Verbindung mit allen möglichen Adresskombinationen herzustellen.

[**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) bezieht sich auf die [**WSAConnectByName-Funktion.**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) Anstatt einen einzelnen Hostnamen zu verwenden, akzeptiert **WSAConnectByList** eine Liste von Hosts (Zieladressen und Portpaare) und stellt eine Verbindung mit einer der Adressen und Ports in der bereitgestellten Liste her. Diese Funktion wurde entwickelt, um Szenarien zu unterstützen, in denen eine Anwendung eine Verbindung mit einem beliebigen verfügbaren Host aus einer Liste potenzieller Hosts herstellen muss.

Ähnlich wie [**bei WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea)reduziert die [**WSAConnectByList-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) den Quellcode, der zum Erstellen, Binden und Verbinden eines Sockets erforderlich ist, erheblich. Diese Funktion erleichtert die Implementierung einer Anwendung, die unabhängig von der IP-Version ist. Die Liste der Adressen für einen Host, der von dieser Funktion akzeptiert wird, kann IPv6- oder IPv4-Adressen sein.

Damit sowohl IPv6- als auch IPv4-Adressen in der einzelnen Adressliste übergeben werden können, die von der Funktion akzeptiert wird, müssen vor dem Aufrufen der Funktion die folgenden Schritte ausgeführt werden:

-   Die [**Setsockopt-Funktion**](/windows/desktop/api/winsock/nf-winsock-setsockopt) muss für einen Socket aufgerufen werden, der für die AF \_ INET6-Adressfamilie erstellt wurde, um die **IPV6 \_ V6ONLY-Socketoption** zu deaktivieren, bevor [**WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)aufgerufen wird. Dies wird erreicht, indem die **setsockopt-Funktion** für den Socket aufgerufen wird, wobei der *Levelparameter* auf **IPPROTO \_ IPV6** festgelegt ist (siehe [IPPROTO \_ IPV6 Socket Options),](ipproto-ipv6-socket-options.md)der *optname-Parameter,* der auf **IPV6 \_ V6ONLY** festgelegt ist, und der *optvalue-Parameterwert* auf 0 (null) festgelegt wird.
-   Alle IPv4-Adressen müssen im IPv4-zugeordneten IPv6-Adressformat dargestellt werden, wodurch eine IPv6-Anwendung nur mit einem IPv4-Knoten kommunizieren kann. Das IPv4-zugeordnete IPv6-Adressformat ermöglicht die Darstellung der IPv4-Adresse eines IPv4-Knotens als IPv6-Adresse. Die IPv4-Adresse wird in die 32 Bits der IPv6-Adresse mit niedriger Ordnung codiert, und die 96 Bits mit hoher Ordnung enthalten das feste Präfix 0:0:0:0:0:FFFF. Das IPv4-zugeordnete IPv6-Adressformat wird in RFC 4291 angegeben. Weitere Informationen finden Sie unter [www.ietf.org/rfc/rfc4291.txt](https://tools.ietf.org/html/rfc4291). Das IN6ADDR \_ SETV4MAPPED-Makro in *Mstcpip.h* kann verwendet werden, um eine IPv4-Adresse in das erforderliche IPv4-zugeordnete IPv6-Adressformat zu konvertieren.

Herstellen einer Verbindung mit [ **WSAConnectByList**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)


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

Die **getaddrinfo-Funktion** führt auch die Verarbeitung vieler Funktionen aus. Zuvor waren Aufrufe einer Reihe von Windows Sockets-Funktionen erforderlich, um eine Adresse zu erstellen, zu öffnen und dann an einen Socket zu binden. Mit der **getaddrinfo-Funktion** können die Quellcodezeilen, die für solche Aufgaben erforderlich sind, erheblich reduziert werden. Die folgenden beiden Beispiele veranschaulichen den Quellcode, der zum Ausführen dieser Aufgaben mit und ohne die **getaddrinfo-Funktion** erforderlich ist.

Ausführen einer Open-, Verbinden- und Bind-Datei mit **getaddrinfo**


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



Ausführen eines Öffnens, Verbinden und Bindens ohne Verwendung von **getaddrinfo**


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



Beachten Sie, dass beide Quellcodebeispiele die gleichen Aufgaben ausführen, aber das erste Beispiel mit der **getaddrinfo-Funktion** erfordert weniger Quellcodezeilen und kann entweder IPv6- oder IPv4-Adressen verarbeiten. Die Anzahl der Quellcodezeilen, die mithilfe der **getaddrinfo-Funktion** entfernt werden, variiert.

> [!Note]  
> Im Quellcode der Produktion durch würde Ihre Anwendung den Satz von Adressen durchlaufen, die von der [**gethostbyname-**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) oder [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) zurückgegeben werden. In diesen Beispielen wird dieser Schritt zugunsten der Einfachheit weggelassen.

 

Ein weiteres Problem, das Sie beim Ändern einer vorhandenen IPv4-Anwendung zur Unterstützung von IPv6 beheben müssen, ist der Reihenfolge zugeordnet, in der Funktionen aufgerufen werden. Sowohl [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) als [**auch gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) erfordern, dass eine Sequenz von Funktionsaufrufen in einer bestimmten Reihenfolge erfolgt.

Auf Plattformen, auf denen sowohl IPv4 als auch IPv6 verwendet werden, ist die Adressfamilie des Remotehostnamens im Voraus nicht bekannt. Daher muss die Adressauflösung mithilfe der [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) zuerst ausgeführt werden, um die IP-Adresse und die Adressfamilie des Remotehosts zu bestimmen. Anschließend kann die [**Socketfunktion**](/windows/desktop/api/Winsock2/nf-winsock2-socket) aufgerufen werden, um einen Socket der Adressfamilie zu öffnen, die von [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo)zurückgegeben wird. Dies ist eine wichtige Änderung beim Schreiben Windows Sockets-Anwendungen, da viele IPv4-Anwendungen in der Regel eine andere Reihenfolge von Funktionsaufrufen verwenden.

Die meisten IPv4-Anwendungen erstellen zunächst einen Socket für die AF \_ INET-Adressfamilie, erstellen dann die Namensauflösung und verwenden dann den Socket, um eine Verbindung mit der aufgelösten IP-Adresse herzustellen. Wenn solche Anwendungen IPv6-fähig [](/windows/desktop/api/Winsock2/nf-winsock2-socket) sind, muss der Socketfunktionsaufruf bis nach der Namensauflösung verzögert werden, wenn die Adressfamilie abgeschreckt wurde. Beachten Sie Folgendes: Wenn die Namensauflösung sowohl IPv4- als auch IPv6-Adressen zurückgibt, müssen separate IPv4- und IPv6-Sockets verwendet werden, um eine Verbindung mit diesen Zieladressen herzustellen. All diese Komplexitäten lassen sich vermeiden, indem Sie die [**WSAConnectByName-Funktion**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) auf Windows Vista und höher verwenden, sodass Anwendungsentwicklern empfohlen wird, diese neue Funktion zu verwenden.

Das folgende Codebeispiel zeigt die richtige Sequenz für die Durchführung der Namensauflösung (in der vierten Zeile im folgenden<sup></sup> Quellcodebeispiel), dann das Öffnen eines Sockets (ausgeführt in der 19. Zeile im folgenden Codebeispiel). Dieses Beispiel ist ein Auszug aus der Datei Client.c im [IPv6-fähigen Clientcode](ipv6-enabled-client-code-2.md) in Anhang B. Die PrintError-Funktion, die im folgenden Codebeispiel aufgerufen wird, ist im Client.c-Beispiel aufgeführt.


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

Schließlich müssen Anwendungen, die die IP-Hilfsfunktion [**GetAdaptersInfo**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersinfo)und die zugehörige Struktur [**IP ADAPTER \_ \_ INFO**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_info)verwenden, erkennen, dass diese Funktion und Struktur auf IPv4-Adressen beschränkt sind. IPv6-fähige Ersetzungen für diese Funktion und Struktur sind die [**GetAdaptersAddresses-Funktion**](/windows/win32/api/iphlpapi/nf-iphlpapi-getadaptersaddresses) und die [**\_ IP-Adapteradressenstruktur. \_**](/windows/win32/api/iptypes/ns-iptypes-ip_adapter_addresses_lh) IPv6-fähige Anwendungen, die die IP-Hilfs-API verwenden, sollten die **GetAdaptersAddresses-Funktion** und die entsprechende IPv6-fähige **\_ IP-ADAPTERADRESSEnstruktur \_** verwenden, die beide im Microsoft Windows Software Development Kit (SDK) definiert sind.

## <a name="recommendations"></a>Empfehlungen

Der beste Ansatz, um sicherzustellen, dass Ihre Anwendung IPv6-kompatible Funktionsaufrufe verwendet, ist die Verwendung der [**getaddrinfo-Funktion**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) zum Abrufen der Host-zu-Adresse-Übersetzung. Ab Windows XP macht die **getaddrinfo-Funktion** die [**gethostbyname-Funktion**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) überflüssig, und Ihre Anwendung sollte daher stattdessen die **getaddrinfo-Funktion** für zukünftige Programmierprojekte verwenden. Während Microsoft weiterhin **gethostbyname** unterstützt, wird diese Funktion nicht erweitert, um IPv6 zu unterstützen. Zur transparenten Unterstützung des Abrufens von IPv6- und IPv4-Hostinformationen müssen Sie **getaddrinfo** verwenden.

Das folgende Beispiel zeigt, wie Die **getaddrinfo-Funktion** am besten verwendet werden kann. Beachten Sie, dass die Funktion bei ordnungsgemäßer Verwendung, wie in diesem Beispiel veranschaulicht, sowohl die IPv6- als auch die IPv4-Host-zu-Adresse-Übersetzung ordnungsgemäß verarbeitet, aber auch andere nützliche Informationen zum Host erhält, z. B. den Typ der unterstützten Sockets. Dieses Beispiel ist ein Auszug aus dem Client.c-Beispiel aus Anhang B.


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
> Die Version der [**getaddrinfo-Funktion,**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) die IPv6 unterstützt, ist für die Windows XP-Version von Windows neu.

 

Zu vermeidende Code

Die Hostadressenübersetzung wurde bisher mithilfe der [**gethostbyname-Funktion**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) erreicht. Ab Windows XP:

-   Die **getaddrinfo-Funktion** macht die **gethostbyname-Funktion** veraltet.
-   Ihre Anwendungen sollten die **getaddrinfo-Funktion** anstelle der **gethostbyname-Funktion** verwenden.

Programmieraufgaben

**So ändern Sie eine vorhandene IPv4-Anwendung, um Unterstützung für IPv6 hinzuzufügen**

1.  Erwerben Sie das Checkv4.exe Hilfsprogramm. Dieses Hilfsprogramm wird als Teil des Windows SDK installiert. Das Windows SDK ist über ein MSDN-Abonnement verfügbar und kann auch von der Microsoft-Website ( heruntergeladen https://msdn.microsoft.com) werden. Eine ältere Version des *Checkv4.exe-Tools* war auch als Teil der Microsoft IPv6 Technology Preview für Windows 2000 enthalten.
2.  Führen Sie *Checkv4.exe* Hilfsprogramm für Ihren Code aus. Unter [Verwenden des Checkv4.exe-Hilfsprogramms](using-the-checkv4-exe-utility-2.md) erfahren Sie, wie Sie das Versions-Hilfsprogramm für Ihre Dateien ausführen.
3.  Das Hilfsprogramm warnt Sie vor der Verwendung der Funktionen [**gethostbyname,**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr)und anderer nur IPv4-ender Funktionen und bietet Empfehlungen dazu, wie sie durch die IPv6-kompatible Funktion ersetzt werden, z. B. [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) und [**getnameinfo.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)
4.  Ersetzen Sie alle Instanzen der **gethostbyname-Funktion** und den zugehörigen Code entsprechend durch die **getaddrinfo-Funktion.** Verwenden Windows Vista die [**WSAConnectByName-**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) oder [**WSAConnectByList-Funktion,**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist) falls zutreffend.
5.  Ersetzen Sie alle Instanzen der [**gethostbyaddr-Funktion**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) und den zugehörigen Code entsprechend durch die [**getnameinfo-Funktion.**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo)

Alternativ können Sie Ihre Codebasis nach Instanzen der **Funktionen gethostbyname** und [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) durchsuchen und diese Nutzung (und gegebenenfalls anderen zugehörigen Code) in die Funktionen **getaddrinfo** und [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) ändern.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Leitfaden für Windows Sockets-Anwendungen](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[Ändern von Datenstrukturen für IPv6 Winsock-Appications](changing-data-structures-2.md)
</dt> <dt>

[Dual-Stack-Sockets für IPv6-Winsock-Anwendungen](dual-stack-sockets.md)
</dt> <dt>

[Verwenden von hartcodierten IPv4-Adressen](use-of-hardcoded-ipv4-addresses-2.md)
</dt> <dt>

[Benutzeroberfläche von IPv6-Winsock-Anwendungen](user-interface-issues-2.md)
</dt> <dt>

[Zugrunde liegende Protokolle für IPv6 Winsock-Anwendungen](underlying-protocols-2.md)
</dt> </dl>

 

 
