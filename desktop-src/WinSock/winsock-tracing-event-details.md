---
description: Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung
ms.assetid: f0386bd3-15d0-45f3-82c9-365d1c9f59c5
title: Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 588363420aee9c3b04f4f8060bbd9c77b9cc3232
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217285"
---
# <a name="winsock-network-event-tracing-details"></a>Details der Winsock-Netzwerk Ereignis Ablauf Verfolgung

Im folgenden werden die einzelnen Winsock-Netzwerkereignisse erläutert, die verfolgt werden können, und es wird beschrieben, welche Parameter und Informationen protokolliert werden.

## <a name="socket-creation"></a>Socketerstellung

Ereignis-ID = 1

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für die Socketerstellung nachverfolgt:

-   Sockethandles, die durch Aufrufe der [**Socket**](/windows/desktop/api/Winsock2/nf-winsock2-socket) -oder [**wsasocket**](/windows/desktop/api/Winsock2/nf-winsock2-wsasocketa) -Funktionen erstellt werden.
-   Akzeptierte Sockethandles für Abhör Sockets.
-   Sockethandles, die durch Aufrufe der [**wsajoinleaf**](/windows/desktop/api/Winsock2/nf-winsock2-wsajoinleaf) -Funktion erstellt werden.
-   Sockethandles, die von Aufrufen der [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex) -Funktion oder der [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex) -Funktion wieder verwendet werden.

Die folgenden Parameter werden für ein Socket-Erstellungs Ereignis protokolliert:



| Parameter                                                                                                        | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                 | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>             | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="SocketType"></span><span id="sockettype"></span><span id="SOCKETTYPE"></span>SocketType<br/>     | Der Typ des Sockets.<br/>                                                     |
| <span id="Protocol"></span><span id="protocol"></span><span id="PROTOCOL"></span>Spezifische<br/>             | Das Protokoll des Sockets.<br/>                                                 |
| <span id="UserModePid"></span><span id="usermodepid"></span><span id="USERMODEPID"></span>Usermodepid<br/> | Die Benutzermodus-Prozess-ID, die den Socket erstellt hat.<br/>                           |



 

## <a name="socket-bind"></a>Socketbindung

Ereignis-ID = 2 (IPv4), Ereignis-ID = 3 (IPv6)

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für einen Bindungs Vorgang nachverfolgt:

-   Implizite oder explizite Bindung eines Sockethandles.

Die folgenden Parameter werden für ein Bindungs Ereignis protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>     | Die lokale IP-Adresse.<br/>                                                       |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                 | Die lokale IP-Portnummer.<br/>                                                   |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Stands<br/>         | Der Status oder Fehlercode, der für den Bindungs Vorgang zurückgegeben wird.<br/>                   |



 

## <a name="failed-bind"></a>Fehlerhafte Bindung

Ereignis-ID = 40

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für einen fehlgeschlagenen Bindungs Vorgang nachverfolgt:

-   Implizite oder explizite Bindung eines Sockethandles, der fehlschlägt.

Die folgenden Parameter werden für ein fehlerhafter Bindungs Ereignis protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der für den fehlgeschlagenen Bindungs Vorgang zurückgegebene Fehlercode.<br/>                     |



 

## <a name="socket-connect"></a>Socketverbindung

Ereignis-ID = 4 (IPv4), Ereignis-ID = 5 (IPv6)

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für eine Anforderung zum Verbindungsvorgang nachverfolgt (ein Rückruf der [**Connect**](/windows/desktop/api/Winsock2/nf-winsock2-connect)-, [**connectex**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_connectex)-, [**wsaconnect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnect)-, [**wsaconnectbylist**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbylist)-oder [**WSAConnectByName**](/windows/desktop/api/Winsock2/nf-winsock2-wsaconnectbynamea) -Funktion):

-   Verbinden eines Sockets mit einem Ziel entweder für einen Verbindungs orientierten oder einen Verbindungs losen Socket.

