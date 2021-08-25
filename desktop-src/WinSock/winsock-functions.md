---
description: Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock-Funktionen. Um weitere Informationen zu einer Funktion zu erhalten, klicken Sie auf den Funktionsnamen.
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Winsock-Funktionen
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 5057a2fa7ff113da3c8e5f9077f9dfb1df83c3a390546b9d49d2d4b94db3625e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119860720"
---
# <a name="winsock-functions"></a>Winsock-Funktionen

Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock-Funktionen. Um weitere Informationen zu einer Funktion zu erhalten, klicken Sie auf den Funktionsnamen.

| Funktion | BESCHREIBUNG |
|-|-|
| [**Akzeptieren**](/windows/win32/api/Winsock2/nf-winsock2-accept) | Lässt einen eingehenden Verbindungsversuch für einen Socket zu. |
| [**AcceptEx**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | Akzeptiert eine neue Verbindung, gibt die lokale adresse und die Remoteadresse zurück und empfängt den ersten Datenblock, der von der Clientanwendung gesendet wird. |
| [**Binden**](/windows/win32/api/winsock/nf-winsock-bind) | Ordnet einem Socket eine lokale Adresse zu. |
| [**closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) | Schließt einen vorhandenen Socket. |
| [**Verbinden**](/windows/win32/api/Winsock2/nf-winsock2-connect) | Stellt eine Verbindung mit einem angegebenen Socket ein. |
| [**ConnectEx**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | Stellt eine Verbindung mit einem angegebenen Socket ein und sendet optional Daten, sobald die Verbindung hergestellt wurde. Wird nur für verbindungsorientierte Sockets unterstützt. |
| [**DisconnectEx**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | Schließt eine Verbindung auf einem Socket und ermöglicht die Wiederverwendung des Sockethandpunkts. |
| [**EnumProtocols**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | Ruft Informationen zu einem angegebenen Satz von Netzwerkprotokollen ab, die auf einem lokalen Host aktiv sind. |
| [**freeaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | Gibt Adressinformationen frei, die von der [**getaddrinfo-Funktion**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) dynamisch in [**addrinfo-Strukturen zugewiesen**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) werden. |
| [**FreeAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | Gibt Adressinformationen frei, die von der [**GetAddrInfoEx-Funktion**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) dynamisch in [**addrinfoex-Strukturen zugewiesen**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) werden. |
| [**FreeAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | Gibt Adressinformationen frei, die von der [**GetAddrInfoW-Funktion**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) dynamisch in [**addrinfoW-Strukturen zugewiesen**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) werden. |
| [**\_strerror**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | Unterstützt das Drucken von Fehlermeldungen basierend auf den EAI-Fehlern, die von der \_ \* [**getaddrinfo-Funktion zurückgegeben**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) werden. |
| [**GetAcceptExSockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | Analysiert die Daten, die aus einem Aufruf der [**AcceptEx-Funktion erhalten**](/windows/win32/api/mswsock/nf-mswsock-acceptex) wurden. |
| [**GetAddressByName**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | Fragt einen Namespace oder eine Reihe von Standardnamespaces ab, um Netzwerkadresseninformationen für einen angegebenen Netzwerkdienst abzurufen. Dieser Prozess wird als Dienstnamenauflösung bezeichnet. Ein Netzwerkdienst kann auch die -Funktion verwenden, um lokale Adressinformationen zu erhalten, die er mit der [**bind-Funktion verwenden**](/windows/win32/api/winsock/nf-winsock-bind) kann. |
| [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | Bietet protokollunabhängige Übersetzung von einem ANSI-Hostnamen in eine Adresse. |
| [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | Bietet protokollunabhängige Namensauflösung mit zusätzlichen Parametern, um zu qualifizieren, welche Namenraumanbieter die Anforderung verarbeiten sollen. |
| [**GetAddrInfoExCancel**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | Bricht einen asynchronen Vorgang durch die [**GetAddrInfoEx-Funktion**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) ab. |
| [**GetAddrInfoExOverlappedResult**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | Ruft den Rückgabecode für eine **OVERLAPPED-Struktur** ab, die von einem asynchronen Vorgang für die [**GetAddrInfoEx-Funktion verwendet**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) wird. |
| [**GetAddrInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | Stellt protokollunabhängige Übersetzung von einem Unicode-Hostnamen in eine Adresse zur Verfügung. |
| [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | Ruft die Hostinformationen ab, die einer Netzwerkadresse entspricht. |
| [**Gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | Ruft Hostinformationen ab, die einem Hostnamen aus einer Hostdatenbank entspricht. Veraltet: Verwenden Sie stattdessen [**getaddrinfo.**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) |
| [**Gethostname**](/windows/win32/api/winsock/nf-winsock-gethostname) | Ruft den Standardhostnamen für den lokalen Computer ab. |
| [**GetHostNameW**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | Ruft den Standardhostnamen für den lokalen Computer als Unicode-Zeichenfolge ab. |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | Ruft den Multicastfilterstatus für einen IPv4-Socket ab. |
| [**GetNameByType**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | Ruft den Namen eines Netzwerkdiensts für den angegebenen Diensttyp ab. |
| [**getnameinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | Stellt die Namensauflösung von einer IPv4- oder IPv6-Adresse zu einem ANSI-Hostnamen und von einer Portnummer zum ANSI-Dienstnamen zur Verfügung. |
| [**GetNameInfoW**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | Stellt die Namensauflösung von einer IPv4- oder IPv6-Adresse zu einem Unicode-Hostnamen und von einer Portnummer zum Unicode-Dienstnamen zur Verfügung. |
| [**getpeername**](/windows/win32/api/winsock/nf-winsock-getpeername) | Ruft die Adresse des Peers ab, mit dem ein Socket verbunden ist. |
| [**getprotobyname**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | Ruft die Protokollinformationen ab, die einem Protokollnamen entspricht. |
| [**getprotobynumber**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | Ruft Protokollinformationen ab, die einer Protokollnummer entspricht. |
| [**getservbyname**](/windows/win32/api/winsock/nf-winsock-getservbyname) | Ruft Dienstinformationen ab, die einem Dienstnamen und Protokoll entspricht. |
| [**getservbyport**](/windows/win32/api/winsock/nf-winsock-getservbyport) | Ruft Dienstinformationen ab, die einem Port und Protokoll entspricht. |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | Ruft Informationen zu einem Netzwerkdienst im Kontext eines Sets von Standardnamespaces oder eines angegebenen Namespaces ab. |
| [**getsockname**](/windows/win32/api/winsock/nf-winsock-getsockname) | Ruft den lokalen Namen für einen Socket ab. |
| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) | Ruft eine Socketoption ab. |
| [**getsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | Ruft den Multicastfilterstatus für einen IPv4- oder IPv6-Socket ab. |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | Ruft eine Diensttyp-GUID für einen Netzwerkdienst ab, der durch den Namen angegeben wird. |
| [**htond**](/windows/win32/api/Winsock2/nf-winsock2-htond) | Konvertiert ein Double **vom** Host in die TCP/IP-Netzwerk-Byte reihenfolge (big-endian). |
| [**htonf**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | Konvertiert einen **Float vom** Host in die TCP/IP-Netzwerk-Byte reihenfolge (big-endian). |
| [**htonl**](/windows/win32/api/winsock/nf-winsock-htonl) | Konvertiert einen **u \_ long vom** Host in die TCP/IP-Netzwerk-Byte reihenfolge (big-endian). |
| [**htonll**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | Konvertiert eine **nicht signierte \_ \_ int64-Datei** vom Host in die TCP/IP-Netzwerk-Byte reihenfolge (big-endian). |
| [**htons**](/windows/win32/api/winsock/nf-winsock-htons) | Konvertiert eine **u \_ short vom** Host in die TCP/IP-Netzwerk-Byte reihenfolge (big-endian). |
| [**\_Inet-Addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | Konvertiert eine Zeichenfolge, die eine gepunktete Ipv4-Adresse des Internetprotokolls enthält, in eine geeignete Adresse für die [**\_ in-Addr-Struktur.**](/windows/win32/api/winsock2/ns-winsock2-in_addr) |
| [**inet \_ ntoa**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | Konvertiert eine (IPv4)-Internetnetzwerkadresse in eine Zeichenfolge im gepunkteten Internetstandardformat. |
| [**InetNtop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | konvertiert eine IPv4- oder IPv6-Internetnetzwerkadresse in eine Zeichenfolge im Internetstandardformat. Die ANSI-Version dieser Funktion befindet sich [**inet \_ ntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw). |
| [**Inet Cogn**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | Konvertiert eine IPv4- oder IPv6-Internetnetzwerkadresse in der Standardtextdarstellungsform in die numerische binäre Form. Die ANSI-Version dieser Funktion ist [**inet \_ pton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw). |
| [**ioctlsocket**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | Steuert den E/A-Modus eines Sockets. |
| [**listen**](/windows/win32/api/Winsock2/nf-winsock2-listen) | Platziert einen Socket in einen Zustand, in dem er auf eine eingehende Verbindung lauscht. |
| [**ntohd**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | Konvertiert eine **nicht signierte \_ \_ int64** aus der TCP/IP-Netzwerkreihenfolge in die Host-Bytereihenfolge (bei Intel-Prozessoren little-endian) und gibt einen **doppelten** zurück. |
| [**ntohf**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | Konvertiert einen **nicht signierten \_ \_ int32** aus der TCP/IP-Netzwerkreihenfolge in die Host-Bytereihenfolge (bei Intel-Prozessoren little-endian) und gibt einen **float-Wert** zurück. |
| [**ntohl**](/windows/win32/api/winsock/nf-winsock-ntohl) | Konvertiert eine u \_ long-Netzwerkreihenfolge von TCP/IP in die Host-Bytereihenfolge (bei Intel-Prozessoren little-endian). |
| [**ntohll**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | Konvertiert eine **nicht signierte \_ \_ int64-Instanz** aus der TCP/IP-Netzwerkreihenfolge in die Host-Bytereihenfolge (bei Intel-Prozessoren little-endian). |
| [**ntohs**](/windows/win32/api/winsock/nf-winsock-ntohs) | Konvertiert eine u \_ short-Instanz aus der TCP/IP-Netzwerk-Bytereihenfolge in die Host-Bytereihenfolge (bei Intel-Prozessoren little-endian). |
| [**Recv**](/windows/win32/api/winsock/nf-winsock-recv) | Empfängt Daten von einem verbundenen oder gebundenen Socket. |
| [**recvfrom**](/windows/win32/api/winsock/nf-winsock-recvfrom) | Empfängt ein Datagramm und speichert die Quelladresse. |
| [**RIOCloseCompletionQueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | Schließt eine vorhandene Vervollständigungswarteschlange, die für die E/A-Abschlussbenachrichtigung verwendet wird, indem Anforderungen mit den bei Winsock registrierten E/A-Erweiterungen gesendet und empfangen werden. |
| [**RIOCreateCompletionQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Erstellt eine E/A-Vervollständigungswarteschlange mit einer bestimmten Größe für die Verwendung mit den bei Winsock registrierten E/A-Erweiterungen. |
| [**RIOCreateRequestQueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | Erstellt einen registrierten E/A-Socketdeskriptor mit einem angegebenen Socket und E/A-Abschlusswarteschlangen für die Verwendung mit den registrierten E/A-Erweiterungen von Winsock. |
| [**RIODequeueCompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Entfernt Einträge aus einer E/A-Vervollständigungswarteschlange für die Verwendung mit den bei Winsock registrierten E/A-Erweiterungen. |
| [**RIODeregisterBuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | Deregistrierung eines registrierten Puffers, der mit den bei Winsock registrierten E/A-Erweiterungen verwendet wird. |
| [**RIONotify**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | Registriert die Methode für das Benachrichtigungsverhalten bei einer E/A-Vervollständigungswarteschlange für die Verwendung mit den bei Winsock registrierten E/A-Erweiterungen. |
| [**RIOReceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | Empfängt Netzwerkdaten auf einem verbundenen registrierten E/A-TCP-Socket oder einem gebundenen registrierten E/A-UDP-Socket für die Verwendung mit den bei Winsock registrierten E/A-Erweiterungen. |
| [**RIOReceiveEx**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | Empfängt Netzwerkdaten auf einem verbundenen registrierten E/A-TCP-Socket oder einem gebundenen registrierten E/A-UDP-Socket mit zusätzlichen Optionen für die Verwendung mit den bei Winsock registrierten E/A-Erweiterungen. |
| [**RIORegisterBuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | Registriert eine [**RIO \_ BUFFERID**](rio-bufferid.md), einen registrierten Pufferdeskriptor, mit einem angegebenen Puffer für die Verwendung mit den registrierten E/A-Erweiterungen von Winsock. |
| [**RIOResizeCompletionQueue**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | Ändert die Größe einer E/A-Vervollständigungswarteschlange so, dass sie für die Verwendung mit den bei Winsock registrierten E/A-Erweiterungen entweder größer oder kleiner ist. |
| [**RIOResizeRequestQueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | Ändert die Größe einer Anforderungswarteschlange so, dass sie für die Verwendung mit den registrierten E/A-Erweiterungen von Winsock entweder größer oder kleiner ist. |
| [**RIOSend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | Sendet Netzwerkdaten an einen verbundenen registrierten E/A-TCP-Socket oder einen gebundenen registrierten E/A-UDP-Socket zur Verwendung mit den bei Winsock registrierten E/A-Erweiterungen. |
| [**RIOSendEx**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | Sendet Netzwerkdaten an einen verbundenen registrierten E/A-TCP-Socket oder einen gebundenen registrierten E/A-UDP-Socket mit zusätzlichen Optionen für die Verwendung mit den bei Winsock registrierten E/A-Erweiterungen. |
| [**Auswählen**](/windows/win32/api/Winsock2/nf-winsock2-select) | Bestimmt den Status eines oder mehrerer Sockets, die bei Bedarf auf die Ausführung synchroner E/A-Vorgänge warten. |
| [**Senden**](/windows/win32/api/Winsock2/nf-winsock2-send) | Sendet Daten an einen verbundenen Socket. |
| [**Sendto**](/windows/win32/api/winsock/nf-winsock-sendto) | Sendet Daten an ein bestimmtes Ziel. |
| [**SetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | Registriert einen Host- und Dienstnamen zusammen mit zugeordneten Adressen bei einem bestimmten Namespaceanbieter. |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | Legt den Multicastfilterstatus für einen IPv4-Socket fest. |
| [**SetService**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | Registriert oder entfernt einen Netzwerkdienst innerhalb eines oder mehrerer Namespaces aus der Registrierung. Kann auch einen Netzwerkdiensttyp innerhalb eines oder mehrerer Namespaces hinzufügen oder entfernen. |
| [**SetSocketMediaStreamingMode**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | Gibt an, ob das Netzwerk für die Übertragung von Streamingmedien verwendet werden soll, die eine Dienstqualität erfordern. |
| [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) | Legt eine Socketoption fest. |
| [**setsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | Legt den Multicastfilterstatus für einen IPv4- oder IPv6-Socket fest. |
| [**Herunterfahren**](/windows/win32/api/winsock/nf-winsock-shutdown) | Deaktiviert Sende- oder Empfangsbenachrichtigungen für einen Socket. |
| [**Socket**](/windows/win32/api/Winsock2/nf-winsock2-socket) | Erstellt einen Socket, der an einen bestimmten Dienstanbieter gebunden ist. |
| [**Transmitfile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | Überträgt Dateidaten über ein verbundenes Sockethandle. |
| [**TransmitPackets**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | Überträgt In-Memory-Daten oder Dateidaten über einen verbundenen Socket. |
| [**WSAAccept**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | Akzeptiert eine Verbindung bedingt basierend auf dem Rückgabewert einer Bedingungsfunktion, stellt die Qualität der Dienstflussspezifikationen bereit und ermöglicht die Übertragung von Verbindungsdaten. |
| [**WSAAddressToString**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | Konvertiert alle Komponenten einer [**Sockaddr-Struktur**](sockaddr-2.md) in eine für Menschen lesbare Zeichenfolgendarstellung der Adresse. |
| [**WSAAsyncGetHostByAddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | Ruft asynchron Hostinformationen ab, die einer Adresse entsprechen. |
| [**WSAAsyncGetHostByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | Ruft asynchron Hostinformationen ab, die einem Hostnamen entsprechen. |
| [**WSAAsyncGetProtoByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | Ruft asynchron Protokollinformationen ab, die einem Protokollnamen entsprechen. |
| [**WSAAsyncGetProtoByNumber**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | Ruft asynchron Protokollinformationen ab, die einer Protokollnummer entsprechen. |
| [**WSAAsyncGetServByName**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | Ruft asynchron Dienstinformationen ab, die einem Dienstnamen und Port entsprechen. |
| [**WSAAsyncGetServByPort**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | Ruft asynchron Dienstinformationen ab, die einem Port und Protokoll entsprechen. |
| [**WSAAsyncSelect**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | Fordert Windows nachrichtenbasierte Benachrichtigung über Netzwerkereignisse für einen Socket an. |
| [**WSACancelAsyncRequest**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | Bricht einen unvollständigen asynchronen Vorgang ab. |
| [**WSACleanup**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | Beendet die Verwendung der \_ Ws2-32.DLL. |
| [**WSACloseEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | Schließt ein geöffnetes Ereignisobjekthandle. |
| [**WSAConnect**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | Stellt eine Verbindung mit einer anderen Socketanwendung her, tauscht Verbindungsdaten aus und gibt die erforderliche Dienstqualität basierend auf der angegebenen [**FLOWSPEC-Struktur**](/windows/win32/api/qos/ns-qos-flowspec) an. |
| [**WSAConnectByList**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | Stellt eine Verbindung mit einem aus einer Sammlung möglicher Endpunkte her, die durch einen Satz von Zieladressen (Hostnamen und Ports) dargestellt werden. |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | Stellt eine Verbindung mit einer anderen Socketanwendung auf einem angegebenen Host und Port her. |
| [**WSACreateEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | Erstellt ein neues Ereignisobjekt. |
| [**WSADeleteSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | Entfernt die Zuordnung zwischen einem Peerzielnamen und einer IP-Adresse für einen Socket. |
| [**WSADuplicateSocket**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | Gibt eine -Struktur zurück, mit der ein neuer Socketdeskriptor für einen freigegebenen Socket erstellt werden kann. |
| [**WSAEnumNameSpaceProviders**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | Ruft Informationen zu verfügbaren Namespaces ab. |
| [**WSAEnumNameSpaceProvidersEx**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | Ruft Informationen zu verfügbaren Namespaces ab. |
| [**WSAEnumNetworkEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | Ermittelt Vorkommen von Netzwerkereignissen für den angegebenen Socket, löscht interne Netzwerkereignisdatensätze und setzt Ereignisobjekte zurück (optional). |
| [**WSAEnumProtocols**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | Ruft Informationen zu verfügbaren Transportprotokollen ab. |
| [**WSAEventSelect**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | Gibt ein Ereignisobjekt an, das dem angegebenen Satz von FD \_ XXX-Netzwerkereignissen zugeordnet werden soll. |
| [**\_\_WSAFDIsSet**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | Gibt an, ob ein Socket in einem Satz von Socketdeskriptoren enthalten ist. |
| [**WSAGetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | Fragt den Status der [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) Socketoption ab. |
| [**WSAGetIcmpErrorInfo**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | Fragt die Quelladresse eines ICMP-Fehlers ab, der während der Verbindungseinrichtung an einem TCP-Socket empfangen wurde. |
| [**WSAGetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | Ruft die benutzerdefinierte IP-Schicht-MTU für einen Socket ab. |
| [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | Gibt den Fehlerstatus für den letzten fehlgeschlagenen Vorgang zurück. |
| [**WSAGetOverlappedResult**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | Ruft die Ergebnisse eines überlappenden Vorgangs für den angegebenen Socket ab. |
| [**WSAGetQOSByName**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | Initialisiert eine [**QOS-Struktur**](/windows/win32/api/winsock2/ns-winsock2-qos) basierend auf einer benannten Vorlage oder stellt einen Puffer bereit, um eine Enumeration der verfügbaren Vorlagennamen abzurufen. |
| [**WSAGetServiceClassInfo**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | Ruft die Klasseninformationen (Schema) für eine angegebene Dienstklasse von einem angegebenen Namespaceanbieter ab. |
| [**WSAGetServiceClassNameByClassId**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | Ruft den Namen des Diensts ab, der dem angegebenen Typ zugeordnet ist. |
| [**WSAGetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | Ruft die maximale Größe einer empfangenen, zusammengefügten Nachricht für einen UDP-Socket ab. |
| [**WSAGetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | Ruft die Größe der Segmentierungsmeldung für einen UDP-Socket ab. |
| [**WSAHtonl**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | Konvertiert eine u \_ long-Reihenfolge von der Host-Bytereihenfolge in die Netzwerk-Bytereihenfolge. |
| [**WSAHtons**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | Konvertiert eine u \_ short-Instanz aus der Host-Bytereihenfolge in die Netzwerk-Bytereihenfolge. |
| [**WSAImpersonateSocketPeer**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | Wird verwendet, um die Identität des Sicherheitsprinzipals zu übernehmen, der einem Socketspeer entspricht, um eine Autorisierung auf Anwendungsebene auszuführen. |
| [**WSAInstallServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | Registriert ein Dienstklassenschema in einem Namespace. |
| [**WSAIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | Steuert den Modus eines Sockets. |
| [**WSAJoinLeaf**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | Verknüpft einen Blattknoten mit einer Multipointsitzung, tauscht Verbindungsdaten aus und gibt die erforderliche Dienstqualität basierend auf den angegebenen Strukturen an. |
| [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | Initiiert eine Clientabfrage, die durch die in einer [**WSAQUERYSET-Struktur**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) enthaltenen Informationen eingeschränkt ist. |
| [**WSALookupServiceEnd**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | Gibt das von vorherigen Aufrufen von [**WSALookupServiceBegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) und [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta)verwendete Handle frei. |
| [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | Rufen Sie die angeforderten Dienstinformationen ab. |
| [**WSANSPIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | Entwickler, die E/A-Steuerelementaufrufe an einen registrierten Namespace vornehmen. |
| [**WSANtohl**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | Konvertiert eine u \_ long-Reihenfolge aus der Netzwerk-Bytereihenfolge in die Host-Bytereihenfolge. |
| [**WSANtohs**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | Konvertiert eine u \_ short-Instanz der Netzwerk-Bytereihenfolge in die Host-Bytereihenfolge. |
| [**WSAPoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | Bestimmt den Status eines oder mehrerer Sockets. |
| [**WSAProviderConfigChange**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | Benachrichtigt die Anwendung, wenn die Anbieterkonfiguration geändert wird. |
| [**WSAQuerySocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | Fragt Informationen zur Sicherheit ab, die auf eine Verbindung auf einem Socket angewendet wird. |
| [**WSARecv**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | Empfängt Daten aus einem verbundenen Socket. |
| [**WSARecvDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | Beendet den Empfang für einen Socket und ruft die Daten zum Trennen der Verbindung ab, wenn der Socket verbindungsorientiert ist. |
| [**WSARecvEx**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | Empfängt Daten aus einem verbundenen Socket. |
| [**WSARecvFrom**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | Empfängt ein Datagramm und speichert die Quelladresse. |
| [**LPFN_WSARECVMSG (WSARecvMsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | Empfängt Daten und optionale Steuerinformationen von verbundenen und nicht verbundenen Sockets. |
| [**WSARemoveServiceClass**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | Entfernt das Dienstklassenschema dauerhaft aus der Registrierung. |
| [**WSAResetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | Setzt den Zustand des angegebenen Ereignisobjekts auf nicht signalisiert zurück. |
| [**WSARevertImpersonation**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | Beendet den Identitätswechsel eines Socketspeer. |
| [**WSASend**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | Sendet Daten an einen verbundenen Socket. |
| [**WSASendDisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | Initiiert die Beendigung der Verbindung für den Socket und sendet Daten zum Trennen der Verbindung. |
| [**WSASendMsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | Sendet Daten und optionale Steuerungsinformationen von verbundenen und nicht verbundenen Sockets. |
| [**WSASendTo**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | Sendet Daten an ein bestimmtes Ziel, wobei ggf. überlappende E/A-Datenübertragungen verwendet werden. |
| [**WSASetEvent**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | Legt den Zustand des angegebenen Ereignisobjekts auf signalisiert fest. |
| [**WSASetFailConnectOnIcmpError**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | Legt den Status der [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) Socketoption fest. |
| [**WSASetIPUserMtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | Legt die benutzerdefinierte IP-Schicht-MTU für einen Socket fest. |
| [**WSASetLastError**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | Legt den Fehlercode fest. |
| [**WSASetService**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | Registriert oder entfernt eine Dienstinstanz in einem oder mehreren Namespaces aus der Registrierung. |
| [**WSASetSocketPeerTargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | Wird verwendet, um den Peerzielnamen (SPN) anzugeben, der einer Peer-IP-Adresse entspricht. Dieser Zielname soll von Clientanwendungen angegeben werden, um den Peer, der authentifiziert werden soll, sicher zu identifizieren. |
| [**WSASetSocketSecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | Aktiviert und wendet Die Sicherheit für einen Socket an. |
| [**WSASetUdpRecvMaxCoalescedSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | Legt die maximale Größe einer zusammengeknüpften Nachricht fest, die für einen UDP-Socket festgelegt ist. |
| [**WSASetUdpSendMessageSize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | Legt die Größe der Segmentierungsmeldung für einen UDP-Socket fest. |
| [**WSASocket**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | Erstellt einen Socket, der an einen bestimmten Transportdienstanbieter gebunden ist. |
| [**WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | Initiiert die Verwendung von \_ WS2-32.DLL durch einen Prozess. |
| [**WSAStringToAddress**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | Konvertiert eine numerische Zeichenfolge in eine [**Sockaddr-Struktur.**](sockaddr-2.md) |
| [**WSAWaitForMultipleEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | Gibt entweder zurück, wenn sich eines oder alle angegebenen Ereignisobjekte im signalisierten Zustand befinden oder wenn das Time out-Intervall abläuft. |
