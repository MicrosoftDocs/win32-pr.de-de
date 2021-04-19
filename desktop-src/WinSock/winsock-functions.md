---
description: Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock-Funktionen. Wenn Sie weitere Informationen zu einer beliebigen Funktion haben, klicken Sie auf den Funktionsnamen.
ms.assetid: edafb5f9-09fe-4f8e-9651-4002b6f622f4
title: Winsock-Funktionen
ms.topic: article
ms.date: 10/01/2019
ms.openlocfilehash: 9bf2205c970eeaaf4e64867565d58680b28298c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373153"
---
# <a name="winsock-functions"></a>Winsock-Funktionen

Die folgende Liste enthält präzise Beschreibungen der einzelnen Winsock-Funktionen. Wenn Sie weitere Informationen zu einer beliebigen Funktion haben, klicken Sie auf den Funktionsnamen.

| Funktion | BESCHREIBUNG |
|-|-|
| [**erst**](/windows/win32/api/Winsock2/nf-winsock2-accept) | Ermöglicht einen eingehenden Verbindungsversuch für einen Socket. |
| [**Akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex) | Akzeptiert eine neue Verbindung, gibt die lokale und die Remote Adresse zurück und empfängt den ersten von der Client Anwendung gesendeten Datenblock. |
| [**Zwick**](/windows/win32/api/winsock/nf-winsock-bind) | Ordnet einem Socket eine lokale Adresse zu. |
| [**closesocket**](/windows/win32/api/winsock/nf-winsock-closesocket) | Schließt einen vorhandenen Socket. |
| [**herzustellen**](/windows/win32/api/Winsock2/nf-winsock2-connect) | Stellt eine Verbindung mit einem angegebenen Socket her. |
| [**Connectex**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_connectex) | Stellt eine Verbindung mit einem angegebenen Socket her und sendet optional Daten, sobald die Verbindung hergestellt wurde. Wird nur für Verbindungs orientierte Sockets unterstützt. |
| [**Disconnectex**](/previous-versions/windows/desktop/legacy/ms737757(v=vs.85)) | Schließt eine Verbindung für einen Socket und ermöglicht die Wiederverwendung des Sockethandles. |
| [**Enumprotokolle**](/windows/win32/api/Nspapi/nf-nspapi-enumprotocolsa) | Ruft Informationen zu einem angegebenen Satz von Netzwerkprotokollen ab, die auf einem lokalen Host aktiv sind. |
| [**"freiaddrinfo"**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfo) | Gibt Adressinformationen frei, die von der [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion dynamisch in [**addrinfo**](/windows/win32/api/ws2def/ns-ws2def-addrinfoa) -Strukturen zugewiesen werden. |
| [**"Freiaddrinfoex"**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfoex) | Gibt Adressinformationen frei, die von der [**getaddrinfoex**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) -Funktion dynamisch in [**addrinfoex**](/windows/win32/api/Ws2def/ns-ws2def-addrinfoexw) -Strukturen zugewiesen werden. |
| [**Freiaddrinfow**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-freeaddrinfow) | Gibt Adressinformationen frei, die von der [**getaddrinfow**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) -Funktion dynamisch in [**addrinfow**](/windows/win32/api/Ws2def/ns-ws2def-addrinfow) -Strukturen zugewiesen werden. |
| [**Gai- \_ Fehler**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-gai_strerrora) | Unterstützt das Drucken von Fehlermeldungen auf der Grundlage der \_ \* von der [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) -Funktion zurückgegebenen EAI-Fehler. |
| [**Getaccept texsockaddrs**](/windows/win32/api/mswsock/nf-mswsock-getacceptexsockaddrs) | Analysiert die Daten, die aus einem-Aufrufs der [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex) -Funktion abgerufen werden. |
| [**GetAddressByName**](/windows/win32/api/Nspapi/nf-nspapi-getaddressbynamea) | Fragt einen Namespace oder einen Satz von Standardnamespaces ab, um Netzwerk Adressinformationen für einen angegebenen Netzwerkdienst abzurufen. Dieser Prozess wird als Dienst Namensauflösung bezeichnet. Ein Netzwerkdienst kann mithilfe der-Funktion auch lokale Adressinformationen abrufen, die er mit der [**Bind**](/windows/win32/api/winsock/nf-winsock-bind) -Funktion verwenden kann. |
| [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) | Stellt eine Protokoll unabhängige Übersetzung von einem ANSI-Hostnamen in eine Adresse bereit. |
| [**GetAddrInfoEx**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) | Stellt eine Protokoll unabhängige Namensauflösung mit zusätzlichen Parametern bereit, um zu qualifizieren, welche namens Speicher Anbieter die Anforderung verarbeiten sollen. |
| [**Getaddrinfoexcancel**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexcancel) | Bricht einen asynchronen Vorgang durch die [**getaddrinfoex**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) -Funktion ab. |
| [**Getaddrinfoexoverlappedresult**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexoverlappedresult) | Ruft den Rückgabecode für eine **über** Lapp Ende Struktur ab, die von einem asynchronen Vorgang für die [**getaddrinfoex**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfoexa) -Funktion verwendet wird. |
| [**Getaddrinfow**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfow) | Stellt eine Protokoll unabhängige Übersetzung von einem Unicode-Hostnamen in eine Adresse bereit. |
| [**gethostbyaddr**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyaddr) | Ruft die Hostinformationen ab, die einer Netzwerkadresse entsprechen. |
| [**gethostbyname**](/windows/win32/api/wsipv6ok/nf-wsipv6ok-gethostbyname) | Ruft Hostinformationen ab, die einem Hostnamen aus einer Host Datenbank entsprechen. Veraltet: Verwenden Sie stattdessen [**getaddrinfo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) . |
| [**GetHostName**](/windows/win32/api/winsock/nf-winsock-gethostname) | Ruft den Standard Hostnamen für den lokalen Computer ab. |
| [**Gethostnamew**](/windows/win32/api/Winsock2/nf-winsock2-gethostnamew) | Ruft den Standard Hostnamen für den lokalen Computer als Unicode-Zeichenfolge ab. |
| [**getipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getipv4sourcefilter) | Ruft den Multicast Filter Zustand für einen IPv4-Socket ab. |
| [**Getnamebytype**](/windows/win32/api/Nspapi/nf-nspapi-getnamebytypea) | Ruft den Namen eines Netzwerk Dienstanbieter für den angegebenen Diensttyp ab. |
| [**getnameingefo**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) | Ermöglicht die Namensauflösung von einer IPv4-oder IPv6-Adresse zu einem ANSI-Hostnamen und von einer Portnummer zum ANSI-Dienstnamen. |
| [**Getnameingefow**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getnameinfow) | Ermöglicht die Namensauflösung von einer IPv4-oder IPv6-Adresse zu einem Unicode-Hostnamen und von einer Portnummer zum Unicode-Dienstnamen. |
| [**getPeer Name**](/windows/win32/api/winsock/nf-winsock-getpeername) | Ruft die Adresse des Peers ab, mit dem ein Socket verbunden ist. |
| [**getprotobyname**](/windows/win32/api/winsock/nf-winsock-getprotobyname) | Ruft die Protokollinformationen ab, die einem Protokollnamen entsprechen. |
| [**getprotobynumber**](/windows/win32/api/winsock/nf-winsock-getprotobynumber) | Ruft Protokollinformationen entsprechend einer Protokollnummer ab. |
| [**getservbyname**](/windows/win32/api/winsock/nf-winsock-getservbyname) | Ruft Dienst Informationen ab, die einem Dienstnamen und einem Protokoll entsprechen. |
| [**getservbyport**](/windows/win32/api/winsock/nf-winsock-getservbyport) | Ruft Dienst Informationen ab, die einem Port und Protokoll entsprechen. |
| [**GetService**](/windows/win32/api/Nspapi/nf-nspapi-getservicea) | Ruft Informationen zu einem Netzwerkdienst im Kontext eines Satzes von Standardnamespaces oder eines angegebenen Namespace ab. |
| [**getsockname**](/windows/win32/api/winsock/nf-winsock-getsockname) | Ruft den lokalen Namen für einen Socket ab. |
| [**getsockopt**](/windows/win32/api/winsock/nf-winsock-getsockopt) | Ruft eine Socketoption ab. |
| [**getsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-getsourcefilter) | Ruft den Multicast Filter Zustand für einen IPv4-oder IPv6-Socket ab. |
| [**GetTypeByName**](/windows/win32/api/Nspapi/nf-nspapi-gettypebynamea) | Ruft eine Diensttyp-GUID für einen durch den Namen angegebenen Netzwerkdienst ab. |
| [**htond**](/windows/win32/api/Winsock2/nf-winsock2-htond) | Konvertiert einen **Double** -Wert von Host in TCP/IP-Netzwerk-Byte Reihenfolge (Big-Endian). |
| [**htonf**](/windows/win32/api/Winsock2/nf-winsock2-htonf) | Konvertiert eine **Gleit** Komma Zahl vom Host in eine TCP/IP-Netzwerk-Byte Reihenfolge (Big-Endian). |
| [**htonl**](/windows/win32/api/winsock/nf-winsock-htonl) | Konvertiert eine **u \_ Long** -Datei vom Host in eine TCP/IP-Netzwerk-Byte Reihenfolge (Big-Endian). |
| [**htonll**](/windows/win32/api/Winsock2/nf-winsock2-htonll) | Konvertiert eine **nicht signierte \_ \_ Int64** vom Host in eine TCP/IP-netzwerkbyte Reihenfolge (Big-Endian). |
| [**htonnen**](/windows/win32/api/winsock/nf-winsock-htons) | Konvertiert eine **u- \_ Kurzform** vom Host in eine TCP/IP-Netzwerk-Byte Reihenfolge (Big-Endian). |
| [**inet \_ addr**](/windows/win32/api/winsock2/nf-winsock2-inet_addr) | Konvertiert eine Zeichenfolge, die eine (IPv4), gepunktete Internet Protokoll Adresse enthält, in eine richtige Adresse für die [**in der \_ addr**](/windows/win32/api/winsock2/ns-winsock2-in_addr) -Struktur. |
| [**inet \_ NUM**](/windows/win32/api/winsock2/nf-winsock2-inet_ntoa) | Konvertiert eine (IPv4)-Internet Netzwerkadresse in eine Zeichenfolge im Internet Standard-gepunkteten Format. |
| [**Inetntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw) | Konvertiert eine IPv4-oder IPv6-Internet Netzwerkadresse in eine Zeichenfolge im Internet Standardformat. Die ANSI-Version dieser Funktion ist " [**inet \_ ntop**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetntopw)". |
| [**Inetpton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw) | Konvertiert eine IPv4-oder IPv6-Internet Netzwerkadresse in Ihrer Standard-Text Präsentationsform in die entsprechende numerische Binär Form. Die ANSI-Version dieser Funktion ist [**inet \_ pton**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-inetptonw). |
| [**ioctlsocket**](/windows/win32/api/winsock/nf-winsock-ioctlsocket) | Steuert den e/a-Modus eines Sockets. |
| [**hin**](/windows/win32/api/Winsock2/nf-winsock2-listen) | Platziert einen Socket in einem Zustand, in dem eine eingehende Verbindung überwacht wird. |
| [**nzu HD**](/windows/win32/api/Winsock2/nf-winsock2-ntohd) | Konvertiert ein **\_ \_ Int64 ohne** Vorzeichen von der TCP/IP-Netzwerk Reihenfolge in die Host-Byte Reihenfolge (Little-Endian auf Intel-Prozessoren) und gibt einen **Double**-Wert zurück. |
| [**NUM HF**](/windows/win32/api/Winsock2/nf-winsock2-ntohf) | Konvertiert ein **\_ \_ Int32 ohne** Vorzeichen von der TCP/IP-Netzwerk Reihenfolge in die Host-Byte Reihenfolge (Little-Endian auf Intel-Prozessoren) und gibt einen **float**-Wert zurück. |
| [**nzu HLS**](/windows/win32/api/winsock/nf-winsock-ntohl) | Konvertiert einen u \_ -Long-Wert von der TCP/IP-Netzwerk Reihenfolge in die Host-Byte Reihenfolge (bei Intel-Prozessoren kleiner endian). |
| [**Nin-HLL**](/windows/win32/api/Winsock2/nf-winsock2-ntohll) | Konvertiert ein **nicht signiertes \_ \_ Int64** von der TCP/IP-Netzwerk Reihenfolge in die Host-Byte Reihenfolge (Little-Endian auf Intel-Prozessoren). |
| [**NUM**](/windows/win32/api/winsock/nf-winsock-ntohs) | Konvertiert eine u \_ Short von der TCP/IP-netzwerkbyte Reihenfolge in die Host-Byte Reihenfolge (bei Intel-Prozessoren Little-Endian). |
| [**empfangener**](/windows/win32/api/winsock/nf-winsock-recv) | Empfängt Daten von einem verbundenen oder gebundenen Socket. |
| [**recvfrom**](/windows/win32/api/winsock/nf-winsock-recvfrom) | Empfängt ein Datagramm und speichert die Quelladresse. |
| [**Rioclosecompletionqueue**](/previous-versions/windows/desktop/legacy/hh448837(v=vs.85)) | Schließt eine vorhandene Vervollständigungs Warteschlange, die für e/a-Abschluss Benachrichtigungen verwendet wird, durch Senden und empfangen von Anforderungen mit den von Winsock registrierten e/a |
| [**Riokreatecompletionqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Erstellt eine e/a-Abschluss Warteschlange mit einer bestimmten Größe für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Riokreaterequestqueue**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riocreaterequestqueue) | Erstellt einen registrierten e/a-socketdeskriptor mithilfe einer angegebenen Socket-und e/a-Vervollständigungs Warteschlange für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Rioabqueuecompletion**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riodequeuecompletion) | Entfernt Einträge aus einer e/a-Vervollständigungs Warteschlange für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Rioderegisterbuffer**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioderegisterbuffer) | Hebt die Registrierung eines registrierten Puffers auf, der bei den von Winsock registrierten e/a-Erweiterungen verwendet wird. |
| [**Rionotifizieren**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rionotify) | Registriert die Methode zur Verwendung für das Benachrichtigungs Verhalten mit einer e/a-Abschluss Warteschlange für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Rioreceive**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceive) | Empfängt Netzwerkdaten für einen verbundenen registrierten e/a-TCP-Socket oder einen gebundenen registrierten e/a-UDP-Socket für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Rioreceiveex**](/windows/win32/api/mswsock/nc-mswsock-lpfn_rioreceiveex) | Empfängt Netzwerkdaten für einen verbundenen registrierten e/a-TCP-Socket oder einen gebundenen registrierten e/a-UDP-Socket mit zusätzlichen Optionen für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Rioregisterbuffer**](/previous-versions/windows/desktop/legacy/hh437199(v=vs.85)) | Registriert eine [**Rio \_ -bufferid**](rio-bufferid.md), einen registrierten Puffer Deskriptor, mit einem angegebenen Puffer für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Rioresizecompletionqueue**](/previous-versions/windows/desktop/legacy/hh437202(v=vs.85)) | Ändert die Größe einer e/a-Vervollständigungs Warteschlange für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Rioresizerequestqueue**](/previous-versions/windows/desktop/legacy/hh437204(v=vs.85)) | Ändert die Größe einer Anforderungs Warteschlange, sodass Sie für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen entweder größer oder kleiner ist. |
| [**Randalisend**](/windows/win32/api/mswsock/nc-mswsock-lpfn_riosend) | Sendet Netzwerkdaten für einen verbundenen registrierten e/a-TCP-Socket oder einen gebundenen registrierten e/a-UDP-Socket für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Riosendex**](/previous-versions/windows/desktop/legacy/hh437216(v=vs.85)) | Sendet Netzwerkdaten für einen verbundenen registrierten e/a-TCP-Socket oder einen gebundenen registrierten e/a-UDP-Socket mit zusätzlichen Optionen für die Verwendung mit den Winsock-registrierten e/a-Erweiterungen. |
| [**Auswahl**](/windows/win32/api/Winsock2/nf-winsock2-select) | Bestimmt den Status von einem oder mehreren Sockets, bei Bedarf auf die Durchführung synchroner e/a-Vorgänge. |
| [**Senden**](/windows/win32/api/Winsock2/nf-winsock2-send) | Sendet Daten an einen verbundenen Socket. |
| [**SendTo**](/windows/win32/api/winsock/nf-winsock-sendto) | Sendet Daten an ein bestimmtes Ziel. |
| [**Absichtbare foex**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setaddrinfoexa) | Registriert einen Host und einen Dienstnamen zusammen mit zugeordneten Adressen bei einem bestimmten Namespace Anbieter. |
| [**setipv4sourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setipv4sourcefilter) | Legt den Multicast Filter Zustand für einen IPv4-Socket fest. |
| [**Setservice**](/windows/win32/api/Nspapi/nf-nspapi-setservicea) | Registriert oder entfernt einen Netzwerkdienst in einem oder mehreren Namespaces aus der Registrierung. Kann auch einen Netzwerk Diensttyp innerhalb eines oder mehrerer Namespaces hinzufügen oder entfernen. |
| [**Setsocketmediastreamingmode**](/windows/win32/api/Socketapi/nf-socketapi-setsocketmediastreamingmode) | Gibt an, ob das Netzwerk zum Übertragen von Streamingmedien verwendet werden soll, für die Quality of Service erforderlich ist. |
| [**setsockopt**](/windows/win32/api/winsock/nf-winsock-setsockopt) | Legt eine Socketoption fest. |
| [**setsourcefilter**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-setsourcefilter) | Legt den Multicast Filter Zustand für einen IPv4-oder IPv6-Socket fest. |
| [**Abschlusses**](/windows/win32/api/winsock/nf-winsock-shutdown) | Deaktiviert das Senden oder empfangen von einem Socket. |
| [**Glühbirne**](/windows/win32/api/Winsock2/nf-winsock2-socket) | Erstellt einen Socket, der an einen bestimmten Dienstanbieter gebunden ist. |
| [**TransmitFile**](/windows/win32/api/mswsock/nf-mswsock-transmitfile) | Überträgt Datei Daten über ein verbundenes Sockethandle. |
| [**Transmitpakete**](/windows/win32/api/Mswsock/nc-mswsock-lpfn_transmitpackets) | Überträgt in-Memory-Daten oder Datei Daten über einen verbundenen Socket. |
| [**Wsaaccept**](/windows/win32/api/Winsock2/nf-winsock2-wsaaccept) | Nimmt bedingt eine Verbindung auf Grundlage des Rückgabewerts einer Bedingungs Funktion an, stellt die Qualität der Dienst Fluss Spezifikationen bereit und ermöglicht die Übertragung von Verbindungsdaten. |
| [**Wsaadresssstostring**](/windows/win32/api/Winsock2/nf-winsock2-wsaaddresstostringa) | Konvertiert alle Komponenten einer [**sockaddr**](sockaddr-2.md) -Struktur in eine lesbare Zeichen folgen Darstellung der Adresse. |
| [**Wsaasyncgethostbyaddr**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyaddr) | Ruft asynchron Hostinformationen ab, die einer Adresse entsprechen. |
| [**Wsaasyncgethostbyname**](/windows/win32/api/winsock/nf-winsock-wsaasyncgethostbyname) | Ruft asynchron Hostinformationen ab, die einem Hostnamen entsprechen. |
| [**Wsaasyncgetprotobyname**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobyname) | Ruft asynchron Protokollinformationen ab, die einem Protokollnamen entsprechen. |
| [**Wsaasyncgetprotobynumber**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetprotobynumber) | Ruft asynchron Protokollinformationen ab, die einer Protokollnummer entsprechen. |
| [**Wsaasyncgetservbyname**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyname) | Ruft asynchron Dienst Informationen ab, die einem Dienstnamen und einem Port entsprechen. |
| [**Wsaasyncgetservbyport**](/windows/win32/api/winsock/nf-winsock-wsaasyncgetservbyport) | Ruft asynchron Dienst Informationen ab, die einem Port und Protokoll entsprechen. |
| [**WSAAsyncSelect**](/windows/win32/api/winsock/nf-winsock-wsaasyncselect) | Fordert Windows-Nachrichten basierte Benachrichtigungen von Netzwerk Ereignissen für einen Socket an. |
| [**Wsacancelasynkrequest**](/windows/win32/api/winsock/nf-winsock-wsacancelasyncrequest) | Bricht einen unvollständigen asynchronen Vorgang ab. |
| [**WSACleanup**](/windows/win32/api/winsock/nf-winsock-wsacleanup) | Beendet die Verwendung des Ws2- \_32.DLL. |
| [**Wsacloseevent**](/windows/win32/api/Winsock2/nf-winsock2-wsacloseevent) | Schließt ein offenes Ereignis Objekt handle. |
| [**Wsaconnct**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnect) | Stellt eine Verbindung mit einer anderen socketanwendung her, tauscht Verbindungsdaten aus und gibt die erforderliche Quality of Service basierend auf der angegebenen [**Flowspec**](/windows/win32/api/qos/ns-qos-flowspec) -Struktur an. |
| [**Wsaconnectbylist**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbylist) | Stellt eine Verbindung mit einer aus einer Auflistung möglicher Endpunkte her, die durch einen Satz von Zieladressen (Hostnamen und Ports) dargestellt werden. |
| [**WSAConnectByName**](/windows/win32/api/Winsock2/nf-winsock2-wsaconnectbynamea) | Stellt eine Verbindung mit einer anderen socketanwendung auf einem angegebenen Host und Port her. |
| [**Wsacreateevent**](/windows/win32/api/Winsock2/nf-winsock2-wsacreateevent) | Erstellt ein neues Ereignis Objekt. |
| [**Wsadeletesocketpeer-TargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsadeletesocketpeertargetname) | Entfernt die Zuordnung zwischen einem peerzielnamen und einer IP-Adresse für einen Socket. |
| [**Wsaduplicatcher**](/windows/win32/api/Winsock2/nf-winsock2-wsaduplicatesocketa) | Gibt eine-Struktur zurück, die zum Erstellen eines neuen socketdeskriptors für einen freigegebenen Socket verwendet werden kann. |
| [**Wsaenumnamespaceproviders**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersa) | Ruft Informationen zu verfügbaren Namespaces ab. |
| [**Wsaenumnamespaceprovidersex**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnamespaceprovidersexa) | Ruft Informationen zu verfügbaren Namespaces ab. |
| [**WSAEnumNetworkEvents**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumnetworkevents) | Ermittelt das Vorkommen von Netzwerk Ereignissen für den festgelegten Socket, das Löschen interner Netzwerk Ereignisdaten Sätze und das Zurücksetzen von Ereignis Objekten (optional). |
| [**Wsaenumprotokolle**](/windows/win32/api/Winsock2/nf-winsock2-wsaenumprotocolsa) | Ruft Informationen zu verfügbaren Transportprotokollen ab. |
| [**WSAEventSelect**](/windows/win32/api/Winsock2/nf-winsock2-wsaeventselect) | Gibt ein Ereignis Objekt an, das dem angegebenen Satz von FD xxx-Netzwerk Ereignissen zugeordnet werden soll \_ . |
| [**\_\_Wsafdisset**](/windows/win32/api/winsock/nf-winsock-__wsafdisset) | Gibt an, ob ein Socket in einem Satz von socketdeskriptoren enthalten ist. |
| [**Wsagetfailconnectoncmperror**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetfailconnectonicmperror) | Fragt den Status der [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) Socketoption ab. |
| [**Wsageticmperrorinfo**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsageticmperrorinfo) | Fragt die Quelladresse eines ICMP-Fehlers ab, der beim Einrichten der Verbindung bei einem TCP-Socket empfangen wurde. |
| [**Wsagetipusermtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetipusermtu) | Ruft die benutzerdefinierte IP-Schicht der MTU für einen Socket ab. |
| [**WSAGetLastError**](/windows/win32/api/winsock/nf-winsock-wsagetlasterror) | Gibt den Fehlerstatus für den letzten fehlgeschlagenen Vorgang zurück. |
| [**Wsagein verlappedresult**](/windows/win32/api/Winsock2/nf-winsock2-wsagetoverlappedresult) | Ruft die Ergebnisse eines überlappenden Vorgangs auf dem angegebenen Socket ab. |
| [**Wsagetqosbyname**](/windows/win32/api/Winsock2/nf-winsock2-wsagetqosbyname) | Initialisiert eine [**QoS**](/windows/win32/api/winsock2/ns-winsock2-qos) -Struktur, die auf einer benannten Vorlage basiert, oder stellt einen Puffer bereit, um eine Enumeration der verfügbaren Vorlagen Namen abzurufen. |
| [**Wsagetserviceclassinfo**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassinfoa) | Ruft die Klassen Informationen (Schema) ab, die sich auf eine angegebene Dienstklasse von einem angegebenen Namespace Anbieter beziehen. |
| [**Wsagetserviceclassnamebyclassid**](/windows/win32/api/Winsock2/nf-winsock2-wsagetserviceclassnamebyclassida) | Ruft den Namen des Dienstes ab, der dem angegebenen Typ zugeordnet ist. |
| [**Wsagetudprecvmaxcoalescedsize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudprecvmaxcoalescedsize) | Ruft die maximale Größe einer empfangenen, zusammengefügten Nachricht für einen UDP-Socket ab. |
| [**Wsagetudpsendmessagesize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsagetudpsendmessagesize) | Ruft die Segmentierungs Nachrichtengröße für einen UDP-Socket ab. |
| [**Wsahtonl**](/windows/win32/api/Winsock2/nf-winsock2-wsahtonl) | Konvertiert eine u \_ Long-Datei von der Host-Byte-Reihenfolge in die Netzwerk-Byte |
| [**Wsahtonnen**](/windows/win32/api/Winsock2/nf-winsock2-wsahtons) | Konvertiert eine u- \_ Kurzform von der Host-Byte Reihenfolge in die Netzwerk-Byte |
| [**Wsaidentität atesocketpeer**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaimpersonatesocketpeer) | Dient zum Annehmen der Identität des Sicherheits Prinzipals, der einem socketpeer entspricht, um die Autorisierung auf Anwendungsebene auszuführen. |
| [**Wsainstallserviceclass**](/windows/win32/api/Winsock2/nf-winsock2-wsainstallserviceclassa) | Registriert ein Dienst Klassen Schema in einem Namespace. |
| [**WSAIoctl**](/windows/win32/api/Winsock2/nf-winsock2-wsaioctl) | Steuert den Modus eines Sockets. |
| [**Wsajoinleaf**](/windows/win32/api/Winsock2/nf-winsock2-wsajoinleaf) | Fügt einen Blattknoten in eine Multipoint-Sitzung ein, tauscht Verbindungsdaten aus und gibt die erforderliche Quality of Service basierend auf den angegebenen Strukturen an. |
| [**Wsalookupservicebegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) | Initiiert eine Client Abfrage, die durch die in einer [**wsaqueryset**](/windows/win32/api/Winsock2/ns-winsock2-wsaquerysetw) -Struktur enthaltenen Informationen eingeschränkt ist. |
| [**WSALookupServiceEnd**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupserviceend) | Gibt das Handle frei, das von vorherigen Aufrufen von [**wsalookupservicebegin**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicebegina) und [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta)verwendet wurde. |
| [**WSALookupServiceNext**](/windows/win32/api/Winsock2/nf-winsock2-wsalookupservicenexta) | Abrufen der angeforderten Dienst Informationen. |
| [**Wsanspioctl**](/windows/win32/api/Winsock2/nf-winsock2-wsanspioctl) | Entwickler, die e/a-Steuerungs Aufrufe an einen registrierten Namespace ausführen. |
| [**Wsanum**](/windows/win32/api/Winsock2/nf-winsock2-wsantohl) | Konvertiert einen u-Long-Wert \_ von der Netzwerk-Byte-Reihenfolge in die Host- |
| [**Wsanum**](/windows/win32/api/Winsock2/nf-winsock2-wsantohs) | Konvertiert eine u- \_ Kurzform von der Netzwerk-Byte-Reihenfolge in die Host-Byte |
| [**Wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) | Bestimmt den Status von einem oder mehreren Sockets. |
| [**Wsaproviderconfigchange**](/windows/win32/api/Winsock2/nf-winsock2-wsaproviderconfigchange) | Benachrichtigt die Anwendung, wenn die Anbieter Konfiguration geändert wird. |
| [**Wsaquerysocketsecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsaquerysocketsecurity) | Fragt Informationen über die Sicherheit ab, die auf eine Verbindung auf einem Socket angewendet wird. |
| [**WSARecv**](/windows/win32/api/Winsock2/nf-winsock2-wsarecv) | Empfängt Daten aus einem verbundenen Socket. |
| [**Wsarecvdisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvdisconnect) | Beendet den Empfang für einen Socket und ruft die Trenn Daten ab, wenn der Socket verbindungsorientiert ist. |
| [**Wsarecvex**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) | Empfängt Daten aus einem verbundenen Socket. |
| [**WSARecvFrom**](/windows/win32/api/Winsock2/nf-winsock2-wsarecvfrom) | Empfängt ein Datagramm und speichert die Quelladresse. |
| [**LPFN_WSARECVMSG (wsarecvmsg)**](/windows/win32/api/mswsock/nc-mswsock-lpfn_wsarecvmsg) | Empfängt Daten und optionale Steuerungsinformationen von verbundenen und nicht verbundenen Sockets. |
| [**Wsareviveserviceclass**](/windows/win32/api/Winsock2/nf-winsock2-wsaremoveserviceclass) | Entfernt permanent das Dienst Klassen Schema aus der Registrierung. |
| [**Wsaresetevent**](/windows/win32/api/Winsock2/nf-winsock2-wsaresetevent) | Setzt den Zustand des angegebenen Ereignis Objekts auf "nicht signalisiert" zurück. |
| [**Wsarevertimpersonations**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsarevertimpersonation) | Beendet den Identitätswechsel eines socketpeers. |
| [**Wsasend**](/windows/win32/api/Winsock2/nf-winsock2-wsasend) | Sendet Daten an einen verbundenen Socket. |
| [**Wsasenddisconnect**](/windows/win32/api/Winsock2/nf-winsock2-wsasenddisconnect) | Initiiert die Beendigung der Verbindung für den Socket und sendet Trennungs Daten. |
| [**Wsasendmsg**](/windows/win32/api/winsock2/nf-winsock2-wsasendmsg) | Sendet Daten und optionale Steuerungsinformationen von verbundenen und nicht verbundenen Sockets. |
| [**WSASendTo**](/windows/win32/api/Winsock2/nf-winsock2-wsasendto) | Sendet Daten an ein bestimmtes Ziel, wobei ggf. überlappende e/a-Vorgänge verwendet werden. |
| [**Wsasetevent**](/windows/win32/api/Winsock2/nf-winsock2-wsasetevent) | Legt den Zustand des angegebenen Ereignis Objekts auf "signalisiert" fest. |
| [**Wsasetfailconnectoncmperror**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetfailconnectonicmperror) | Legt den Status der [**TCP_FAIL_CONNECT_ON_ICMP_ERROR**](./ipproto-tcp-socket-options.md) Socketoption fest. |
| [**Wsasetipusermtu**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetipusermtu) | Legt die benutzerdefinierte IP-Ebenen-MTU auf einem Socket fest. |
| [**Wsasetlasterror**](/windows/win32/api/winsock/nf-winsock-wsasetlasterror) | Legt den Fehlercode fest. |
| [**Wsasetservice**](/windows/win32/api/Winsock2/nf-winsock2-wsasetservicea) | Registriert oder entfernt eine Dienst Instanz in einem oder mehreren Namespaces aus der Registrierung. |
| [**Wsasetsocketpeer-TargetName**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketpeertargetname) | Wird verwendet, um den Peer Zielnamen (SPN) anzugeben, der einer Peer-IP-Adresse entspricht. Dieser Zielname soll von Client Anwendungen angegeben werden, um den Peer, der authentifiziert werden soll, sicher zu identifizieren. |
| [**Wsasetsocketsecurity**](/windows/win32/api/Ws2tcpip/nf-ws2tcpip-wsasetsocketsecurity) | Aktiviert und wendet die Sicherheit für einen Socket an. |
| [**Wsasetudprecvmaxcoalescedsize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudprecvmaxcoalescedsize) | Legt die maximale Größe einer zusammengefügten Nachricht fest, die für einen UDP-Socket festgelegt wurde. |
| [**Wsasetudpsendmessagesize**](/windows/win32/api/ws2tcpip/nf-ws2tcpip-wsasetudpsendmessagesize) | Legt die Segmentierungs Nachrichtengröße für einen UDP-Socket fest. |
| [**Wsasocket**](/windows/win32/api/Winsock2/nf-winsock2-wsasocketa) | Erstellt einen Socket, der an einen bestimmten Transport Dienstanbieter gebunden ist. |
| [**WSAStartup**](/windows/win32/api/winsock/nf-winsock-wsastartup) | Initiiert die Verwendung von ws2- \_32.DLL durch einen Prozess. |
| [**WSAStringToAddress**](/windows/win32/api/Winsock2/nf-winsock2-wsastringtoaddressa) | Konvertiert eine numerische Zeichenfolge in eine [**sockaddr**](sockaddr-2.md) -Struktur. |
| [**Wsawaitformultipleevents**](/windows/win32/api/Winsock2/nf-winsock2-wsawaitformultipleevents) | Gibt entweder dann zurück, wenn sich eines oder alle der angegebenen Ereignis Objekte im signalisierten Zustand befinden oder wenn das Timeout Intervall abläuft. |