Die folgenden Parameter werden für ein Connect-Ereignis protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>     | Die Remote-IP-Adresse.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                 | Die Remote-IP-Portnummer.<br/>                                                  |



 

## <a name="connect-completed"></a>Verbindung abgeschlossen

Ereignis-ID = 6

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn eine Verbindung abgeschlossen wurde:

-   Der Verbindungsvorgang ist abgeschlossen.

Die folgenden Parameter werden für ein Connect-abgeschlossenes Ereignis protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der Fehlercode, der für den Verbindungsvorgang zurückgegeben wird.<br/>                          |



 

## <a name="afd-initiated-abort"></a>Abbruch AFD-Initiated

Ereignis-ID = 7

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für durch Winsock initiierte Abbrüche oder Abbruch Vorgänge nachverfolgt:

-   Ein Abbruch aufgrund von ungelesenen Empfangsdaten, die nach dem Schließen gepuffert werden.
-   Ein Abbruch nach einem Aufrufen der [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) -Funktion *mit dem fest* gelegten Parameter auf SD \_ Receive und einem Aufrufen der [**closesocket**](/windows/desktop/api/winsock/nf-winsock-closesocket) -Funktion mit ausstehenden Daten empfangen.
-   Ein Abbruch nach einem fehlgeschlagenen Versuch, den Endpunkt zu leeren.
-   Abbruch nach einem internen Winsock-Fehler.
-   Ein Abbruch aufgrund einer Verbindung mit Fehlern und der Anwendung, die zuvor angefordert hat, dass die Verbindung unter bestimmten Umständen abgebrochen wird. Ein Beispiel für diesen Fall wäre eine Anwendung, die " \_ LINGER" mit einem Timeout von 0 (null) festgelegt hat und noch nicht bestätigte Daten für die Verbindung vorhanden sind.
-   Ein Abbruch für eine Verbindung, die nicht vollständig mit dem akzeptieren des Endpunkts verknüpft ist.
-   Ein Abbruch bei einem fehlgeschlagenen Aufrufs der [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept) -oder [**Accept tex**](/windows/win32/api/mswsock/nf-mswsock-acceptex) -Funktion.
-   Ein Abbruch aufgrund eines fehlgeschlagenen Empfangs Vorgangs.
-   Ein Abbruch aufgrund eines Plug & Play Ereignisses.
-   Ein Abbruch aufgrund einer fehlgeschlagenen Leerungs Anforderung.
-   Ein Abbruch aufgrund einer fehlgeschlagenen Anforderung zum Empfangen von Daten.
-   Ein Abbruch aufgrund einer fehlgeschlagenen Sende Anforderung.
-   Ein Abbruch aufgrund einer abgebrochenen Sende Anforderung.
-   Ein Abbruch aufgrund eines abgebrochenen Aufrufs für die [**transmitpaketen**](/windows/desktop/api/Mswsock/nc-mswsock-lpfn_transmitpackets) -Funktion.

Die folgenden Parameter werden für einen Winsock-initiierten Abbruch-oder Abbruch Vorgang protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Weshalb<br/>         | Der Grund für den Abbruch-oder Abbruch Vorgang.<br/>                               |



 

## <a name="transport-initiated-abort"></a>Abbruch Transport-Initiated

Ereignis-ID = 8

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für vom Transport initiierte Abbruch-oder Abbruch Vorgänge verfolgt:

-   Zurücksetzen, angegeben durch den Transport.

Die folgenden Parameter werden für einen Winsock-initiierten Abbruch-oder Abbruch Vorgang protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Weshalb<br/>         | Der Grund für den Abbruch-oder Abbruch Vorgang.<br/>                               |



 

## <a name="failed-send-request"></a>Fehlgeschlagene Sende Anforderung

Ereignis-ID = 9

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden bei [**Sende**](/windows/desktop/api/Winsock2/nf-winsock2-send) -oder [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) -Anforderungen auf Fehler nachverfolgt:

-   Bei fehlgeschlagenen [**Sende**](/windows/desktop/api/Winsock2/nf-winsock2-send) -oder [**wsasend**](/windows/desktop/api/Winsock2/nf-winsock2-wsasend) -Anforderungen zurückgegebene Fehler.

Die folgenden Parameter werden für Sende Anforderungen protokolliert, die zu einem Fehler führen:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der für den Vorgang zurückgegebene Fehlercode.<br/>                                  |



 

## <a name="failed-wsasendmsg-request"></a>Wsasendmsg-Anforderung fehlgeschlagen

Ereignis-ID = 10

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden auf Fehler bei [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Anforderungen nachverfolgt:

-   Bei fehlgeschlagenen [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Anforderungen zurückgegebene Fehler.

Die folgenden Parameter werden für Sende Anforderungen protokolliert, die zu einem Fehler führen:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der für den Vorgang zurückgegebene Fehlercode.<br/>                                  |



 

## <a name="failed-recv-request"></a>Fehlgeschlagene recv-Anforderung

Ereignis-ID = 11

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden auf Fehler bei [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv)-, [**WSARecv**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecv)-oder [**wsarecvexeanforderungen**](/windows/win32/api/mswsock/nf-mswsock-wsarecvex) nachverfolgt:

-   Bei fehlgeschlagenen Empfangs Anforderungen zurückgegebene Fehler.

Die folgenden Parameter werden für Sende Anforderungen protokolliert, die zu einem Fehler führen:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der für den Vorgang zurückgegebene Fehlercode.<br/>                                  |



 

## <a name="failed-recvfrom-request"></a>Fehlgeschlagene recvfrom-Anforderung

Ereignis-ID = 12

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden auf Fehler bei [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -oder [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) -Anforderungen nachverfolgt:

-   Fehler, die für fehlerhafte [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -oder [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) -Anforderungen zurückgegeben wurden.

Die folgenden Parameter werden für eine Anforderung vom Typ " [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) " oder " [**WSARecvFrom**](/windows/desktop/api/Winsock2/nf-winsock2-wsarecvfrom) " protokolliert, die zu einem Fehler führt:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der für den Vorgang zurückgegebene Fehlercode.<br/>                                  |



 

## <a name="socket-close"></a>SocketClose

Ereignis-ID = 13

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für SocketClose-Vorgänge nachverfolgt:

-   Ein Sockethandle ist geschlossen.

Die folgenden Parameter werden für ein Socket Close-Ereignis protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der Rückgabewert für den SocketClose-Vorgang.<br/>                            |



 

## <a name="socket-cleanup"></a>Socketcleanup

Ereignis-ID = 14

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für die socketbereinigungs Vorgänge (Herunterfahren) nachverfolgt:

-   Die [**Shutdown**](/windows/desktop/api/winsock/nf-winsock-shutdown) -Funktion wird für einen Socket aufgerufen.
-   Der Transport gibt an, dass eine fehlerhafte Verbindung getrennt wurde

Die folgenden Parameter werden für ein socketcleanup (Shutdown) oder ein Socket Close-Ereignis protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der Rückgabewert für die socketbereinigungs Operation (Shutdown).<br/>               |



 

## <a name="socket-accept"></a>Socketannahme

Ereignis-ID = 15 (IPv4), Ereignis-ID = 16 (IPv6)

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für eine [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)-, [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)-oder [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktions Anforderung nachverfolgt:

-   Eine [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)-, [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)-oder [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Funktions Anforderung für ein Sockethandle.

Die folgenden Parameter werden für ein Accept-Ereignis protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>     | Die Remote-IP-Adresse.<br/>                                                      |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                 | Die Remote-IP-Portnummer.<br/>                                                  |
| <span id="Status"></span><span id="status"></span><span id="STATUS"></span>Stands<br/>         | Der Status oder Fehlercode, der für den Accept-Vorgang zurückgegeben wird.<br/>                 |



 

## <a name="accept-failed"></a>Annahme fehlgeschlagen

Ereignis-ID = 17

Ebene = 4 (Informationen)

Die folgenden Winsock-Ereignisse werden für einen fehlgeschlagenen Accept-Vorgang nachverfolgt:

-   Eine [**Accept**](/windows/desktop/api/Winsock2/nf-winsock2-accept)-, [**akzeptex**](/windows/win32/api/mswsock/nf-mswsock-acceptex)-oder [**wsaaccept**](/windows/desktop/api/Winsock2/nf-winsock2-wsaaccept) -Anforderung für ein Sockethandle, das fehlschlägt.

Die folgenden Parameter werden für ein fehlgeschlagenes Accept-Ereignis protokolliert:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der für den fehlgeschlagenen Accept-Vorgang zurückgegebene Fehlercode.<br/>                   |



 

## <a name="send-posted"></a>Senden gepostet

Ereignis-ID = 18

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden nach Vorgängen für Socket Send-und Receive-Puffer nachverfolgt:

-   Eine Anwendung sendet einen Send-Vorgang.
-   Ein Sendevorgang wird in Winsock abgeschlossen.

Die folgenden Parameter werden für Socketsendevorgänge protokolliert:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Ein boolescher Wert, der angibt, ob ein schnelles Pfad-e/a verwendet wurde.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Die Puffer Anzahl.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers. Bei verketteten Puffern ist dieser Parameter die Gesamtzahl der Bytes in allen Puffern in der Kette.<br/>  |



 

Wenn FastPath den Wert true hat, wird die Usermode-Adresse des ersten Puffers im Puffer Array im Puffer Parameter protokolliert. Wenn FastPath den Wert false hat, wird die Winsock-Kernel Puffer Adresse im buffer-Parameter protokolliert.

## <a name="receive-posted"></a>Empfangen gesendet

Ereignis-ID = 19

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden für Post-Vorgänge des Socket-Empfangspuffers nachverfolgt:

-   Eine Anwendung sendet einen Empfangs-.
-   Ein Empfangsvorgang wird in Winsock abgeschlossen.

Die folgenden Parameter werden für Socket-Empfangs Vorgänge protokolliert:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Ein boolescher Wert, der angibt, ob ein schnelles Pfad-e/a verwendet wurde.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Die Puffer Anzahl.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers. Bei verketteten Puffern ist dieser Parameter die Gesamtzahl der Bytes in allen Puffern in der Kette.<br/>  |



 

Wenn FastPath den Wert true hat, wird die Usermode-Adresse des ersten Puffers im Puffer Array im Puffer Parameter protokolliert. Wenn FastPath den Wert false hat, wird die Winsock-Kernel Puffer Adresse im buffer-Parameter protokolliert.

## <a name="recvfrom-posted"></a>Recvfrom gepostet

Ereignis-ID = 20

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden nach einem postvorgang eines [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -Puffers für einen Socket nachverfolgt:

-   Eine Anwendung sendet einen Receive from-Vorgang.

Die folgenden Parameter werden für den Vorgang "recvfrom" protokolliert:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Ein boolescher Wert, der angibt, ob ein schnelles Pfad-e/a verwendet wurde.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Die Puffer Anzahl.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers. Bei verketteten Puffern ist dieser Parameter die Gesamtzahl der Bytes in allen Puffern in der Kette.<br/>  |



 

Wenn FastPath den Wert true hat, wird die Usermode-Adresse des ersten Puffers im Puffer Array im Puffer Parameter protokolliert. Wenn FastPath den Wert false hat, wird die Winsock-Kernel Puffer Adresse im buffer-Parameter protokolliert.

## <a name="sendto-posted"></a>SendTo gepostet

Ereignis-ID = 21 (IPv4), Ereignis-ID = 22 (IPv6)

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden nachverfolgt [**, wenn ein SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -Puffer postvorgang für einen Socket ausgeführt wird:

-   Eine Anwendung sendet einen Sendevorgang von.

Die folgenden Parameter werden für den [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -Vorgang protokolliert:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                |
|----------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                          |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                     |
| <span id="FastPath"></span><span id="fastpath"></span><span id="FASTPATH"></span>FastPath<br/>                 | Ein boolescher Wert, der angibt, ob ein schnelles Pfad-e/a verwendet wurde.<br/>                                                                       |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Die Puffer Anzahl.<br/>                                                                                                               |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/> |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers. Bei verketteten Puffern ist dieser Parameter die Gesamtzahl der Bytes in allen Puffern in der Kette.<br/>  |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>                     | Die Remote-IP-Adresse des Sockets.<br/>                                                                                            |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                                 | Die Remote-IP-Portnummer des Sockets.<br/>                                                                                        |



 

Wenn FastPath den Wert true hat, wird die Usermode-Adresse des ersten Puffers im Puffer Array im Puffer Parameter protokolliert. Wenn FastPath den Wert false hat, wird die Winsock-Kernel Puffer Adresse im buffer-Parameter protokolliert.

## <a name="recv-completed"></a>Recv abgeschlossen

Ereignis-ID = 23

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden für abgeschlossene Socket-Empfangs Vorgänge nachverfolgt:

-   Ein Sendevorgang wird für den Transport abgeschlossen.
-   Ein Empfangsvorgang wird für den Transport abgeschlossen.

Die folgenden Parameter werden für den Abschluss eines Sendevorgangs protokolliert, oder der Empfangsvorgang wurde abgeschlossen:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                              |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers der empfangenen Bytes. Bei verketteten Puffern handelt es sich bei diesem Parameter um die Gesamtanzahl der Bytes, die in allen Puffern der<br/> |



 

## <a name="send-completed"></a>Sendevorgang abgeschlossen

Ereignis-ID = 24

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden für abgeschlossene Socket Send-Vorgänge nachverfolgt:

-   Ein Sendevorgang wird für den Transport abgeschlossen.

Die folgenden Parameter werden für den Abschluss eines Sendevorgangs protokolliert:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers von gesendeten Bytes. Bei verketteten Puffern handelt es sich bei diesem Parameter um die gesamten bytes, die von allen Puffern in der Kette<br/> |



 

## <a name="sendmsg-completed"></a>Sendmsg abgeschlossen

Ereignis-ID = 25

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn ein [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Puffer postvorgang für einen Socket abgeschlossen wird:

-   Eine Anwendung schließt einen [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) -Vorgang ab.

Die folgenden Parameter werden für die Ausführung von [**wsasendmsg**](/windows/desktop/api/winsock2/nf-winsock2-wsasendmsg) protokolliert:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Die Puffer Anzahl.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers von gesendeten Bytes. Bei verketteten Puffern handelt es sich bei diesem Parameter um die gesamten bytes, die von allen Puffern in der Kette<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>                     | Die Remote-IP-Adresse des Sockets.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                                 | Die Remote-IP-Portnummer des Sockets.<br/>                                                                                           |



 

## <a name="recvfrom-completed"></a>Recvfrom abgeschlossen

Ereignis-ID = 26 (IPv4), Ereignis-ID = 27 (IPv6)

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn ein [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -Puffer postvorgang für einen Socket abgeschlossen wird:

-   Eine Anwendung schließt einen [**recvfrom**](/windows/desktop/api/winsock/nf-winsock-recvfrom) -Vorgang ab.

Die folgenden Parameter werden für [**den Abschluss der**](/windows/desktop/api/winsock/nf-winsock-recvfrom) Wiederholung protokolliert:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                         |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                                   |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                              |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Die Puffer Anzahl.<br/>                                                                                                                        |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/>          |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers der empfangenen Bytes. Bei verketteten Puffern handelt es sich bei diesem Parameter um die Gesamtanzahl der Bytes, die in allen Puffern der<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>                     | Die Remote-IP-Adresse des Sockets.<br/>                                                                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                                 | Die Remote-IP-Portnummer des Sockets.<br/>                                                                                                 |



 

## <a name="sendto-completed"></a>SendTo abgeschlossen

Ereignis-ID = 28

Ebene = 5 (ausführlich)

Um Benutzer Puffer Beschädigungen zu diagnostizieren (z. b. Wenn eine Anwendung denselben Puffer in einem anderen Sende-oder Empfangsport wieder verwendet, während Sie noch verwendet wird), wird der Datenpuffer protokolliert, wenn er an Winsock gesendet wird, und nach Abschluss des zugrunde liegenden Transports. Die folgenden Winsock-Ereignisse werden nachverfolgt [**, wenn ein SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -Puffer postvorgang für einen Socket abgeschlossen wird:

-   Eine Anwendung schließt einen [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) -Vorgang ab.

Die folgenden Parameter werden für die Beendigung der [**SendTo**](/windows/desktop/api/winsock/nf-winsock-sendto) protokolliert:



| Parameter                                                                                                            | BESCHREIBUNG                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                                                             |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                 | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                                                        |
| <span id="BufferCount"></span><span id="buffercount"></span><span id="BUFFERCOUNT"></span>BufferCount<br/>     | Die Puffer Anzahl.<br/>                                                                                                                  |
| <span id="Buffer"></span><span id="buffer"></span><span id="BUFFER"></span>Ert<br/>                         | Die virtuelle Adresse des Puffers. Bei verketteten Puffern ist dieser Parameter die virtuelle Adresse des ersten Puffers in der Kette.<br/>    |
| <span id="BufferLength"></span><span id="bufferlength"></span><span id="BUFFERLENGTH"></span>Pufferlänge<br/> | Die Länge des Puffers von gesendeten Bytes. Bei verketteten Puffern handelt es sich bei diesem Parameter um die gesamten bytes, die von allen Puffern in der Kette<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>                     | Die Remote-IP-Adresse des Sockets.<br/>                                                                                               |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                                 | Die Remote-IP-Portnummer des Sockets.<br/>                                                                                           |



 

## <a name="socket-option-set"></a>Socketoptionssatz

Ereignis-ID = 29

Ebene = 5 (ausführlich)

Wenn eine Anwendung bestimmte socketoptionswerte und IOCTLs ändert, werden die neuen Werte protokolliert. Die protokollierten Optionen können verwendet werden, um eine schlechte Leistung oder ein ungewöhnliches Verhalten in Anwendungen zu diagnostizieren. Die folgenden Winsock-Ereignisse werden für bestimmte Socketoptionen und IOCTLs nachverfolgt:

-   \_Sndbuf ändert sich also.
-   \_Rcvbuf ändert sich also.
-   FIONBIO
-   SIO \_ Aktivieren von \_ zirkulären \_ Warteschlangen
-   \_Konfigurations-UDP-Zusammensetzung \_
-   \_oobinline

Die folgenden Parameter werden für [**setsockopt**](/windows/desktop/api/winsock/nf-winsock-setsockopt) -und [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) -Funktionsaufrufe protokolliert, die jeden der obigen Werte ändern:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Option"></span><span id="option"></span><span id="OPTION"></span>Andere<br/>         | Die Socketoption oder IOCTL, die geändert wird. <br/>                                |
| <span id="Value"></span><span id="value"></span><span id="VALUE"></span>Wert<br/>             | Der neue Wert für die Socketoption oder ioctl. <br/>                              |



 

## <a name="selectpoll-posted"></a>SELECT/Abruf gepostet

Ereignis-ID = 30

Ebene = 5 (ausführlich)

Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn eine Anwendung die Funktion [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) aufruft:

-   Die Anwendung stellt eine [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Anforderung zur Anwendung.

Die folgenden Parameter werden für [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Ereignisse protokolliert:



| Parameter                                                                                                        | BESCHREIBUNG                                                                                                    |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                 | Die besitzende Prozess-ID.<br/>                                                                              |
| <span id="HandleCount"></span><span id="handlecount"></span><span id="HANDLECOUNT"></span>HandleCount<br/> | Die Anzahl der Handles, die von der Anwendung weitergegeben werden (nur gültig für das initiierende Ereignis).<br/>            |
| <span id="Timeout"></span><span id="timeout"></span><span id="TIMEOUT"></span>Zeit<br/>                 | Die maximale Zeit, die die [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Funktion warten soll.<br/> |



 

## <a name="selectpoll-completed"></a>SELECT/Abruf abgeschlossen

Ereignis-ID = 31

Ebene = 5 (ausführlich)

Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn eine Anwendung die Funktion [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) aufruft:

-   Winsock schließt einen [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Befehl ab.

Die folgenden Parameter werden protokolliert, wenn ein [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Vorgang abgeschlossen wird:



| Parameter                                                                                            | BESCHREIBUNG                                                                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                                              |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/>                         |
| <span id="Error"></span><span id="error"></span><span id="ERROR"></span>Zeit<br/>             | Der für den [**Select**](/windows/desktop/api/Winsock2/nf-winsock2-select) -oder [**wsapoll**](/windows/win32/api/winsock2/nf-winsock2-wsapoll) -Vorgang zurückgegebene Fehlercode.<br/> |



 

## <a name="wsaeventselect"></a>WSAEventSelect

Ereignis-ID = 32

Ebene = 5 (ausführlich)

Die folgenden Winsock-Ereignisse werden nachverfolgt, wenn eine Anwendung die [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktion aufruft:

-   Protokolliert die Ereignis Maske, die in der [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktion gegeben wurde.

Die folgenden Parameter werden für [**WSAEventSelect**](/windows/desktop/api/Winsock2/nf-winsock2-wsaeventselect) -Funktionsaufrufe protokolliert:



| Parameter                                                                                                | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>         | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>     | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="EventMask"></span><span id="eventmask"></span><span id="EVENTMASK"></span>EventMask<br/> | Der Wert für die Ereignis Maske. <br/>                                              |



 

## <a name="dropped-datagram"></a>Gelöschter Datagramm

Ereignis-ID = 33 (IPv4), Ereignis-ID = 34 (IPv6)

Ebene = 5 (ausführlich)

Um Probleme mit datagrammanwendungen zu diagnostizieren, werden die folgenden Winsock-Ereignisse nachverfolgt:

-   Wenn ein Datagramm eintrifft und es gelöscht wird, reicht dies nicht aus.
-   Bei einem verbundenen Datagramm, wenn Daten von einer anderen Quelle als dem verbundenen Ziel empfangen werden.

Die folgenden Parameter werden für gelöschte Datagramme protokolliert:



| Parameter                                                                                                    | BESCHREIBUNG                                                                            |
|--------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>             | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>         | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="PacketSize"></span><span id="packetsize"></span><span id="PACKETSIZE"></span>PacketSize<br/> | Die Größe des Pakets, das gelöscht wurde. <br/>                                   |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>             | Die IP-Adresse der Quelle des Pakets. <br/>                                |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                         | Die IP-Portnummer der Quelle des Pakets.<br/>                             |
| <span id="Reason"></span><span id="reason"></span><span id="REASON"></span>Weshalb<br/>                 | Der Fehlercode oder der Grund, warum das Paket gelöscht wurde.<br/>                            |



 

## <a name="connection-indicated"></a>Verbindung angegeben

Ereignis-ID = 35 (IPv4), Ereignis-ID = 36 (IPv6)

Ebene = 5 (ausführlich)

Die folgenden Winsock-Ereignisse werden für die von der Verbindung genannten Vorgänge nachverfolgt:

-   Eine Anwendung empfängt eine Verbindungsanforderung.

Die folgenden Parameter werden für Verbindungen protokolliert, die von Transport Ereignissen angegeben werden:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>     | Die Remote-IP-Adresse. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                 | Die Remote-IP-Portnummer.<br/>                                                  |



 

## <a name="data-indicated"></a>Daten angegeben

Ereignis-ID = 37

Ebene = 5 (ausführlich)

Die folgenden Winsock-Ereignisse werden für Daten, die für die Daten angezeigt werden, verfolgt

-   Eine Anwendung empfängt Daten auf einem verbundenen Socket.

Die folgenden Parameter werden für Daten protokolliert, die von Transport Ereignissen angegeben werden:



| Parameter                                                                                                                        | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                                 | Die besitzende Prozess-ID.<br/>                                                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                             | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes angegeben<br/> | Die Anzahl der Bytes, die im Socket empfangen wurden.<br/>                                 |



 

## <a name="data-indicated-from-transport"></a>Daten, die vom Transport angegeben werden

Ereignis-ID = 38 (IPv4), Ereignis-ID = 39 (IPv6)

Ebene = 5 (ausführlich)

Die folgenden Winsock-Ereignisse werden für Daten nachverfolgt, die von Transportvorgängen angegeben werden:

-   Eine Anwendung sendet eine Empfangs Anforderung und empfängt Daten.

Die folgenden Parameter werden für Daten protokolliert, die von Transport Ereignissen angegeben werden:



| Parameter                                                                                                                        | BESCHREIBUNG                                                                            |
|----------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>                                 | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/>                             | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |
| <span id="Address"></span><span id="address"></span><span id="ADDRESS"></span>Adresse<br/>                                 | Die Remote-IP-Adresse. <br/>                                                     |
| <span id="Port"></span><span id="port"></span><span id="PORT"></span>Port<br/>                                             | Die Remote-IP-Portnummer.<br/>                                                  |
| <span id="Bytes_Indicated"></span><span id="bytes_indicated"></span><span id="BYTES_INDICATED"></span>Bytes angegeben<br/> | Die Anzahl der Bytes, die im Socket empfangen wurden.<br/>                                 |



 

## <a name="disconnect-indicated-from-transport"></a>Verbindung wird vom Transport angegeben

Ereignis-ID = 41

Ebene = 5 (ausführlich)

Die folgenden Winsock-Ereignisse werden für die durch Trenn Vorgänge gekennzeichneten Vorgänge nachverfolgt:

-   Eine Anwendung empfängt eine Disconnect-Anzeige.

Die folgenden Parameter werden für die Trennung protokolliert, die von Transport Ereignissen angezeigt wird:



| Parameter                                                                                            | BESCHREIBUNG                                                                            |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| <span id="Process"></span><span id="process"></span><span id="PROCESS"></span>ESS<br/>     | Die Kernel-EPROCESS-Struktur Adresse für den Prozess.<br/>                      |
| <span id="Endpoint"></span><span id="endpoint"></span><span id="ENDPOINT"></span>Dreher<br/> | Die Winsock-Kernel-Socketadresse, die als eindeutiger Bezeichner für einen Socket verwendet wird.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Kontrolle über die Winsock-Ablauf Verfolgung](control-of-winsock-tracing.md)
</dt> <dt>

[Winsock-Ablauf Verfolgung](winsock-tracing.md)
</dt> <dt>

[Details zur Änderung der Winsock-Katalog Änderung](winsock-layered-service-provider-tracing-event-details.md)
</dt> <dt>

[Winsock-Ablauf Verfolgungs Ebenen](winsock-tracing-levels.md)
</dt> </dl>

 

 
